![HUAWEI](https://tva1.sinaimg.cn/large/00831rSTly1gck8vzyxc4g305k09t48a.gif)

![HUAWEI (https://tva1.sinaimg.cn/large/00831rSTly1gck991obyhg305k09t45z.gif)](/Users/wislie/Pictures/com.tencent.qq/HUAWEI (1).gif)



主要分3个小块: 发射器, 气泡, 圆环

**思路:**

**一.发射器(完全不透明):**

位于屏幕最下方, 取圆弧上的3点, 用3阶贝塞尔构成path

**二.气泡(不完全透明):**

1.发射器处随机产生气泡,气泡的数量默认为10;

2.气泡未离开发射器的部分会被发射器遮挡;

3.气泡刚离开发射器,会有一个黏性的变化效果, 使用3阶贝塞尔曲线,将多个变化的点连接起来,构成path;

4.气泡在往上移动中,半径会变小, 小于一定值,气泡会消失;

5.气泡靠近圆环到一定距离,也会有一个黏性变化效果,并且速度变慢, 使用方式类似于3

6.气泡与圆环的零距离时,气泡消失

**三.圆环:**

1.由多个长度不一的片段构成, 圆弧上的3个点构成一个片段,采用的也是3阶贝塞尔曲线;

2.每个片段都围绕圆环中心旋转,透明度在某个区间不断变化; 旋转速度在某几个值之间也不断改变,从而影响片段之间的开口大小

3.如果手机电量发生改变，显示的电量百分比也发生改变；拖动进度条可改变电量百分比和 发射器,气泡,圆环的颜色







