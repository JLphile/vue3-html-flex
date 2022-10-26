## 1.容器的属性

### flex-direction 属性

flex-direction 属性决定主轴的方向（即项目的排列方向）
基本语法格式如下：

```html
.box{ flex-direction: row | row-reverse | column | colum-reverse; }
```

它可能有 4 个值。

row(默认值)：主轴为水平方向，起点在左端。
row-reverse：主轴为水平方向，起点在右端。
column：主轴为垂直方向，起点在上沿。
column-reverse：主轴为垂直方向，起点在下沿。

### flex-wrap 属性

默认情况下，项目都在一条线（轴线）上。flex-wrap 属性定义，如果一条轴线排不下，如何换行。

基本语法如下：

```html
.box{ flex-wrap: nowrap | wrap | wrp-reverse; }
```

```
nowrap(默认):不换行。
wrap：换行，第一行在上方。
wrap-reverse：换行，第一行在下方。
```

### flex-flow 属性

flex-flow 属性是 flex-direction 属性和 flex-wrap 属性的简写，默认 row nowrap。

```html
.box { flex-flow: <flex-direction> <flex-wrap>; }</flex-wrap></flex-direction>
```

### justify-content 属性

justify-content 属性定义了项目在主轴上的对齐方式。

基本语法格式如下：

```html
.box { justify-content: flex-start | flex-end | center | space-between |
space-around; }
```

对齐方式与主轴方向有关，当主轴沿水平方向从左到右时，具体含义为：

- flex-start （默认值）：左对齐
- flex-end：右对齐
- center：居中
- space-between：两端对齐，项目之间的间隔都相等。
- space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。相当于每个项目先均分容器空间，然后在分得的空间内居中。

### align-items 属性

align-items 属性定义项目在与主轴垂直交叉轴上的对齐方式。

基本语法如下：

```html
.box { align-items: flex-start | flex-end | center | baseline | stretch; }
```

具体的对齐方式与交叉轴的方向有关，当主轴水平时，其具体含义为：

- flex-start：交叉轴的起点对齐。
- flex-end：交叉轴的终点对齐。
- center：交叉轴的中点对齐。
- baseline：项目的第一行文字的基线对齐。
- stretch（默认值）：如果项目未设置高度或设为 auto，将占满整个容器高度。

### align-content 属性

用于控制多行项目的对齐方式，如果项目只有一行则不起作用；注意当有多行时，定义了 align-content 后，align-items 属性将失效。默认 stretch，即在项目没设置高度，或高度未 auto 情况下让项目填满整个容器，与 align-items 类似。align-content 可能值含义如下（假设主轴为水平方向）

基本语法如下：

```
.box {
	align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

**注意：**

align-items：时作用于容器内的每一行在当前交叉轴的对齐位置，如果容器内有多行，则以每行的交叉轴为标准来对齐

align-content：设置容器内部所有行作为一个整体在垂直方向排列方式，针对多行作为一个整体在交叉轴上的排列，改属性对单行无效。
