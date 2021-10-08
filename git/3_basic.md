# 3. basic

## git `Workflow`
![gitWorkflow](git/../picture/workflow.png)
 - working directory : 작업하고 있는 파일들
 - staging area : 작업을 마치고 저장할 준비를 하고 있는 파일들
 - .git directory : staging area 에서 commit 명령어를 이요해서 깃버전 히스토리에 저장 하게 된다 checkout 명령어를 통해서 언제든 working directory로 돌아갈 수 있다.
 - remote directory :  local directory에서 push 명령어를 통해서 서버에 저장할 수 있다.
  각각의 스냅샷은 해쉬코드가 있어서 그걸 기준으로 되돌리고 올리고 사용할 수 있다

**워킹 디렉토리**
![gitWorkflow](git/../picture/workingDirectory.png)
- 깃이 트랙하고 있는 tracked 영역
- 새로만들어지거나 git을 초기화 하게 되면 깃이 파일에 대한 정보가 없기 떄문에 아직 트래킹하고 있지 않은파일
  
***  

![gitWorkflow](git/../picture/workingDirectory2.png)
- 깃이 트래킹 하고 있는 파일 중에서도 수정된 파일과 수정되지 않은 파일 두가지 영역으로 나뉩니다.
수정이 되지 않은영역은 수정된 영역만 staging area로 옮겨 갈 수 있습니다. 



## git add
```
austin@laonstory-mac-austinui-MacBookPro git % echo hello world >a.txt
austin@laonstory-mac-austinui-MacBookPro git % echo hello world >b.txt
austin@laonstory-mac-austinui-MacBookPro git % echo hello world >c.txt
austin@laonstory-mac-austinui-MacBookPro git % git st
현재 브랜치 master
커밋하도록 정하지 않은 변경 사항:
  (무엇을 커밋할지 바꾸려면 "git add <파일>..."을 사용하십시오)
  (use "git restore <file>..." to discard changes in working directory)
	수정함:        b.txt
	수정함:        c.txt

추적하지 않는 파일:
  (커밋할 사항에 포함하려면 "git add <파일>..."을 사용하십시오)
	a.txt

커밋할 변경 사항을 추가하지 않았습니다 ("git add" 및/또는 "git commit -a"를
사용하십시오)
austin@laonstory-mac-austinui-MacBookPro git % git add .
austin@laonstory-mac-austinui-MacBookPro git % git st
현재 브랜치 master
커밋할 변경 사항:
  (use "git restore --staged <file>..." to unstage)
	새 파일:       a.txt
	수정함:        b.txt
	수정함:        c.txt

austin@laonstory-mac-austinui-MacBookPro git % echo austin >> a.txt
austin@laonstory-mac-austinui-MacBookPro git % git st
현재 브랜치 master
커밋할 변경 사항:
  (use "git restore --staged <file>..." to unstage)
	새 파일:       a.txt
	수정함:        b.txt
	수정함:        c.txt

커밋하도록 정하지 않은 변경 사항:
  (무엇을 커밋할지 바꾸려면 "git add <파일>..."을 사용하십시오)
  (use "git restore <file>..." to discard changes in working directory)
	수정함:        a.txt

austin@laonstory-mac-austinui-MacBookPro git % git add .
austin@laonstory-mac-austinui-MacBookPro git % git st
현재 브랜치 master
커밋할 변경 사항:
  (use "git restore --staged <file>..." to unstage)
	새 파일:       a.txt
	수정함:        b.txt
	수정함:        c.txt
```

## git ignore 
추가하고 싶지 않은 파일들
.gitignore 파일에 추가
-> 깃이나 깃허브에 올리고 싶지 않은 파일들 -> 트랙 되지 않음

## git diff
어떠한 내용이 바꼈는지 확인
git di
a