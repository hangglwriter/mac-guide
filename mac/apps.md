# 필수 앱 & 설치법

> 맥에서 앱을 설치하는 방법과 민티에어에 설치한 앱 목록

## 맥에서 앱 설치하는 3가지 방법

### 1. App Store

아이폰 앱스토어처럼, 맥에도 App Store가 있다. 검색 → 설치 끝.

### 2. 웹에서 다운로드 (dmg / zip)

1. 공식 사이트에서 `.dmg` 또는 `.zip` 다운로드
2. **dmg**: 더블클릭 → 열리는 창에서 앱을 Applications로 드래그
3. **zip**: 더블클릭 → 나오는 `.app` 파일을 Applications로 이동
4. 처음 실행할 때 "인터넷에서 다운로드한 앱입니다" 경고 → "열기" 클릭

### 3. Homebrew (터미널에서 한 줄 설치)

```bash
# 일반 CLI 도구 설치
brew install 패키지명

# GUI 앱 설치
brew install --cask 앱이름
```

Homebrew는 맥의 "패키지 관리자"다. 앱스토어에 없는 개발 도구나 유틸리티를 터미널 한 줄로 설치할 수 있다.

**Homebrew 설치 방법**: [터미널 - 자주 쓰는 명령어](/terminal/basic-commands) 참고

## 민티에어에 설치한 앱 목록

### 브라우저
| 앱 | 설치 방법 | 용도 |
|----|----------|------|
| Safari | 기본 내장 | 기본 브라우저 |
| Google Chrome | 웹 다운로드 | 메인 브라우저 |
| Firefox | `brew install --cask firefox` | 서브 브라우저 |
| Naver Whale | `brew install --cask naver-whale` | 네이버 서비스용 |

### 생산성 도구
| 앱 | 설치 방법 | 용도 |
|----|----------|------|
| Microsoft Word | 웹/App Store | 문서 작성 |
| Microsoft Excel | 웹/App Store | 스프레드시트 |
| Microsoft PowerPoint | 웹/App Store | 프레젠테이션 |
| Pages / Numbers / Keynote | 기본 내장 | Apple 오피스 (무료) |

### 유틸리티
| 앱 | 설치 방법 | 용도 |
|----|----------|------|
| **Shottr** | `brew install --cask shottr` | 스크린샷 캡처 (OCR, 스크롤 캡처, 주석) |
| 카카오톡 | App Store | 메신저 |

### 개발 & AI 도구
| 앱 | 설치 방법 | 용도 |
|----|----------|------|
| **iTerm2** | 웹 다운로드 (zip) | 고급 터미널 |
| **Claude** | 웹 다운로드 | AI 데스크톱 앱 |
| Claude Code | `npm install -g @anthropic-ai/claude-code` | AI 터미널 도구 |
| GitHub CLI (gh) | `brew install gh` | GitHub 터미널 관리 |

### 스마트폰 미러링
| 앱 | 설치 방법 | 용도 |
|----|----------|------|
| **scrcpy** | `brew install scrcpy` | 안드로이드 화면을 맥에 미러링 |
| android-platform-tools | `brew install --cask android-platform-tools` | scrcpy에 필요한 adb 도구 |

## Shottr - 스크린샷 앱 사용법

맥 기본 스크린샷(Cmd+Shift+4)보다 훨씬 편한 캡처 앱.

### 주요 기능
- **영역 캡처**: 단축키로 바로 캡처
- **스크롤 캡처**: 긴 페이지 전체 캡처
- **OCR (텍스트 인식)**: 캡처한 이미지에서 텍스트 추출
- **주석**: 화살표, 박스, 텍스트 추가
- **핀 기능**: 캡처를 화면 위에 고정

### 설치

```bash
brew install --cask shottr
```

### 관련 링크
- [Shottr 공식 사이트](https://shottr.cc/)

## scrcpy - 스마트폰 미러링 사용법

안드로이드 폰 화면을 맥북에 띄우는 무료 도구. 강의 중 폰 화면 시연할 때 유용.

### 설치

```bash
brew install scrcpy
brew install --cask android-platform-tools
```

### 사용법

1. 안드로이드 폰에서 **개발자 옵션** 활성화 (설정 → 소프트웨어 정보 → 빌드번호 7번 탭)
2. **USB 디버깅** 켜기
3. USB 케이블로 맥북과 연결
4. 터미널에서 실행:

```bash
sc          # 단축 명령어 (민티에어에 설정됨)
# 또는
scrcpy      # 원래 명령어
```

### 관련 링크
- [scrcpy GitHub](https://github.com/Genymobile/scrcpy)

## 앱 삭제 방법

### 간단한 방법
Applications 폴더에서 앱을 휴지통으로 드래그

### 깔끔하게 (설정 파일까지 삭제)
[AppCleaner](https://freemacsoft.net/appcleaner/) 앱 사용 - 앱을 드래그하면 관련 파일까지 찾아서 한번에 삭제

### Homebrew로 설치한 앱

```bash
brew uninstall 패키지명
brew uninstall --cask 앱이름
```
