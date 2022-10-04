## 프로젝트를 내 컴퓨터에 받기
1. gitlab 에서 프로젝트를 fork 한다.
2. 내 컴퓨터에서 프로젝트를 저장할 디렉토리로 이동한다. 오른쪽 클릭하여 git-bash를 실행한다. fork 했던 프로젝트를 clone한다.(원본 프로젝트가 아님)
```
git clone 주소
```
```
// 예시
$ git clone ssh://git@gitserver.dev.iochord.co.kr:2222/process-re-engineering/apps/front/ipr-fe-core.git
Cloning into 'ipr-fe-core'...
remote: Enumerating objects: 183, done.
remote: Counting objects: 100% (183/183), done.
remote: Compressing objects: 100% (157/157), done.
remote: Total 183 (delta 47), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (183/183), 464.81 KiB | 3.81 MiB/s, done.
Resolving deltas: 100% (47/47), done.
```
3. 클론한 프로젝트로 디렉토리를 이동한다.
```
cd ./ipr-fe-core
```
4. 현재 브랜치가 develop인지 확인한다. 아니라면 develop 브랜치로 이동한다.
```
$ git branch
* develop
```
```
$ git checkout develop
Already on 'develop'
Your branch is up to date with 'origin/develop'.
```
## 프로젝트 최신 버전 유지하기
1. 본 프로젝트 원격저장소를 추가한다. 보통 upstream 이름을 사용한다.
```
$ git remote add upstream ssh://git@gitserver.dev.iochord.co.kr:2222/process-re-engineering/apps/front/ipr-fe-core.git
```
```
$ git remote show
origin
upstream
```
2. 본 프로젝트의 업데이트된 커밋들을 다운받아서 내 프로젝트와 병합한다.
```
$ git pull upstream develop
```
## Merge Request 하기: 내 커밋들을 본 프로젝트에 병합 요청.
1. 먼저 내 계정의 fork한 프로젝트로 내 커밋들을 push한다. (develop 브랜치의 커밋들을 병합요청하는 것을 기준)
```
$ git push origin develop
```
2. gitlab 사이트에서 fork한 프로젝트로 이동한다. 커밋들이 잘 업로드되었는지 확인한다.
3. make pull request 버튼을 클릭한다.
4. 병합 요청을 위한 설명들을 작성하고, 확인을 누른다.
5. merge request를 수정하고 싶다면, gitlab 본 프로젝트 사이트로 이동하여 merge request 메뉴를 클릭해서 들어간다. 내가 요청한 merge reuqest를 클릭하여 수정한다.
