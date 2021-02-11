git --version 查詢版本

git init 建立git庫
git config -l 查詢所有設定檔
git config --global user.name "XXX" 設定使用者名稱
git config --global user.email "XXX@gmail.com" 設定使用者信箱
git config --global color.ur true "設定區別顏色介面"

git help config or git config --help 查詢指令

git status 查詢檔案索引狀態
git add 檔案 將檔案加入索引
git add . 將所有檔案加入索引
git commit -m "備註" 將索引檔案提交至本地庫
git log 查詢git提交履歷
git log -n 顯示前n筆資料
git log --oneline 簡略顯示
git log -p 詳細顯示
git log --stat 修改顯示
git log --help

git status
git restore 檔案 恢復檔案(進入索引區前)
git restore --staged 檔案 將檔案退出索引區

git diff 查詢修改內容(進入索引區前)
git diff --cached 查詢修改內容(索引區或本地庫)

git mv 檔案 新檔名 更改檔案名稱
git rm --cached 移除檔案

.gitignore 忽略管理

git mommit --amend 重新提交覆蓋最後一次的紀錄(兩次大寫ZZ可以保存退出)

git reset --hard HEAD 恢復到最新的版本
git reset --hard HEAD~ 恢復到最新的版本-1
git reset --hard HEAD~n 恢復前n個版本
git reset --hard 版本ID 恢復到特定版本

git reflog 回復記錄查詢
git reflog -n 回復記錄查詢出現前n筆

git branch 查詢分支狀態(主分支為master)
git branch XX 新增XX分支
git checkout XX 切換分支到XX

git merge xx 將XX分支合併(記得切回master)
git branch -d XX 將XX分支刪除.

git checkout -b XX 新建XX分支並且切換
(同時分支修改commit，進行merge會產生合併衝突)
解決方式
(若使用VS code 可點選如何合併，再重新commit即可)

git tag 查詢標籤內容
git tag VXXX.XXX.XXX 新增標籤為VXXX.XXX.XXX (搭配上一次的commit)
git show VXXX.XXX.XXX 觀看當時VXXX.XXX.XXX標籤的所有狀態

VNNN.abc.xxx
NNN:大版本號
abc:每次做出的小更新時，發布的版本號
xxx:每次的bug修正時發布的版本號

git config --global alias.XX commit 將commit指令(可以換成其他指令)以XX代替

git clone URL 將線上的git複製至本機
git branch -a 查詢包含線上的分支內容
git branch XXX remotes/origin/XXX 對應遠端分支
git remote -v 觀看遠程分支具體設置
git push origin dev 將本地庫檔案推上遠端庫
(github要設定token)
--------------------------------------------------------------------------
echo "# mygit" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main 主分支命名為 main
git remote add origin https://github.com/Fang45896/mygit.git
git push -u origin main