# Codex·Claude 사용량 위젯과 Codex 데스크톱 펫

Windows 작업표시줄에서 Codex와 Claude의 잔여 한도를 확인하거나, 바탕화면에서 애니메이션 펫과 함께 Codex 사용량을 볼 수 있습니다.

## 작업표시줄 위젯

처음 설치한다면 V5를 선택하세요. 버전별 ZIP에는 실행에 필요한 Python 소스와 리소스가 들어 있습니다.

| 다운로드 | 주요 기능 |
| --- | --- |
| [V5 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/widget-v5/AI-Usage-Taskbar-Dock-v5.zip) | Claude CLI와 데스크톱 앱에서 확인한 값 중 더 최근의 잔여량을 표시합니다. 사용량 추이를 그래프로 보고, 관측 기록이 충분하면 예상 소진 시각도 확인할 수 있습니다. |
| [V4 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/widget-v4/AI-Usage-Taskbar-Dock-v4.zip) | 5시간·주간 잔여량을 두 줄 픽셀 게이지로 표시합니다. |
| [V3 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/widget-v3/AI-Usage-Taskbar-Dock-v3.zip) | Claude 계정 조회 옵션과 활동·시스템 상세 카드를 제공합니다. |
| [V2 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/widget-v2/AI-Usage-Taskbar-Dock-v2.zip) | Codex와 Claude를 각각 또는 함께 표시합니다. Claude 데스크톱의 로컬 기록을 활용합니다. |
| [V1 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/widget-v1/AI-Usage-Taskbar-Dock-v1.zip) | 작업표시줄 시계 옆에서 Codex 주간 잔여량을 확인하고, 위젯을 펼쳐 다음 리셋 시각을 볼 수 있습니다. |

### 위젯 실행 방법

Windows 11과 Python 3.13 기준입니다. 원하는 ZIP을 풀고, 그 안의 폴더에서 PowerShell을 열어 다음 명령을 실행하세요.

```powershell
py -3.13 -m pip install -r requirements.txt
.\start-dock.bat
```

이후에는 같은 폴더의 `start-dock.bat`을 더블클릭하면 됩니다. 다른 버전으로 전환할 때는 실행 중인 위젯을 우클릭해 **종료**한 뒤 원하는 버전을 실행하세요. V2 이상에서는 우클릭 → **설정**에서 표시할 서비스를 선택할 수 있습니다.

## Codex 데스크톱 펫

바탕화면에 좋아하는 펫을 놓아두면, 펫 옆에 Codex 잔여량과 다음 리셋 시각이 함께 표시됩니다. [펫 ZIP 다운로드](https://github.com/voltage-gated/ai-usage-widgets/releases/download/v0.1.0/codex-pet-overlay-dist.zip)

### 펫 기능

- Codex 사용량, 남은 비율, 한도 초기화 시간을 펫 옆에 표시
- 펫 6종 포함: guga, BitBoy, Byte, Java, nono, Point Fox
- 드래그로 위치 이동, 더블클릭으로 펫·크기·테마 설정
- 기본 5분 간격 조회 및 우클릭 메뉴의 수동 새로고침

표시되는 사용량 구간은 현재 로그인한 계정과 Codex가 제공하는 응답에 따라 달라질 수 있습니다.

### 펫 실행 방법

Windows 10 또는 11, Python 3.10 이상, 로그인된 Codex CLI가 필요합니다.

1. [펫 릴리스](https://github.com/voltage-gated/ai-usage-widgets/releases/tag/v0.1.0)에서 `codex-pet-overlay-dist.zip`을 다운로드하고 압축을 풉니다.
2. `install-deps.bat`을 한 번 실행해 Pillow를 설치합니다.
3. `start-pet.bat`을 실행합니다.

사용법과 설정 방법은 ZIP에 포함된 `사용자_가이드.md`를 참고하세요. 기술 구조는 `LLM_GUIDE.md`에 설명되어 있습니다.

### 펫의 사용량 조회

프로그램은 PC에 설치된 Codex CLI의 App Server를 통해 사용량을 조회합니다. 계정 비밀번호나 API 키를 프로그램에 입력할 필요가 없습니다. 로컬 세션 기록을 읽는 대체 조회 기능은 기본적으로 꺼져 있으며 설정에서 선택할 수 있습니다.

## 안내

이 프로젝트는 커뮤니티에서 만든 비공식 도구입니다. 포함된 캐릭터와 폰트의 권리는 각각의 원저작자에게 있습니다.
