## ReactNative
### 一、环境搭建
#### Windosw:
    1. 安装最新版软件Node10,Python3.7,Jdk1.8,AndroidStudio3.1.4,安卓模拟器
    2. 打开命令行 安装yarn-reactnative的命令行工具
    安装：npm install -g yarn react-native-cli
    配置：
    yarn config set registry https://registry.npm.taobao.org --global
    yarn config set disturl https://npm.taobao.org/dist --global
    3. 配置android-home,java-home，jdk目录
    4. 创建一个react-native 项目 react-native init AwesomeProject
    5. 运行项目
    cd AwesomeProject
    react-native run-android

Issue:

1. 安卓模拟器：The development server returned response error code: 500

解决方法：

react-native init Project

cd Project

npm uninstall react-native

npm install --save react-native@0.55.4

npm uninstall --save babel-preset-react-native

npm install --save babel-preset-react-native@4.0.0

react-native run-android

之后重启命令行工具。问题解决

### Mac

按照 [https://reactnative.cn/docs/getting-started.html](https://reactnative.cn/docs/getting-started.html "mac-rn")配置即可