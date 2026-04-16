# qn

터미널에서 빠르게 마크다운 노트를 생성하고 관리하는 CLI 도구입니다.

## 설치

```bash
# 저장소 클론
git clone https://github.com/keplerisgone/qn.git
cd qn

# bin/qn 을 PATH가 통하는 디렉토리에 복사하거나 심링크
ln -sf "$(pwd)/bin/qn" ~/.local/bin/qn
```

실행 권한이 없다면:

```bash
chmod +x bin/qn
```

## 사용법

```
qn                   노트 폴더를 에디터로 열기
qn <title>           노트 생성 또는 열기 (<title>.md)
qn -l                노트 목록 출력
qn -s <keyword>      제목 + 내용 검색
qn -d <dir>          기본 디렉토리 변경
qn -h                도움말 출력
```

### 예시

```bash
# "회의록" 노트 생성 후 에디터로 열기
qn 회의록

# 노트 목록 확인
qn -l

# "TODO" 키워드로 제목과 내용 검색
qn -s TODO

# 기본 노트 저장 위치 변경
qn -d ~/Documents/notes
```

## 설정

첫 실행 시 `~/.config/qn/.qnrc` 가 자동으로 생성됩니다.

```bash
# ~/.config/qn/.qnrc

QN_EDITOR="nvim"                   # 기본 에디터 (vim, code, nano 등)
QN_DIR="$HOME/.config/qn/notes"   # 노트 저장 디렉토리
```

설정 파일을 직접 수정하거나 `qn -d <dir>` 명령어로 디렉토리를 변경할 수 있습니다.

## 요구 사항

- bash 3.2 이상
- 기본 Unix 도구 (`find`, `grep`, `sed`)
