# DrawTree
通过解析字符串画出图形

首先，计算机绘图也是要确定一个起始点和开始画线的方向这叫做初始状态，当画图进行到任意一个阶段的时候，我们可以用（x,y,a）这三个量来确定任意一个画图的状态，即当前的坐标x,y和当前要画线条的方向角a。然后，我们需要考虑的是状态到状态是如何转换的。我们把状态之间的转换称为动作，不难看出，仅仅用平移和旋转方向就能完成状态之间的转换。接下来，我们用符号定义一些简单的动作（包括评议、旋转和辅助动作）。

F：表示在当前的位置画一条长为l的直线段。l是由用户事先任意设定的数值，表示基本线段的长度。
+：表示逆时针旋转一个角θ，θ的数值由用户事先确定.
-：表示顺时针旋转一个角θ.
[：表示暂时保存当前的画图状态.
]：表示提取出保存的画图状态。 “[”和“]”要成对的出现。


这样，确定了开始的坐标和方向，由上面符号组成的任意的一系列指令就能指导画图了。
