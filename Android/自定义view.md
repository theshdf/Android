#### 基础知识
#### 理解：


view在绘制的过程中，是从最外层开始绘制的，先绘制父布局，再绘制子view，在绘制父布局的时候会给出子view绘制的宽高的大小的建议，并确定子view的绘制位置，然后在绘制子view的时候，子view会根据父布局给出的建议，最终计算出自己的宽高，然后通过onsizechanged方法确定宽高


#### 坐标系

在自定义view中共有两个坐标系：
屏幕坐标系：屏幕左上角为坐标原点(0,0)，向右为坐标轴正方向，向下为y轴正方向
最外层的view就是在屏幕坐标系上
内部控件的坐标系是以父控件为坐标系，向右为x轴正方向，向下为y轴正方向

#### 宽高
屏幕坐标系有两种，那么每次点击的位置的横纵坐标也有两个，一个是在屏幕坐标系的位置，一个是在父控件当中的位置

#### 获取屏幕宽高：

1. 
> DisplayMetrics displayMetrics = getResources().getDisplayMetrics();
> width = displayMetrics.widthPixels;
> height = displayMetrics.heightPixels;

2. onDraw()中getWidth(),getHeight也可以获取

构造方法：四个

绘制：重写draw（）进行绘制，通过画笔（Paint）在画布（Canvas）上绘制。

#### [自定义view中wrapcontent不起作用。](https://blog.csdn.net/carson_ho/article/details/62037760)

#### 自定义view继承viewgroup

学习目标：自定义relativelayout实现通用的titlebar

#### Canvas-画布
1. 作用：绘制矩形，正方形，圆角矩形，圆形，椭圆形，弧形


#### path
1. 作用：可以实现canvas中简单的图形绘制，也可以绘制复杂的图形，如心形等，也可以绘制指定路径的文字,裁减画布
2. 方法：lineTo(x,y),moveTo(x,y),setLastPoint(x,y),close()
> lineTo():从当前坐标到lineTo当中指定的坐标，默认坐标是所在父控件的左上角。
> moveTo():用moveTo当中的坐标替换当前的坐标为起点坐标，注意：替换后即使坐标位置相同，也不是同一个起点，在使用close()方法时，如果使用moveTo(),则无法闭合图形
> setLastPoint()：修改要绘制的终点坐标位置，用来替换lineTo()中的坐标
> close()。形成闭合图形。如果起点，终点，连接后不能闭合，则不连接起点和终点


#### 实现一个并列柱状图

1. 两根柱子在同一坐标系中，x轴和y轴的最大值和最小值相同
2. 相邻两个柱子的间距要小于两个柱子和两个柱子之间的间距
3. 每根柱子的底部文字绘制方向向下，或者两个柱子只用颜色区分，对颜色作出说明
4. 对柱子添加点击事件
