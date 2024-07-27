E:\git-repo\cjh-repo\maven-learn\dependency-mediation\mediation-dependency1>mvn dependency:tree -Dverbose
[INFO] Scanning for projects...
[INFO]
[INFO] -----------< org.example.learn.maven:mediation-dependency1 >------------
[INFO] Building mediation-dependency1 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-dependency-plugin:2.8:tree (default-cli) @ mediation-dependency1 ---
[INFO] org.example.learn.maven:mediation-dependency1:jar:1.0-SNAPSHOT
[INFO] +- org.example.learn.maven:service-a:jar:1.0-SNAPSHOT:compile
[INFO] |  \- com.alibaba:fastjson:jar:2.0.21:compile
[INFO] |     \- com.alibaba.fastjson2:fastjson2-extension:jar:2.0.21:compile
[INFO] |        \- com.alibaba.fastjson2:fastjson2:jar:2.0.21:compile
[INFO] \- org.example.learn.maven:service-b:jar:1.0-SNAPSHOT:compile
[INFO]    \- (com.alibaba:fastjson:jar:2.0.23:compile - omitted for conflict with 2.0.21)
[INFO] ------------------------------------------------------------------------
