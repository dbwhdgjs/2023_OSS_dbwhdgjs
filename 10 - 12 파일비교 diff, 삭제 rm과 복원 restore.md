# 10 파일 비교 diff
## 파일 비교
+ 깃 3 영역의 파일 비교

![image](https://github.com/dbwhdgjs/2023_OSS_dbwhdgjs/assets/127083569/fa964712-efba-4f9b-a971-aac8e9e5caa1)  
  - $ git diff : 스테이징 영역 기준에서 작업 디렉토리 비교
  - $ git diff --staged [HEAD] : 깃 저장소 HEAD 기준으로 스테이징 영역 비교
  - $ git diff HEAD : 깃 저장소 HEAD 기준으로 작업 디렉토리 비교
    
+ 커밋 간의 파일 비교
  - HEAD~, HEAD^ : 하나 전 커밋
  - git diff [비교할commit해쉬1] [비교할commit해쉬2]
     * $ git diff HEAD^ HEAD
     * $ git diff 048171 0c747d
+ 브랜치 간의 파일 비교

# 11. 파일 삭제 rm과 복원 restore
## 파일 삭제 rm
+ 파일 삭제
  -  리눅스 명령 파일 삭제
    * $ rm [file] : 작업 디렉토리에서 file 삭제
  - 깃 명령 파일 삭제
    * $ git rm [file] : 작업 디렉토리와 스테이징 영역에서 모두 file 삭제
    * $ git rm –-cached [file] : 스테이징 영역에서만 file 삭제
+ 커밋 삭제
  - $ git commit –m ‘Delete g’ 
## 파일 복원 restore
+ 깃 저장소 상태를 스테이징 영역에 복원
  - $ git restore f : 작업 디렉토리의 파일 f를 스테이징 영역의 파일 상태로 복구
+ 깃 저장소 상태를 작업 디렉토리에 복원
  - $ git restore --source=HEAD --worktree f
  - $ git restore --source=HEAD f
+ 깃 저장소 상태를 스테이징 영역과 작업 디렉토리에 함께 복원
  - $ git restore --source=HEAD --staged --worktree f
