# 자주 쓰는 명령어

> 터미널에서 일상적으로 쓰는 명령어 모음

## 이동 & 확인 (가장 많이 씀)

| 명령어 | 의미 | 설명 |
|--------|------|------|
| `pwd` | Print Working Directory | 지금 어디에 있는지 경로 표시 |
| `ls` | List | 현재 폴더의 파일/폴더 목록 |
| `ls -la` | List -long -all | 숨김 파일 포함, 상세 목록 |
| `cd 폴더명` | Change Directory | 해당 폴더로 이동 |
| `cd ..` | | 상위 폴더로 이동 |
| `cd ~` | | 홈 폴더로 이동 |
| `cd ~/Projects` | | Projects 폴더로 이동 |

### 실전 예시

```bash
# 지금 어디 있지?
pwd
# /Users/storywinner

# 여기 뭐가 있지?
ls

# Sites 폴더로 이동
cd Projects/Sites

# 상위 폴더로 돌아가기
cd ..

# 홈으로 바로 가기
cd ~
```

## 파일 & 폴더 관리

| 명령어 | 설명 | 예시 |
|--------|------|------|
| `mkdir 이름` | 폴더 만들기 | `mkdir my-project` |
| `mkdir -p a/b/c` | 중간 폴더까지 한번에 | `mkdir -p Projects/Sites/new` |
| `touch 파일명` | 빈 파일 만들기 | `touch memo.txt` |
| `cp 원본 대상` | 파일 복사 | `cp a.txt b.txt` |
| `cp -r 원본 대상` | 폴더 복사 | `cp -r old-folder new-folder` |
| `mv 원본 대상` | 이동 또는 이름 변경 | `mv old.txt new.txt` |
| `rm 파일명` | 파일 삭제 (휴지통 안 거침!) | `rm temp.txt` |
| `rm -r 폴더명` | 폴더 삭제 | `rm -r old-folder` |

> **주의**: `rm`은 휴지통을 거치지 않고 바로 삭제한다. 복구 불가능하니 신중하게!

## 파일 내용 보기

| 명령어 | 설명 |
|--------|------|
| `cat 파일명` | 파일 내용 전체 출력 |
| `head 파일명` | 앞부분 10줄만 보기 |
| `tail 파일명` | 뒷부분 10줄만 보기 |
| `open 파일명` | 기본 앱으로 파일 열기 |
| `open .` | 현재 폴더를 파인더로 열기 |

### 실전 예시

```bash
# 현재 폴더를 파인더로 열기 (자주 씀!)
open .

# 파일을 기본 앱으로 열기
open document.pdf

# 특정 앱으로 열기
open -a "Google Chrome" index.html
```

## 검색

| 명령어 | 설명 | 예시 |
|--------|------|------|
| `find . -name "파일명"` | 파일 찾기 | `find . -name "*.md"` |
| `grep "텍스트" 파일명` | 파일 안에서 텍스트 찾기 | `grep "hello" memo.txt` |
| `which 명령어` | 명령어 위치 찾기 | `which git` |

## Homebrew (맥의 앱 설치 관리자)

### 설치

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

설치 후 PATH 등록 필요 (안내 메시지를 따라하면 됨).

### 주요 명령어

| 명령어 | 설명 |
|--------|------|
| `brew install 패키지` | CLI 도구 설치 |
| `brew install --cask 앱` | GUI 앱 설치 |
| `brew uninstall 패키지` | 삭제 |
| `brew list` | 설치된 목록 |
| `brew update` | Homebrew 자체 업데이트 |
| `brew upgrade` | 설치된 패키지 전부 업데이트 |
| `brew search 키워드` | 패키지 검색 |

### 실전 예시

```bash
# 스크린샷 앱 설치
brew install --cask shottr

# GitHub CLI 설치
brew install gh

# 뭐가 설치돼있지?
brew list
```

## 민티에어에 설정된 단축 명령어 (alias)

`.zshrc` 파일에 등록해둔 명령어 별명:

| 단축 명령어 | 원래 명령어 | 용도 |
|------------|-----------|------|
| `sc` | `scrcpy` (adb 경로 포함) | 스마트폰 미러링 |
| `cldp` | `claude --dangerously-skip-permissions` | 클로드코드 (권한 스킵) |

### alias 추가하는 법

```bash
# .zshrc 파일 열기
open ~/.zshrc

# 또는 터미널에서 직접 추가
echo "alias 별명='원래명령어'" >> ~/.zshrc

# 변경사항 적용
source ~/.zshrc
```

## 기타 유용한 명령어

| 명령어 | 설명 |
|--------|------|
| `clear` | 화면 청소 (Cmd + K도 가능) |
| `history` | 이전에 입력한 명령어 기록 |
| `위쪽 화살표` | 이전 명령어 불러오기 |
| `Tab` | 자동완성 (파일명, 폴더명) |
| `Ctrl + C` | 실행 중인 명령 중단 |
| `Ctrl + L` | 화면 청소 (clear와 동일) |

> **팁**: `Tab` 키를 생활화하자. 긴 파일명/폴더명을 몇 글자만 치고 Tab 누르면 자동완성된다.
