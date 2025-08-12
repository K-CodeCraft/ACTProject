# ACTProject: DirectX 11 Game Project

## 프로젝트 소개 (Introduction)

**ACTProject**는 C++와 DirectX 11 API를 기반으로 개발된 3D 액션 게임 프로젝트입니다. 자체 제작된 게임 엔진을 통해 렌더링, 물리, 애니메이션, AI 등 게임의 핵심 시스템을 구현했습니다.

이 프로젝트는 플레이어, 다양한 몬스터, 보스 몬스터 컨트롤러 등을 포함하고 있어, 복잡한 게임플레이 로직과 상호작용을 구현하는 것을 목표로 합니다.

---

## 📹 데모
- Another Crab’s Treasure 모작: https://www.youtube.com/watch?v=rzVMixfNDG0&t=4s

---

## 🚀 주요 기능 (Features)

### 🎮 Custom 3D Game Engine
- **렌더링 파이프라인 (Rendering Pipeline)**: DirectX 11을 사용한 그래픽스 렌더링, 그림자(Shadow), 동적 광원(Light), 스카이박스(Skybox) 기능을 지원합니다.
- **물리 시스템 (Physics System)**: AABB, OBB 등 다양한 충돌체(Collider)를 지원하며, Rigidbody를 이용한 물리 시뮬레이션이 가능합니다.
- **게임 오브젝트 모델 (Game Object Model)**: Scene, GameObject, Component 기반의 유연한 객체 관리 시스템을 갖추고 있습니다.
- **애니메이션 시스템 (Animation System)**: `Assimp` 라이브러리를 활용하여 3D 모델의 애니메이션을 제어합니다.
- **UI 시스템 (UI System)**: 게임 내 UI와 디버깅을 위한 `ImGui`를 통합하여 사용합니다.
- **AI 및 게임플레이 (AI & Gameplay)**: A* 알고리즘을 이용한 길찾기, 플레이어와 다양한 AI 몬스터 컨트롤러를 구현했습니다.
- **리소스 관리 (Resource Management)**: 텍스처, 모델, 사운드 등 게임 리소스를 효율적으로 관리하는 시스템을 포함합니다.

## 📂 프로젝트 구조 (Project Structure)

```
ACTProject/
├─ ACT-Project_DX11/            # 솔루션/프로젝트 루트
│  ├─ Engine/                   # 엔진(코어) 레이어
│  │  ├─ Core/                  # 엔트리/윈도우/타이밍/입력/로깅
│  │  ├─ Graphics/              # DX11 디바이스/스왑체인/파이프라인/셰이더/리소스
│  │  ├─ Scene/                 # GameObject, Component, System, Scene 관리
│  │  ├─ Physics/               # Collider, BroadPhase(Octree), 충돌 판정/반응
│  │  ├─ Animation/             # 상태 머신, 트랜지션, 이벤트
│  │  ├─ Camera/                # 1·3인칭/컷신/디버그 카메라
│  │  └─ Utils/                 # 수학(행렬/벡터), 파일 IO, 프로파일러
│  ├─ Game/                     # 게임 레이어(플레이어/몬스터/오브젝트/스테이트)
│  ├─ Shaders/                  # HLSL (.hlsl)
│  ├─ Assets/                   # 모델/텍스처/애니메이션 데이터
│  ├─ External/                 # 외부 라이브러리(IMGUI, DirectXTex 등 선택)
│  └─ ACTProject.sln            # 솔루션
└─ docs/                        # 문서, 스크린샷, 다이어그램
```

---

## 🎮 기본 조작(예시)
| 동작 | 키 |
|---|---|
| 이동 | WASD |
| 카메라 회전 | 마우스 이동 |
| 점프 | Space |
| 회피(구르기) | Ctrl |
| 기본 공격/콤보 | LMB |
| 차지/대시 공격| Q / Shift+LMB |
| 일시정지 | Esc |

---

## 🛠 빌드
- **언어**: C++20 / **API**: DirectX 11 / **IDE**: Visual Studio 2022 / **OS**: Windows 10/11 x64
1) 레포 클론 → 2) `ACTProject.sln` 열기 → 3) x64 `Release` 또는 `Debug` 빌드 → 4) 실행(F5)  
> 첫 실행 시 `Assets/` 상대경로와 Working Directory를 확인하세요.

---