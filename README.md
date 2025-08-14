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
Another Crab's Treasure (DirectX 11 Engine)
│
├── Engine (자체 제작 게임 엔진)
│   ├── Core Systems & Managers (Singleton Pattern)
│   │   └── Scene, Time, Input, Sound, Resource...
│   │       - 엔진 전반의 핵심 기능과 매니저 클래스
│   │       - 싱글톤 패턴으로 전역 접근 및 상태 관리
│   ├── Rendering Pipeline
│   │   └── Graphics, Camera, Light, Instancing (Flyweight)...
│   │       - DirectX 11 기반 렌더링 처리
│   │       - Flyweight 패턴을 활용한 인스턴싱 최적화
│   ├── Physics System
│   │   └── Collision, Rigidbody, Octree...
│   │       - 충돌 감지 및 물리 연산 처리
│   │       - 옥트리(Octree)를 통한 공간 분할 및 연산 효율화
│   └── Game Object Model
│       └── GameObject, Component, Transform (Component Pattern)
│           - 컴포넌트 패턴 기반 객체 모델
│           - 재사용성과 기능 확장성 강화
│
├── Client (게임 콘텐츠 및 로직)
│   ├── Main.cpp (프로그램 진입점)
│   │   - 엔진 초기화 및 게임 루프 실행
│   ├── Controllers (State Pattern)
│   │   └── Player, Monsters, Bosses...
│   │       - 상태 패턴 기반의 캐릭터/오브젝트 동작 제어
│   └── Game Scenes
│       └── Title, In-Game...
│           - 씬 전환 및 콘텐츠 구성
│
├── Shaders (HLSL)
│   - GPU 연산 및 렌더링 파이프라인 전용 쉐이더 코드
│
└── Resources (Assets)
    - 모델, 텍스처, 사운드 등 게임 리소스

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
