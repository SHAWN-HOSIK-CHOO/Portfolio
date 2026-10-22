# [기획서] 융합(합성) 시스템 규격서

## 1. 개요
본 문서는 보유 중인 에이전트(몬스터), 스킬카드, 아이템 중 3종을 조합하여 새로운 에이전트, 스킬카드, 아이템을 생성하는 **융합(합성) 시스템**의 상세 기획 및 스탯 보너스 계산 로직을 정의한다.

---

## 2. 융합 시스템 기본 메커니즘

### 2.1 융합 연출
* **파형 변화**: 플레이어가 생성기 UI에 재료를 드롭하는 순간 합성기의 파형이 변화한다.
<img width="600" height="300" alt="Image" src="https://github.com/user-attachments/assets/342cc546-bf52-4a9f-ac04-da5ccdb9c31d" />

### 2.1 융합 재료 및 결과
* **재료 구성**: 플레이어가 보유한 **[에이전트], [스킬카드], [아이템]** 중 총 **3개**를 자유롭게 선택
* **융합 결과**: 재료의 조합에 따라 **[에이전트], [스킬카드], [아이템]** 중 1종 결과물 창조
* **조합 관리**: 모든 조합 레시피 및 결과 데이터는 `FusionInfo_Result.json` 테이블로 관리

### 2.2 에이전트 융합 시 세부 변화
융합 결과물이 **에이전트**인 경우 아래 규칙이 적용된다.
1. **신규 에이전트 탄생**: 조합 공식에 따른 새로운 에이전트 생성
2. **스킬 계승**: 재료 에이전트에 장착되어 있던 스킬 및 재료 스킬카드 중 **최대 3개 스킬 계승**
3. **스탯 변화 (스킬 기반 보너스)**:
   * **스킬 스크랩**: 융합 재료 에이전트들의 장착 스킬 + 재료로 사용된 스킬카드 각각의 스킬 수집
   * **스탯 합산**: 수집된 스킬들의 카테고리를 분류하고, 카테고리별 부여 스탯을 최종 에이전트에 스탯 보너스로 합산 적용

---

## 3. 스킬 카테고리별 스탯 매핑 규칙

스킬 스크랩 과정으로 수집된 모든 스킬들에 대해 아래 매핑표에 맞는 보너스 스탯을 부여한다.

| 카테고리 (Category) | 감정 / 속성 | 매핑 조건 (AttackType / EventType) | 부여 스탯 (Stats) |
| :--- | :--- | :--- | :--- |
| **Joy** | 기쁨 | `JoyAttack` | `EmoAttack` +1.0, `HP` +10 |
| **Sadness** | 슬픔 | `SadnessAttack` | `EmoDefense` +1.0, `PhysicsDefense` +1.0, `EmoSensitivity` +0.5 |
| **Fear** | 공포 | `FearAttack` | `MoveSpeed` +1.5, `CriticalRate` +0.2 |
| **Anger** | 분노 | `AngerAttack` | `PhysicsAttack` +1.0, `EmoAttack` +1.0 |
| **Surprise** | 놀람 | `SurpriseAttack` | `CriticalDamage` +0.02, `CriticalRate` +0.1 |
| **Disgust** | 혐오 | `DisgustAttack` | `EmoDefense` +1.0, `EmoAttack` +0.5 |
| **Trust** | 신뢰 | `TrustAttack`  | `HP` +25, `PhysicsDefense` +0.5 |
| **Anticipation** | 기대 | `AnticipationAttack`  | `MoveSpeed` +2.0, `EmoSensitivity` +1.0 |
| **Physics** | 물리 | `PAttack` | `PhysicsAttack` +1.5, `HP` +10 |
| **Buff** | 강화/보조 | `EventType`: `Buff` | `HP` +15, `PhysicsDefense` +0.5, `EmoDefense` +0.5 |
| **Debuff** | 약화/방해 | `EventType`: `Debuff` | `EmoSensitivity` +1.5, `CriticalDamage` +0.03 |

---

## 4. 융합 재화 및 비용 산정 규칙

### 4.1 기본 규격
* 융합은 횟수 제한 없이 **무제한** 시도 가능
* 융합 실행 버튼 클릭 시 재화(골드) 차감

### 4.2 비용 산정 방식
* **산정 기준 ($X$)**: 융합 재료에 에이전트가 포함된 경우, 해당 에이전트들의 누적 합성 횟수 중 **가장 높은 합성 횟수**를 $X$로 지정한다. (에이전트 미포함 시 $X = 0$)
* **비용 계산식**:
  $$\text{비용} = \text{기본비용} \times (X + 1)^{1.5}$$

---

## 5. FusionInfo_Result.json 데이터 구조 예시

```json
{
  "FusionRecipes": [
    {
      "RecipeID": "RECIPE_001",
      "Ingredients": [
        { "Type": "Agent", "ID": "AGENT_001" },
        { "Type": "SkillCard", "ID": "SKILL_001" },
        { "Type": "Item", "ID": "ITEM_001" }
      ],
      "Result": {
        "Type": "Agent",
        "ResultID": "AGENT_002",
        "MaxSkillInheritCount": 3
      }
    }
  ]
}
```
