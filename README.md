# CS-NOTE

#  Linux 背景知識:
## 1.Debian 2.Fedora 3.SUSE

#  檔案命名原則：
## 區分英文字元的大小寫，基本以小寫為主。
## 檔名不可使用："?"(問號),"*"(星號), " "(空格), "$"(貨幣符), "&", 擴號, "/" (斜線)，"." , ".."

# 絕對路徑&相對路徑
## 絕對路徑：路徑的寫法『一定由根目錄 / 寫起』，例如： /usr/share/doc 這個目錄。
## 相對路徑：路徑的寫法『不是由 / 寫起』，例如由 /usr/share/doc 要到 /usr/share/man 底下時，寫成： 『cd ../man』，相對路徑意指『相對於目前工作目錄的路徑！』

# 基本指令:
## cd  變換目錄
## pwd 顯示目前的目錄
## mkdir 建立一個新目錄
## rmdir 刪除一個裡面是空的空目錄
## cp 複製
## mv 移動
## ls 顯示目錄下的所有內容
## cat 查看檔案內容
## ls-al 查看每個答案與目錄用有者與群組
## chmod 控制檔案如何被他人調用

# 看懂權限： 
## 目錄/rwx/ rwx/ rwx/ 擁有者/ 擁有群組/ 檔案大小/ 檔案名稱

# 為什麼要壓縮檔案：
## 1.備份資料的時候，方便整理。
## 2.將檔案變小，節省電腦硬碟的空間。(但圖片、音訊、視訊等多媒體檔案壓縮率低，並不能有效節省空間)
## 3.將無數個散亂的檔案打包成一個較小的檔案，亦方便資訊在網路上流通。(可將永久免費版之付費軟體輕鬆分享)
## 4.壓縮檔案時，可以視情況進行加密。

# 壓縮檔案原理：將重複的資料進行統計紀錄。
## 例如：資料裡有（111...)，壓縮過後會記錄成「一百個1」，這樣就可以減少檔案空間的佔用

# 壓縮檔案指令：
## gzip FileName
## gunzip FileName.gz/ gzip -d FileName.gz

# 檔案搜尋：
## find [path] [option] [action] filename
### option:
#### -size EX：找出大於500M的檔案 → -size +500M
#### -name EX：找出為照片的檔案 → -name "*.jpg"
#### -type EX：-type f → 一般檔案;-type d→一般目錄
#### -user EX：同時找兩個擁有者的檔案 → -user user1 -o -user user2
### action -exec:
#### ls
#### print
## filenames
### -n<文件名長度>指定文件名長度，指定的長度必須大於或等於所有文件中最長的文件名。
### -p<文件名長度>與-n参數相同，但此處的<文件名長度>包括了文件的路徑。
### -w指定輸出欄位的寬度。
### -V顯示版本訊息。

# 檔案內容查閱
## cat  從第一行顯示檔案內容、形成新檔案
###  -n file1 > file2 → 把file1的檔案內容加上行號後輸入file2檔案
#### "-n" → 由1開始對所有輸出的行數編號
#### ">" → 將多個文件覆蓋到目標文件中
#### ">>" → 將多個文件追加到目標文件中
## tac  從最後一行開始顯示
### tac -r -s 'x\|[^x]' test.log → 一個接著一個字符的反轉一個文件
#### "-r" → 將分隔符作為基礎正規表達是處理
#### "-s" → 使用String作為分隔符代替默認的換行符
## more 一頁一頁的顯示檔案內容
### more +20 testfile → 從第20行開始顯示testfile的文檔內容
#### ENTER：向下n行(default為1行)
#### Ctrl+F/SPACE：向下滾動一屏
#### Ctrl+B：返回上一屏
## less 與 more 類似，顯示檔案室允許用戶既可以向前又可以向後翻頁閱讀檔案
### ps -ef |less → "ps"查看進程信息並通過"less"分頁顯示	
#### j → 下一行
#### k → 上一行
#### G → 移動到最後一行
#### g → 移動到第一行
## head/tail 只看頭/尾巴幾行
### head -n 20 state.txt | tail -10 → 顯示11~20行的內容


# 實際操作截圖
https://cdn.discordapp.com/attachments/854701007045001264/907141604031213618/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907144589205446667/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907147834405580821/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907153946722828288/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907153994927976458/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907155772822147092/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907159336902606848/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907160345724977152/unknown.png


#Git 指令
###初始化專案：git init
###單一檔案加入索引(暫存區)：git add <檔案名稱>
###所有檔案加入索引(暫存區)：git add .(#.的意思代表全部)
###觀看當前狀態：git status
###提交版本：git commit -m “修改紀錄”
###瀏覽歷史紀錄：git log
###取消追蹤檔案：git rm –cached <檔案名稱>
###取消commit：git reset --mixed HEAD^
###連接遠端數據庫：git remote add origin <remote網址>
###將本地資料推到remote端：git push -u origin master
###將遠端資料拉回來：git fetch
###將拉回的資料和本地資料合併：git merge
###git pull = git fetch + git merge


#Git-版本控制流程
##工作目錄         暫存區         本地數據庫       遠端數據庫
###      git add     ->   git commit   ->  git push
###   git checkout/git merge      <-        git fetch
###                <-      git pull   <-

#Git- 不再追蹤檔案 & 取消commit
##工作目錄         暫存區         本地數據庫       遠端數據庫
###    git rm –cached     git reset HEAD^ 
###         <-              <-


#Git- 取消追蹤檔案
###修改index.html：vi index.html
###查看狀態：$ git status
###將檔案加入索引：$ git add index.html
###查看狀態：$ git status
###取消追蹤檔案：$ git rm –cached index.html
###查看狀態：$ git status


#Git- 取消commit
###新增檔案：vi hello.py
###將檔案加入索引：$ git add .
###提交版本：$ git commit -m “print method”
###查看歷史紀錄：$ git log
###取消commit：$ git reset --mixed HEAD^
###查看歷史紀錄：$ git log
###查看狀態：$ git status

#Git- Reset模式
##Reset有三種模式：
####--mixed：預設模式，Commit 拆出來的檔案會留在工作目錄，但不會留在暫存區
####--soft：工作目錄跟暫存區的檔案都不會被丟掉
####--hard：工作目錄以及暫存區的檔案都會丟掉


#Git-使用方法

##六. 進入Remote repository(遠端數據庫)
###1.雲端跟本地端連動：
####$ git remote add origin <remote網址>

###2.Push Local master(主幹)進入Remote：
####$ git push --set-upstream origin master

###3.回到Github查看


#Git-使用方法
###1.到github上新增或編輯README.md
###2.把遠端東西拉回來：$ git fetch
###3.查看狀態：$ git status
###4.查看歷史紀錄：$ git log
###5.比較本地分支和遠端分之內容的不同：$ git diff origin/master
###6.將遠端和本地端的內容做合併：$ git merge origin/master
###7查看狀態：$ git status
###8.Pull下載更新：$ git pull origin


#Git Flow 分支應用
###Master 分支
####主要是用來放穩定、隨時可上線的版本。
####這個分支的來源只能從別的分支合併過來
####通常會在這個分支上的 Commit 上打上版本號標籤。
###Develop 分支
####所有開發的基礎分支
####當要新增功能的時候，所有的 Feature 分支都是從這個分支切出去的。而功能完成後，也都會合併回來這個分支。
###Hotfix 分支
####當線上產品發生緊急問題的時候，會從 Master 分支開一個 Hotfix 分支出來進行修復，Hotfix 分支修復完成之後，會合併回 Master 分支，也同時會合併一份到 Develop 分支。
###Release 分支
####當認為 Develop 分支夠成熟了，就會合併到 Release 分支，在這邊進行上線前的最後測試。
####測試完成後，Release 分支將會同時合併到 Master 以及 Develop 這兩個分支上
###Feature 分支
####當要開始新增功能的時候
####從 Develop 分支來的，完成之後再併回 Develop 分支。









