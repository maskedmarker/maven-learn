# 关于maven原理的练习

Dependency mediation - this determines what version of an artifact will be chosen when multiple versions are encountered as dependencies.
Maven picks the "nearest definition".
Note that if two dependency versions are at the same depth in the dependency tree, the first declaration wins.

"nearest definition" means that the version used will be the closest one to your project in the tree of dependencies.


## 关键概念
project object model(POM)
effective pom
build lifecycle
build profile
build phrase
managed-dependency(即dependencyManagement section中dependencies,限定依赖的版本号)
直接依赖,间接依赖(transitive dependency)
source(指代码,比如java)
resource(指配置文件)
testSource(测试代码)
testResource(测试相关的配置文件)

# 冲突仲裁
优先就近优先原则;其次靠前优先原则


# 验证
mvn dependency:tree -Dverbose


# 注意事项
## managed-dependency
dependencyManagement声明中的managed-dependency有以下作用:
1. 可以对未指定版本号的直接依赖起到兜底作用(间接依赖肯定有版本号)
2. 可以控制间接依赖的版本(即使间接依赖已经指定了版本号)
3. 无法控制已声明版本号的直接依赖

## 配置动态化
1. Explicit command-line trigger(mvn命令行参数, -P)
2. Maven settings trigger(利用pom文件中的<settings>/<activeProfiles>(hard-coded))
3. Environment specifc trigger(JVM参数, -D)

## 插件
查看maven插件的详情,通过下面命令
1. mvn help:describe -Dplugin=<plugin-id>  (第一步确定插件有哪些goal)
2. mvn <goal-prefix>:help -Ddetail=true -Dgoal=<goal-name> (第二步确定该插件的help goal,通过该goal获取其他goal的详情)
