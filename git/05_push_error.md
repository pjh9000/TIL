## 실습

### 사전 준비

1. 로컬
   1. bigdata/  git init
   2. README.md 파일만들고 commit

2. Github
   1.  원격 저장소 만들기
   2. 로컬 push



## 원격 저장소 충돌 재현

1. Github 파일 직접 수정

2. 로컬

   ```bash
   #변경 사항 아무거나
   $ touch test.txt
   $ git ad  .
   $ git commit -m 'add tset'
   $ git push origin master
   ```



## 원격 저장소 push 시 오류

```bash
$ git push origin master
To https://github.com/pjh9000/bigdata.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/pjh9000/bigdata.git'
hint: Updates were rejected because the remote contains work that you do
# 원격 저장소의 작업(commit)이 로컬에 없음
hint: not have locally. This is usually caused by another repository pushing
# 다른 저장소에 푸시하는 경우도 발생 가능
hint: to the same ref. You may want to first integrate the remote changes
# 원격 저장소의 변경사항을 먼저 로컬과 통합해야함
hint: (e.g., 'git pull ...') before pushing again.
# 이걸로 한 번 해결해볼래?
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

```bash
$ git log --online
# 로컬과 원격의 Commit History commit 주소 다름 
# vim 편집기가 뜬 이유 => 합쳐졌다라는 사실을 commit

$ git pull origin master
```

- 원격 저장소와 로컬 저장소의 commit history 확인 후 위 명령어 입력
  - vim 편집기 창에서 나오기

- log 확인

  ```bash
  $ git log --online
  
  # vim 편집기가 뜬 이유 => 합쳐졌다라는 사실을 커밋으로 남김
  833856a (HEAD -> master) Merge branch 'master' of https://github.com/edutak/bigdata
  # 로컬 작업한 것
  936167c Add test
  # 원격 저장소에서 작업한 것
  17e362c (origin/master) Update README.md
  38567d6 Init
  ```

- 다시 push



## pull

- 원격 저장소의 변경 사항을 받아옴 

```bash
$ git pull origin master
```



