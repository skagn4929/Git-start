# Git & Github
- [Git & Github 강의](https://www.youtube.com/watch?v=1I3hMwQU6GU)


본 강의를 통해 깃과 깃허브에 대하여 학습하고 배운 내용을 VSC를 사용하여 실습한 내용입니다.

---
## 1. Git 설치 (MAC)
- https://git-scm.com/download/mac 참조하여 Git 최신 버전 설치
  - Homebrew 설치 : https://brew.sh/ 
  - 다음 명령어로 Git 설치
      ```brew install git```

- 터미널 재실행 후 ```git --version```으로 확인   
  - 23.06.01 기준 2.41.0 버전

## 2. SourceTree 설치
- https://www.sourcetreeapp.com/ -Git을 GUI로 다룰 수 있도록 해주는 툴입니다.

## 3. Git 최초 설정
- Git 전역으로 사용자 이름과 이메일 주소를 설정
  - Github 계정과는 별도   

- 터미널 프로그램에서 아래 명령어 실행   
```git config --global user.name "기남후"```   
```git config --global user.email "skagn4929@naver.com"```   

- 기본 브랜치명 변경   
```git config --global init.defaultBranch main```

## 4. 프로젝트 생성 & Git 관리 시작
- 바탕화면에 **Git-start** 폴더를 생성하고 VSC로 열람

- 다음 명령어 입력 ```git init```
  - 새로운 Git 저장소(repository) 생성    

- 다음 파일들 생성 *tiger.yaml*, *lions.yaml*

- 파일 상태 확인 ```git status```






## Reference
- [Git-commands](https://git-scm.com/docs/git#_git_commands)

깃 명령어를 참고합니다.
