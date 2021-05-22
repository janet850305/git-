# Git

link: https://git-scm.com/downloads
 mac : iTerm2
 
查詢版本：git version
查詢設定列表：git config --list
輸入姓名：git config --global user.name "你的名字"
輸入email：git config --global user.email "你的email"
- 在開始使用git 之前要進行姓名及email的設定，並且使用config --list確認是否設定完成才能進行下一步

![](https://i.imgur.com/DE7pEYj.png)

### 建立本地數據庫：git init
- 在特定資料夾輸入git init會建立一個.git的隱藏資料夾
- .git儲存該特定資料夾的歷史紀錄，像是變更，增加，刪除...
- mac指令： “command + shift + .（dot）”來顯示隱藏檔案/檔案夾。
    
開新資料夾：mkdir 資料夾名稱
開新檔案：touch 檔案名稱
### 新增至索引：git add .
利用git add . 來將新的資料新增到索引
git add "檔名.副檔名" 可指定特定檔案新增到索引
### 查看索引狀態：git status
利用git status查看目前索引是否有更新資料並加入索引
### 提交更新：git commit -m "更新名稱"（從索引提交到本地數據庫）

- 在使用git add之後不會有任何的顯示，可以用git status查詢所更新的新索引，像是新的檔案，編輯程式碼...
- 索引提交（commit）到本地數據庫後，git status就會清空

### 查詢記錄：git log
- 查詢本地數據庫的更新紀錄

### 忽略檔案：
1. touch .gitignore
2. 在.gitignore中加入想要忽略的檔案全名
    可使用格式：
    1. index.html  (特定檔案)
    2. *.html (所有html檔案)
    3. css/ (特定資料夾)
### 取消索引：
全部檔案取消索引：git reset HEAD
取消單一檔案索引：git reset HEAD 檔案名稱.副檔名

### 還原檔案：
恢復單一檔案到最新commit的狀態：git checkout 檔案名稱.副檔名
恢復所有檔案到最新commit狀態：git reset --hard
- 也就是說可以用來還原改壞且尚未update的檔案，只要還沒commit就可以還原，刪除的檔案也可以藉此救回