# Git & Github
- [Git & Github 강의](https://www.youtube.com/watch?v=1I3hMwQU6GU)


본 강의를 통해 깃과 깃허브에 대하여 학습하고 배운 내용을 VSC를 사용하여 실습한 내용입니다.

---
## 1. Git 설치 (MAC)
- https://git-scm.com/download/mac - 참조하여 Git 최신 버전 설치
  - Homebrew 설치 : https://brew.sh/ 
  - 다음 명령어로 Git 설치
      ```brew install git```

- 터미널 재실행 후 ```git --version```으로 확인   
  - 23.06.01 기준 2.41.0 버전

## 2. SourceTree 설치
- https://www.sourcetreeapp.com/ - Git을 GUI로 다룰 수 있도록 해주는 툴입니다.

## 3. Git 최초 설정
- Git 전역으로 사용자 이름과 이메일 주소를 설정
  - Github 계정과는 별도   

- 터미널 프로그램에서 아래 명령어 실행   
  - ```git config --global user.name "사용자 이름"```   
  - ```git config --global user.email "사용자 이메일"```   

- 기본 브랜치명 변경   
  - ```git config --global init.defaultBranch main```

## 4. 프로젝트 생성 & Git 관리 시작
- 바탕화면에 **Git-start** 폴더를 생성하고 VSC로 열람

- 다음 명령어 입력 ```git init```
  - 새로운 Git 저장소(repository) 생성    

- 다음 파일들 생성 *tiger.yaml*, *lions.yaml*

- 파일 상태 확인 ```git status```

- Git의 관리에서 특정 파일/폴더를 배제해야 할 경우
  - *.gitignore* 파일을 사용해서 배제할 요소들을 지정할 수 있습니다.
  - https://git-scm.com/docs/gitignore 참조

## 5. 변화를 타임캡슐에 담아 묻기
- 프로젝트의 변경사항들을 타임캡슐(버전)에 담기
  - 변경사항 확인 `git status` ※ untracked 파일 : Git의 관리에 들어간 적 없는 파일
  - 파일 하나 담기 `git add tigers.yaml`
  - 모든 파일 담기 `git add .`

- 타임캡슐 묻기
  - `git commit -m "FIRST COMMIT"`

- `add` 와 `commit` 한꺼번에
  - `git commit -am "커밋메시지"` ※ 새로 추가된(untracked) 파일이 없을 때 한정

## 6. Git에서 과거로 돌아가는 두 가지 방법
- `reset`: 원하는 시점으로 돌아간 뒤 이후 내역들을 지웁니다.
  - `git reset --hard (돌아갈 커밋 해시)`

- `revert`: 되돌리기 원하는 시점의 커밋을 거꾸로 실행합니다.
  - `git revert (되돌릴 커밋 해시)`

## 7. branch
프로젝트를 하나 이상의 모습으로 관리해야 할 때, 여러 작업들이 각각 독립되어 진행될 때   
이 모든 것을 하나의 프로젝트 폴더에서 진행할수 있도록 하는 것.
- 브랜치 생성 / 이동 / 삭제하기
  - `add-coach`란 이름의 브랜치 생성 `git branch add-coach`
  - 브랜치 목록 확인 `git branch`
  - `add-coach` 브랜치로 이동 `git switch add-coach`
  - 브랜치 삭제하기 `git branch -d (삭제할 브랜치명)` 

- 브랜치를 합치는 두 가지 방법
  - `merge`: 두 브랜치를 한 커밋에 이어붙입니다.
    - 브랜치 사용내역을 남길 필요가 있을 때 적합한 방식입니다.
  - `rebase`: 브랜치를 다른 브랜치에 이어붙입니다.
    - 한 줄로 깔끔히 정리된 내역을 유지하기 원할 때 적합합니다.

## 8. GitHub 시작하기
- https://github.com/ - Git으로 관리되는 프로젝트의 원격 저장소

- 가입하고 토큰 만들기
 1. `Sign up`으로 가입 후 로그인
 2. **Personal access token** 만들기
    - 우측 상단의 프로필 - `settings`
    - `Developer Settings`
    - `Personal access tokens` - `Generate new token`
    - `repo` 및 원하는 기능에 체크, 기간 설정 뒤 `Generate token`
    -  토큰 안전한 곳에 보관하기
 3. GitHub에 새 **Repository** 생성 
    - `Public`: 모두에게 보일 수 있는 프로젝트
    - `Private`: 허용된 인원만 볼 수 있는 프로젝트
 4. 협업할 팀원 추가
    - 레포지토리의 `Settings` - `Collaborators`
    - `Add people`

## 9. 원격 저장소 사용하기
- 로컬에 원격 저장소 추가 후 푸시
    - GitHub 레포지토리 생성 후 다음 명령어 입력
    - `git remote add origin (원격 저장소 주소)` - 로컬의 Git 저장소에 원격 저장소로의 연결 추가
    - `git branch -M main` - 기본 브랜치명을 `main`으로
    - `git push -u origin main` - 로컬 저장소의 커밋 내역들 원격으로 `push`(업로드)
    - `git remote` - 원격 목록 보기

- 원격으로 커밋 밀어올리기(**push**)
    - `git push`

- 원격의 커밋 당겨오기(**pull**)
    - `git pull`




---
### 참고
- [Git-commands](https://git-scm.com/docs/git#_git_commands)

다양한 깃 명령어
