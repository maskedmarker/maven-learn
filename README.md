#关于maven原理的练习

Dependency mediation - this determines what version of an artifact will be chosen when multiple versions are encountered as dependencies.
Maven picks the "nearest definition".
Note that if two dependency versions are at the same depth in the dependency tree, the first declaration wins.

"nearest definition" means that the version used will be the closest one to your project in the tree of dependencies.


## 关键概念
effective pom



#冲突仲裁
优先就近优先原则;其次靠前优先原则


#验证
mvn dependency:tree -Dverbose

##如下待确认
这里的距离衡量标准是节点的depth,而不是distance.这棵树的根节点是当前项目本身.
不管是从parent继承来的还是当前项目的pom中声明的依赖,都是子节点.
不同点是:继承来的依赖相当于是在本pom声明的,depth=1.
当前项目和parent的依赖冲突时,当前项目的依赖胜利.
