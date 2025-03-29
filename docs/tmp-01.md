# maven的常用命令

## 查看maven设置

如果要查看全局设置, 在非项目目录执行
```text
mvn help:effective-settings
```

如果要查看某个项目的设置, 在项目根目录执行
```text
mvn help:effective-settings
```


## 查看项目生效的 POM 配置
```text
mvn help:effective-pom
```


## 查看项目的实际依赖树
```text
mvn dependency:tree
mvn dependency:tree -Dverbose
```
使用-Dverbose时,可以更清晰的知道哪些依赖因为depth的原因被omitted或version managed



## 手动下载依赖

使用-Dtransitive=true还可以自动下载间接依赖
```text
mvn dependency:get -Dtransitive=true -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging-type>
```

## 手动安装依赖

mvn install:install-file 是 Maven 的一个命令，用于将本地文件（通常是 JAR 包）安装到 Maven 的本地仓库中
```text
mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging-type>
```