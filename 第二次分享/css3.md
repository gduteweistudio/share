###css3
####圆角与阴影
#####盒子圆角
**border-radius**

**功能**：可以将盒子的四个角设置为圆角的风格

* 值：
    数值：border-radius:10px;
    百分比（基于宽度高度）：border-radius:50%;
值设为百分比时有如下两种情况：
`百分比的宽是以 宽度（高度为参考的百分比）`
1. 如果是一个长方形那么它是一个椭圆

2. 高度宽度一致（正方形）时为正圆
border-radius:50%;

* 单个圆角：
    border-top-lelft-radius：上左角
    border-top-right-radius：上右角
    border-bottom-lelft-radius：下左角
    border-bottom-right-radius：下右角

* 复合属性：
    四个值：border-radius:上左 上右 下右 下左；
    三个值：border-radius:上左 上右与下左 下右 ；
    两个值：border-radius:上左与下右 上右与下左；
    一个值：border-radius:四个角；

#####阴影
属性：border-radus /  text-shadow

功能：设置元素或文字的阴影

值：
* `h-shadow`：阴影X轴的偏移量。允许负值，必选
* `v-shadow`：阴影Y轴的偏移量。允许负值，必选
* `blur`：阴影模糊度。必选
* `spread`：阴影面积增量。可选
* `color`：阴影的颜色，必选
* `inset`：阴影的风格。可选，默认值为outset

多层阴影：一个元素可以设置多层阴影，阴影的属性之间用逗号隔开
    示例：
```
style{
        box-shadow:/*盒子阴影*/
            0 0 10px red;
            0 0 20px blue;
      text-shadow：0px 0px 10px black；/*文本阴影*/
    }
```

**单个shadow的使用**
*   给出两个、三个或四个数字值的情况。
    *   如果只给出两个值, 这两个值将被浏览器解释为x轴上的偏移量[<offset-x>](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#%3Coffset-x%3E%20%3Coffset-y%3E)和y轴上的偏移量[<offset-y>](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#%3Coffset-x%3E%20%3Coffset-y%3E)。
    *   如果给出了第三个值, 这第三个值将被解释为模糊半径的大小 [<blur-radius>](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#%3Cblur-radius%3E)。
    *   如果给出了第四个值, 这第四个值将被解释为扩展半径的大小 [<spread-radius>](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#%3Cspread-radius%3E)。
*   可选， 关键词[inset](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#inset)。
*   可选， 颜色值 [<color>](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow#%3Ccolor%3E)。
####过渡（transition）
过渡的作用是在元素的某些属性发生改变的时候，比如宽度从 100px 改变至 200px 的过程中，有一个渐渐改变的效果，从而实现一些类似动画的效果
* `transition-property`：需要过渡的属性。all全部属性
* `transition-duration`：过渡完成 一次的总时间
* `transition-timing-function`：规定过渡进行时速度曲线。
* `transition-delay`：规定给过渡效果开始前的延迟时间。

**简写格式**：过渡的复合样式的时候可以省略一些不必要的参数，省略的参数均为默认值
    `示例`：
```
        transition:2s; 
        transition:color 2s;
```
复合属性设置多个值：过渡的复合属性通过逗号隔开同样的可以设置多个不同的渐变属性
    `示例`：
```
        transition:
            width 2s,
            height 4s;
```
**`过渡的注意点`**：
    1. 只有当元素的属性值发生改变的时候过渡才有意义
    2. `display:none`;到`display:block`;之间不能过渡，并且会影响到其他过渡
    3. 部分值不能过渡：
        过渡属性查询网址：http://www.css88.com/book/css/properties/transition/transition-property.htm
