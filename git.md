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
git branch -M main
git remote add origin https://github.com/macdivaz/KTJ.git
git push -u origin main
---
…or push an existing repository from the command line
git remote add origin https://github.com/macdivaz/KTJ.git
git branch -M main
git push -u origin main
-u 是 --set-upstream 的縮寫，表示將本地分支與遠端分支建立關聯。​