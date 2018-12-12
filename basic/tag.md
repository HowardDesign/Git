# git tag

# 輕量標籤(Lightweight tag)
* 某個commit物件的別名
* .git/refs/tags

# 標示標籤(Annotated tag)
* git 物件的一種
* 包含訊息、日期、作者等資料
* 關聯到某一個commit物件
* .git/objects/

# 列出標籤
```
git tag
git tag -n
```

# 建立標籤
```
git tag v1
git tag -am "tag message" v1.1
```

# 追加標籤
```
git tag v1.2 9fceb02
```

# 推送標籤
```
git push origin v1.3
```

# 刪除標籤
```
git tag -d tagname
```