# Git 初始化

git版本控制會產生.git資料夾

# 語法
```
git init [-q | --quiet] [--bare] [--template=<template_directory>]
	  [--separate-git-dir <git dir>]
	  [--shared[=<permissions>]] [directory]
```

# 選項

| 欄位一        | 欄位二       |
| ------------- |-------------|
| -q  <br/> --quiet     |  |                     
| --bare | 建立純倉儲庫 |
| --template=<template_directory> | |
| --separate-git-dir=<git dir> | |
| --shared | |

# 範例
```
D:\Temp>git init test1 & git init test2 --bare
Initialized empty Git repository in D:/Temp/test1/.git/
Initialized empty Git repository in D:/Temp/test2/
```

```
D:\Temp>dir /a test1 test2
 磁碟區 D 中的磁碟沒有標籤。
 磁碟區序號:  6402-6C96

 D:\Temp\test1 的目錄

2016/11/29  下午 04:26    <DIR>          .
2016/11/29  下午 04:26    <DIR>          ..
2016/11/29  下午 04:26    <DIR>          .git
               0 個檔案               0 位元組

 D:\Temp\test2 的目錄

2016/11/29  下午 04:26    <DIR>          .
2016/11/29  下午 04:26    <DIR>          ..
2016/11/29  下午 04:26               104 config
2016/11/29  下午 04:26                73 description
2016/11/29  下午 04:26                23 HEAD
2016/11/29  下午 04:26    <DIR>          hooks
2016/11/29  下午 04:26    <DIR>          info
2016/11/29  下午 04:26    <DIR>          objects
2016/11/29  下午 04:26    <DIR>          refs
               3 個檔案             200 位元組
               6 個目錄  365,395,038,208 位元組可用
```

# 資料夾
* hooks：存儲鉤子的檔案夾
* logs：存儲日誌的檔案夾
* objects：存放git物件
* refs：存儲指向各個分支的指針(SHA-1標識)檔案

# 檔案
* config：存放各種設置文件
* HEAD：指向當前所在分支的指針檔案路徑，一般指向refs下的某檔案

# 物件類型 
* Blob: 記錄檔案內容
* Tree: 記錄該目錄下有哪些檔案(檔名、內容的SHA1)和 Trees
* Commit: 記錄 commit 訊息、Root tree 和 Parent commits 的 SHA1
* Tag: 記錄標籤

# Git References
* head: 是一個指向你當前所在分支的引用標示符號
* tag: tag 可以是一個物件也可以是一個引用
* remote: 是一個標示符號指向你最後一次和伺服器的通訊的分支
* branch: 是一個指向每個分支最前面 commit 的指標，告訴使用者分支名稱