# Git 사용법

## 초기 세팅
### https://github.com 가입
### https://git-scm.com/downloads 설치
```
# 버전 확인
git version
# 초기설정
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"
```
### 새 Repo 만들기
github.com 로그인 -> new repository -> Repository name 입력, README 파일 없음 -> Create repository
-> 해당 로컬 폴더 이동 -> terminal 실행 -> "create a new repository on the command line" 따라 실행


## Repository 관리
###  Repo 연결
```
# 해당 로컬폴더로 이동 후
# 저장소 초기화
git init
# 저장소 연결
git remote add origin https://github.com/"계정"/"Repo명.git"
# 연결상태 확인
git remote -v
```

### 기존 Repo remote 제거
```
git remote remove origin
```



### 기존 Repo pull / push
```
git pull
# 전체 파일 add
git add .
# commit 명령어로 스냅샷 찍음.
git commit -m "clean push"
# 마스터 브런치에 업로드
git push -u origin master
```

### git push 에러 발생시
```
# new repo 만들때, README.md 파일을 함께 만들 경우 에러 발생
git pull
git pull origin master --allow-unrelated-histories
git commit
```


## 파일 관리
### 파일 삭제
```
# 현재폴더 + git 에서 파일 삭제
git rm "file" 
# 파일 삭제 + staged 상태

# 현재(로컬)폴더만 삭제
rm "file" 
# 이 경우 파일 삭제가 staged 상태가 아니므로, git add 명령어를 통해 staged 하게 만들어줌

# git에서만 삭제
git rm --cached "file"
# 보통 .gitignore 파일에 추가하는 작업을 빼먹었거나 실수로 불필요한 파일을 Git에 등록했을 때 필요한 작업

# 완전히 반영
git commit
```

### 상태 확인
```
git status
```



