#### Gradle是什么?

项目依赖构建工具，基于groovy语言，主要用于java面向对象构建项目

#### Android Studio 构建项目

Android项目的编译是gradle来完成，每次编译时根据*.gradle配置文件来进行编译项目，编译之后生成*.apk，然后安装运行apk。

#### Android Studio 使用Gradle操作
1. 在Android Studio的界面上提供了两个构建命令，Android Studio ->Build ->clean project/build project。界面中的clean每次执行都会删除build下的一些文件，而不会删除build目录。rebuild会重新生成被删除的文件，也会生成debug.apk文件

2. 左下角Build Varians. Build Varians = Build type + product flavor的组合。
build type配置的是debug和release包。product flavor是用来打多渠道版本包，两者结合起来就是build varians-即把每个渠道的debug和release包都打出来。所以只有build type的情况下使用build varians或者gradle中的build打包都是一样的。
使用：选中build varians-》选择要打的包类型-》android studio build选项 -》build apks

3. 右上角 Gradle.
可以选择打debug包还是release包，也可以全都打出来

4. build ->generate sign apk ->填写信息打包（这种情况是build.gradle中没有配置signingConfig的，如果配置好了，就没必要每次用该方法）

5. 其他命令行
---
    1. gradlew -v 查看当前gradle版本
    2. gradlew clean 删除build目录，比界面中的clean删除的更彻底
    3. gradlew build 重新生成build目录，并根据*.gradle配置文件----该命令打包只能打debug包
    4. gradlew assembleDebug 打所有的debug包
    5. gradlew assembleRelease 打所有的release包

    
    
6. gradle的配置文件

从project statuct 中进行选择填写即可

7. BuildConfig类

 Android 项目中有一个 BuildConfig 默认生成了gradle 中定义的变量buildConfigField "boolean", "LOG_DEBUG", "true"
可以通过该值控制测试地址和线上地址的修改，也可以控制日志的打印。


