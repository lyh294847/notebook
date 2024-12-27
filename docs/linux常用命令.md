### 11
查询创建时间早于YYYY-MM-DD的文件
```
find /path/to/directory -type f ! -newermt 'YYYY-MM-DD'
```

查询创建时间早于30天的文件并删除
```
find /path/to/directory -type f -ctime +30 -exec rm -f {} \;
```

查询文件夹大小
```
du -h /path/to/folder | sort -hr | head -n 10
```

# 查询文件大小并排序
```
du -sh * | sort -hr
```

