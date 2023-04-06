# 关于maven原理的练习

Dependency mediation - this determines what version of an artifact will be chosen when multiple versions are encountered as dependencies.
Maven picks the "nearest definition".
Note that if two dependency versions are at the same depth in the dependency tree, the first declaration wins.

"nearest definition" means that the version used will be the closest one to your project in the tree of dependencies.


## 关键概念
effective pom
project object model(POM)
build lifecycle
build profile

# 冲突仲裁
优先就近优先原则;其次靠前优先原则


# 验证
mvn dependency:tree -Dverbose
通过IDEA的右键/maven/show effectvie pom并不是可靠的途径

