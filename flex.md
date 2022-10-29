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

## 2.字体图标 Icon Font

字体图标显示的并不是具体的文字之类的，而是各种图标。因为他是字体，所以可以当成字体来用，只需要给出对应的字符而不需要通过测量背景图片位置那么麻烦。字体图标最大的好处，在于它不会变形且加载速度快。字体图标可以像文字一样，随意通过 css 来控制它的大小和颜色，对于建网站来说，非常方便。

Icon Font 优缺点：首先它的体积比图片小很多，而且还具有更好的可维护性（因为是矢量，所以拉伸不变形；可以随意的改变颜色、产生阴影、透明效果等等）不需要下载一个图像，可以减少 HTTP 请求。当然，Icon Font 也是有缺点的，由于是字体，支持简单的颜色，多种颜色兼容性不好。

### **1.下载兼容字体包**

阿里巴巴矢量图标库（www.iconfont.cn)

1. 资源管理->我的项目->新建项目，右边点击新建项目，用于保存自己常用的图标。

2. 项目新建完成后，王项目里添加我们要项使用的图标，找到图标库，搜索一个想要的图标，然后添加到购物车；

3. 添加到购物车后，将打包好的字体文件（icon font.ttf | iconfont.woff | iconfont.woff2 | iconfont.css）下载到本地添加到你的项目中。

4. 将下载的文件夹解压，放到你的项目目录中，再在你的项目中引入 iconfont.css 文件。

### 2.字体图标引入到 HTML

项目中引入样式文件，直接 link 进来就行了

**html 引入**

```js
<link rel='stylesheet' href='font/iconfont.css'
```

如何在项目中使用字体图标呢，其实很简单。创建一个 i 标签或者 span 标签，添加两个类名，一个固定类名是 iconfont，另一个是你 i 想要的那个图标对应的类名。

**vue3 引入**

```vue
<template>
  <div>
    <i class="iconfont">&#xe641;</i>
    <i class="iconfont icon-qiandao"></i>
  </div>
</template>

<script setup></script>

<style scoped>
@import "@/assets/iconfont.css";
</style>
```

**iconfont.css**

```css
@font-face {
  font-family: "iconfont"; /* Project id 3732672 */
  src: url("./fonts./iconfont.woff2?t=1666849095233") format("woff2"), url("./fonts/iconfont.woff?t=1666849095233")
      format("woff"),
    url("./fonts/iconfont.ttf?t=1666849095233") format("truetype");
}

[class^="icon-"],
[class*="icon-"] {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.icon-qiandao:before {
  content: "\e641";
}
```

**小技巧：增加伪类扩大点击范围**

```css
<style>
.icon-qiandao {
  position: relative;
  color: orange;
}
.icon-qiandao:after {
  content: "";
  position: absolute;
  top: -15px;
  left: -15px;
  bottom: -15px;
  right: -15px;
}
</style>
```

### 3.vite+vue3 中使用 iconfont 的 svg 图标

1、登录阿里图标库，把需要的字体图标加入到自己的项目中，

阿里图标库地址：[iconfont-阿里巴巴矢量图标库](https://www.iconfont.cn/)

2、进入图标添加的项目中，点击 Symbol，然后点击暂无代码，点击生成：

![img](https://img-blog.csdnimg.cn/683a493ce733409fae232968a5928a31.png)

3、然后会生成一个链接，点击链接，进入后全选内容并复制：

![img](https://img-blog.csdnimg.cn/50710186ad9c44c1b6e61f824ac28927.png)

4、在项目中新建一个文件，将复制的内容放到新建的文件里面。

![img](https://img-blog.csdnimg.cn/66642388ff6e4754aaa15acc314e589c.png)

5、创建一个 SvgIcon 公共组件，代码如下：

```TypeScript
<template>
  <svg :class="svgClass" aria-hidden="true">
    <use :xlink:href="iconClassName" :fill="color" />
  </svg>
</template>

<script setup lang="ts">
  import { computed } from 'vue'
  const props = defineProps({
    iconName: {
      type: String,
      required: true,
    },
    className: {
      type: String,
      default: '',
    },
    color: {
      type: String,
      default: '#5c6b77',

    },
  })

  // 图标在 iconfont 中的名字

  const iconClassName = computed(() => {
    return `#${props.iconName}`
  })

  // 给图标添加上类名

  const svgClass = computed(() => {

    if (props.className) {

      return `svg-icon ${props.className}`

    }
    return 'svg-icon'
  })
</script>

<style scoped>

  .svg-icon {
    width: 3em;
    height: 3em;
    position: relative;
    fill: currentColor;
    vertical-align: -2px;
  }
</style>
```

6、在 main.ts 中，注册为全局组件：

```TypeScript
import SvgIcon from '@/components/SvgIcon/index.vue'

app.Component('SvgIcon',SvgIcon)
```

7、在页面中使用：

```TypeScript
<svg-icon iconName="icon-huiyuan" />
```

## 3.css3 线性渐变

为了创建 一个线性渐变，你必须至少定义两种颜色节点。颜色结点即你想要呈现平稳过渡的颜色。同时，你也可以设置一个起点和一个方向（或者一个角度）。

**线性渐变-从上到下（默认情况下）**

下面的实例演示了从顶部开始的线性渐变。起点是红色，慢慢过渡到绿色：

从上到下的线性渐变：

```css
.box {
  background: linear-gradient(red, green);
}
```

**线性渐变-从左到右**

下面的实例演示了从左到右的线性渐变。起点是红色，慢慢过渡到绿色：

```css
.box {
  background: linear-gradient(to right, red, green);
}
```

**使用角度**

如果希望对渐变角度做更多的控制，您可以定义一个角度，来取代预定义的方向（向下、向上、向右、向左、向右下等等）。值 0deg 等于向上（to top）。值 90deg 等于向右（to right）。值 180deg 等于向下（to bottom）。

带有指定的角度的线性渐变：

```css
.box {
  background: linear-gradient(180deg, red, green);
}
```

![img](https://img-blog.csdnimg.cn/20200421101616546.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ2NTgyNDIx,size_16,color_FFFFFF,t_70)

**左上到右下**

```
.box {
  background-image: linear-gradient(to bottom right, red, yellow);
}
```

## 4.css3 结构伪类选择器

CSS 中的结构伪类选择器是根据 HTML 页面元素之间的关系来定位 HTML 元素，从而减少对 HTML 元素的 id 属性和 class 属性的依赖

1. 作用：根据元素在根据 HTML 页面元素之间的关系查找元素
2. 优势：减少对 HTML 元素中类的依赖，有利于保持代码整洁

**css3 选择器 nth-child(n)**

nth-child(n),n 可以是数字、关键词或公式。选择器匹配属于其父元素的第 N 个子元素，不论元素的类型。

序号写法：li:nth-child(3){background:orange;} 把第 3 个 LI 的背景设为橙色

倍数写法：li:nth-child(3n){background:orange;} 把第 3，6，9…个 LI 的背景设为橙色

序号写法：li:nth-child(3n+1){background:orange;} 把第 1,4,7…个 LI 的背景设为橙色
