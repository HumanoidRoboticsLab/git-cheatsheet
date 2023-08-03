# Welcome to Humanoid Robotics' demo respository

### Git Uses
* 일반적으로 feature/xxxx 브랜치에서 개발 -> 완성된 feature를 develop브랜치로 Pull Request(PR) -> develop브랜치에서 feature 테스트 -> 모든게 완벽하게 돌아간다는 전제하에 최종적으로 master브랜치로 PR.
* 깃헙 사용 전략 및 브랜칭 전략은 imgs/에 예시로 넣어놨음. 본인만의 스타일 찾아도 괜찮을듯.

### Git branch Naming Rules (example)
* master
* develop
* feature/method1
* feature/method2
* feature/method3

### Git Command Cheatsheet
```console
// 원하는 특정 브랜치가 있다면 앞에 -b flag랑 브랜치 혹은 태그명을 넣어서 클론 (optional),
// 클론하는 소스의 디렉토리명을 특정하고 싶으면 뒤, [directory name]에 원하는 폴더명 기입 (optional).
$ git clone [-b branch/tag name] <remote-repo-url> [directory name]
```

```console
\\ 코드작업 시작하기 전에, git pull을 습관화해야 git 꼬이는걸 예방할 수 있음.
$ git pull origin [pull from certain branch]
\\ 작업을 위해서 branch 하나를 새로 만들고 싶다면,
\\ 아래 커맨드를 치면 알아서 해당 브랜치로 변경 됨
$ git checkout -b [branch name]
\\ 현재 내가 작업하고 있는 브랜치를 알고 싶다면,
$ git branch -a
\\ 현재 브랜치에서 다른 기존에 있던 브랜치로 바꾸고 싶으면,
$ git checkout [branch name]
```

```console
// 코드 변경 사항 확인
$ git status
// 깃허브에 푸쉬할 디렉토리 혹은 파일 추가
$ git add [directory/file path]
// 추가된 코드의 주요 변경사항에 대해 설명
$ git commit -m "commit detail"
// 원하는 타켓 브랜치에 코드 푸쉬, 일반적으로 본인이 작업하던 브랜치로 푸쉬하면 됨
$ git push origin [push to target branch] // ex: master, branch 이름, ...
```

```console
\\ 만약 변경된 소스에서 뭐가 바뀌었는지 보고싶을 때 컨맨드
\\ 파일명 뿐만 아니라 디렉토리만 기입해도, 해당 디렉토리에서의 모든 변경 사항 확인 가능
$ git diff [directory/file path]
```

```console
\\ 깃이 꼬였을땐, push도 pull도 안먹는다,
\\ 그럴땐 stash 명령어 사용, 근데 무지성으로 그냥 쓰다가 잘못해서 
\\ 본인이 작업하던 코드 다 날릴수도 있으니, 조심조심 써야하고, 웬만하면 평소에 pull잘하면 됨...
$ git stash save
$ git stash list
$ git stash pop
```

```console
$ git remote -v
```

```console
$ git submodule
```

### Ref
깃헙 명령어가 이것말고도 엄청 많은데, 참고하면 좋을 사이트들 모음입니다. ( [ref0](https://backlog.com/git-tutorial/kr/), [ref1](https://www.edureka.co/blog/git-commands-with-example/), [ref2](https://gorokke.tistory.com/22), [ref3](https://nack1400.tistory.com/entry/Git-Git-%EB%AA%85%EB%A0%B9%EC%96%B4-%ED%84%B0%EB%AF%B8%EB%84%90-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC-%EC%BB%A4%EB%A7%A8%EB%93%9C-%EB%AA%85%EB%A0%B9%EC%96%B4) )