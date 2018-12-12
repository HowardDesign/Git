# 三個區域
* Working Directory: 所有的修改、變動都發生在這個階段
* Staging area: 作為一個中繼的工作區，在將檔案放入資料庫之前做確認及檢查的工作區，確認無誤後就可以將檔案轉移至資料庫
* Repository: 資料庫，儲存著更新的 commit，而線上資料庫會和本機的這個區域進行同步

![basic](2.png)

# 初始化版本庫
```
D:\>git init test1 & cd test1
Initialized empty Git repository in D:/test1/.git/
```

# 加入檔案
```
D:\test1>echo a > a.txt & git add . & dir /a:d .git\objects
 磁碟區 D 中的磁碟沒有標籤。
 磁碟區序號:  6402-6C96

 D:\test1\.git\objects 的目錄

2016/11/30  上午 11:29    <DIR>          .
2016/11/30  上午 11:29    <DIR>          ..
2016/11/30  上午 11:29    <DIR>          0d
2016/11/30  上午 11:25    <DIR>          info
2016/11/30  上午 11:25    <DIR>          pack
               0 個檔案               0 位元組
               5 個目錄  365,397,213,184 位元組可用
```

# 加入版本庫
```
D:\test1>git commit -m "add a.txt" & dir /a:d .git\objects
[master (root-commit) 45a49e6] add a.txt
 1 file changed, 1 insertion(+)
 create mode 100644 a.txt

 磁碟區 D 中的磁碟沒有標籤。
 磁碟區序號:  6402-6C96

 D:\test1\.git\objects 的目錄

2016/11/30  上午 11:32    <DIR>          .
2016/11/30  上午 11:32    <DIR>          ..
2016/11/30  上午 11:32    <DIR>          0d
2016/11/30  上午 11:32    <DIR>          11
2016/11/30  上午 11:32    <DIR>          45
2016/11/30  上午 11:30    <DIR>          info
2016/11/30  上午 11:30    <DIR>          pack
               0 個檔案               0 位元組
               7 個目錄  365,397,213,184 位元組可用
```

# log
```
D:\test1>git log
commit 45a49e68500553ca6e11ecacd2d7eaf7766186f0
Author: xian <xian@xsg.com.tw>
Date:   Wed Nov 30 11:32:22 2016 +0800

    add a.txt
```

# commit
```
D:\test1>git cat-file -p 45a49e68500553ca6e11ecacd2d7eaf7766186f0
tree 1107339ad97f894e44e6f6ed9fccfc444e7ded6e
author xian <xian@xsg.com.tw> 1480476742 +0800
committer xian <xian@xsg.com.tw> 1480476742 +0800

add a.txt
```

# tree
```
D:\test1>git ls-tree 1107339ad97f894e44e6f6ed9fccfc444e7ded6e
100644 blob 0d13814d585b11dbeae7a42377d7422f93d2be15    a.txt
```

# 檔案內容
```
D:\test1>git cat-file -p 0d13814d585b11dbeae7a42377d7422f93d2be15
a
```