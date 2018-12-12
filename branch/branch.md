# 分支與合併

# 開分支b1
```
D:\Temp\test1>git branch b1 & git branch
  b1
* master
```

# 開分支b2
```
D:\Temp\test1>git branch b2 & git branch
  b1
  b2
* master
```

# 切換分支b1
```
D:\Temp\test1>git checkout b1 & git branch
Switched to branch 'b1'
* b1
  b2
  master
```

# 增加b1分支異動記錄
```
D:\Temp\test1>echo b1 > b1.txt & git add . & git commit -m "branch b1 add b1.txt"  & git log
[b1 7d11f3f] branch b1 add b1.txt
 1 file changed, 1 insertion(+)
 create mode 100644 b1.txt
commit 7d11f3fde09a30bd4aabd8b963ca7d982a43f291
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:44:37 2016 +0800

    branch b1 add b1.txt

commit 4f644b07dca48c718fb07797aa03c05cd7066f69
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:38:29 2016 +0800

    edit a.txt

commit cd65db760226f7a11889344c638679db423c2005
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:37:31 2016 +0800

    add a.txt
```

# 切換分支b2
```
D:\Temp\test1>git checkout b2 & git branch
Switched to branch 'b2'
  b1
* b2
  master
```

# 增加b2分支異動記錄
```
D:\Temp\test1>echo b2 > b2.txt & git add . & git commit -m "branch b2 add b2.txt" & git log
[b2 eeb4b8f] branch b2 add b2.txt
 1 file changed, 1 insertion(+)
 create mode 100644 b2.txt
commit eeb4b8f35a279f009782e8f19b41488118829e97
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:46:23 2016 +0800

    branch b2 add b2.txt

commit 4f644b07dca48c718fb07797aa03c05cd7066f69
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:38:29 2016 +0800

    edit a.txt

commit cd65db760226f7a11889344c638679db423c2005
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:37:31 2016 +0800

    add a.txt
```

# 切換回master並合併b1和b2
```
D:\Temp\test1>git checkout master & git merge b1 b2 & git log
Switched to branch 'master'
Fast-forwarding to: b1
Trying simple merge with b2
Merge made by the 'octopus' strategy.
 b1.txt | 1 +
 b2.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 b1.txt
 create mode 100644 b2.txt
commit f84a80ca5c445c21182bd0eef95c259db321eedd
Merge: 7d11f3f eeb4b8f
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:46:51 2016 +0800

    Merge branches 'b1' and 'b2'

commit eeb4b8f35a279f009782e8f19b41488118829e97
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:46:23 2016 +0800

    branch b2 add b2.txt

commit 7d11f3fde09a30bd4aabd8b963ca7d982a43f291
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:44:37 2016 +0800

    branch b1 add b1.txt

commit 4f644b07dca48c718fb07797aa03c05cd7066f69
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:38:29 2016 +0800

    edit a.txt

commit cd65db760226f7a11889344c638679db423c2005
Author: 李明憲 <xian@xsg.com.tw>
Date:   Tue Nov 29 16:37:31 2016 +0800

    add a.txt
```

