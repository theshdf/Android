#### Activity

>简单理解: activity是一个与用户进行交互的窗口，用户所有的操作都是通过和avtivity交互完成的

* #### 生命周期
>oncreate->onstart
->onresume->onrestart
->onpause->onstop->ondestroy

几种情况的对应的生命周期：

1. 打开一个页面时:oncreate->onstart->onresume
2. 再打开一个页面：上层页面：oncreate->onstart->onresume.底部页面：onpause->onstop
3. 顶层页面退出：顶层页面：pause->onstop->ondestroy.底部页面：onrestart->onstart->onresume

* activity加载过程
  
* 横竖屏切换
* 文字描述：Android中的横竖屏切换是由代码控制的，而不是由手机中横竖屏设置控制的。当代码设置默认值的时候，手机的屏幕才根据手机旋转进行横竖屏切换，在横竖屏切换的过程中，activity会先被销毁然后又重建。

##### 横竖屏设置
  >unspecified：系统默认的横竖屏切换方式是和手机的横竖屏相关，手机横屏，屏幕就转换为横屏，反之就是竖屏

  >landscape：横屏显示

  >portrait：竖屏展示

  >locked: 锁死当前屏幕的方向

  ##### 生命周期

  如果不想重建activity，那么需要在manifest中声明 configChanges="orientation|keyboardHidden|screenSize".那么在acitivty中重写onConfigurationChanged。

  #### 横竖屏切换顺便切换布局

  在res下面定义layout-land 和layout-port。在屏幕切换时会自动加载对应的布局。

* #### 启动模式
* 
  1. standar
   >每次启动一个activity，都会创建一个新的并放在栈顶

  2. singletop
   >判断启动的activity是不是在栈顶，如果是，则不会创建新的activity，并调用onnewintent(),如果不是则会创建一个新的activity

  3. singletask
   
  4. singleinstance

#### Fragment

1. 生命周期

2. fragment+viewpage时数据的预加载和懒加载

3. 底部切换fragment的实现方式

#### Service
