[中文README传送门](https://github.com/TRaaSStack/auto-unit-test-case-generator/blob/main/README_CN.md)
# What is Auto-Unit-Test-Case-Generator
Auto-Unit-Test-Case-Generator generates JUnit test suites for Java class just as its name. During test generation, Auto-Unit-Test-Case-Generator aims to generate high code-coverage (e.g., Branch Coverage and Line Coverage) unit test suites with full automation. This tools is widely used in ANT Group, supports automatic generation of unit tests for more than 1000 projects. 
Advantages of Auto-Unit-Test-Case-Generator:

- High coverage and assertion level

The average line coverage within Ant Group by using the generator is over 60%
The unit test  generated by this tool is highly effective assertions during the practice in Ant Group

- Easy to use

The process of generation of this tool is fully automated. 

# Main Features
Auto-Unit-Test-Case-Generator is developed based on EvoSuite. In Auto-Unit-Test-Case-Generator, we optimized several algorithms to achieve higher code coverage, more efficiency and effectiveness, better structure of test case.
Main Features of Auto-Unit-Test-Case-Generator:

- Suitable for Spring Framework

In Auto-Unit-Test-Case-Generator, we can generate complete mock statements for autowired fields to form meaningful test case,  avoid throwing NullPointerException.

- More efficiency and effectiveness

Like EvoSuite, Auto-Unit-Test-Case-Generator also use the Search Based Software Testing(SBST)  as main algorithm framework. However, random search algorithm will encounter performance problems when class under test uses lots of String which has almost infinite search space. In Auto-Unit-Test-Case-Generator, we proposed and achieved accutare search algorithm to achieve higher efficiency and effectiveness.

- Better structure of test case

In Auto-Unit-Test-Case-Generator, the optimal call sequence algorithm is used through the initialization, insertion, modification and deletion of test case statements, so that the structure of test case is more readable and logical.


# Building Auto-Unit-Test-Case-Generator
To install Auto-Unit-Test-Case-Generator by using Maven, run:
```shell
mvn clean install -Dmaven.test.skip=true
```
Copy smartut.jar to your own Execution path, for example, current path.
```shell
cp ${user.home}/.m2/repository/org/smartut/smartut-master/1.1.0/smartut-master-1.1.0.jar smartut.jar
```


# Using Auto-Unit-Test-Case-Generator
## Prepare dependencies
Before using smartut.jar to generate cases, You need to execute the following commands to prepare dependencies in project under test.
```shell
mvn clean compile
mvn clean install -Dmaven.test.skip=true
mvn dependency:copy-dependencies
```
## Setup
To generate unit test suites, the generator needs to be set up by project classpath first.
```shell
java -jar ./smartut.jar -setup example/target/classes/ example/target/dependency/*.jar
```
## Generate for a specific class
You can run this command to generate unit test suites for a specific class
```shell
java -jar ./smartut.jar -class com.alipay.test.example
```
## Generate for entire folder
You can run this command to generate unit test suites for all classes in `classes` folder:
```shell
java -jar ./smartut.jar -target example/target/classes/
```


# Contact us
If you encounter any problems during use this generator, please contact us via email: smartunit_opensource@service.alipay.com

Also, Auto-Unit-Test-Case-Generator is providing Software-as-a-Service (SaaS). It supports the full lifecycle/evolution of unit test cases, including test case generation, execution,iteration and regression analysis . All stages are triggered automatically by simply providing [Github](https://github.com/) or [Gitee](https://gitee.com/) link. You can visit our SaaS website through https://smartunit.opentrs.com.

# 
 
