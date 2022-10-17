## 트러블 슈팅 기록하는 노트 📃 

#### 1. npm install 오류 (python2 is not found error) 
- 사용하는 프로젝트와 설치된 node의 버전이 맞지 않아 발생한 오류였다. 

#### node 버전 변경 방법
```
# 버전 조회
nvm list available
# 원하는 버전 설치
nvm install {원하는 버전}
# 설치된 버전
nvm list
# 버전 변경
nvm use {사용할 버전}
nvm use 명령어가 잘 안 먹히는 경우
'Program Files/nodejs' 폴더를 -> 'Program Files/nodejsx' 로 변경
관리자 권한에서 명령어 실행
```
