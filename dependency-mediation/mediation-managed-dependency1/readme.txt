E:\git-repo\cjh-repo\maven-learn\dependency-mediation\mediation-managed-dependency1>mvn dependency:tree -Dverbose
[INFO] Scanning for projects...
[INFO]
[INFO] -------< org.example.learn.maven:mediation-managed-dependency1 >--------
[INFO] Building mediation-managed-dependency1 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-dependency-plugin:2.8:tree (default-cli) @ mediation-managed-dependency1 ---
[INFO] org.example.learn.maven:mediation-managed-dependency1:jar:1.0-SNAPSHOT
[INFO] \- org.example.learn.maven:service-a:jar:1.0-SNAPSHOT:compile
[INFO]    +- com.alibaba:fastjson:jar:2.0.21:compile
[INFO]    |  \- com.alibaba.fastjson2:fastjson2-extension:jar:2.0.21:compile
[INFO]    |     \- com.alibaba.fastjson2:fastjson2:jar:2.0.21:compile
[INFO]    +- com.google.guava:guava:jar:29.0-jre:compile
[INFO]    |  +- com.google.guava:failureaccess:jar:1.0.1:compile
[INFO]    |  +- com.google.guava:listenablefuture:jar:9999.0-empty-to-avoid-conflict-with-guava:compile
[INFO]    |  +- com.google.code.findbugs:jsr305:jar:3.0.2:compile
[INFO]    |  +- org.checkerframework:checker-qual:jar:2.11.1:compile
[INFO]    |  +- com.google.errorprone:error_prone_annotations:jar:2.3.4:compile
[INFO]    |  \- com.google.j2objc:j2objc-annotations:jar:1.3:compile
[INFO]    \- xstream:xstream:jar:1.1.3:compile
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.876 s
[INFO] Finished at: 2023-04-04T23:37:11+08:00
[INFO] ------------------------------------------------------------------------
