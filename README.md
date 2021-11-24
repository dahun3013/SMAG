# SMAG
AI arithmetic study game
(Game Engine : Unity)


## 환경 설정
(1) 원격 저장소 push 권한 (git clone 후 아래를 입력)
```
> git config credential.helper store
```


## 기획서
https://www.notion.so/AI-Arithmetic-Study-Game-Project-878fcf59d3134062bffe50e46dfc75d9
<br><br>


## 개발 코드 깃 형상 관리
master branch : pull request 후 merge 로 진행한다. <br>
develop branch : TBD <br>
(이 외에 필요하다면, 별도의 브랜치 생성) <br><br>
항상 git pull 을 통해 로컬을 최신화하고 작업하는 습관을 가집시다. <br><br>

Master : 배포되어서 사용자가 사용할 수 있는 버전의 가장 최신 버전 (개발완료 상태)
- Merge : develop -> Master (개발 배포 직후)
- Merge : HotFix -> Master (라이브이슈 수정 후 배포 직후)

HotFix : 배포되기 전의 라이브이슈가 해결된 가장 최신 버전 (개발완료 상태)
- Merge : develop -> HotFix (개발 배포 직후)
- Merge : live-issue -> HotFix (라이브이슈 수정 후 배포 전)

Develop : 배포되기 전의 가장 최신 버전 (개발중 상태)
- Merge : live-issue/... -> Develop (다음버전 배포전)
- Merge : feature/... -> Develop (다음버전 배포전)
- Merge : bts/... -> Develop (다음버전 배포전)

Feature : 다음버전 배포되기 전 기능 추가/수정 (기능추가, 유지보수 상태)
- 1. [첫 생성] new Branch : Develop -> new select Branch
- 2. [작업전, push 전] pull : Develop
- 3. [작업후] push : Feature
- 4. [PR] pull-request : Feature -> Develop

Bts : 다음버전 배포되기 전 Feature 이슈 수정 (개발중 발견한 이슈 브런치)
- 1. [첫 생성] new Branch : Develop -> new select Branch
- 2. [작업전, push 전] pull : Develop
- 3. [작업후] push : Bts
- 4. [PR] pull-request : Bts -> Develop

live-issue : 다음버전 배포되기 전 Live이슈 수정 (배포이후 발견된 이슈 수정을 위한 브런치)
- 1. [첫 생성] new Branch : HotFix -> new select Branch
- 2. [작업전, push 전] pull : HotFix
- 3. [작업후] push : live-issue
- 4. [PR] pull-request : live-issue -> HotFix
