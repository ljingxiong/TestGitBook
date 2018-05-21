作者：潇13狼

链接：https://www.zhihu.com/question/24826065/answer/194294438

来源：知乎

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

  


  


了解一样东西,我认为最重要的莫过于了解Ta的过去,Ta的现状,以及Ta的未来.学习CSS也不外乎如此.

通过网络学习一样新东西,最大的困惑就是----网上的文章,写得非常好.但就是碎片化,不系统.而且还有个情况就是:有些问题,大神们觉得很简单,不屑一提或者毫无意识的内容或知识,对于那些刚入门的人因为不知道,也没人点播,有可能会在这个问题上迷茫很久.这一点我体会颇深.

经验分享:**入门阶段不要管好那么多细节,记忆之类的东西,尽快地入门才是最重要的.其实入门,无非就是对所学内容形成一套概念,知其然,所以然.大概的就成了.**

我就结合自己的学习历程和踩过的一些坑,来谈谈我对CSS的认识吧.希望可以帮助到刚刚入门想学习CSS的童鞋,建立起对CSS的认知体系.

~Hope you like it~

相关回答

[潇13狼：如何有效快速的学习HTML/CSS/JS？](https://www.zhihu.com/question/23714828/answer/194892525)

[潇13狼：想要学CSS应该如何入门？](https://www.zhihu.com/question/24826065/answer/194294438)

[潇13狼：什么才是JS模块化？](https://www.zhihu.com/question/39825164/answer/194940548)

  


## **前言**

如果说,前端最令人苦恼的事情,我相信百分之百的童鞋都会说,浏览器的兼容性问题.这是一个大坑.而**浏览器的兼容性问题,99%来自于CSS——层叠样式表**.

目前CSS的版本就是,一般指的就是CSS2.1这个版本,而现在正在推广的版本是CSS3.国外已经基本用上了,国内正在推广.CSS3有很多新功能,但我认为最重要的一点就是,因为这个版本的CSS是几大浏览器厂商谈出来的,所以在兼容性方面会有很大提升.

CSS层叠样式表,主要有两个功能:一是组件的具体样式\(如字体,背景,边框等等\);二是网页的布局.

## **网页布局**

先谈一下网页布局吧,最早的网页布局,是table\(html标签的一种,意为表格\)布局,这是由两个原因造成的,1最早的网页只有html,没有css. 所以html身兼两职,内容与样式.而后来随着前端技术的发展,出现了css,开始了内容与样式的分离,table布局这种hack写法才逐渐消亡.\(名词解释:hack,黑客,在前端中,意为使用特殊而不正规的代码解决浏览器的兼容性问题,虽然我知道这种写法不好,但它就是管用.所以你就得用,在低版本ie中最为常见.只能记,没有什么规律\) 现在的主流是div+css布局.但是初入门的童鞋不要觉得这很高大上,其实这个现在已经是非常非常基础的概念的,对于现在只要是个网页都是DIV+CSS.前几年,这个概念还算是比较新,比如学校图书馆里就借到过标题为”DIV+CSS”的书.好像现在当当上还有.但我建议吧,到现在还用这个概念宣传的书,可以不用买的.

> PS:Div和Table都是html里的标签,区别在于: 标签Table,意为表格.主职是展示以表格的形式展示大量的数据,曾经的布局功能,是hack写法,现在不推荐.标签DIV,无含义标签,布局是其主要功能.

刚开始初入门前端的时候,[http://www.w3school.com.cn/](https://link.zhihu.com/?target=http%3A//www.w3school.com.cn/).

例子都很简单,很好上手,但过于细了.但有些可以需要注意的,部分内容建议跳过.比如说用html实现样式效果的部分..因为这种写法是最早的写法,那时没有css,而现在已经不推荐了.我一开始自学的时候,这一部分的内容,对我后面学习css造成了一定的困扰,因为有些属性名会互相干扰.

其实,单独拿出来说,是想表达----对于有些已经过时的内容,就应该果断跳过.因为人的记忆和时间都是有限的,也是宝贵的.如果是为了考试或者是笔试,那么加强一下记忆是很有必要的.但是一般工作,你都是可以根据手册,搜索,书籍,或者参考代码找到你需要的东西.很多东西用的多了,自然就记住了.

**这也是一个经验吧,入门阶段不要管好那么多细节,记忆之类的东西,尽快地入门才是最重要的.其实入门,无非就是形成一套概念,知其然,所以然.大概的就成了.如果入了半天,还停留在细节处的熟悉,会对信心造成打击.极端情况下,会造成学一样东西,入半天门而不得入,然后换一样东西,继续入半天门而不得入的情况.**

## **基础概念**

**CSS盒模型.**

盒子模型有两种,分别是 IE 盒子模型和标准 W3C 盒子模型.他们对盒子模型的解释各不相同.先来看看我们熟悉的标准盒子模型.

  


&lt;

img src="https://pic1.zhimg.com/50/v2-9694298277c4e739856be3bc1a58bd2c\_hd.jpg" data-rawwidth="554" data-rawheight="338" class="origin\_image zh-lightbox-thumb" width="554" data-original="https://pic1.zhimg.com/v2-9694298277c4e739856be3bc1a58bd2c\_r.jpg"

&gt;

![](https://pic1.zhimg.com/80/v2-9694298277c4e739856be3bc1a58bd2c_hd.jpg)

  


　　从上图可以看到标准 W3C 盒子模型的范围包括 margin,border,padding,content,并且 content 部分不包含其他部分.

&lt;

img src="https://pic2.zhimg.com/50/v2-5b1deff12e612ac1516f42feafff1b74\_hd.jpg" data-rawwidth="553" data-rawheight="323" class="origin\_image zh-lightbox-thumb" width="553" data-original="https://pic2.zhimg.com/v2-5b1deff12e612ac1516f42feafff1b74\_r.jpg"

&gt;

![](https://pic2.zhimg.com/80/v2-5b1deff12e612ac1516f42feafff1b74_hd.jpg)

  


从上图可以看到 IE 盒子模型的范围也包括 margin,border,padding,content,和标准 W3C 盒子模型不同的是:IE 盒子模型的 content 部分包含了 border 和 pading.

  


问题1:那应该选择哪种盒子模型呢?

当然是“标准 W3C 盒子模型”了.

问题2:怎么样才算是选择了“标准 W3C 盒子模型”呢?

很简单,就是在网页的顶部加上 DOCTYPE 声明.如果不加 DOCTYPE 声明,那么各个浏览器会根据自己的行为去理解网页,即 IE 浏览器会采用 IE 盒子模型去解释你的盒子,而 FF 会采用标准 W3C 盒子模型解释你的盒子,所以网页在不同的浏览器中就显示的不一样了.反之,如果加上了 DOCTYPE 声明,那么所有浏览器都会采用标准 W3C 盒子模型去解释你的盒子,网页就能在各个浏览器中显示一致了.

## **CSS网页布局**

**CSS传统解决方案**

CSS实现页面布局,或者是在页面上做些小效果的时候经常会用到 display,position和float 属性,如果对它们不是很了解的话,很容易出现一些莫名其妙的效果,让我们从基础的CSS知识谈起,相信很多初学者一样不明白CSS原理,一味追求效果,结果页面漏洞百出,错误匪夷所思.\(参考:”[CSS布局 ——从display,position, float属性谈起](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/dolphinX/archive/2012/10/13/2722501.html)”,链接:[http://www.cnblogs.com/dolphinX/archive/2012/10/13/2722501.html](https://link.zhihu.com/?target=http%3A//www.cnblogs.com/dolphinX/archive/2012/10/13/2722501.html)\).

这里面有几个地方讲的比较好,我摘录一下.其实这些内容,网上还有很多相同的,但都不太系统,一篇文章只讲一个内容.我这里把他们串起来,方便理解认识.

**块级元素与行内元素**

首先谈谈人们经常提及的**块级元素**和**行内\(内联\)元素**

p, ul, form, div等元素被称为块级元素,这些元素显示为一块儿内容（会自动换行）,span, input 等元素称为行内元素,这两者主要区别就是块级元素会从上到下一个个垂直排列,每个自占一行,而行内元素在一行中水平排列,行内元素的高度由其内容撑开,不可显示的设置其高度,这就是为什么我们一次次的在span上设置height属性不好使的原因.

简单了解了这些知识,让我们看看display常用的几个属性.

&lt;

img src="https://pic2.zhimg.com/50/v2-857b4acc2e0c0b2024528d2138fa0486\_hd.jpg" data-rawwidth="554" data-rawheight="221" class="origin\_image zh-lightbox-thumb" width="554" data-original="https://pic2.zhimg.com/v2-857b4acc2e0c0b2024528d2138fa0486\_r.jpg"

&gt;

![](https://pic2.zhimg.com/80/v2-857b4acc2e0c0b2024528d2138fa0486_hd.jpg)

* 在显示隐藏元素的时候经常会用到把display设为none或者’’,设为none效果很明显,就是让元素脱离文档流,不显示,不占文档空间.
* inline-block属性是CSS2.1新加值,IE8以上及其他主流浏览器都已经支持,它可以使元素像行内元素那样水平一次排列,但是框的内容符合块级元素行为,能够显示设置宽,高,内外边距.很有意思.
* 还有一点儿很有意思,可以通过不同的赋值改变元素生成框的类型,也就是说,通过将display属性设置为block,可以使行内元素表现的像块级元素一样,反之亦然.

**position属性**

要想了解CSS元素定位就需要了解position属性.position属性有几个常用值如下:

&lt;

img src="https://pic4.zhimg.com/50/v2-aaeacd589d25e53f17a859203f75f808\_hd.jpg" data-rawwidth="554" data-rawheight="352" class="origin\_image zh-lightbox-thumb" width="554" data-original="https://pic4.zhimg.com/v2-aaeacd589d25e53f17a859203f75f808\_r.jpg"

&gt;

![](https://pic4.zhimg.com/80/v2-aaeacd589d25e53f17a859203f75f808_hd.jpg)

**定位机制**

CSS有三种基本的定位机制:普通流,绝对定位和浮动.

普通流

* **普通流是默认定位方式,在普通流中元素框的位置由元素在html中的位置决定.**
  元素position属性为static或继承来的static时就会按照普通流定位,这也是我们最常见的方式.
  **\(position : static\)**
* 相对定位比较简单,对应position属性的relative值,如果对一个元素进行相对定位,它将出现在他所在的位置上,然后可以通过设置垂直或水平位置,让这个元素相对于它自己移动,在使用相对定位时,无论元素是否移动,元素在文档流中占据原来空间,只是表现会改变.
  **相对定位可以看作特殊的普通流定位,元素位置是相对于他在普通流中位置发生变化.**
  **\(position : relative\)**

绝对定位

* **绝对定位的元素的位置是相对于距离他最近的非static祖先元素位置决定的.**
  绝对定位使元素的位置与文档流无关,也不占据文档流空间,普通流中的元素布局就像绝对定位元素不存在一样.如果元素没有已定位的祖先元素,那么他的位置就相对于初始包含块儿（body或html）元素.因为绝对定位与文档流无关,所以绝对定位的元素可以覆盖页面上的其他元素,可以通过z-index属性控制叠放顺序,z-index越高,元素位置越靠上.
  **\(position : absolute\)**
* 最后要说的就是fixed属性了,fixed定位也叫固定定位,
  **固定定位是绝对定位的一种**
  .固定定位的元素也不包含在普通文档流中,差异是该元素的包含块儿是视口（viewport）.所谓视口,说简单点,就是指浏览器窗口.最常见一些页面弹出窗口,总在浏览器窗口的右下角,估计用的是类似技术.
  **\(position : fixed\)**

浮动

* 首先介绍一些浮动模型的基本知识:浮动模型也是一种可视化格式模型,浮动的框可以左右移动（根据float属性值而定）,直到它的外边缘碰到包含框或者另一个浮动元素的框的边缘.浮动元素不在文档的普通流中,文档的普通流中的元素表现的就像浮动元素不存在一样.
  **\(float: left / float: right\)**

  


## **CSS弹性布局**

&lt;

img src="https://pic3.zhimg.com/50/v2-219e1fa03615c213c2865b0eb8585d57\_hd.jpg" data-rawwidth="455" data-rawheight="239" class="origin\_image zh-lightbox-thumb" width="455" data-original="https://pic3.zhimg.com/v2-219e1fa03615c213c2865b0eb8585d57\_r.jpg"

&gt;

![](https://pic3.zhimg.com/80/v2-219e1fa03615c213c2865b0eb8585d57_hd.jpg)

此段参考: 阮一峰-Flex 布局教程:语法篇 [http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html](https://link.zhihu.com/?target=http%3A//www.ruanyifeng.com/blog/2015/07/flex-grammar.html)

布局的传统解决方案,基于[盒状模型](https://link.zhihu.com/?target=https%3A//developer.mozilla.org/en-US/docs/Web/CSS/box_model),依赖 [display](https://link.zhihu.com/?target=https%3A//developer.mozilla.org/en-US/docs/Web/CSS/display) 属性 + [position](https://link.zhihu.com/?target=https%3A//developer.mozilla.org/en-US/docs/Web/CSS/position)属性 + [float](https://link.zhihu.com/?target=https%3A//developer.mozilla.org/en-US/docs/Web/CSS/float)属性.它对于那些特殊布局非常不方便,比如,[垂直居中](https://link.zhihu.com/?target=https%3A//css-tricks.com/centering-css-complete-guide/)就不容易实现.2009年,W3C 提出了一种新的方案----Flex 布局,可以简便、完整、响应式地实现各种页面布局.目前,它已经得到了所有浏览器的支持.

&lt;

img src="https://pic4.zhimg.com/50/v2-9f7a07cbed3322d5ae2dbba5383844c8\_hd.jpg" data-rawwidth="530" data-rawheight="187" class="origin\_image zh-lightbox-thumb" width="530" data-original="https://pic4.zhimg.com/v2-9f7a07cbed3322d5ae2dbba5383844c8\_r.jpg"

&gt;

![](https://pic4.zhimg.com/80/v2-9f7a07cbed3322d5ae2dbba5383844c8_hd.jpg)

这意味着,现在就能很安全地使用这项功能.Flex 布局将成为未来布局的首选方案.

## **Flex 布局是什么**

Flex 是 Flexible Box 的缩写,意为"弹性布局",用来为盒状模型提供最大的灵活性.

任何一个容器都可以指定为 Flex 布局.

```
.box
{
display
:
flex
;}
```

行内元素也可以使用 Flex 布局.

```
.box
{
display
:
inline
-
flex
;}
```

Webkit 内核的浏览器,必须加上-webkit前缀.

```
.box
{
display
:
-
webkit
-
flex
;
/* Safari */
display
:
flex
;}
```

注意,设为 Flex 布局以后,子元素的float、clear和vertical-align属性将失效.

## **Flex 基本概念**

采用 Flex 布局的元素,称为 Flex 容器（flex container）,简称"容器".它的所有子元素自动成为容器成员,称为 Flex 项目（flex item）,简称"项目".

&lt;

img src="https://pic1.zhimg.com/50/v2-31d08d465e227052fc214b957f7e9aef\_hd.jpg" data-rawwidth="563" data-rawheight="333" class="origin\_image zh-lightbox-thumb" width="563" data-original="https://pic1.zhimg.com/v2-31d08d465e227052fc214b957f7e9aef\_r.jpg"

&gt;

![](https://pic1.zhimg.com/80/v2-31d08d465e227052fc214b957f7e9aef_hd.jpg)

容器默认存在两根轴:水平的主轴（main axis）和垂直的交叉轴（cross axis）.主轴的开始位置（与边框的交叉点）叫做main start,结束位置叫做main end；交叉轴的开始位置叫做cross start,结束位置叫做cross end.

项目默认沿主轴排列.单个项目占据的主轴空间叫做main size,占据的交叉轴空间叫做cross size.

**Flex 容器的属性**

以下6个属性设置在容器上.

* **flex-direction**
* **flex-wrap**
* **flex-flow**
* **justify-content**
* **align-items**
* **align-content**

**Flex项目的属性**

以下6个属性设置在项目上.

* **order**
* **flex-grow**
* **flex-shrink**
* **flex-basis**
* **flex**
* **align-self**

## **CSS的书写**

CSS层叠样式表之——层叠.简单点就是说,你所看到样式,其实父级元素的样式,加上子级元素的样式共同决定的,而共同决定的方式也即为层叠.既然是层叠,难免会有重复冲突的地方,那么听谁的,这里面就有一个优先级的问题.一般来说,id&gt;class.其实在一般的实践过程中,id因为特指单一,一般用于js的选取,而css很少用id. 而css中的属性又不是全部都能由子元素继承.所以有些属性会继承,有些不会.比如...比如...

Css作为样式的实现,相当的方便.一种效果,通常都会有好几种实现方式,但考虑到后期的修改,以及扩展,css的层级不能过于复杂,应尽可能精简.故而,如何组织CSS代码,就成为必须考虑的问题.&lt;xxxx&gt;书里推荐的是原子化,但有的人持另外的观点,强烈反对之,但不管怎样,我认为这本书的出发点,是可供学习的,就是css代码好坏,应该从可复用性,可扩展性,可维护性出发.打比方说,...

  


随便说一下吧,想说的东西太多,但很不好组织,先写出来吧.

## **CSS RESET与Normalize.css**

摘录至:[http://jerryzou.com/posts/aboutNormalizeCss/](https://link.zhihu.com/?target=http%3A//jerryzou.com/posts/aboutNormalizeCss/) 译至官网,感谢作者的翻译.

Normalize.css 只是一个很小的CSS文件,但它在默认的HTML元素样式上提供了跨浏览器的高度一致性.相比于传统的CSS reset,Normalize.css是一种现代的、为HTML5准备的优质替代方案.Normalize.css现在已经被用于Twitter Bootstrap、HTML5 Boilerplate、[http://GOV.UK](https://link.zhihu.com/?target=http%3A//GOV.UK)、Rdio、CSS Tricks 以及许许多多其他框架、工具和网站上.

**概念综述**

Normalize.css是一种CSS reset的替代方案.经过@necolas和@jon\_neal花了几百个小时来努力研究不同浏览器的默认样式的差异,这个项目终于变成了现在这样.

**Normalize VS Reset**

知道Normalize.css和传统Reset的区别是非常有价值的.

1. Normalize.css 保护了有价值的默认值

Reset通过为几乎所有的元素施加默认样式,强行使得元素有相同的视觉效果.相比之下,Normalize.css保持了许多默认的浏览器样式.这就意味着你不用再为所有公共的排版元素重新设置样式.当一个元素在不同的浏览器中有不同的默认值时,Normalize.css会力求让这些样式保持一致并尽可能与现代标准相符合.

2. Normalize.css 修复了浏览器的bug

它修复了常见的桌面端和移动端浏览器的bug.这往往超出了Reset所能做到的范畴.关于这一点,Normalize.css修复的问题包含了HTML5元素的显示设置、预格式化文字的font-size问题、在IE9中SVG的溢出、许多出现在各浏览器和操作系统中的与表单相关的bug.

3. Normalize.css 不会让你的调试工具变的杂乱

使用Reset最让人困扰的地方莫过于在浏览器调试工具中大段大段的继承链,如下图所示.在Normalize.css中就不会有这样的问题,因为在我们的准则中对多选择器的使用时非常谨慎的,我们仅会有目的地对目标元素设置样式.

4. Normalize.css 是模块化的

这个项目已经被拆分为多个相关却又独立的部分,这使得你能够很容易也很清楚地知道哪些元素被设置了特定的值.因此这能让你自己选择性地移除掉某些永远不会用到部分（比如表单的一般化）.

5. Normalize.css 拥有详细的文档

Normalize.css的代码基于详细而全面的跨浏览器研究与测试.这个文件中拥有详细的代码说明并在Github Wiki中有进一步的说明.这意味着你可以找到每一行代码具体完成了什么工作、为什么要写这句代码、浏览器之间的差异,并且你可以更容易地进行自己的测试.

这个项目的目标是帮助人们了解浏览器默认是如何渲染元素的,同时也让人们很容易地明白如何改进浏览器渲染.

  


## **CSS 预处理器框架/CSS扩展语言**

  


有一种说法,CSS是设计人员的语言,不是程序猿的语言.没有变量,重复的东西要写那么多次,频繁修改怎么办,这些都让程序猿们感觉很不对付.所以机智的程序猿们决定改变这一现状,于是出现了CSS预处理器框架,也称之为CSS扩展语言.目前流行的主要有LESS,SASS.

介绍几个概念:

**基础概念**

首先我们来简单介绍下什么是 CSS 预处理器,CSS 预处理器是一种语言用来为 CSS 增加一些编程的的特性,无需考虑浏览器的兼容性问题,例如你可以在 CSS 中使用变量、简单的程序逻辑、函数等等在编程语言中的一些基本技巧,可以让你的 CSS 更见简洁,适应性更强,代码更直观等诸多好处.

LESS和SASS之所以被称为预处理器,是因为在正式的生产环境中,都需要被预先编译成CSS文件\(备注: LESS文件在相应的JS文件支持下,可以直接应用于生产环境,但由于速度的原因,不推荐\).

LESS依赖于NodeJS,在sublime编辑器中,加装插件,实现代码提示,以及编译功能.这非常非常地棒.因为墙的原因,有可能不能如官网介绍的那样直接安装成功,所以要在国内网站上找版本.而这里面有个比较坑的情况是,网上找到的版本大多来自某前端网分享出来的,很多链接其实都指向这个源头,但这个版本文件是缺失的,是无法正常运行的.好在我是找东西比较厉害的,也没那么容易放弃了,终于找到了一个完整的版本.可以正确运行.

sass基于Ruby语言开发而成,因此安装sass前需要安装Ruby.（注:mac下自带Ruby无需在安装Ruby!）window下安装SASS首先需要安装Ruby,先从官网下载Ruby并安装.安装过程中请注意勾选Add Ruby executables to your PATH添加到系统环境变量.

**关于LESS**

官网:[http://lesscss.cn](https://link.zhihu.com/?target=http%3A//lesscss.cn)

Less 是一门 CSS 预处理语言,它扩展了 CSS 语言,增加了变量、Mixin、函数等特性,使 CSS 更易维护和扩展.Less 可以运行在 Node 或浏览器端.

**关于SASS**

官网:[https://www.sass.hk/](https://link.zhihu.com/?target=https%3A//www.sass.hk/)

Sass是最早的css预处理语言,有比less更为强大的功能.但因其一开始的缩进式语法并不能被开发者们接受,所以使用率不高,不过由于其强大的功能和Ruby on Rails 的大力推动,逐渐被更多开发者使用.

Sass是采用的Ruby语言编写的一款css预处理语言,它诞生于2007年,是最早成熟css预处理语言.最初它是为了配合haml而设计的,因此有着和haml一样的缩进式风格.

Sass从第三代开始,放弃了缩进式风格,并且完全向下兼容普通的css代码,这一代的sass也被称为Scss.

**补充说明**

在这里我要澄清一些问题,很多人觉得哇噻,又要学习新东西,感觉很头大.具体情况具体分析,学习这两个预编译器,其实学习成本都非常非常地低,Less我花了一个下午基本就入门了.其实道理很简单,听我分析,只要你会基本的CSS,其实语法/结构都差不多,然后你又有一点基本的编程基础,基本就很简单了.说到SASS有人觉得Ruby,呀,没学过,有排斥心理.比如说,我自己,之前刚接触的时候选择Less,就是这个原因,后来因为工作原因,也接触了SASS,就知道,这样的担心是多余的,其实和LESS写起来差不多的.所以,有另外一种担心说,没有时间学两种,但怕只学一种,另一种不会怎么办?这两种的迁移成本是比较低的.会了一种,另一种也就差不多.

网上经常有争论说哪种好,两者各自的官网,都说是自己的好.相对来说,SASS要强大一点,但日常工作中,SASS强大的部分,又有多少应用率呢?与其停留在选择的徘徊中,不如直接学了再说.我认为这种争论是无谓的,大概和程序猿争论哪种语言好一样,大家都认为自己的语言才是最好的.

## **CSS in JS**

&lt;

img src="https://pic2.zhimg.com/50/v2-5d7226bd673749f5a14fa9446aa1f497\_hd.jpg" data-rawwidth="553" data-rawheight="311" class="origin\_image zh-lightbox-thumb" width="553" data-original="https://pic2.zhimg.com/v2-5d7226bd673749f5a14fa9446aa1f497\_r.jpg"

&gt;

![](https://pic2.zhimg.com/80/v2-5d7226bd673749f5a14fa9446aa1f497_hd.jpg)

参考文档: 阮一峰 - CSS in JS 简介 [www.ruanyifeng.com/blog/2017/04/css\_in\_js.html](https://link.zhihu.com/?target=http%3A//xn--www-p18dy69dn5d87mtp7ajypo7ao98n.ruanyifeng.com/blog/2017/04/css_in_js.html)

  


既然说到了CSS预处理器,就顺便提一下这个概念吧~

问题1:它们与"CSS 预处理器"（比如 Less 和 [Sass](https://link.zhihu.com/?target=http%3A//www.ruanyifeng.com/blog/2012/06/sass.html),包括 PostCSS）有什么区别?

答: CSS in JS 使用 JavaScript 的语法,是 JavaScript 脚本的一部分,不用从头学习一套专用的 API,也不会多一道编译步骤.简单点说,就是用JavaScript写CSS.

这与最早的JavaScript直接操作css代码的方式略略有点相通,但这里的实现比较高级,是通过构建成第三方的库,来封装CSS.目前就有数十种库.比如说[polished.js](https://link.zhihu.com/?target=https%3A//polished.js.org/).很遗憾的是,目前还看不出哪个库会脱颖而出,成为主流.

问题2:为什么会出现这么多的CSS in JS的库呢?

答:这一切都是因为一个框架React.它非常地火,前端技术比较颠覆.但由于其对CSS 的封装非常弱\(React 对 CSS 封装非常简单,就是沿用了 DOM 的 style 属性对象\),由此催生了一系列的第三方库,用来加强 React 的 CSS 操作.

问题3:为什么React需要加强对CSS的操作?

答:React 是组件结构,它强制要求把 HTML、CSS、JavaScript 写在一起.

表面上,React 的写法是 HTML、CSS、JavaScript 混合在一起.但是,实际上不是.它是用 JavaScript 在写 HTML 和 CSS.React 在 JavaScript 里面实现了对 HTML 和 CSS 的封装,我们通过封装去操作 HTML 和 CSS.也就是说,网页的结构和样式都通过 JavaScript 操作.

**补充说明**

最后说两句个人观点,因为React对前端的颠覆比较大,基本上就是构建了属于自己的一个前端生态圈,学习成本也比较大.但它的影响又比较大,写这篇文章又不能完成忽略它,故此一提,有兴趣的童鞋,自行深入学习.

  


## **CSS框架**

因为 CSS 布局很难使用,所以催生了不少 CSS 框架来帮助开发者.如果你想看看那么这里有一些.只有在框架的功能满足你的需求时,使用框架才是个好主意.掌握CSS的工作方式是无可替代的.

&lt;

img src="https://pic1.zhimg.com/50/v2-bbd06523acb08ce2090fe8d5e79b700a\_hd.jpg" data-rawwidth="554" data-rawheight="425" class="origin\_image zh-lightbox-thumb" width="554" data-original="https://pic1.zhimg.com/v2-bbd06523acb08ce2090fe8d5e79b700a\_r.jpg"

&gt;

![](https://pic1.zhimg.com/80/v2-bbd06523acb08ce2090fe8d5e79b700a_hd.jpg)

> CSS框架的实际数量远不止以上几种

在实际的工作中,构建CSS样式表中,使用框架反而是更为常见的选择.框架的使用有很多好处,比如框架可以替你预处理掉很多问题,让你能更专注于代码开发工作.在使用框架的过程中,只要多翻阅手册,基本上大多数问题都能得到解决.而另一方面,基本上,大多数公司都会选择并使用一套框架,而且不会轻易变更.你需要适应公司的要求.而框架因为其本身的适用场景限制,适用于PC网站的,不一定适用于移动版. 还有另外一个比较麻烦的地方,框架不可能百分百适用于你的项目,通常需要自己也写一些CSS文件来配合框架的使用.通常地,当使用框架所实现的某一效果,与要求不符甚至冲突,都需要你小心翼翼地增添或修改代码.

以我个人的经验来说,我曾将Bootstrap框架套在一个商城项目上,然后也把这个商城项目搬到移动端,虽然Bootstrap支付移动版,但毕竟存在不少问题.后面重新开发,不用框架了,我参考借鉴的是小米商城和京东商城的移动版.整个过程,磕磕碰碰,遇到很多问题,解决很多问题,进步也挺大的.感觉就是小米的代码很干净;京东的就复杂得多,因为应该场景很多,要考虑很多问题.抄网站,确实是一个学习CSS,学习前端的好方法.

大概就酱了~

