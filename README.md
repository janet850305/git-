# git- 

上傳至github的步驟:  </br>
1.下載git   </br>
2.對目標資料夾案右鍵並選git bash  </br>
3.登入github  </br>
4.指示碼步驟  </br>
&nbsp;&nbsp;&nbsp; git init </br>
&nbsp;&nbsp;&nbsp; git add .   </br>
&nbsp;&nbsp;&nbsp; git commit -m ‘first commit’  </br>
&nbsp;&nbsp;&nbsp; git remote add origin 網址  </br>
&nbsp;&nbsp;&nbsp; git push -u origin master </br>
 
init 為創造該檔案本地資料庫，使之後變更的紀錄都可以被儲存在裡面，會創造出一個隱藏的.git資料夾
add . 將所有的檔案由工作目錄儲存到索引
commit 將修改紀錄儲存到本地數據庫
push 將本地數據庫的東西推送到遠端數據庫進行更新
 
為什麼要有索引的存在
https://hackernoon.com/understanding-git-index-4821a0765cf

未完
