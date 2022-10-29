# flex布局（弹性布局）基础知识



# 一、 flex 布局（弹性布局）基础知识

## 1. flex 布局中常用术语(三个二)

| 序号 | 简记   | 术语                                    |
| ---- | ------ | --------------------------------------- |
| 1    | 二成员 | 容器和项目(`container / item`)          |
| 2    | 二根轴 | 主轴与交叉轴(`main-axis / cross-axis`)  |
| 3    | 二根线 | 起始线与结束线(`flex-start / flex-end`) |

## 2. `display`属性

| 序号 | 属性值         | 描述               | 备注                                                     |
| ---- | -------------- | ------------------ | -------------------------------------------------------- |
| 1    | `flex;`        | 创建 flex 块级容器 | 内部子元素自动成为 flex 项目                             |
| 2    | `inline-flex;` | 创建 flex 行内容器 | 内部子元素自动成为 flex 项目，多个`inline-flex;`才有效果 |

## 3.flex 容器属性

| 序号 | 属性              | 描述                                                         |
| ---- | ----------------- | ------------------------------------------------------------ |
| 1    | `flex-direction`  | 设置容器中的主轴方向: 行/水平方向, 列/垂直方向               |
| 2    | `flex-wrap`       | 是否允许创建多行容器,即 flex 项目一行排列不下时, 是否允许换行 |
| 3    | `flex-flow`       | 简化 `flex-direction, flex-wrap` 属性                        |
| 4    | `justify-content` | 设置 flex 项目在主轴上对齐方式                               |
| 5    | `align-items`     | 设置 flex 项目在交叉轴上对齐方式                             |
| 6    | `align-content`   | 多行容器中,项目在交叉轴上的对齐方式                          |

## 4.flex 容器属性

| 序号 | 属性          | 描述                                                         |
| ---- | ------------- | ------------------------------------------------------------ |
| 1    | `flex-basis`  | 项目宽度: 项目分配主轴剩余空间之前, 项目所占据的主轴空间宽度 |
| 2    | `flex-grow`   | 项目的宽度扩展: 将主轴上的剩余空间按比例分配给指定项目       |
| 3    | `flex-shrink` | 项目的宽度收缩: 将项目上多出空间按比例在项目间进行缩减       |
| 4    | `flex`        | 是上面三个属性的简化缩写: `flex: flex-grow flex-shrink flex-basis` |
| 5    | `align-self`  | 单独自定义某个项目在交叉轴上的对齐方式                       |
| 6    | `order`       | 自定义项目在主轴上的排列顺序,默认为 0,书写顺序,值越小位置越靠前 |

------

# 二、 代码演示 flex 属性

## 1、display属性

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            /*设置容器为弹性容器，容器内项目自动转为弹性项目,默认水平排列*/
            /*display: flex;*/
            display: inline-flex;
        }
        .container2 {
            width: 300px;
            height: 150px;
            /*设置容器为弹性容器，容器内项目自动转为弹性项目,默认水平排列*/
            /*display: flex;*/
            display: inline-flex;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 1.1 `display: flex;`设置容器为弹性容器，容器内项目自动转为弹性项目

![img](https://img.php.cn/upload/image/976/381/811/1586530687690965.png)

### 1.2 `display: inline-flex;`：创建 flex 行内容器，多个才有效

![img](https://img.php.cn/upload/image/531/996/248/1586530712478550.png)

------

## 2、flex-wrap：设置容器主轴方向

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            display: flex;
            /*flex-direction: row;*/
            /*flex-direction: row-reverse;*/
            /*flex-direction: column;*/
            flex-direction: column-reverse;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 2.1 `flex-direction：row;`：设置主轴方向：水平，默认值

![img](https://img.php.cn/upload/image/607/736/418/1586531056491272.png)

### 2.2 `flex-direction: row-reverse;`：设置主轴方向：水平，右到左

![img](https://img.php.cn/upload/image/301/812/862/1586531068853524.png)

### 2.3 `flex-direction: column;`：设置主轴方向：垂直，上到下

![img](https://img.php.cn/upload/image/841/448/123/1586531096625404.png)

### 2.4 `flex-direction: column;`：设置主轴方向：垂直，下到上

![img](https://img.php.cn/upload/image/630/101/963/1586531113254231.png)

------

## 3、flex-wrap：设置项目在容器主轴是否换行

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            display: flex;
            /*flex-wrap: nowrap;*/
            /*flex-wrap: wrap;*/
            flex-wrap: wrap-reverse;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 3.1 `flex-wrap: nowrap;`：默认值，不换行,如果当前容器容纳不小, 项目会自动收缩

![img](https://img.php.cn/upload/image/237/421/570/1586531498656777.png)

### 3.2 `lex-wrap: wrap;`：换行, 当前行容纳不下的项目会换行显示,此时,创建的容器叫:多行容器

![img](https://img.php.cn/upload/image/445/517/855/1586531518265959.png)

### 3.3 `flex-wrap: wrap-reverse;`：换行,反向

![img](https://img.php.cn/upload/image/795/338/501/1586531538955678.png)

------

## 4、flex-flow: row nowrap;：设置容器主轴与项目是否换行简写

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            display: flex;
            /*flex-flow: row nowrap;*/
            /*flex-flow: row wrap;*/
            /*flex-flow: row wrap-reverse;*/
            /*flex-flow: column nowrap;*/
            /*flex-flow: column wrap;*/
            flex-flow: column wrap-reverse;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 4.1 `flex-flow: row nowrap;`：水平，不换行

![img](https://img.php.cn/upload/image/650/550/319/1586531934919932.png)

### 4.2 `flex-flow: row wrap;`：水平，换行

![img](https://img.php.cn/upload/image/554/535/342/1586531961363097.png)

### 4.3 `flex-flow: row wrap-reverse;`：水平，换行，反向

![img](https://img.php.cn/upload/image/758/604/397/1586535615412171.png)

### 4.4 `flex-flow: column nowrap;`：垂直，不换行（列）

![img](https://img.php.cn/upload/image/182/473/261/1586535630601488.png)

### 4.5 `flex-flow: column wrap;`：垂直，换行（列）

![img](https://img.php.cn/upload/image/821/593/140/1586535651226561.png)

### 4.6 `flex-flow: column wrap-reverse;`：垂直，换行（列），反向

![img](https://img.php.cn/upload/image/528/200/234/1586535679859204.png)

------

## 5、justify-content：弹性项在目容器主轴上的对齐方式

```css
<style>
        .container {
            width: 400px;
            height: 150px;
            display: flex;
            /*justify-content: flex-start;*/
            /*justify-content: flex-end;*/
            /*justify-content: center;*/
            /*justify-content: space-between;*/
            /*justify-content: space-around;*/
            justify-content: space-evenly;
        }
        .item {
            width: 80px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 5.1 `justify-content: flex-start;`：主轴起始线对齐，默认

![img](https://img.php.cn/upload/image/511/246/698/1586535734764084.png)

### 5.2 `display: inline-flex;`：主轴终止线对齐

![img](https://img.php.cn/upload/image/482/581/983/1586535815261092.png)

### 5.3 `display: inline-flex;`：居中对齐

![img](https://img.php.cn/upload/image/335/251/647/1586535836175494.png)

### 5.4 `flex-wrap: nowrap;`：两端对齐—剩余空间在头尾项目之外的项目间平均分配

![img](https://img.php.cn/upload/image/117/408/786/1586535859899316.png)

### 5.5 `display: inline-flex;`：分散对齐—剩余空间在每个项目二侧平均分配

![img](https://img.php.cn/upload/image/579/610/915/1586535878906858.png)

### 5.6 `display: inline-flex;`：平均对齐—剩余空间在每个项目之间平均分配

![img](https://img.php.cn/upload/image/572/430/858/1586535896472219.png)

------

## 6、align-items：容器交叉轴项目对齐

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            display: flex;
            /*align-items: flex-start;*/
            /*align-items: flex-end;*/
            align-items: center;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 6.1 `align-items: flex-start;`：与交叉轴起始线对齐

![img](https://img.php.cn/upload/image/530/156/976/1586535925813795.png)

### 6.2 `align-items: flex-end;`：与交叉轴终止线对齐

![img](https://img.php.cn/upload/image/237/376/257/1586535939852195.png)

### 6.3 `align-items: center;`：居中对齐

![img](https://img.php.cn/upload/image/647/238/267/1586535958617123.png)

------

## 7、align-content：多行容器中项目在交叉轴的对齐方式

```css
<style>
        .container {
            width: 300px;
            height: 200px;
            display: flex;
            /*设置换行变为多行容器*/
            flex-wrap: wrap;
            /*align-content: stretch;*/
            /*align-content: flex-start;*/
            /*align-content: flex-end;*/
            /*align-content: center;*/
            /*align-content: space-between;*/
            /*align-content: space-around;*/
            align-content: space-evenly;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
    </style>
```

### 7.1 `align-content: stretch;`：项目拉伸占据整个交叉轴

![img](https://img.php.cn/upload/image/493/595/647/1586536016608654.png)

### 7.2 `align-content: flex-start;`：所有项目与交叉轴起始线(顶部)对齐

![img](https://img.php.cn/upload/image/193/150/369/1586536037585719.png)

### 7.3 `align-content: flex-end;`：所有项目与交叉轴终止线对齐

![img](https://img.php.cn/upload/image/459/535/535/1586536077846054.png)

### 7.4 `align-content: center;`：所有项目与交叉轴中间线对齐: 居中对齐

![img](https://img.php.cn/upload/image/998/491/897/1586536098338472.png)

### 7.5 `align-content: space-between;`：两端对齐: 剩余空间在头尾项目之外的项目间平均分配

![img](https://img.php.cn/upload/image/877/562/685/1586536117525384.png)

### 7.6 `align-content: space-around;`：分散对齐: 剩余空间在每个项目二侧平均分配

![img](https://img.php.cn/upload/image/471/845/138/1586536141737746.png)

### 7.7 `align-content: space-evenly;`：平均对齐: 剩余空间在每个项目之间平均分配

![img](https://img.php.cn/upload/image/290/298/793/1586536159187883.png)

------

## 8、`align-self`：单独某个项目在交叉轴的对齐方式

- 该属性可覆盖容器的`align-items`, 用以自定义某个项目的对齐方式

### 8.1 `align-self: auto;`：继承 `align-items` 属性值

### 8.2 `align-self: flex-start;`：与交叉轴起始线对齐

### 8.3 `align-self: flex-end;`：与交叉轴终止线对齐

### 8.4 `align-self: center;`：与交叉轴中间线对齐: 居中对齐

### 8.5 `align-self: stretch;`：在交叉轴方向上拉伸

### 8.6 `align-self: baseline;`：与基线对齐(与内容相关用得极少)

```css
  <style>
        .container {
            width: 300px;
            height: 200px;
            display: flex;
        }
        .item {
            width: 100px;
            height: 50px;
            background-color: skyblue;
        }
        .item:first-of-type {
            background-color: lightcoral;
            align-self: flex-start;
        }
        .item:nth-of-type(2) {
            background-color: wheat;
            align-self: flex-end;
        }
        .item:nth-of-type(3) {
            align-self: center;
        }
        .item:nth-of-type(4) {
            height: inherit;
            align-self: stretch;
            background-color: lightgreen;
        }
        .item:last-of-type {
            align-self: baseline;
        }
    </style>
```

![img](https://img.php.cn/upload/image/918/402/280/1586534048752185.png)

------

## 9、`flex-grow`：项目放大因子：分配主轴剩余空间

### 9.1 `flex-grow: 0; / flex-grow: initial;`：不放大,保持初始值

### 9.2 `flex-grow: n;`：n为正数，创建 flex 行内容器

```css
<style>
        .container {
            width: 480px;
            height: 150px;
            display: flex;
        }
        .item {
            width: 80px;
            height: 50px;
            background-color: skyblue;
        }
        .item:first-of-type {
            background-color: lightgreen;
            flex-grow: 1;
        }
        .item:nth-of-type(2) {
            background-color: lightcoral;
            flex-grow: 2;
        }
        .item:last-of-type {
            background-color: wheat;
            flex-grow: 3;
        }
    </style>
```

![img](https://img.php.cn/upload/image/277/995/788/1586534627637741.png)

------

## 10、flex-shrink：项目收缩因子：主轴空间小于项目空间时，收缩顶目空间

```css
<style>
        .container {
            width: 300px;
            height: 150px;
            display: flex;
        }
        .item {
            width: 120px;
            height: 50px;
            background-color: skyblue;
            /*flex-shrink: 0;*/
        }
        .item:last-of-type {
            /*flex-shrink: 0.5;*/
        }
```

### 10.1 `flex-shrink: 1; / flex-shrink: initial;`：允许项目收缩

### 10.2 `flex-shrink: 0;`：禁止收缩

![img](https://img.php.cn/upload/image/129/523/484/1586535176424180.png)

### 10.3 `flex-shrink: n;`：n为正数，创建 flex 行内容器

![img](https://img.php.cn/upload/image/399/831/373/1586535194608205.png)

------

## 11、flex-basis：项目计算尺寸

- width < flex-basis < min/max-width;

```css
<style>
        /* 容器 */
        .container {
            width: 300px;
            height: 150px;
            display: flex;
            flex-flow: row wrap;
        }
        /* 项目/子元素 */
        .item {
            width: 50px;
            height: 50px;
            background-color: skyblue;
        }
        .item {
             /*auto === width 50px*/
            /*flex-basis: auto;*/
            flex-basis: 70px;
            /*flex-basis: 20%;*/
            /*flex-basis: 5rem;*/
            /*max-width: 100px;*/
            /*flex-basis: 150px;*/
        }
    </style>
```

------

## 12、flex：项目缩放的简写

```css
<style>
      .container {
        width: 300px;
        height: 150px;
        display: flex;
      }
      .item {
        width: 100px;
        height: 50px;
        background-color: skyblue;
        font-size: 1.5rem;
      }
      .item:first-of-type {
        background-color: lightgreen;
        /* 默认:不放大,允许收缩, 以项目的width为准 */
        flex: 0 1 auto;
        flex: 1 1 auto;
        /* flex: 0 1 80px; */
      }
      .item:nth-of-type(2) {
        background-color: lightcoral;
        flex: 0 100px;
      }
      .item:last-of-type {
        background-color: wheat;
        flex: auto;
        flex: 1;
        flex: none;
        flex: 0 0 auto;
        flex: 0 0 250px;
      }
    </style>
```

### 12.1 三值语法: `flex: flex-grow flex-shrink flex-basis`

| 序号 | 案例              | 描述                            |
| ---- | ----------------- | ------------------------------- |
| 1    | `flex: 0 1 auto`  | 默认值: 不放大,可收缩, 初始宽度 |
| 2    | `flex: 1 1 auto`  | 项目自动放大或收缩适应容器      |
| 3    | `flex: 0 0 100px` | 按计算大小填充到容器中          |

### 12.2 二值语法: `flex: flex-grow flex-basis`

| 案例            | 描述                            |
| --------------- | ------------------------------- |
| `flex: 0 180px` | 禁止放大,按计算大小填充到容器中 |

### 12.3 单值语法

| 序号 | 案例          | 描述              |
| ---- | ------------- | ----------------- |
| 1    | `flex: 1`     | `flex: 1 1 auto`  |
| 2    | `flex: 180px` | `flex: 1 1 180px` |
| 3    | `initial`     | `flex: 0 1 auto`  |
| 4    | `auto`        | `flex: 1 1 auto`  |
| 5    | `none`        | `flex: 0 0 auto`  |

# 三、 课程总结

## 1、`flex`简写是难点，基础知识，多写，多记，可以先从`flex`三值语法先熟悉。

## 2、`flex: 1`、`flex: 0`：比较常用，不理解可以，背下来。