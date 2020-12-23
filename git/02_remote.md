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

## Clone

```bash
$ git clone ___
$ git add .
$ git commit -m '__'
```

- 다른 장소에서도 이어서 작업 가능

```bash
$ git push origin master
```

- 같은 이름의 폴더 가지고 있으면 안된다.
- 로컬 저장소의 폴더 생성됨. 아니면 로컬 저장소에 저장경로를 다르게 하든가

 - Clone vs zip download 
   - Clone - 이력까지. 
   -  zip download - 최신파일만

## DVCS, CVCS

### DVCS (분산형 버전 관리 시스템)

- 한 곳 불나도 다른 곳 안전. 이력 보존



### CVCS (중앙 버전 관리 시스템)

- 한 곳 불나면 망

