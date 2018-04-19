thymeleaf
1 、变量表达式
    语法：${....}
    例如 <th th:text=" ${userModel.user.id}">..</th>
2 、 消息表达式
    语法：#{....}
    例如 <th th:text=" #{userModel.user.id}">..</th>
3、  选择表达式
    语法: *{...}
    <div th:object ="${book}">
      ....
        <span th:text ="*{title}">....</span>
      ...
    </div>
    与变量 式区别：他们是在当前选择的对象而不是整个上下文变量映射上执行
 4、链接表达式
   语法： @{...}
   链接 表达式可以是相对的，在这种情况下，应用程序上下文将不会作为URL的前缀
   <a href="@{../documents/report}">...</a>
 5、分段表达式
   语法：th:insert 或th:replace
    <div th:replace="~{fragments/header :: header}">...</div>
 6、字面量
   布尔 <div th:if="${user.isAdmin{}} == false">....
7、基本迭代器 th:each
   <li th:each ="book :${book}" th:text ="${book.title}">  </li>
    
   
