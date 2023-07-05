# git & github 

## Git의 사용목적과 장점
1. Git은 프로젝트의 **시간과 차원**을 자유롭게 넘나들수 있도록 해줍니다.
* **시간** - 프로젝트의 버전을 과거로 되돌리거나 특정 내역을 취소할 수 있습니다.
* **차원** - 프로젝트의 여러 모드를 쉽게 전환하고 관리할 수 있습니다.

2. Git은 여러 사람들이 프로젝트에서 **협업**할 수 있도록 도와줍니다.
___

## Git을 사용하는 방법은 아래의 둘로 나뉘게 됩니다. 

  1. 터미널에 명령어를 이용하는 CLI 방식 (ex: gitbash, cmd)
![gitbash](https://blog.kakaocdn.net/dn/n1QDr/btqCJlFVXg4/QZCZAKcQXNRkRtxB3vnkoK/img.png)
  2. 소스트리 등의 프로그램을 사용하는 GUI 방식
* GUI 사용을 위해 쓰이는 [sourcetree](https://www.sourcetreeapp.com/)
___


## Git에서 과거로 돌아가는 두 방식 
1. reset : 원하는 시점으로 돌아간 뒤 이후 내역들을 지웁니다.
2. revert : 되돌리기 원하는 시점의 커밋을 거꾸로 실행합니다.
___

## Git에서 여러가지 branch 생성

Branch: 분기된 가지 (다른 차원)
* 프로젝트를 하나 이상의 모습으로 관리해야 할 때
  * 예) 실배포용, 테스트서버용, 새로운 시도용
* 여러 작업들이 각각 독립되어 진행될 때
  * 예) 신기능 1, 신기능 2, 코드개선, 긴급수정

* 각각의 차원에서 작업한 뒤 확정된 것을 메인 차원에 통합

___

## Branch를 합치는 두가지 방법
서로 다른 branch를 합치는 두 방식 

1. merge : 두 브랜치를 한 커밋에 이어붙입니다.
![merge](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=1084) 
2. rebase : 브랜치를 다른 브랜치에 이어붙입니다.
![rebase](https://wac-cdn.atlassian.com/dam/jcr:2908e0e6-f74b-4425-b5d2-f5eca8cfcd99/05%20Rebasing%20the%20main%20branch.svg?cdnVersion=1084)
___

## Git 명령어

```
git init #폴더에 숨김모드로 .git 폴더 생성

git status #변경사항 확인

git add (file name) #파일 하나 담기

git add . #모든 파일 담기

git commit #vim이 실행되어 vi 명령어 사용  

git commit -m "COMMIT NAME" #커밋: 쉽게 얘기하여 파일의 생성과 변경사항, 삭제등과 같은 변화를 각 타임캡슐에 담는다.

git commit -am "COMMIT NAME" #위의 -m과 다른 점은 -am은 새로 추가된(untracked) 파일이 없을 때 한정으로 사용 가능하다.

git log #커밋한 내용 확인 

git reset --hard (돌아갈 커밋 해시) #과거의 커밋으로 돌아간 뒤 이후 내역은 삭제

git revert (되돌릴 커밋 해시) #revert 뜻 그대로 커밋을 되돌리기

git branch BRANCH NAME #branch 생성

git branch #branch 목록 확인

git switch BRANCH NAME #이동하고자 하는 BRANCH로 이동

git switch -c new-teams #branch 생성과 동시에 이동

git branch -m (기존 브랜치명) (새 브랜치명) #branch명 변경

git log --all --decorate --oneline --graph #GUI 형태로 branch를 확인

git merge BRANCH NAME #병합할 branch의 명을 입력 

git branch -d BRANCH NAME #병합 후 branch는 삭제

git rebase BRANCH NAME #합칠 branch의 명을 입력

git remote add origin (원격 저장소 주소) #로컬의 Git 저장소에 원격 저장소로의 연결 추가 *원격 저장소 이름에 흔히 origin 사용. 다른 것으로 수정 가능

git branch -M main #기본 브랜치명을 main으로 권장

git push -u origin main #로컬 저장소의 커밋 내역들 원격으로 push(업로드)

git remote #원격 목록보기

git remote remove (origin 등 원격 이름) #원격 목록 지우기

git push #원격으로 커밋 밀어올리기

git pull #원격으로 커밋 당겨오기 

git push --force #강제 push

git fetch #원격의 변경사항들을 확인

git push (원격 이름) --delete (원격의 브랜치명) #원격의 브랜치 삭제
```
___