# ChoiDaeYoung
### Unity · C# Game Client Developer

Unity와 C#으로 게임플레이와 게임 시스템을 구현합니다.  
모바일 게임, Photon Fusion 기반 멀티플레이, 데이터로 구성하는 스킬 시스템과 빌드 자동화 프로젝트를 정리했습니다.

[기술 블로그](https://young-94.tistory.com/) · [전체 저장소](https://github.com/ChoiDaeYoung-94?tab=repositories)

## 대표 프로젝트

| 프로젝트 | 소개 | 주요 구현 · 살펴볼 내용 |
| :--- | :--- | :--- |
| **[Monster Tamer](https://github.com/ChoiDaeYoung-94/Tamer)** | 몬스터를 동료로 모아 전투하는 Android 3D 게임 | 이동·전투·동료·버프, PlayFab 연동, 광고·IAP |
| **[SuddenForce-FPS](https://github.com/ChoiDaeYoung-94/SuddenForce-FPS)** | Photon Fusion 기반 3D 멀티플레이 FPS | 멀티플레이, 재활용 스크롤 UI, Additive 씬 전환 |
| **[SkillSystem](https://github.com/ChoiDaeYoung-94/SkillSystem)** | 블리츠크랭크 Q 스킬을 재현한 시스템 프로젝트 | Actor / Skill / Effect 구조, CSV 기반 스킬 설정 |
| **[Incremental](https://github.com/ChoiDaeYoung-94/Incremental)** | 2D 방치형 게임의 기반 시스템 | 오브젝트 풀링, 로그인·데이터 저장, 게임 UI |
| **[unity-cicd](https://github.com/ChoiDaeYoung-94/unity-cicd)** | Unity Android 빌드 자동화 스크립트와 가이드 | GitHub Actions, Python CLI, 빌드 버전 관리 |

## 코드로 보는 구현

### 게임플레이 · 서비스 연동
**Monster Tamer** — [게임플레이 코드](https://github.com/ChoiDaeYoung-94/Tamer/tree/main/Assets/Scripts/Creatures) · [관리자 코드](https://github.com/ChoiDaeYoung-94/Tamer/tree/main/Assets/Scripts/Managers) · [트레일러](https://github.com/user-attachments/assets/243e5193-5e8f-4966-8b98-c724b62767dd)

플레이어와 몬스터의 이동·전투·동료·버프 처리, 데이터와 서비스 연동을 살펴볼 수 있습니다. 현재 Unity 6 / Android 환경으로 복구·검증을 진행 중이며, 검증 결과와 남은 작업은 [개발 문서](https://github.com/ChoiDaeYoung-94/Tamer/blob/main/docs/revival/completion-summary.ko.md)에 정리되어 있습니다.

### 스킬 구조 · 데이터 분리
**SkillSystem** — [Actor](https://github.com/ChoiDaeYoung-94/SkillSystem/blob/main/Assets/Scripts/Actor.cs) · [Skill](https://github.com/ChoiDaeYoung-94/SkillSystem/blob/main/Assets/Scripts/Skill.cs) · [Effect](https://github.com/ChoiDaeYoung-94/SkillSystem/blob/main/Assets/Scripts/Effect.cs) · [스킬 데이터](https://github.com/ChoiDaeYoung-94/SkillSystem/blob/main/Assets/Skill_Info.csv)

여러 캐릭터에 적용할 수 있도록 액터·스킬·효과를 나누고, 스킬 정보를 CSV에서 설정하도록 구성한 프로젝트입니다.

### 멀티플레이 · UI · 씬 전환
**SuddenForce-FPS** — [게임 코드](https://github.com/ChoiDaeYoung-94/SuddenForce-FPS/tree/main/Assets/Scripts) · [룸 목록 UI](https://github.com/ChoiDaeYoung-94/SuddenForce-FPS/blob/main/Assets/Scripts/UI/RecyclableScrollView/RoomManage.cs) · [씬 관리자](https://github.com/ChoiDaeYoung-94/SuddenForce-FPS/blob/main/Assets/Scripts/Managers/SceneManager.cs)

Photon Fusion을 사용한 멀티플레이 프로젝트입니다. 재활용 스크롤 UI와 대상 씬을 Additive로 로드한 뒤 기존 씬을 해제하는 전환 방식을 적용했습니다.

### 개발 도구 · 공통 기반
**[unity-cicd](https://github.com/ChoiDaeYoung-94/unity-cicd)**에는 Unity 빌드 스크립트, Python CLI와 GitHub Actions 구성을, **[project-base](https://github.com/ChoiDaeYoung-94/project-base)**에는 프로젝트 시작에 사용하는 공통 씬·스크립트·프리팹을 정리했습니다. 빌드 자동화 저장소에는 기존 App Center 배포 구성이 포함되어 있습니다.

## 프로젝트에서 사용한 기술

- **게임 개발:** Unity, C#, Android
- **멀티플레이 · 서비스:** Photon Fusion, PlayFab, Google Play Games, Unity IAP, Google Mobile Ads
- **UI · 데이터:** DOTween, CSV 기반 설정, 오브젝트 풀링
- **개발 도구:** Git, GitHub Actions, Python, Unity Editor 빌드 스크립트

---
게임의 동작은 영상으로, 구현 방식은 코드로 확인하실 수 있도록 프로젝트별 링크를 연결했습니다.
