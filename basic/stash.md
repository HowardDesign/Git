# git stash
* 將尚未commit的異動建立暫存版本
* 在.git\refs\stash建立暫存commit物件

# 建立暫存版本
```
git stash save -u "add stash message"
```

# 列出暫存版本
```
git stash list
```

# 顯示暫存版本commit物件
```
git stash show -p stash@{0}
```

# 套用暫存版本
```
git stash apply
```

# 刪除暫存版本
```
git stash drop
```

# 套用暫存版本並刪除記錄
```
git stash pop
```

# 刪除所有暫存版本
```
git stash clear
```