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



https://cdn.discordapp.com/attachments/854701007045001264/907141604031213618/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907144589205446667/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907147834405580821/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907153946722828288/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907153994927976458/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907155772822147092/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907159336902606848/unknown.png
https://cdn.discordapp.com/attachments/854701007045001264/907160345724977152/unknown.png
