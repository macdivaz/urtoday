--papaya git 初學文件
https://www.youtube.com/watch?v=FKXRiAiQFiY
git --version 查看版本
git config --global user.name "divazchen" 設定姓名
git config --global user.email "macdivas@gmail.com" 設定信箱
git init 初始化，才能變成git資料庫
git add git.md / git add *.md / git add . 新增索引
git log / git log --oneline 查看log

clear 清除螢幕

git remote add origin https://github.com/macdivaz/urtoday.git 遠端 新增 遠端儲存庫名稱 遠端儲存庫網址
git remote add origin https://github.com/macdivaz/urtoday.git

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

---
…or push an existing repository from the command line

--
按下 Esc 鍵，確保您處於正常模式。
輸入 :wq，然後按下 Enter 鍵，這將會儲存並退出編輯器。
或者，您也可以按下 Esc，然後按下 Shift + Z 兩次（即 ZZ），這同樣會儲存並退出。

--learn git in 30 days 保哥學git
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