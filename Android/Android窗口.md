![](http://o86ou4qz3.bkt.clouddn.com/window.png)

>Android中与用户进行交互的操作由Activity完成。activity中包含一个窗口类(Window)的实现类Phonewindow,activity通过这个类来管理窗口。PhoneWindow中通过DecorView来管理界面的展示，界面中的内容包含了通知栏，标题栏，内容区，Decorview是一个实现了linearlayout的根布局，内容区是一个Framelayout布局区域，setcontentView中的内容展示在这里

1. 设置屏幕全屏
2. 设置屏幕content展示内容
3. 设置标题栏的状态