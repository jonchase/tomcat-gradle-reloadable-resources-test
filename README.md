tomcat-gradle-reloadable-resources-test
=======================================

First edit webmodule1/src/main/webapp/META-INF/context.xml
* Specify absolute paths to docBase and extraResourcePaths

Then enable JRebel:
```
export GRADLE_OPTS="-noverify -Drebel.log=true -javaagent:${JREBEL_HOME}/jrebel.jar"
```

Then run Tomcat and test:
```
cd webmodule1
../gradlew tomcatRun

http://localhost:8080/index.jsp    <-- comes from webmodule1
http://localhost:8080/module1.jsp  <-- comes from module1
http://localhost:8080/module1.html <-- comes from module1
```