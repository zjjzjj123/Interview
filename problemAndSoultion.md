1.jsp中El 和 JSTL表达式不能正常使用

- 可能是因为相应的包没有在maven中导入 可自行搜索maven库导入相关的el和jstl表达式
- 也可能是因为导入了包 但是web的版本问题导致一些表达式不能使用 改变web.xml的头版本
- 永久更改web.xml头文件直接在maven库中修改即可

2.在使用maven构建项目中，在src中单独建立test文件，使用org.junit.test是不能正常工作的，可以在java中建立test文件夹 在里面建立测试类使用org.junit.test就正常了

3.在maven项目中不能通过pom文件导入依赖 可能是因为maven版本过高导致的 更换低一些的版本就可正常导入

4.在web.xml中加入spring的监听器之后就不能正常跳转页面了 问题主要是springmvc.xml和spring.xml的配置文件被我搞反了  配置文件头配置错了 会出现问题 两者的配置文件头是不一样的

5.spring里的测试org.junit.test不行 就是版本的问题 存在有时候能加载 有时候不能加载 可能就是和maven的版本不匹配 一般应该用junit12  但是这次用11好用

6.使用maven时 更改了东西 首先应该先清除clean然后再去执行  这样有效去除缓存 和target里面的以前编译的内容