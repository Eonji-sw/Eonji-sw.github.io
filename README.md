# Eonji-sw.github.io
소프트웨어학부 20212979 김언지

## protject build process
4주에 걸쳐 수업한 강의에 맞춰 4단계로 과정 기술

### blog_one : Git 로컬 저장소 생성
(Git이 이미 설치되어 있는 상태에서 시작)
$ git init 명령어를 통해 작업할 디렉토리를 git 저장소로 지정
Github에서 <username>.github.io 이름의 Repository 생성
Remote Repository의 주소를 복사하여 $ git clone <repo_name> <path>로 clone

### blog_two : Jekyll 생성
index.html을 예시 문서로 작성
$ git add index.html
$ git commit -m "commit message"
$ git push origin main
순서로 원격 저장소에 작성한 문서 반영
(Token은 기존에 이미 생성되어 있는 상태라 새로 생성하지 않음)
Github Page 설정에서 username.github.io 접속하여 작성한 문서 확인
사이트를 통해 Ruby, Jekyll 설치

### blog_three : Jekyll 시작 및 테마 적용
$ jekyll new . --force 명령어를 통해 현재 디렉토리에 Jekyll 설치
$ bundle exec jekyll serve 실행으로 localhost:4000 사이트 접속 가능, 기본 테마로 된 Jekyll 사이트 생성 확인
_config.yml 파일로 블로그 수정, $ bundle exec jekyll serve 명렁어로 사이트 확인
이후 $ git add, $ git rm 명령어로 변경사항 반영할 파일 지정 후 commit과 push 진행 및 <username>.github.io에 반영된 것 확인
_posts 폴더에서 YYYY-MM-DD-TITLE.md 형태로 새로운 문서 작성, add, commit, push 순으로 git에 반영
제공한 사이트에서 원하는 디자인의 테마 선택
git clone을 통해 로컬에 테마 받아온 후 변경된 파일 git에 반영
visual Studio Code를 통해 받아온 테마에서 원하는 부분(문구, 이미지 등) 수정 후 add, commit, push 순으로 반영

### blog_four : Blog 커스터마이즈
Disqus 가입 및 세팅
_config.yml 파일에 comment, provider, disqus, shortname의 key-value 추가
Disqus 홈페이지에서 Universal Code 복사하여 _layouts/post.html에서 페이지에 맞게 수정, PAGE_URL과 PAGE_IDENTIFIER 설정
_posts/*.md 파일에서 댓글을 허용하고 싶은 곳에 comments: true 작성