tomcat-gradle-reloadable-resources-test
=======================================

Test for https://github.com/bmuschko/gradle-tomcat-plugin/issues/29#issuecomment-6994568

```
cd webmodule1
gradle tomcatRun

http://localhost:8080/index.jsp    <-- comes from webmodule1
http://localhost:8080/module1.jsp  <-- comes from module1
http://localhost:8080/module1.html <-- comes from module1
```

Edit module1/src/main/resources/META-INF/resources/module1.* and reload page - no changes reflected.