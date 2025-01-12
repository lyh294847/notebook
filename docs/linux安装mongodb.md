# Linux安装MongoDB

参考官方  
https://www.mongodb.com/zh-cn/docs/v7.0/tutorial/install-mongodb-on-red-hat/#install-mongodb-community-edition

## 设置密码登陆
修改配置文件
`vim /usr/local/mongodb/mongod.conf`
增加
```
security:
  authorization: enabled
```

进入mongo shell  
`mongosh`  

切换到admin数据库  
`use admin`  

创建用户  
`db.createUser({
  user: "root",
  pwd: "VAOPJFA1244gr",
  roles: [{ role: "userAdminAnyDatabase", db: "admin" }]
})`

角色比较：
- root: 最高权限，可以执行任何操作
- userAdminAnyDatabase: 只能管理用户，不能操作数据
- readWriteAnyDatabase: 可以读写所有数据库，但不能管理用户
- dbAdminAnyDatabase: 可以执行数据库管理操作，但不能管理用户

修改用户  
`db.updateUser("root",
  {
    pwd: "VAOPJFA1244gr",
    roles: [{ role: "root", db: "admin" }]
  }
)`

修改密码  
`db.changeUserPassword("root", "xxxxx")`

查询用户是否创建成功  
`db.getUser("root")`





