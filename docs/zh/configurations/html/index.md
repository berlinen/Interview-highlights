---
title: 'html 相关'
---

<Block>
# html 相关
</Block>

<Block>
##  关于doctype

###  doctype 作用? 严格模式与混杂模式如何区分？它们有何意义?

!DOCTYPE>声明叫做文件类型定义（DTD），声明的作用为了告诉浏览器该文件的类型。让浏览器解析器知道应该用哪个规范来解析文档。<!DOCTYPE>声明必须在 HTML 文档的第一行，这并不是一个 HTML 标签。

严格模式：又称标准模式，是指浏览器按照 W3C 标准解析代码。

混杂模式：又称怪异模式或兼容模式，是指浏览器用自己的方式解析代码。

如何区分：浏览器解析时到底使用严格模式还是混杂模式，与网页中的 DTD 直接相关。

1、如果文档包含严格的 DOCTYPE ，那么它一般以严格模式呈现。（严格 DTD ——严格模式）
2、包含过渡 DTD 和 URI 的 DOCTYPE ，也以严格模式呈现，但有过渡 DTD 而没有 URI （统一资源标识符，就是声明最后的地址）会导致页面以混杂模式呈现。（有 URI 的过渡 DTD ——严格模式；没有 URI 的过渡 DTD ——混杂模式）
3、DOCTYPE 不存在或形式不正确会导致文档以混杂模式呈现。（DTD不存在或者格式不正确——混杂模式）
4、HTML5 没有 DTD ，因此也就没有严格模式与混杂模式的区别，HTML5 有相对宽松的语法，实现时，已经尽可能大的实现了向后兼容。（ HTML5 没有严格和混杂之分）

### doctype 有什么作用？怎么写？

每个页面都要从 doctype 开始，它为浏览器指定这个页面的文档类型，以便浏览器更正确的显示 HTML 。只要按照这样的格式和位置写，那么浏览器就会认为你在使用标准 HTML 。这样写的好处是：不用再像 HTML5 出来之前那样，既要写上 HTML 版本号，又要写上这个 HTML 文档所依据的标准是在什么位置。一劳永逸，之后不管 HTML 再怎么更新，我们的文档都可以被浏览器以最正确的方式显示出来。

</Block>

<Block>
## 关于 html

### html

 对于元素，html页面中的所有内容都嵌套在这个元素中。

### 页面出现了乱码，是怎么回事？如何解决？

 当编码是一种方式，而解码又是另一种方式时，页面就会出现“乱码”；

 解决方式：只需要知道我在编辑器保存这个 HTML 文件时，保存的是什么编码格式，然后在头部中告诉浏览器用什么方式来解码。

### <img> 有两个必要的属性：src 和 alt

src: 它是 source 的缩写，意指这个图像来源自哪里（这后边可以放所在文件的路径，也可以是一个所在的 URL）；

alt：这个属性主要是为了规避例如：因网速差、硬件设备限制等外部因素，我们的浏览器不能很好的显示出图像，那 alt 后边的文本将会取代图像告诉用户这里会是什么东西（参考后边最终的页面展现）。

### W3C是什么?什么是W3C标准?

W3C是英文 World Wide Web Consortium 的缩写

1.结构标准，代表语言是xHTML

2.表现标准，代表语言是CSS

3.动作标准，代表语言是JavaScrip

### HTML 全局属性（global attribute）有哪些？

accesskey 规定激活元素的快捷键；

class 规定元素的一个或多个类名（引用样式表中的类）；

contenteditable 规定元素内容是否可编辑；

contextmenu 规定元素的上下文菜单。上下文菜单在用户点击元素时显示。

data-* 用于存储页面或应用程序的私有定制数据。

dir 规定元素中内容的文本方向。

draggable 规定元素是否可拖动。

dropzone 规定在拖动被拖动数据时是否进行复制、移动或链接。

hidden  样式上会导致元素不显示，但是不能用这个属性实现样式。

id 规定元素的唯一 id。

lang 规定元素内容的语言。

spellcheck 规定是否对元素进行拼写和语法检查。

style 规定元素的CSS行内元素。

tabindex 规定元素的tab键次序。

title 规定有关元素的额外信息。

translate 规定是否应该翻译元素内容。

### 列出常见h5的标签，并简单介绍这些标签用在什么场景？

<Example>
```html
<article> 用于一篇文章。<article>a self-contained article</article>
<aside> 用于页面的侧边栏。<aside>some content</aside>
<figcaption> 用于一张图表的说明文字
<figure> 用于一张图表
<footer> 用于包裹页面的底部内容
<header> 用于包裹页面的头部内容
<section> 用于包裹一部分有逻辑关第的页面内容
<select> 用于制作一个下拉列表选框
```

</Example>

### 如何理解标签语义化

正确的标签做正确的事情
页面内容结构化
无CSS样子时也容易阅读，便于阅读维护和理解
便于浏览器、搜索引擎解析。 利于爬虫标记、利于SEO

###  在 input 里，name 有什么作用？

用途1： 作为可与服务器交互数据的HTML元素的服务器端的标示，比如input、select、textarea、和button等。我们可以在服务器端根据其Name通过Request.Params取得元素提交的值。

用途2： HTML元素Input type='radio'分组，我们知道radio button控件在同一个分组类，check操作是mutex的，同一时间只能选中一个radio，这个分组就是根据相同的Name属性来实现的。

用途3： 建立页面中的锚点，我们知道a href="URL"是获得一个页面超级链接，如果不用href属性，而改用Name，如：a name="PageBottom" 我们就获得了一个页面锚点。

用途4： 作为对象的Identity，如Applet、Object、Embed等元素。比如在Applet对象实例中，我们将使用其Name来引用该对象。

用途5： 在IMG元素和MAP元素之间关联的时候，如果要定义IMG的热点区域，需要使用其属性usemap，使usemap="#name"(被关联的MAP元素的Name)。

用途6：  某些特定元素的属性，如attribute，meta和param。例如为Object定义参数 PARAM NAME = "appletParameter" VALUE = "value" 或Meta中 META NAME = "Author" CONTENT = "Dave Raggett"

### label 有什么作用？如何使用？

Label标签有两个属性，一个是for，一个是 accesskey。

for功能：表示这个Lable是为哪个控件服务的，Label标签要绑定了for指定HTML元素的ID或name属性，你点击这个标签的时候，所绑定的元素将获取焦点 ，点击label所包裹内容，自动指向for指定的id或name

accesskey则定义了访问这个控件的热键( 所设置的快捷键不能与浏览器的快捷键冲突，否则将优先激活浏览器的快捷键)

### radio如何分组

<Example>
```html
 <form>
    <input type="radio" name="sex" value="male"> 男 <br>
    <input type="radio" name="sex" value="female"> 女<br>
    <input type="radio" name="age" value="adult"> 已成年<br>
    <input type="radio" name="age" value="child"> 未成年
  </form>
```

</Example>

### placeholder 属性有什么作用?
placeholder 属性提供可描述输入字段预期值的提示信息（hint）。

该提示会在输入字段为空时显示，并会在字段获得焦点时消失。

注释：placeholder 属性适用于以下的 <input> 类型：text, search, url, telephone, email 以及 password。

<Example>
```html
  <form action="demo_form.asp" method="get">
    <input type="search" name="user_search" placeholder="Search W3School" />
    <input type="submit" />
  </form>
```
</Example>

###  type=hidden 隐藏域有什么作用？举例说明。

1. 隐藏域的作用是帮助表单收集和发送信息，便于后端处理数据。用户点击提交数据的时候，隐藏域的信息也被一起发送到了后端。

2. 后端接收前端传来的数据，需要确认前端的身份，是本公司的网页传来的数据，而不是其他黑客知道后端地址后传来的假数据。那么就加一个隐藏域，验证value里的值和数据库里name的值是不是对应的，类似于“天王盖地虎，宝塔镇河妖”，暗号对的上，才能证明是自己人，O(∩_∩)O~。

3. 有时候一个表单里有多个提交按钮，后端怎么知道用户是点击哪个按钮提交过来的呢？这时候我们只要加隐藏域，对每一个按钮起个名字(value值)，后端接收到数据后，检查value值，就能知道是哪个按钮提交的了。

4. 有时候一个网页中有多个form，我们知道多个form是不能同时提交的，但有时这些form确实相互作用，我们就可以在form中添加隐藏域来使它们联系起来。

5. JavaScript不支持全局变量，但有时我们必须用全局变量，我们就可以把值先存在隐藏域里，它的值就不会丢失了。

6. 还有个例子，比如按一个按钮弹出四个小窗口，当点击其中的一个小窗口时其他三个自动关闭．可是IE不支持小窗口相互调用，所以只有在父窗口写个隐藏域，当小窗口看到那个隐藏域的值是close时就自己关掉。

###  CSRF 攻击是什么？如何防范？

CSRF（Cross-site request forgery），中文名称：跨站请求伪造。攻击者盗用了你的身份，以你的名义发送恶意请求。

Cross-site request forgery 跨站请求伪造，也被称为 “one click attack” 或者 session riding，通常缩写为 CSRF 或者 XSRF，是一种对网站的恶意利用；可以这么理解CSRF攻击：攻击者盗用你的身份，以你的名义向第三方网站发送恶意请求。CRSF能做的事情包括利用你的身份发邮件，发短信，进行交易转账，甚至盗取账号信息

<Example>

<img :src="$withBase('/img/csrf.png')" />

</Example>

#### 如何防止？

1. 验证 HTTP Referer 字段

HTTP头中的Referer字段记录了该 HTTP 请求的来源地址。在通常情况下，访问一个安全受限页面的请求来自于同一个网站，而如果黑客要对其实施 CSRF 攻击，他一般只能在他自己的网站构造请求。因此，可以通过验证Referer值来防御CSRF 攻击。

2. 使用验证码

关键操作页面加上验证码，后台收到请求后通过判断验证码可以防御CSRF。但这种方法对用户不太友好。

3. 在请求地址中添加token并验证

CSRF 攻击之所以能够成功，是因为黑客可以完全伪造用户的请求，该请求中所有的用户验证信息都是存在于cookie中，因此黑客可以在不知道这些验证信息的情况下直接利用用户自己的cookie 来通过安全验证。要抵御 CSRF，关键在于在请求中放入黑客所不能伪造的信息，并且该信息不存在于 cookie 之中。可以在 HTTP 请求中以参数的形式加入一个随机产生的 token，并在服务器端建立一个拦截器来验证这个 token，如果请求中没有token或者 token 内容不正确，则认为可能是 CSRF 攻击而拒绝该请求。这种方法要比检查 Referer 要安全一些，token 可以在用户登陆后产生并放于session之中，然后在每次请求时把token 从 session 中拿出，与请求中的 token 进行比对，但这种方法的难点在于如何把 token 以参数的形式加入请求。

4. 在HTTP 头中自定义属性并验证

这种方法也是使用 token 并进行验证，和上一种方法不同的是，这里并不是把 token 以参数的形式置于 HTTP 请求之中，而是把它放到 HTTP 头中自定义的属性里。通过 XMLHttpRequest 这个类，可以一次性给所有该类请求加上 csrftoken 这个 HTTP 头属性，并把 token 值放入其中。这样解决了上种方法在请求中加入 token 的不便，同时，通过 XMLHttpRequest 请求的地址不会被记录到浏览器的地址栏，也不用担心 token 会透过 Referer 泄露到其他网站中去。

</Block>

<Block>
## 关于meta

### meta 有哪些常见的值？

一、http-equiv属性

1.Expires:用于设定网页的到期时间。网页一旦到期，必须从服务器接收数据。

<Example>

```html
<meta http-equiv="expires" content="Wed, 20 Jun 2007 22:33:00 GMT">
```
</Example>

2.Pragma:cache模式-用于设定禁止浏览器从本地机的缓存中调阅页面内容，设定后一旦离开网页就无法从cache中再调出，从而无法脱机浏览

<Example>

``` html
<meta http-equiv="Pragma" content="no-cache">
```
</Example>

3.Set-Cookie:cookie设定-如果网页过期，那么存盘中的cookie将被删除

<Example>
```html
<meta http-equiv="Set-Cookie" content="cookievalue=xxx;expires=Wednesday, 20-Jun-2007 22:33:00 GMT； path=/">
```

</Example>

4.Refresh：刷新机制-表示自动刷新并指向新页面

<Example>

```html
<meta http-equiv="Refresh" content="2；URL=http://www.net.cn/">
```
</Example>

2指的是2秒后自动刷新到新的URL网址。

5.Window-target:显示窗口的设定-强制页面在当前窗口以独立页面显示，防止别人在框架里调用自己的页面

<Example>
```html
<meta http-equiv="Window-target" content="_top">
```
</Example>

6.content-Type：设定页面使用的字符集

<Example>

```html
<meta http-equiv="content-Type" content="text/html; charset=gb2312">
```

</Example>

7.Pics-label：网页等级评定，在IE的Internet选项中可以设置来防止浏览一些受限制的网站，网站的限制级别就是通过这个属性来设置的

<Example>
```html
<meta http-equiv="Pics-label" contect="">
```
</Example>

8.cache-control:清除缓存，再次访问这个网站要重新下载

<Example>
```html
<meta http-equiv="cache-control" content="no-cache">
```

</Example>

9.Access-Control-Allow-Origin:跨域请求
```html
<meta http-equiv="Access-Control-Allow-Origin" content="*">
```

10.content-language:显示语言的设定

<Example>

```html
<meta http-equiv="Content-Language"content="zh-cn"/>
```
</Example>

11.imagetoolbar:指定是否显示图片工具栏，false表示不显示

<Example>
```html
<meta http-equiv="imagetoolbar"content="false"/>
```
</Example>

12.Content-Script-Type:W3C网页指定页面中的脚本的类型：

<Example>
```html
<meta http-equiv="Content-Script-Type"Content="text/javascript">
```
</Example>

### 二、name属性

name属性主要用于描述网页，与之对应的属性值为content，content中的内容主要是便于搜索引擎机器人查找信息和分类信息用的。

1.keywords:设置关键字，给搜索引擎用的

<Example>
```html
<meta name="keywords" content="keyword1,keyword2,keyword3">
```
</Example>

2.description：页面描述

<Example>
```html
<meta name="description" content="This is my page">
```
</Example>

3.robots:用于告诉搜索机器人哪些页面需要索引，哪些页面不用

<Example>
```html
<meta name="robots"content="none">
```
</Example>

content的参数有all（文件将被检索，且页面上的链接可以被查询）,none（文件将不被检索，且页面上的链接不可以被查询）,index（文件将被检索）,noindex（文件将不被检索，但页面上的链接可以被查询）,follow（页面上的链接可以被查询）,nofollow（文件将被检索，但页面上的链接不可以被查询）。默认是all。

4.author:标注网页的作者

<Example>
```html
<meta name="author"content="root,root@xxxx.com">
```
</Example>

5.generator:说明网站采用什么软件做的

<Example>
```html
<meta name="generator"content="信息参数"/>
```
</Example>

6.copyright:网站版权信息

<Example>
```html
<meta name="copyright" content="信息参数">
```
</Example>

###  meta viewport 是做什么用的，怎么写？

name为viewport表示供移动设备使用. content定义了viewport的属性.
width表示移动设设备下显示的宽度为设备宽度(device-width)
height表示移动设设备下显示的宽度为设备宽度.
user-scalable表示用户缩放能力, no表示不允许.
initial-scale表示设备与视口的缩放比率
maximum和minimum分别表示缩放的最大最小值, 要注意的是, maximum必须必minimum大.

</Block>

<Block>
##  post 和 get 方式提交数据有什么区别？

1. GET使用URL或Cookie传参，而POST将数据放在BODY中”，这个是因为HTTP协议用法的约定。并非它们的本身区别。

2. GET方式提交的数据有长度限制，则POST的数据则可以非常大”，这个是因为它们使用的操作系统和浏览器设置的不同引起的区别。也不是GET和POST本身的区别。

3. POST比GET安全，因为数据在地址栏上不可见”，这个说法没毛病，但依然不是GET和POST本身的区别。

4. 内置区别

GET和POST最大的区别主要是GET请求是幂等性的，POST请求不是。这个是它们本质区别，上面的只是在使用上的区别。

<Example>
```text
什么是幂等性？幂等性是指一次和多次请求某一个资源应该具有同样的副作用。

简单来说意味着对同一URL的多个请求应该返回同样的结果。
```
</Example>
正因为它们有这样的区别，所以不应该且不能用get请求做数据的增删改这些有副作用的操作。因为get请求是幂等的，在网络不好的隧道中会尝试重试。如果用get请求增数据，会有重复操作的风险，而这种重复操作可能会导致副作用（浏览器和操作系统并不知道你会用get请求去做增操作）。

</Block>







