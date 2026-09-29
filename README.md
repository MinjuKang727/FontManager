# FontManager
> Windows TTF & OTF 폰트 자동 설치 프로그램

폴더 내에 있는 **TTF, OTF 폰트 파일**을 하위 폴더까지 재귀적으로 탐색하여 윈도우 시스템에 자동으로 설치해주는 Python 기반 GUI 프로그램입니다.  
압축 파일(ZIP) 자동 해제 및 스마트 중복 검사 기능을 제공합니다.

<br><br>

## ✨ 주요 기능

* **자연스러운 하위 폴더 탐색**: 선택한 폴더 안의 모든 하위 폴더를 뒤져 `.ttf`, `.otf` 파일을 찾아냅니다.
* **ZIP 압축 파일 자동 해제**: 폴더 내에 있는 압축 파일(`*.zip`)을 자동으로 감지하고 임시 폴더에 해제하여 그 안의 폰트까지 깔끔하게 설치합니다.
* **스마트 중복 검사 (Pass)**: 이미 시스템에 설치되어 있거나 레지스트리에 등록된 폰트는 자동으로 건너뛰어(Pass) 중복 설치를 방지합니다.
* **시스템 자동 브로드캐스트**: 폰트 설치 직후 별도의 재부팅 없이 포토샵, 일러스트레이터, 한글, 오피스 등 실행 중인 프로그램에서 즉시 인식할 수 있도록 시스템에 신호를 보냅니다.
* **스마트 정리 옵션 지원**:
  * 압축 해제된 원본 `.zip` 파일 삭제 옵션
  * 임시로 생성된 압축 해제 폴더 자동 정리 옵션
  * 작업 완료 후 폴더 내 모든 파일 일괄 삭제 옵션 (필요시)


<br><br>


## 🛠️ 기술 스택 (Tech Stack)

* **Language**: Python 3.x (외부 라이브러리 설치 필요 없음, 순수 내장 모듈 사용)
* **GUI Framework**: `tkinter`
* **System Control**: `ctypes`, `winreg`, `shutil`, `pathlib`, `zipfile`[cite: 3]


<br><br>

## 실행 파일 다운로드
👉 [최신 버전 다운로드](https://github.com/MinjuKang727/FontManager/releases)

<br><br>

## 🚀 실행 방법 및 주의사항

1. 반드시 **관리자 권한(Administrator)**으로 프로그램을 실행해야 Windows 시스템 폴더(`C:\Windows\Fonts`)와 레지스트리(`HKEY_LOCAL_MACHINE`)에 폰트를 등록할 수 있습니다.
   * 프로그램 실행 파일 우클릭 👉 **[관리자 권한으로 실행]** 선택
   <img width="1357" height="713" alt="image" src="https://github.com/user-attachments/assets/09aa4e90-a916-4f0e-b1d9-903b75d776dc" />


2. **[폴더 선택]** 버튼을 눌러 폰트가 들어있는 폴더를 지정합니다.
3. 필요한 정리 옵션(압축 해제 여부 등)을 체크한 뒤 **[윈도우에 폰트 자동 설치 시작]** 버튼을 누릅니다.
<img width="896" height="932" alt="image" src="https://github.com/user-attachments/assets/b06f8a14-81fc-4978-86e1-eea08c4680dc" />

