# Sunrise Capture

**최신 정식 릴리즈: v4.2.1 (2026-10-28)** · Windows 10/11 x64 · 설치형

Sunrise Capture는 보고서 작성, 업무 매뉴얼 제작, 오류 기록, 자료 검토 등에서 화면을 캡처·녹화·편집하고 관리하는 Sunrise Group의 데스크톱 프로그램입니다.

[**v4.2.1 다운로드 및 릴리즈 안내**](https://github.com/Peter-msk/Sunrise_capture/releases/tag/v4.2.1) · [공지사항](https://github.com/Peter-msk/Sunrise_capture/blob/main/notice.txt)

## v4.2.1 주요 업데이트

- **전후 화면 비교:** 동일 화면 영역을 두 번 캡처하여 나란히 배치하고 변화 영역을 표시합니다. UI 수정 전후 확인, 오류 증빙, 업무 보고에 활용할 수 있습니다.
- **비차단 오류 안내:** 일반 캡처 오류가 발생했을 때 모달 확인창이 작업을 막지 않도록 안내와 화면 복구 절차를 개선했습니다.
- **Sunrise Control v1 정책 재점검:** 실행·업데이트 제어, 네트워크 장애 시 캐시·기본 정책 처리의 정합성을 보완했습니다.
- **빌드·보안 체계 유지:** PowerShell/PS1을 사용하지 않는 CMD + Python 빌드, 서명 및 SHA-256 무결성 확인, 설치형 업데이트 계약을 유지했습니다.

## 주요 기능

| 분류 | 제공 기능 |
| --- | --- |
| 기본 화면 캡처 | 지정 영역, 반복 영역, 전체 화면, 활성 창, 모니터 선택 |
| 복합 캡처 | 다중영역 캡처, 스크롤 캡처, JPG 바로 저장 |
| 전후 화면 비교 | 동일 영역 변경 전·후 비교 및 변화 부분 표시 |
| 화면 녹화 | 영역 지정 MP4 녹화, 품질 선택, 일시정지/재개 |
| 이미지 편집 | 펜, 화살표, 도형, 텍스트, 형광펜, 모자이크, 되돌리기 |
| 결과 관리 | 저장·다른 이름으로 저장·클립보드 복사·최근 항목·플로우 이미지·복구 |

## 설치 및 사용

1. [v4.2.1 정식 릴리즈](https://github.com/Peter-msk/Sunrise_capture/releases/tag/v4.2.1)에서 `SunriseCapture_Setup.exe`를 내려받습니다.
2. 설치하고 프로그램을 실행합니다.
3. 필요한 캡처 또는 녹화 기능을 선택하고 대상 영역을 지정합니다.
4. 결과를 편집하고 파일로 저장하거나 클립보드로 복사합니다.
5. 기존 사용자에 대한 앱 내 업데이트 알림은 **Sunrise Control의 현재 정책 및 버전 판단**에 따라 적용됩니다.

설치된 프로그램 사용에는 별도 Python 설치가 필요하지 않습니다. Windows 보안 정책이나 일부 보호 화면에 의해 캡처가 제한될 수 있습니다.

## 업데이트·보안 운영

- 중앙 Control v1은 제품별 `operation`, `update`, `minimum_version`을 통해 실행 및 업데이트 허용 여부를 결정합니다. **운영 정책은 원격 Control 설정을 따르며 수시로 달라질 수 있습니다.**
- 업데이트가 실제 허용되고 새 버전이 확인되면 프로그램의 업데이트 계약에 따라 처리됩니다.
- 공식 설치파일의 서명 및 무결성 검증 정책을 유지합니다.
- 개발용 빌드 진입점은 Windows CMD 기반 `BUILD.cmd Release /noninteractive`이며 PowerShell 스크립트를 사용하지 않습니다.

## 릴리즈 정보

- **현재 공개 배포:** [v4.2.1](https://github.com/Peter-msk/Sunrise_capture/releases/tag/v4.2.1)
- 설치 파일: `SunriseCapture_Setup.exe`
- [이전 버전 및 전체 릴리즈](https://github.com/Peter-msk/Sunrise_capture/releases)
- [업데이트 공지](https://github.com/Peter-msk/Sunrise_capture/blob/main/notice.txt)

---
Copyright © 2026 Sunrise Group. All rights reserved.
