# iTerm2 설치 & 설정

> macOS 기본 터미널 대신 쓰는 고급 터미널 앱

## iTerm2란?

맥에 기본으로 깔려있는 "터미널" 앱의 업그레이드 버전이라고 생각하면 된다. 기본 터미널로도 되지만, iTerm2가 더 편하고 기능이 많다.

## 설치 방법

### 1. 다운로드

[iTerm2 공식 사이트](https://iterm2.com/)에서 zip 파일 다운로드

### 2. 설치

```bash
# zip 파일이 Downloads에 있을 때
cd ~/Downloads
unzip iTerm2-*.zip -d /tmp/iterm_install
cp -R /tmp/iterm_install/iTerm.app /Applications/
```

또는 수동으로:
1. zip 더블클릭해서 압축 해제
2. `iTerm.app`을 Applications 폴더로 드래그
3. 기존 버전이 있으면 "Replace(대치)" 선택

### 3. 실행

- Spotlight (Cmd + Space) → "iTerm" 검색 → 실행
- "인터넷에서 다운로드한 앱입니다" 경고 뜨면 "열기" 클릭

## 버전 확인

```bash
defaults read /Applications/iTerm.app/Contents/Info.plist CFBundleShortVersionString
```

## 관련 링크

- [iTerm2 공식 사이트](https://iterm2.com/)
- [iTerm2 문서](https://iterm2.com/documentation.html)
