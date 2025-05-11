git --version
git config --global user.name "divazchen"
git config --global user.email "macdivas@gmail.com"
git init
git add git.md / git add *.md / git add ,
git log / git log --oneline
git checkout #number -- filename
git diff #number -- filename
clear
git reset --hard #number
---
…or create a new repository on the command line
echo "# KTJ" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main 分支管理 重新命名 新的分支名
git remote add origin https://github.com/macdivaz/urtoday.git 遠端 新增 遠端儲存庫名稱 遠端儲存庫網址
git push -u origin main
git mv test unit-test 檔案/目錄改名字
---
…or push an existing repository from the command line
git remote add origin https://github.com/macdivaz/urtoday.git
git branch -M main
git push -u origin main 推送 建立關聯 遠端名稱 本地名稱
-u 是 --set-upstream 的縮寫，表示將本地分支與遠端分支建立關聯。​

--
按下 Esc 鍵，確保您處於正常模式。
輸入 :wq，然後按下 Enter 鍵，這將會儲存並退出編輯器。
或者，您也可以按下 Esc，然後按下 Shift + Z 兩次（即 ZZ），這同樣會儲存並退出。

--git init --bare 建立共用儲存庫