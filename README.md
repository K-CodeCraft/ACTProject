# ACTProject: DirectX 11 Game Project

## 1. 프로젝트 소개 (Introduction)

**ACTProject**는 C++와 DirectX 11 API를 기반으로 개발된 3D 액션 게임 프로젝트입니다. 자체 제작된 게임 엔진을 통해 렌더링, 물리, 애니메이션, AI 등 게임의 핵심 시스템을 구현했습니다.

이 프로젝트는 플레이어, 다양한 몬스터, 보스 몬스터 컨트롤러 등을 포함하고 있어, 복잡한 게임플레이 로직과 상호작용을 구현하는 것을 목표로 합니다.

## 2. 주요 기능 (Features)

### 🎮 Custom 3D Game Engine
- **렌더링 파이프라인 (Rendering Pipeline)**: DirectX 11을 사용한 그래픽스 렌더링, 그림자(Shadow), 동적 광원(Light), 스카이박스(Skybox) 기능을 지원합니다.
- **물리 시스템 (Physics System)**: AABB, OBB 등 다양한 충돌체(Collider)를 지원하며, Rigidbody를 이용한 물리 시뮬레이션이 가능합니다.
- **게임 오브젝트 모델 (Game Object Model)**: Scene, GameObject, Component 기반의 유연한 객체 관리 시스템을 갖추고 있습니다.
- **애니메이션 시스템 (Animation System)**: `Assimp` 라이브러리를 활용하여 3D 모델의 애니메이션을 제어합니다.
- **UI 시스템 (UI System)**: 게임 내 UI와 디버깅을 위한 `ImGui`를 통합하여 사용합니다.
- **AI 및 게임플레이 (AI & Gameplay)**: A* 알고리즘을 이용한 길찾기, 플레이어와 다양한 AI 몬스터 컨트롤러를 구현했습니다.
- **리소스 관리 (Resource Management)**: 텍스처, 모델, 사운드 등 게임 리소스를 효율적으로 관리하는 시스템을 포함합니다.

## 3. 프로젝트 구조 (Project Structure)

```
ACTProject/
├── ACT-Project_DX11/      # 메인 프로젝트 폴더
│   ├── Engine/            # 게임의 핵심 기능을 담당하는 엔진 소스 코드
│   ├── Client/            # 엔진을 사용하여 게임 로직을 구현하는 클라이언트 소스 코드
│   ├── Shaders/           # HLSL 셰이더 파일
│   ├── Resources/         # 3D 모델, 텍스처 등 게임 에셋
│   ├── Libraries/         # 외부 라이브러리 (Assimp, FMOD 등)
│   └── DX11.sln           # Visual Studio 솔루션 파일
└── ...
```

## 4. 시작하기 (Getting Started)

프로젝트를 빌드하고 실행하는 방법입니다.

### 사전 요구 사항 (Prerequisites)
- **Visual Studio 2019 이상**: C++을 사용한 게임 개발 워크로드 설치 필요
- **DirectX 11 SDK**

### 빌드 방법 (Building)
1. 이 저장소를 로컬 컴퓨터에 클론합니다.
2. `ACT-Project_DX11/DX11.sln` 파일을 Visual Studio에서 엽니다.
3. 솔루션 탐색기에서 `Client` 프로젝트를 **시작 프로젝트로 설정**합니다.
4. `Debug` 또는 `Release` 모드로 솔루션을 빌드하고 실행합니다.