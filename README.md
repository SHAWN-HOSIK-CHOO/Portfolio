# Portfolio

게임개발을 즐기고 게임화(Gamify)로 일상을 즐겁게 바꾸는 것에 관심이 많습니다.

---

<details open>
<summary><h2 style="display: inline;">2026년 프로젝트</h2></summary>

<br>

### MageNet (개발 중)
- **한 줄 소개:** [핵심 게임 콘셉트 한 줄 요약을 입력해 주세요]
- **장르 / 플랫폼:** 3D Action RPG / PC
- **사용 엔진:** Unreal Engine 5.6
- **개발 기간:** 2026.03 ~ 진행 중
- **개발 인원:** 2인
- **담당 역할:** 게임플레이 기획 / 프로그래밍 / 모델링

**[상세 게임 개발 문서 (GDD & Tech Spec)](./docs/2026_magenet_gdd.md)**  
**[시연 영상 (YouTube)](#)**

</details>

---

<details open>
<summary><h2 style="display: inline;">2025년 프로젝트</h2></summary>

<br>

### Crash
<img width="300" height="300" alt="Image" src="https://github.com/user-attachments/assets/535b0ad8-676e-4085-9060-1d9765f0719d" />
<img width="450" height="300" alt="Image" src="https://github.com/user-attachments/assets/f24ed6e0-8710-4c61-a79c-de88406a5dc4" />

- **한 줄 소개:** 스케이트보드를 타고 속도와 질량을 키워 상대를 격파하는 2인 실시간 멀티플레이 결투 게임
- **장르 / 플랫폼:** 2인 온라인 배틀 액션 / PC
- **사용 엔진 / 기술:** Unity 6, Unity Relay, Unity NGO
- **개발 인원:** 2인
- **담당 역할:** 게임플레이 기획 / UI / 모델링 / 클라이언트 및 서버 프로그래밍
- **주요 특징:**
  - **속도 & 질량 기반 물리 충돌:** 더 빠르게, 더 무거운 상태에서 부딪힐수록 상대에게 강한 데미지와 먼 거리 넉백(Knockback) 부여
  - **전략적 아이템 파밍:** 필드 아이템을 획득해 질량 증가, 속도 증가, 체력 회복 등 능력을 강화
  - **승리 조건:** 상대를 필드 밖으로 날려버리거나 체력을 0으로 감소시킬 시 승리
  - **실시간 네트워크:** Unity Relay 기반 2인 대전 환경 구축

**[상세 게임 개발 문서 (GDD & Tech Spec)](./docs/2025_crash_gdd.md)**  

---

### AR 도슨트 카메라 (Art AR Camera)
<img width="300" height="300" alt="Image" src="https://github.com/user-attachments/assets/998faaa7-da05-459a-b68f-d7ecba188830" />
<img width="200" height="400" alt="Image" src="https://github.com/user-attachments/assets/78fdf553-a98a-4097-8537-fc8a0135f826" />

- **한 줄 소개:** Teachable Machine 으로 학습시킨 Tensorflow Lite 모델과 Unity AR을 연동해 미술 작품을 실시간으로 인식하고 정보를 제공하는 모바일 AR 앱
- **장르 / 플랫폼:** AR 교육용 모바일 앱 / Android (타깃 기기: Galaxy S10)
- **사용 엔진 / 기술:** Unity, Unity AR Foundation, Teachable Machine (Machine Learning Model)
- **개발 기간:** 1학기 (미술사 강의 연계 학기 프로젝트)
- **개발 인원:** 1인
- **주요 특징:**
  - **머신러닝 이미지 인식:** 수업 시간에 배운 미술 작품 데이터를 크롤링 하고, Teachable Machine으로 학습시켜 유니티 엔진과 실시간 연동
  - **유사도 기반 캐러샐 UI:** 셔터 클릭 시 ML 모델이 추론한 가장 비슷한 작품들을 확률 순으로 캐러샐(Carousel) 형태 표시
  - **인터랙티브 작품 설명:** 캐러샐의 작품 카드를 선택하면 해당 미술 작품의 상세한 해설 정보 출력
 

</details>

---

<details open>
<summary><h2 style="display: inline;">2024년 프로젝트</h2></summary>

<br>

### Escape The Wonderland
<img width="500" height="300" alt="Image" src="https://github.com/user-attachments/assets/0c0cca39-7d0d-457f-b860-a652a27e127c" />
<img width="550" height="300" alt="Image" src="https://github.com/user-attachments/assets/f93e1037-b2ad-4c7a-822a-26c688f19037" />

- **한 줄 소개:** PCG 기반의 무작위 던전을 탐험하며 타이밍 기반 랭크 시스템으로 전투를 펼치는 2D 던전 탐험 RPG
- **장르 / 플랫폼:** 2D Dungeon Crawler RPG / PC
- **사용 엔진 / 언어:** Unity / C#
- **개발 인원:** 3인
- **담당 역할:** 던전, 컨텐츠 기획 및 프로그래밍 / 전투 시스템 기획
- **주요 특징:**
  - **절차적 콘텐츠 생성 (PCG):** SunnyValleyStudio의 맵 생성 알고리즘을 프로젝트 구조에 맞춰 수정·적용해 매번 새로운 던전 환경 구축
  - **던전 진행 및 보스전:** 층별 게이트키퍼 처치 및 포털 탐색으로 고층 진입, 총 4개 던전의 정상에 위치한 보스를 처치하는 명확한 클리어 구조
  - **타이밍 기반 랭크 전투 시스템:** 공격 시 기를 모으는 원형 이펙트 타임에 맞춰 정교하게 입력할 경우 D~S 까지 랭크 상승, S 랭크 달성 시 강력한 일반 공격 발동

**[시연 영상 (YouTube)](https://youtu.be/sKflh7oV4LU)**
**[게임 관련 문서](https://github.com/SHAWN-HOSIK-CHOO/Portfolio/blob/main/Resources/EscapeTheWonderland.md)**  

---

### VRRepo
<img width="450" height="300" alt="Image" src="https://github.com/user-attachments/assets/c2266d6b-9483-40a0-8ed8-af5ca3d245a9" />
<img width="550" height="300" alt="Image" src="https://github.com/user-attachments/assets/8897392f-1149-45ee-aa24-c23553414cd5" />

- **한 줄 소개:** 시각장애인의 도시 인프라 이용 제약을 가상현실 환경에서 간접 경험하도록 설계된 게이미피케이션 VR 시뮬레이션
- **장르 / 플랫폼:** VR 체험 시뮬레이션 / Meta Quest 2
- **사용 엔진 / 기술:** Unity, Meta Quest SDK, Haptic Feedback, Spatial Audio
- **담당 역할:** 퀘스트 및 시스템 기획, 프로그래밍
- **개발 인원:** 3인
- **주요 특징:**
  - **체험형 게이미피케이션:** 제한 시간 내 이동, 보행자 충돌 회피 등 목표 제시를 통해 높은 몰입감 형성
  - **청각 기반 상황 판단 (Spatial Audio):** 신호등이 고장 난 횡단보도 등 제한된 시야 조건에서 차량 소리만으로 정차 여부를 판별하도록 유도
  - **촉각 피드백 (Haptic Feedback):** 컨트롤러 진동 반응으로 점자 블록 보행 감각을 직접 전달

**[프로젝트 보고서](https://github.com/SHAWN-HOSIK-CHOO/VR_Repo)**  
**[시연 영상 (YouTube)](https://youtu.be/yPFpLxnLda4)**

---

### Aquiet
<img width="550" height="300" alt="Image" src="https://github.com/user-attachments/assets/6ae6b5f9-5a8e-4cd2-9e2b-ea9d1d797da3" />
<img width="550" height="300" alt="Image" src="https://github.com/user-attachments/assets/949d78a1-ca82-4570-a3ef-203ab1eec9ca" />

- **한 줄 소개:** Face Tracking 기술과 수집형 게이미피케이션을 결합해 지속적인 명상 습관 형성을 돕는 모바일 AR 앱  
- **장르 / 플랫폼:** AR 명상 & 게이미피케이션 / Mobile  
- **사용 엔진 / 기술:** Unity, Unity AR Foundation (Face Tracking)  
- **담당 역할:** 물고기 수집 시스템 기획 / 프로그래밍 / UI 디자인  
- **개발 인원:** 3인  
- **주요 특징:**  
  - **자가진단 & 명상 세션:** 사용자 자가진단 완료 후 5분간의 AR 명상 환경 제공  
  - **Face Tracking 기반 집중도 측정:** 트래킹 기술을 통해 5분간 가만히 유지한 정도를 감지하고 화면에 물이 차오르는 시각적 피드백 전달  
  - **수집 요소 기반 게이미피케이션:** 자가진단 결과와 명상 집중도에 따라 차별화된 물고기 종류와 크기를 보상으로 지급해 지속적인 이용(주 2~3회) 유도  

**[시연 영상 (YouTube)](https://youtu.be/3gmM3KpIsLM)**

</details>

---

## Tech Stack
- **Engines & Hardware:** Unreal Engine 5.6, Unity 6, Unity AR Foundation, Meta Quest 2
- **Networking & ML:** Unity Relay, Unity NGO, Teachable Machine
- **Languages:** C#, C++, Blueprints
