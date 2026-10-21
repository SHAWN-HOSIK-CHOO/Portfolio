# Portfolio

---

<details open>
<summary><h2 style="display: inline;">2026년 프로젝트</h2></summary>

<br>

### MageNet (개발 중)
* **한 줄 소개:** [핵심 게임 콘셉트 한 줄 요약을 입력해 주세요]
* **장르 / 플랫폼:** 3D Action RPG / PC
* **사용 엔진:** Unreal Engine 5.6
* **개발 기간:** 2026.03 ~ 진행 중
* **개발 인원:** 2인
* **담당 역할:** 게임플레이 기획 / 프로그래밍 / 모델링

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

* **한 줄 소개:** 스케이트보드를 타고 속도와 질량을 키워 상대를 격파하는 2인 실시간 멀티플레이 결투 게임
* **장르 / 플랫폼:** 2인 온라인 배틀 액션 / PC
* **사용 엔진 / 기술:** Unity 6, Unity Relay, Unity NGO
* **개발 인원:** 2인
* **담당 역할:** 게임플레이 기획 / UI / 모델링 / 클라이언트 및 서버 프로그래밍
* **주요 특징:**
  - **속도 & 질량 기반 물리 충돌:** 더 빠르게, 더 무거운 상태에서 부딪힐수록 상대에게 강한 데미지와 먼 거리 넉백(Knockback) 부여
  - **전략적 아이템 파밍:** 필드 아이템을 획득해 질량 증가, 속도 증가, 체력 회복 등 능력을 강화
  - **승리 조건:** 상대를 필드 밖으로 날려버리거나 체력을 0으로 감소시킬 시 승리
  - **실시간 네트워크:** Unity Relay 기반 2인 대전 환경 구축

**[상세 게임 개발 문서 (GDD & Tech Spec)](./docs/2025_crash_gdd.md)**  

---

### AR 도슨트 카메라 (Art AR Camera)
<img width="300" height="300" alt="Image" src="https://github.com/user-attachments/assets/998faaa7-da05-459a-b68f-d7ecba188830" />
<img width="200" height="400" alt="Image" src="https://github.com/user-attachments/assets/78fdf553-a98a-4097-8537-fc8a0135f826" />

* **한 줄 소개:** Teachable Machine 학습 모델과 Unity AR을 연동해 미술 작품을 실시간으로 인식하고 정보를 제공하는 모바일 AR 앱
* **장르 / 플랫폼:** AR 교육용 모바일 앱 / Android (타깃 기기: Galaxy S10)
* **사용 엔진 / 기술:** Unity, Unity AR Foundation, Teachable Machine (Machine Learning Model)
* **개발 기간:** 1학기 (미술사 강의 연계 학기 프로젝트)
* **담당 역할:** [예: AR 카메라 인터페이스 구축, ML 모델 연동, 캐러샐 UI 구현]
* **주요 특징:**
  - **머신러닝 이미지 인식:** 수업 시간에 배운 미술 작품 데이터를 Teachable Machine으로 학습시켜 유니티 엔진과 실시간 연동
  - **유사도 기반 캐러샐 UI:** 셔터 클릭 시 ML 모델이 추론한 가장 비슷한 작품들을 확률 순으로 캐러샐(Carousel) 형태 표시
  - **인터랙티브 작품 설명:** 캐러샐의 작품 카드를 선택하면 해당 미술 작품의 상세한 해설 정보 출력

**[상세 개발 문서 & 프로젝트 보고서](./docs/2025_art_ar_gdd.md)**  
**[프로젝트 Repository 바로가기](#)**

</details>

---

<details>
<summary><h2 style="display: inline;">2024년 프로젝트</h2></summary>

<br>

### Escape The Wonderland
<img width="500" height="300" alt="Image" src="https://github.com/user-attachments/assets/0c0cca39-7d0d-457f-b860-a652a27e127c" />

* **한 줄 소개:** PCG 기반의 무작위 던전을 탐험하며 타이밍 기반 랭크 시스템으로 전투를 펼치는 2D 던전 탐험 RPG
* **장르 / 플랫폼:** 2D Dungeon Crawler RPG / PC
* **사용 엔진 / 언어:** Unity / C#
* **개발 인원:** 3인
* **담당 역할:** 던전 및 컨텐츠 기획 및 프로그래밍 / 
* **주요 특징:**
  - **절차적 콘텐츠 생성 (PCG):** SunnyValleyStudio의 맵 생성 알고리즘을 프로젝트 구조에 맞춰 수정·적용해 매번 새로운 던전 환경 구축
  - **던전 진행 및 보스전:** 층별 게이트키퍼 처치 및 포털 탐색으로 고층 진입, 총 4개 던전의 정상에 위치한 보스를 처치하는 명확한 클리어 구조
  - **타이밍 기반 랭크 전투 시스템:** 공격 시 기를 모으는 원형 이펙트 타임에 맞춰 정교하게 입력할 경우 D~S 까지 랭크 상승, S 랭크 달성 시 강력한 일반 공격 발동

**[상세 게임 개발 문서 (GDD & Tech Spec)](./docs/2024_wonderland_gdd.md)**  
**[시연 영상 (YouTube)](https://youtu.be/sKflh7oV4LU)**

</details>

---

## Tech Stack
- **Engines:** Unreal Engine 5.6, Unity 6, Unity AR Foundation
- **Networking & ML:** Unity Relay, Teachable Machine
- **Languages:** C#, C++, Blueprints
