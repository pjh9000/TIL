## 원격저장소 활용

> 원격 저장소 (remote repository)를 제공하는 서비스는 github, gitlab, bitbucket 등이 있다. 

```bash
$ git remote add origin (url)

```

- 깃아 원격저장소를 추가해줘. (add) origin이라는 이름으로 URL을

- 원격 저장소 설정을 삭제하는 명령어는 다음과 같다.

  ```bash
  $ git remote rm origin
  ```



## 2. 원격 저장소 확인하기

```bash
$ git remove -v
origin https://github.com/jhyeok-park/project-test.git (fetch)
origin https://github.com/jhyeok-park/project-test.git (push)
```



## 3. push

```bash
$ git push origin master
```

- `origin` 저장소의 `master` 브랜치로 `push`

## 로컬 저장소 설정

1. TIL 폴더를 로컬 저장소로 정의

2. commit

---

## 원격 저장소 설정

1. 저장소를 새로 만들고
2. remote로 추가하고
3. push

```bash
$ git init
$ git status
$ git add .
$ git commit -m "메시지"
$ git log
$ git remote add origin url
$ git push origin master
```

