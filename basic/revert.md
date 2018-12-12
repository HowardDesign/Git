# git revert
* 復原指定版本的變更
* 會新增一筆commit

# 初始化
```
d:\Temp\test1>git init
Initialized empty Git repository in d:/Temp/test1/.git/
```

# 加入a.txt
```
d:\Temp\test1>echo a > a.txt & git add . & git commit -m "add a.txt"
[master (root-commit) de9d813] add a.txt
 1 file changed, 1 insertion(+)
 create mode 100644 a.txt
```

# 加入b.txt
```
d:\Temp\test1>echo b > b.txt & git add . & git commit -m "add b.txt"
[master a810acd] add b.txt
 1 file changed, 1 insertion(+)
 create mode 100644 b.txt
 ```

# 加入c.txt
 ```
 d:\Temp\test1>echo c > c.txt & git add . & git commit -m "add c.txt"
[master 1444d05] add c.txt
 1 file changed, 1 insertion(+)
 create mode 100644 c.txt
 ```

# revert前的log
```
d:\Temp\test1>git log --oneline
1444d05 add c.txt
a810acd add b.txt
de9d813 add a.txt
```

# 還原a810acd版本
```
d:\Temp\test1>git revert a810acd
[master 0142b7a] Revert "add b.txt"
 1 file changed, 1 deletion(-)
 delete mode 100644 b.txt
```

# revert後的log
```
d:\Temp\test1>git log --oneline
0142b7a Revert "add b.txt"
1444d05 add c.txt
a810acd add b.txt
de9d813 add a.txt
```