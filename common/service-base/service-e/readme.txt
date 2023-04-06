Microsoft Windows [版本 10.0.22621.1413]
(c) Microsoft Corporation。保留所有权利。

E:\git-repo\cjh-repo\maven-learn\common\service-base\service-e>mvn dependency:tree -Dverbose
[INFO] Scanning for projects...
[INFO]
[INFO] -----------------< org.example.learn.maven:service-e >------------------
[INFO] Building service-e 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-dependency-plugin:2.8:tree (default-cli) @ service-e ---
[INFO] org.example.learn.maven:service-e:jar:1.0-SNAPSHOT
[INFO] +- com.alibaba:fastjson:jar:2.0.21:compile
[INFO] |  \- com.alibaba.fastjson2:fastjson2-extension:jar:2.0.22:compile (version managed from 2.0.21)
[INFO] |     \- com.alibaba.fastjson2:fastjson2:jar:2.0.22:compile
[INFO] \- com.google.guava:guava:jar:29.0-jre:compile
[INFO]    +- com.google.guava:failureaccess:jar:1.0.1:compile
[INFO]    +- com.google.guava:listenablefuture:jar:9999.0-empty-to-avoid-conflict-with-guava:compile
[INFO]    +- com.google.code.findbugs:jsr305:jar:3.0.2:compile
[INFO]    +- org.checkerframework:checker-qual:jar:2.11.1:compile
[INFO]    +- com.google.errorprone:error_prone_annotations:jar:2.3.4:compile
[INFO]    \- com.google.j2objc:j2objc-annotations:jar:1.3:compile
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.825 s
[INFO] Finished at: 2023-04-06T19:58:26+08:00
[INFO] ------------------------------------------------------------------------
