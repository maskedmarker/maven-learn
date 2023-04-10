super pom在仓库中的位置 ${M2_HOME}/lib/maven-model-builder-3.0.3.jar/org/apache/maven/model/pom-<version>.xml

参考:
https://stackoverflow.com/questions/13354531/maven-project-build-directory


预定义的一些变量
  <build>
    <directory>${project.basedir}/target</directory>
    <outputDirectory>${project.build.directory}/classes</outputDirectory>
    <finalName>${project.artifactId}-${project.version}</finalName>
    <testOutputDirectory>${project.build.directory}/test-classes</testOutputDirectory>
    <sourceDirectory>${project.basedir}/src/main/java</sourceDirectory>
    <scriptSourceDirectory>${project.basedir}/src/main/scripts</scriptSourceDirectory>
    <testSourceDirectory>${project.basedir}/src/test/java</testSourceDirectory>
    <resources>
      <resource>
        <directory>${project.basedir}/src/main/resources</directory>
      </resource>
    </resources>
    <testResources>
      <testResource>
        <directory>${project.basedir}/src/test/resources</directory>
      </testResource>
    </testResources>
  </build>

maven中的预定义变量的表达式与xpath路径定位类似.比如
${project.version} 的值等于xml文件中的<project>/<version>的元素值
${project.build.directory} 的值等于xml文件中的<project>/<build>/<directory>的元素值


预定义的一些配置文件路径
    <resources>
      <resource>
        <directory>${project.basedir}/src/main/resources</directory>
      </resource>
    </resources>
    <testResources>
      <testResource>
        <directory>${project.basedir}/src/test/resources</directory>
      </testResource>
    </testResources>


预定义的plugin
