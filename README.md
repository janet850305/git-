# git- 

1.註冊 GitHub (或其他常見的服務平台如 GitLab、Bitbucket）

2.設置 SSH key

實際應用時，在本地輸入指令 git push 就可以推上去指定的儲存庫，但 GitHub 怎麼判斷這個儲存庫誰可以上傳上來呢？我們可以設置 ssh key 讓 GitHub 去控管權限。

在終端機中生成為一組成對的公鑰、私鑰，將公鑰設定在 GitHub 中，共 GitHub 透過比對公、私鑰是否對得起來而控制上傳權限。

$ ssh-keygen
在終端機中產生金鑰

$ ls -al ~/.ssh
查詢是否有 SSH Key了(出現檔案id_rsa.pub 或 id_dsa.pub 就成功囉)

$ pbcopy < ~/.ssh/id_rsa.pub / $ clip < ~/.ssh/id_rsa.pub
複製公鑰 ( Mac / windows )

至 GitHub 的 Setting 頁 貼上 SSH Key就完成配置囉！
https://git-scm.com/book/zh-tw/v2/%E9%96%8B%E5%A7%8B-%E5%88%9D%E6%AC%A1%E8%A8%AD%E5%AE%9A-Git
初次使用(剛灌git 需要設定username 與useremail)</br>

$ git config --global user.name name

$ git config --global user.email Email

配置你的 username 與 email　(與 GitHub 帳號、Email 一致)
可以用git config --list 是否設定完成
$ git remote add origin repositoryURL
連結遠端Repo (repositoryURL = 剛剛複製的那個 SSH 位址)


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
