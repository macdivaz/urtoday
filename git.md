--papaya git 初學文件
https://www.youtube.com/watch?v=FKXRiAiQFiY
git --version 查看版本
git config --global user.name "divazchen" 設定姓名
git config --global user.email "macdivas@gmail.com" 設定信箱
git init 初始化，才能變成git資料庫

git log / git log --oneline 查看log

clear 清除螢幕

git remote add origin https://github.com/macdivaz/urtoday.git 遠端 新增 遠端儲存庫名稱 遠端儲存庫網址
git remote add origin https://github.com/macdivaz/urtoday.git

git add git.md / git add *.md / git add . 新增索引
git commit -m ""
git push

git push -u origin main 推送 建立關聯 遠端名稱 本地名稱
git push -u origin main
-u 是 --set-upstream 的縮寫，表示將本地分支與遠端分支建立關聯。​

git branch -M main 分支管理 改名 名稱
git branch -M main 分支管理 重新命名 新的分支名

git checkout #number -- filename 還原到該索引當下的檔案資料狀態
git diff #number -- filename  查看特定版本與指定檔案差別
git reset --hard #number 還原到某個時間點，之後的紀錄會刪除

---
…or create a new repository on the command line
echo "# KTJ" >> README.md
git init
git add README.md
git commit -m "first commit"
git mv test unit-test 檔案/目錄改名字

本地分支尚未設定對應的遠端追蹤分支，因此 Git 無法自動判斷應該從哪個遠端分支拉取更新。
git branch --set-upstream-to=origin/main main

如果您尚未推送本地分支到遠端，您可以在首次推送時同時設定追蹤關係
git push -u origin main

查看本地分支的追蹤狀態：
git branch -vv

---
…or push an existing repository from the command line

--
按下 Esc 鍵，確保您處於正常模式。
輸入 :wq，然後按下 Enter 鍵，這將會儲存並退出編輯器。
或者，您也可以按下 Esc，然後按下 Shift + Z 兩次（即 ZZ），這同樣會儲存並退出。

--learn git in 30 days 保哥學git
https://github.com/doggy8088/Learn-Git-in-30-days
https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/01.md
Day1 第 01 天：認識 Git 版本控管
Day2 第 02 天：在 Windows 平台必裝的三套 Git 工具
Day3 第 03 天：建立儲存庫

--git init --bare 建立共用儲存庫
git checkout master Gruntfile.js
git checkout main 檔案名稱

Day4 第 04 天：常用的 Git 版本控管指令
避免使用 git reset --hard 一次把所有檔案都給還原了！

Day5 第 05 天：了解儲存庫、工作目錄、物件與索引之間的關係

Day6 第 06 天：解析 Git 資料結構 - 物件結構
檢查 Git 維護的檔案系統是否完整，可以執行以下指令: git fsck

Day7 第 07 天：解析 Git 資料結構 - 索引結構
git diff --cached 就與 git diff --staged 是完全同義的。
git add -u 則可以僅將「更新」或「刪除」的檔案變更寫入到「索引檔」中。
只想刪除索引檔中的該檔，又要保留工作目錄下的實體檔案 
git rm --cached a.txt
git ls-files 查看目前索引內有哪些檔案

Day8 第 08 天：關於分支的基本觀念與使用方式
echo. > a.txt 建立 a.txt 檔案
echo 1 > a.txt 輸入文字到 a.txt檔案

git branch [branch_name]/git branch branch-1 建立分支branch-1
git branch checkout -b branch-2 建立branch-2且切換到此分支
git checkout [branch_name] 切換到此分支
git branch -D [branch_name] 刪除分支
小結
git branch 查詢現在有的分支
git branch [branch_name] 新增分支
git checkout -b [branch_name] 建立分支且跳到該分支
git checkout [branch_name] 跳到該分支
git branch -d [branch_name] 刪除該分支
git log

Day9 第 09 天：比對檔案與版本差異
git diff
commit graph 存在的tree object
index, git add時 tree已被建立
dirtectory 工作目錄
四種基本比較方式
git diff 工作目錄&索引
gid diff commit 工作目錄&指定的commit物件裡tree物件
git diff --cached commit 當前索引狀態&指定commit物件裡的tree物件
-- git diff --cached HEAD
-- git diff --cached == git diff --staged
-- git diff --cached == git diff --cached HEAD
git diff commit1 commit2
小結
git diff                 => 工作目錄 vs 索引
git diff HEAD            => 工作目錄 vs HEAD
git diff --cached HEAD   => 索引     vs HEAD
git diff --cached        => 索引     vs HEAD
git diff HEAD^ HEAD	     => HEAD^   vs HEAD
整理
git log
git diff
git diff HEAD
git diff --cached
git diff --staged
git diff HEAD^ HEAD

Day 10 第 10 天：認識 Git 物件的絕對名稱
git cat-file -p commitid 查看commit物件,commit id 不得少於4碼
git log --pretty=oneline 簡短log 有物件絕對名稱的簡短語法
git log --pretty=oneline --abbrev-commit 僅輸出部分的絕對名稱

Day11 第 11 天：認識 Git 物件的一般參照與符號參照
dir .git\refs\heads 查看本地分支的參照名稱
type .git\refs\heads\newbranch1 打開指定路徑下的目錄
git cat-file -p 0bd0(Commit ID)/Branch Name
git show 0bd0(Commit ID)

本地分支：.git/refs/heads/
遠端分支：.git/refs/remotes/
標　　籤：.git/refs/tags/

ref/heads/branch name;commit ID >> git cat-file -p 

.git/<參照簡稱>
.git/refs/<參照簡稱>
.git/refs/tags/<參照簡稱;標籤名稱>
.git/refs/heads/<參照簡稱;本地分支名稱>
.git/refs/remotes/<參照簡稱>
.git/refs/remotes/<參照簡稱;遠端分支名稱>/HEAD

.git/f2e --> 找不到此檔案
.git/refs/f2e --> 找不到此檔案
.git/refs/tags/f2e --> 找不到此檔案
.git/refs/heads/f2e --> 找到了參照名稱，以下就不繼續搜尋
.git/refs/remotes/f2e
.git/refs/remotes/f2e/HEAD

head
orig_head
fetch_head
merge_head

git update-ref 就可以自由建立「一般參照」
git update-ref Name ObjectID
git symbolic-ref
git show-ref
