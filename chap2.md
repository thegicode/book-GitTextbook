# 2장

> $ git 명령어 또는 옵션

```
git help --a
git --version
명령어를 여러개 묶어서 사용 : git tag; git branch
```

## config 명령어

```
$ git config 설정값
$ git config --unset 이메일주소
옵션 확인 : $ git config -help
```

## 로컬 사용자

cd 저장소 폴더 (깃 저장소 폴더)

```
$ git config user.name "사용자이름"
$ git config user.email "이메일주소"
```

## 글로벌 사용자(추천)

```
$ git config --global user.name "사용자이름"
$ git config --global user.email "이메일주소"

```

## 환경 설정 파일 확인 및 직접 수정

```
$ mkdir gitstudy02
$ cd gitstudy02

$ git init

$ git config user.name "username"
$ git config user.email "user@email.com"

$ ls .git

$ ls ~/.gitconfig : gitconfig 폴더의 경로보기

$ cat .git/config

$ code .git/config

// 환경 설정 파일을 직접 수정하면 철자 오류 등 여러가지 이유 때문에 정상적으로 동작하지 않을 수 있으니, 가능하면 config 명령어를 사용 권장
$ git config --global color.ui auto

```

## 별칭

별칭은 복잡한 깃 명령어를 단순하게 닉네임 형태로 등록해 두는 기능

```
$ git config --global alias.show-graph 'log --graph --pretty=oneline'
```
