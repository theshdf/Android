https://juejin.im/post/5b631d326fb9a04fce524db2
[中文文档]{https://flutterchina.club/setup-windows/}
#### 环境搭建
* 下载flutter包并解压缩  https://flutter.io/sdk-archive/#windows
* 设置环境变量 在用户变量下Path下添加flutter\bin的全路径。创建PUB_HOSTED_URL = https://pub.flutter-io.cn 和FLUTTER_STORAGE_BASE_URL = https://storage.flutter-io.cn并设置值
* 运行flutter doctor命令进行检查
* 打开android studio创建flutter项目

### Dart语言：
#### 基本类型
String
nubmber：int,double
bool
#### 变量
>所有的基本数据类型和类都继承自object，默认值都是NULL,并且自带了getter，setter方法，如果用final或者const修饰，那么只有getter方法
>* dart中数据类型转换字符串需要显示转换，不同于java
>声明列表： var list = []

#### 方法

#### Widget
在flutter中，界面中的显示都是widget，widget是一切的基础，等同于android原生中的view。widget中的数据刷新是通过mvvm机制实现的。我们所做的就是要实现widget界面，并将界面和数据绑定。

#### 页面导航-页面之间的切换
>