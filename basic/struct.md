# 資料結構

# 每個commit物件包含一個tree物件和上一個commit
![s01](s01.png)

# 每個tree包含當次版本的所有檔案快照
![s01](s02.png)

# 分支名稱只是一個指向到commit的連結
![s01](s03.png)

# 新建分支只是在refs/heads內新增一個對應的檔案(41byte)
![s01](s04.png)

# HEAD指向到目前分支的最新版本
![s01](s05.png)

# 切換分支時只是切換HEAD對應的索引
![s01](s06.png)

# 分支commit一個版本，HEAD也會跟著移動一個版本
![s01](s07.png)

# 切換回master分支，HEAD也更新回master的最新值
![s01](s08.png)

# master commit一個版本，HEAD也跟者移動一個版本
![s01](s09.png)