## canvas 炫酷时钟

### 实现功能
* [x]小球动态时钟
* [x]彩色小球动画

### 实现步骤
1. 构建一个点阵的二维数组（0-9）
2. 创建画布
3. 获取当前的时分秒分别执行绘制函数
4. 设置定时器执行绘制时钟函数
5. 对比绘制时钟前的时间和绘制时钟后的时分秒，有变动就执行生成小方块函数

### 可能会碰到的问题
1. 当前时分秒有个位数如何处理？
    >一个以%取余数，一个除以10
2. 彩色小球重叠绘制？
    >绘制之后的小球没有做动画，一直在原坐标点上
3. 运行久了消耗电脑CPU
    >页面ball.message数组一直在增加，删除走出画面的小球
    >1. 判断小球是否在画面内（判断左边缘和右边缘）
    >2. 如果小球还在画面内，就放到数组前面
    >3. 如果当前小球大于在画面中的小球数量，就删除后面的小球数组
