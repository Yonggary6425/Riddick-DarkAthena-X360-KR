# 리딕 연대기: 어설트 온 다크 아테나 (Xbox 360) 비공식 한글 패치

*The Chronicles of Riddick: Assault on Dark Athena* Xbox 360 북미판(Title ID `494707EE`)을 Xenia Canary에서 한글로 즐기기 위한 팬 번역 패치입니다.

한글화: **Yonggary6425**

## 다운로드

[Releases](../../releases/latest) 페이지에서 `Riddick_DarkAthena_X360_KR_Patch_v1.0.zip`을 받으세요. 변경 내용은 [RELEASE_NOTES.md](RELEASE_NOTES.md)에 있습니다.

> 저장소의 초록색 **Code > Download ZIP**으로 받은 파일은 패처로 쓸 수 없습니다. 패치 데이터(`.rkp`)가 Releases의 zip에만 들어 있습니다.

게임 ISO는 제공하지 않습니다. 본인이 소유한 게임에서 직접 덤프한 원본 ISO가 있어야 합니다.

## 준비물

| 항목 | 내용 |
|---|---|
| 원본 ISO | `Chronicles of Riddick, The - Assault on Dark Athena (USA) (En,Fr,De,Es,It).iso` |
| 크기 | 7,838,695,424 바이트 |
| MD5 | `45402d19d28f80915ada6b74f2bf25ba` |
| 에뮬레이터 | Xenia Canary |
| 디스크 여유 공간 | 약 8GB |
| 운영체제 | Windows (PowerShell 기본 포함, 별도 설치 없음) |

## 적용 방법

1. zip 파일의 압축을 풉니다.
2. `한글패치_적용.bat`을 실행합니다. 원본 ISO를 bat 파일 위에 끌어다 놓아도 됩니다.
3. 원본 ISO를 MD5로 확인한 뒤 같은 폴더에 `... [KOR].iso`를 새로 만듭니다. 원본은 수정하지 않습니다.
4. 안내에 따라 Xenia Canary 폴더를 지정하면 `patches` 폴더에 메뉴 한글용 코드 패치가 설치됩니다.
5. Xenia Canary에서 `[KOR].iso`를 실행합니다.

권장 Xenia 설정(`xenia-canary.config.toml`):

```toml
readback_resolve = "fast"
force_depth_clamp = true
```

> **`[KOR].iso`와 `494707EE - Assault on Dark Athena.patch.toml`은 짝으로 동작합니다.**
> 패치 파일 없이 `[KOR].iso`를 실행하면 큐브 메뉴 글자가 깨집니다.
> 영어 원본 ISO를 실행할 때는 `patches` 폴더에서 이 파일을 빼 두세요.

## 한글화 범위

- 메뉴, UI, 목표, 튜토리얼, 아이템, 멀티플레이 문자열 3,872개
- 대사 자막 66,237개 항목 (고유 문장 6,025개, 전체 대사 2회 검수)
- 큐브 메뉴(시작 메뉴, 옵션, 정보 창 등) 한글 표시
- 추가 콘텐츠의 인물 소개와 소설 발췌문
- 이미지 속 영문 일부 (조작법 화면, 지도 5장, 모드/메뉴 로고 9종)
- 시작 시 ESRB 화면 다음에 한글화 안내 화면 약 4초

음성은 영어 그대로이고, 제작진 이름과 상표는 번역하지 않았습니다.

## 알려진 제한

- Xenia Canary 전용입니다. 큐브 메뉴 한글 표시에 Xenia 코드 패치를 쓰므로 Xbox 360 실기는 지원하지 않습니다.
- 지원하는 원본은 위 MD5의 북미판 ISO뿐입니다.
- 저장 안내 화면의 작은 글자는 직접 확인하지 못했고, 검수로 바뀐 대사 대부분은 실제 플레이로 확인하지 못했습니다.

## 문제 해결

| 증상 | 확인할 내용 |
|---|---|
| `크기 불일치` 또는 `MD5 불일치` 오류 | 위 표의 크기와 MD5가 같은 수정되지 않은 북미판 ISO가 필요합니다. 다른 지역판이나 이미 패치한 ISO는 쓸 수 없습니다 |
| `[KOR].iso`의 큐브 메뉴 글자가 깨짐 | Xenia의 `patches` 폴더에 `494707EE - Assault on Dark Athena.patch.toml`이 있는지 확인하세요 |
| 영어 원본 ISO의 메뉴 글자가 깨짐 | `patches` 폴더에서 위 파일을 빼 두세요 |
| 결과 ISO 검증 실패 | 디스크 여유 공간을 확인하고 zip을 다시 받아 압축을 푼 뒤 실행하세요 |

## 저장소 구성

| 경로 | 내용 |
|---|---|
| `RELEASE_NOTES.md` | 배포판별 안내와 체크섬 |
| `patcher/` | 적용 스크립트, 안내문, Xenia 코드 패치. 패치 데이터(`.rkp`)는 용량 때문에 Releases에만 있습니다 |
| `source/` | 번역 빌드와 ISO 패치에 쓴 Python 스크립트 |
| `translation/` | 문자열 ID별 한국어 번역 |
| `docs/` | 파일 형식과 빌드 과정 기술 노트 |

게임에서 추출한 파일과 영어 원문 대사는 저장소에 포함하지 않았습니다. 그래서 이 저장소만으로는 패치를 다시 빌드할 수 없습니다. 자세한 내용은 [docs/기술노트.md](docs/기술노트.md)를 참고하세요.

## 저작권 및 면책

- 이 프로젝트는 비공식 팬 번역이며 Starbreeze, Tigon Studios, Atari, Vivendi 등 원저작권사와 무관합니다.
- 게임 ISO를 공유하거나 요청하지 마세요. 상업적으로 이용하지 마세요.
- 패치 파일에는 ISO 전체가 아니라 바뀐 구간만 들어 있으며, 그 구간에는 다시 인코딩된 게임 텍스처와 대사 파일 구조 일부가 포함됩니다.
- 권리자의 요청이 있으면 해당 내용을 내리겠습니다.
- 한글 글자는 [Noto Sans KR](https://fonts.google.com/noto/specimen/Noto+Sans+KR)(SIL Open Font License 1.1)로 만들었습니다. `patcher/LICENSE_OFL.txt`를 참고하세요.
