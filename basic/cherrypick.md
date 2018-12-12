# git cherry-pick

* 從其他的分支挑選版本到目前分支
* 套用該版本異動並建立新commit物件

# 套用版本加入來源記錄
```
git cherry-pick SHA1 -x
```

# 套用版本前先編輯訊息
```
git cherry-pick SAH1 -e
```

# 僅套用挑選版本不建立commit
```
git cherry-pick SHA1 -n
```