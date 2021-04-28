### 깃허브 커밋 날짜 변경

마지막 Commit 날짜를 현재 날짜로 설정

git commit --amend --no-edit --date "$(date)"

마지막 Commit 날짜를 임의의 날짜로 설정

git commit --amend --no-edit --date "Mar 06 2021 20:20:20 +0900"

"" 사이에 원하는 날짜,연도,시간을 기입하면 됨.
