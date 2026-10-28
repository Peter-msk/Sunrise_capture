# Sunrise Capture

**개발 기준본: v4.2.1** · **현재 공개 설치본: v4.2.0** · Windows 10/11 x64

Sunrise Group의 업무용 화면 캡처·녹화·편집 프로그램입니다. 보고서 작성, 오류 기록, 업무 매뉴얼 제작, UI 변경 전후 검증 등에서 사용할 수 있습니다.

> **배포 상태 (2026-10-28):** v4.2.1은 소스 검증을 완료한 개발·인계 기준본이며, **Windows 실빌드/설치 검증 및 v4.2.1 설치본 배포는 아직 완료되지 않았습니다.** 현재 공개 설치본과 `latest.json`은 v4.2.0입니다. Sunrise Control v1의 `sunrise_capture` 정책은 `operation=allow`, `update=block`으로 **업데이트가 중지**되어 있습니다. 이 README/공지 갱신은 자동 업데이트나 배포를 시작하지 않습니다.

## 주요 기능

- 영역·반복 영역·다중영역·전체 화면·모니터별·활성 창 캡처
- 스크롤 캡처 및 영역 MP4 녹화
- **전후 화면 비교:** 동일 영역의 변경 전후 이미지를 나란히 배치하고 변화 영역을 강조 (v4.2.1 개발 기준본에 포함)
- 이미지 편집: 펜·도형·화살표·텍스트·형광펜·모자이크, 되돌리기/다시실행
- 클립보드 복사, JPG 저장, 최근 항목·플로우 이미지·작업 복구
- 일반 캡처 오류의 **비모달 안내** 및 작업 화면 복구

## v4.2.1 개발 기준본 변경사항

1. 제품 버전 식별자를 **4.2.1**로 통일했습니다(본체·Updater·설치 패키징 템플릿 및 소스 검증 기준).
2. Control v1 / revision 2와 정합되도록 **오프라인·유효 캐시 없음 상태의 업데이트 기본값을 `block`**으로 변경했습니다.
3. 전후 화면 비교 기능과 일반 오류의 비차단 알림을 유지했습니다.
4. PowerShell/PS1을 사용하지 않는 **CMD + Python 빌드** 구조 및 검증 완료된 소스 검사 재사용 정책을 유지합니다.
5. 소스 검증 **267 tests(실패 0, 오류 0, 환경 skip 1)** 및 Release validator **253/253 PASS**. **Windows 4.2.1 실빌드·설치·GUI 검증은 PENDING**입니다.

## Windows 환경과 개발 검증

| 구분 | 기준 |
| --- | --- |
| 운영체제 | Windows 10 / 11 x64 |
| 공개 설치본 | [v4.2.0 Release](https://github.com/Peter-msk/Sunrise_capture/releases/tag/v4.2.0) |
| 개발 소스 버전 | v4.2.1 (Windows 동적 Gate 진행 전) |
| 빌드 셸 | CMD-only (PowerShell/PS1 미사용) |
| 개발 소스 Windows 빌드 진입점 | `BUILD.cmd Release /noninteractive` |
| 설치/실행 검증 진입점 | `scripts\\RUN_WINDOWS_VALIDATION.cmd /noninteractive` |
| 중앙 운영정책 | Control v1/revision 2, 실행 허용·업데이트 차단 |

## 설치 및 이용

현재 이용 가능한 공식 Windows 설치파일은 [GitHub Releases](https://github.com/Peter-msk/Sunrise_capture/releases)에서 확인할 수 있습니다. v4.2.1 개발 소스 ZIP은 **설치 실행파일이 아니며**, 확인된 Windows Release 빌드와 설치 검증 전에는 새 정식 배포본으로 안내하지 않습니다.

1. 공식 설치본을 내려받아 설치합니다.
2. 캡처·녹화 도구를 선택해 업무 화면을 기록합니다.
3. 필요한 경우 결과를 편집하고 저장·복사합니다.
4. 정책상 허용되는 경우에만 중앙 Control과 제품 업데이트 계약에 따라 업데이트합니다.

## 업데이트 및 보안 정책

- 운영 Control: `[product.sunrise_capture] operation=allow / update=block / minimum_version=공란`.
- 네트워크 장애·유효 캐시 없음 시 기본동작: `operation=allow / update=block`.
- 중앙 Control이 허용하고 신규 버전이 실제로 제공되는 경우에만 필수 업데이트 UI(업데이트 실행 또는 창 닫기→프로그램 종료)가 적용됩니다.
- `latest.json`, 공개 릴리즈, 중앙 Control 설정은 **별도 승인 없이 변경하지 않습니다**.
- 공식 설치 파일은 서명 및 SHA-256 무결성 검증 계약을 따릅니다.

## 관련 자료

- [현재 공지사항](https://github.com/Peter-msk/Sunrise_capture/blob/main/notice.txt)
- [공식 릴리즈 목록](https://github.com/Peter-msk/Sunrise_capture/releases)
- [중앙 Control 정책 저장소](https://github.com/Peter-msk/Sunrise_Control)

---
Copyright © 2026 Sunrise Group. All rights reserved.
