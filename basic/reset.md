# git reset

* 復原到指定的版本庫狀態
* 直接修改ref/heads內指針對應的位置
* 後續的commit記錄會消失

# 參數比較
| 參數名稱  | HEAD的位置 | 索引 | 工作目錄 |
|----------|------|--------|-------|
| soft     | 修改	| 不修改 | 不修改 |
| mixed    | 修改	| 修改   | 不修改 |
| hard     | 修改	| 修改   | 修改   |

# 復原到版本庫最新版並保留剛剛的修改內容
```
git reset
git reset --soft
```

# 復原到版本庫最新版並移除還原資料夾內的檔案
```
git reset --hard
```

# 復原最後一個版本的異動
```
git reset HEAD~ --hard
```

# 復原上一個版本的異動
```
git reset ORIG_HEAD --hard
```

# 修改最後一次送交記錄
```
git commit --amend
```