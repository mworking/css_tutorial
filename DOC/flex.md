1. 文档流
1. display 属性
1. 盒模型
1. flex 布局

### 注意:
1. 属性因该是配合着使用，单个属性可能起不了作用
```
 .first-face {
    display: flex;
    justify-content: center;
    align-items: center;
  }
```
for example:
justify-content 属性肯定需要 display设置为 flex 的配合


### 容器的属性
1.flex-direction
    row | row-reverse | column | column-reverse

    row（默认值）：主轴为水平方向，起点在左端。
    row-reverse：主轴为水平方向，起点在右端。
    column：主轴为垂直方向，起点在上沿。
    column-reverse：主轴为垂直方向，起点在下沿。

2.flex-wrap
    flex-wrap: nowrap | wrap | wrap-reverse;

    nowrap（默认）：不换行
    wrap：换行，第一行在上方
    wrap-reverse：换行，第一行在下方

3.flex-flow
    <flex-direction> || <flex-wrap>

4.justify-content  属性定义了项目在主轴上的对齐方式
    flex-start | flex-end | center | space-between | space-around;

    flex-start（默认值）：左对齐
    flex-end：右对齐
    center： 居中
    space-between：两端对齐，项目之间的间隔都相等。
    space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。


5.align-items 属性定义项目在交叉轴上如何对齐
    flex-start | flex-end | center | baseline | stretch;

    flex-start：交叉轴的起点对齐。
    flex-end：交叉轴的终点对齐。
    center：交叉轴的中点对齐。
    baseline: 项目的第一行文字的基线对齐。
    stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。


6.align-content  属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
    flex-start | flex-end | center | space-between | space-around | stretch;

    flex-start：与交叉轴的起点对齐。
    flex-end：与交叉轴的终点对齐。
    center：与交叉轴的中点对齐。
    space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
    space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
    stretch（默认值）：轴线占满整个交叉轴。


### 项目的属性
1.order
    order: <integer>;
    order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0

2.flex-grow
    flex-grow: <number>; /* default 0 */
    flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。

3.flex-shrink
  flex-shrink: <number>; /* default 1 */
  flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。

4.flex-basis
    flex-basis: <length> | auto; /* default auto */
    flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。

5.flex
    flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
    flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。

6.align-self
    align-self: auto | flex-start | flex-end | center | baseline | stretch;
    align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。


