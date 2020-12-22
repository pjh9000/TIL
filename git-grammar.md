## Git 기초문법

> Git은 분산형 버전관리시스템 (DVCS)이다.

### Git 사전준비

1. 윈도우: [git bash](https"//gitforwindows.org/)를 설치한다.
2. 로컬 설정

```bash
$ git config --global user.name 'jhyeok-park'
$ git config --global user.email 'mintwaffle@gmail.com'
```

- 처음 git을 설치하면 , commit을 하는 자성자(author)를 설정해야 한다.
- email 정보는 github에 등록된 이메일을 설정하는 것을 추천
- 설정된 내용을 확인하기 위해서는 아래의 명령어 입력

```bash
$git config --global -l
user.name=jhyeok-park
user.email=mintwaffle@gmail.com
```

- 오프라인 강의장에서 하는 경우 반드시 체크(위에 global)

## 기초흐름

> 작업 ->ad d => commit
>
> 작업이 끝나면 ,commit할 파일을 모아서 (add), commit. (버전 기록)



## 0. 저장소 설정

```bash
$ git init

$ (master)
```

- git 저장소로 활용하기 위해서는 위의 명령어를 활용한다.
  - .git 폴더가 생성
  - (master)로 현재 작업중인 브랜치 확인

### 1. add

> commit을 위한 파일 목록(staging area)

- add 전 모습

```bash
$ touch test.txt
On branch master

No commits yet
# untracked file present: WD O
Untracked files:
	#use git add command
	#to include what should be committed
	(use "git add <file>..." to include in what will be committed)
		test.txt
# Last line : wrapping up..
# nothing added to commit : staging area X
# untracked files present : WD O
nothing added to commit but untracked fiels present (use "git add" to track)
```

- add 후 모습

```bash
$ git add .
$ git status
On branch master 

No commits yet
# any changes to be committd : SA O
Changes to be committed:
	(use "git rm --cached <file>..." to unstage)
		 # 새 파일 : test.txt
		 new file:	test.txt
```

## 2. Commit

> 버전을 기록(snapshot)

```bash
$ git commit -m 'commit message'
[master (root-commit) 93fff17] commit message
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt
```

- commit message는 현재 작업의 내용을 알 수 있도록 명확하게 작성한다.

- commit log를 확인 하기 위해서는 아래 명령어를 입력

```bash
$ git log
commit 93fff1719414946bab471e8f9de13a44909fd0ca (HEAD -> master)
Author : jhyeok-park <mintwaffle@gmail.com>
Date :	Tue Dec 22 14:35:50 2020 +0900

	commit message
```

- 추가옵션

```bash
$ git log -1
$ git log --online
93fff17 (HEAD -> amster) commit message #한줄로 나타냄
$ git log --online -1
```

## 상태 확인

> git 저장소의 현재 상태는 status로 확인하는 습관을 가지자.

```bash
$ git status
```





