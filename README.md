# Web-Security
Notes For Web Security

Linux 指令
===
ls
---
    * -l列出檔案的詳細資料
    * -a 列出所有隱藏檔案
    * -al == -a && -l

mkdir
---
    在目前的資料夾下建立一個新資料夾

vim
---
    * dd刪除一行
    * cc 剪下一行
    * p 貼上
    * :w 儲存(write)
    * :q 離開(quit)
    * :!強制執行
    * :%!xxd顯示檔案的hexdump

cat
---
    顯示檔案的內容
  
rm
---
    * -r如果裡面有東西，就先刪裡面的
    * -f強制刪除，不想打sudo時很好用
    * -d 刪除資料夾(限空白的)，功能和rmdir一樣
    * 超強用法rm–r <directory>

cd
---
    變更當前的目錄
  
cp
---
    * cp <file> <directory_position>
    * 將file 複製到指定位置
    * cp <file_1> <file_2>
    * 建一個名字為file_2 的檔案，其內容和file_1一樣
  
echo
---
    * -e 可以利用ascii碼印出字元
    * -n 印出來的字串結尾不加’\n’
  
chmod
---
    * ±r新增、移除讀取權限
    * ±w 新增、移除寫入權限
    * ±x新增、移除執行權限
    * directory, owner, group, other
    * example : chmodu=rwx<file_name>
    * r = 4
    * w= 2
    * x = 1
    * example : chmod777 <file_name>

grep
---
    搜尋特定字串
    * 被搜尋字串中如果有‘ ‘, ‘\n’, ‘\b’ 等特殊字元時，需要將字串用’’ 包起來

ping
---

tar
---
    * -c打包一個tar 檔案
    * -x解開一個tar 檔案
    * -t檢視tar 檔案的內容
    * -z使用gzip壓縮
    * -v顯示建立tar 檔案的過程
    * -P使用絕對路徑
    * -f指定tar 檔案的檔案名稱(通常加在最後)
    * Examples :
    –壓縮 tar -zcvfbird.tar.gzbird
    –解壓縮 tar -zxvfbird.tar.gz
  
su
---
    取得root 權限
    * su-
    login as root
    * su-c <instruction>
    以root的權限執行instruction 後離開su模式
    * su-l <user_name>
    可以login其他的帳號
  
sudo
---
    功能類似su-c
    * -u <user_name> <instruction>
    先切換成<user_name> 的權限，再執行instruction
    * -g <group_name> <instruction>

ifconfig
---

net cat
---
    連線到指定網址
    * -p 指定要連線到哪個port
    * 用法：nc<options> <host_name>

Linux tools
===
1.看binary 檔案的內容
---
      strings:印出檔案中所有可視字元
      xxd:顯示檔案的Hexdump

2.安裝套件指令
---

  ### apt
    * 使用前：
    apt-get update
    * 用法：
    apt-get install <package_name>
  
  ### wget
    * 用法：wget<options> <url>
    * 參數：-r : 遞迴下載，把文件中所有的連結都下載回來。
    -P : 指定下載到某個目錄下
  
  ### curl
    * 用法：
    curl <options><url>
    * 參數：
    -i只顯示header
    -v 顯示全部詳細資料
    -X用不同的method 去request
    -L如果有重導向的話就繼續跟蹤
    -o將頁面原始碼存到電腦上
  ### pip
    專門安裝python 的package
    * 用法：pip install <package_name>
           pip uninstall <package_name>
           
3.啟用插件
---
   1.im-config
   2.reboot


  


  


  
