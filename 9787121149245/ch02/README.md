# 第 2 章 入门


## 获得命令行程序

* SQLite 命令行程序(后面简称为 CLP)


## 命令行程序

* 可以运行在 Shell 模式下以交互的方式执行查询操作
* 可以运行在命令行模式下完成各种数据库管理

### Shell 模式下的 CLP

* CLP 会将输入的任何语句当成查询命令，除非命令以(`.`)开始
* `.help` 可以得到这些操作的完整列表

## 数据库管理

创建数据库

```
sqlite3 test.db
```

改善显示格式

```
.mode column
.headers on
```

获得最后插入的自增量值

```
select last_insert_rowid();
```

所有表和视图的列表

```
.tables
```

查看表的索引

```
.indices [table name];
```

查看一个表或视图的定义语句


* 更详细的 schema 信息可以通过 SQLite 的重要系统视图 `sqlite_master` 得到


```
.schema [table name]
```
