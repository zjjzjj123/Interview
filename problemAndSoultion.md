1.jsp中El 和 JSTL表达式不能正常使用

- 可能是因为相应的包没有在maven中导入 可自行搜索maven库导入相关的el和jstl表达式
- 也可能是因为导入了包 但是web的版本问题导致一些表达式不能使用 改变web.xml的头版本
- 永久更改web.xml头文件直接在maven库中修改即可