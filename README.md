# Git 사용법

## Repository 관리

### 기존 Repo pull / push
```
git pull
git add .
git commit -m "clean push"
git push
```

### 기존 Repo remote 제거
```
git remote remove origin
```

### 새 Repo remote 추가
```
git remote add origin https://github.com/"계정"/"Repo명"
```

### git push 에러 발생시
```
# new repo 만들때, README.md 파일을 함께 만들 경우 에러 발생
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



