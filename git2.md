## SSH 키가 생성되었다면

-   키를 ssh 에이전트에 추가

    ssh-add ~/.ssh/id_ed25519

-   저장소의 url을 ssh로 변경

    git remote set-url origin git@github.com:username/repository.git

<br><br>

---

<br><br>

## 깃 명령어

-   git
-   git init
-   git status
-   git ls-files --stage
-   git clone 원격저장소URL 새폴더이름
-   git add 파일이름 : 파일 등록
-   git rm --cached 파일이름 : 파일 등록 취소
-   git mv 파일이름 새파일이름 : 등록된 파일 이름
-   git checkout -- 수정파일이름 : 수정된 파일 되돌리기
-   git add 수정파일이름 : 스테이지에 등록
-   git commit
-   git commit -a : 파일 등록과 커밋을 동시에
-   git commit -m "커밋메시지"
-   git commit -am "커밋메시지" : 파일 등록과 한 줄짜리 커밋 메시지 등록
    -   첫번째 커밋은 예외
-   git commit --allow-empty-message -m "" : 커밋 메시지를 작성하지 않음
-   git commit --amend: 방금 전에 작성한 커밋 메시지 수정
-   git commit -v : diff 내용을 추가하여 커밋
-   git log
    -   -p : diff 기능(수정한 라인 비교)을 같이 포함하여 출력할 수 있다.
    -   --stat : 히스토리를 출력
    -   --pretty=oneline : 각 커밋을 한 줄로 표시
-   git log --pretty=shrot
-   git log 파일명
-   git show 커밋ID
-   git diff : 스테이지 vs 워킹 디렉터리 비교
-   git diff head : 최신 커밋과 변경 내용을 비교
-   git remote : 원격 저장소의 이름(별칭)을 출력
-   git remote -v : 원격 저장소의 별칭 이름과 URL을 확인
-   git remote add 원격저장소별칭 원격저장소URL
    -   git remote add origin https://~
-   git remote rename 변경전 변경후
-   git remote show 원격저장소별칭
    -   git remote show origin
-   git remote rm 원격저장소별칭 : 원격 서버 삭제
-   git oull
-   git push 원격저장소별칭 브랜치이름
    -   git push origin master

<br><br>

---

<br><br>

## 관련

-   code 파일명 : 편집기 연결
-   ls -a : 숨겨진 파일 같이 출력
-   ls .git : 깃 목록 보기
-   ls ~/.gitconfig: .gitconfig 폴더의 경로 보기

<br><br>

---

<br><br>

## .gitignore 파일 표기법

```
# 주석 표기

# 애스터리스크 \* : 패턴 정의, 문자열을 대체, \*.obj
*.obj


# 제외하지 않는 파일과 필요한 파일은 ! 사용
!config.php

# 현재 디렉터리 안에 있는 파일 무시
/readme.txt

# /pup/ 디렉토리 안의 모든 것을 무시
/pup/

# doc 디렉토리 아래의 모든 .txt 파일 무시
doc/**/*.txt

```

<br><br>

## vi 에디터

-   종료 : <kbd>:</kbd> + <kbd>q</kbd>
-   입력 : esc를 누른 후 <kbd>i</kbd>를 누른다
-   작성한 후 저장과 종료는 esc를 누른 후 : <kbd>:</kbd> + <kbd>w</kbd>, <kbd>q</kbd>

## vi 에디터 이외의 에디터를 사용하고 싶다면 깃의 환경 설정을 변경하다.

-   git config --global core.editor "에디터경로"
