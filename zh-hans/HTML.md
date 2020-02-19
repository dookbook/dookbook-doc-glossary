TOPICS: HyperText Markup Language

# 超文本标记语言 (HyperText Markup Language, HTML)

**HTML**（**HyperText Markup Language**，**超文本标记语言**）是用来定义**网页结构**的一种*描述性*的、*标记*语言。

HTML文件通常会以 **`.htm`** 或 **`.html`** 为扩展名。用户可以从Web服务器中下载，并使用任何
*[Web浏览器](/zh-hans/glossary/Web_browser)* 来解析和显示。

## 发展简史

1990年，由于对[Web](/zh-hans/glossary/World_Wide_Web)未来发展的远见，*Tim Berners-Lee*提出了
**[超文本](/zh-hans/glossary/Hypertext)** 的概念，并与第二年在 **[[SGML]]**的基础上将其正式定义为一个标记语言。
**[[IETF]]**于1993年正式开始制定HTML规范，并在经历了几个版本的草案后于1995年发布了
*HTML 2.0*版本。1994年，*Berners-Lee*为了Web发展而成立了**[[W3C]]**。
1996年，W3C接管了HTML的标准化工作，并在1年后发布了*HTML 3.2推荐标准*。1999年，*HTML 4.0*发布，并在2000年成为[[ISO]]标准。

自那以后，W3C几乎放弃了HTML而转向*[[XHTML]]*，并于2004年成立了另一个独立的小组**[[WHATWG]]**。幸运的是，WHATWG后来又转回来参与了*HTML5*标准的制定，
两个组织（即[[W3C]]和[[WHATWG]]）在2008年发布了第一份草案，并在2014年发布了HTML5标准的最终版。

## 文档类型 (Doctype)

**文档类型** (**Doctype**)是在所有文档顶部必需的，如：“**`<!DOCTYPE html>`**”前导。其唯一的目的是防止渲染文档时浏览器切换到所谓的“*怪异模式*”
("*quirks mode*")。
也就是说，“`<!DOCTYPE html>`”文档类型可确保浏览器尽最大努力遵循相关规范，而不是使用不兼容的其他渲染模式。

## 元素 (Element)

HTML文档是包含多个HTML**元素**的*文本*文档。

![HTML元素的结构剖析](/media/glossary__anatomy-of-an-html-element.png)

**元素**被匹配的开始和关闭**标签**包围。*元素*和*标签*是不同的东西。标签在源代码中以元素开头或结尾，而元素是 **[[DOM]]**（用于在[浏览器](/zh-hans/glossary/Web_browser/)中显示页面的文档模型）的一部分。

每个典型的元素都包含一个**开始标签**，一些**属性**，**对应的文本内容**，和一个**结束标签**。

### 空元素 (Empty Elements)

也有一部分标签中不需要包含文本，这些标签称为 **[空标签](/zh-hans/webfrontend/Empty_Element)**，如[`<img>`](/zh-hans/webfrontend/<img>)。

### 块级元素和内联元素

在HTML中有两种你需要知道的重要元素类别，**块级元素**(**Block Elements**)和**内联元素**(**Inline Elements**)。

- **块级元素**在页面中以块的形式展现 —— 相对于其前面的内容它会出现在新的一行，其后的内容也会被挤到下一行展现。块级元素通常用于展示页面上结构化的内容，例如段落 (`<p>`)、
  列表 (`<ul>`, `<ol>`)、导航菜单 ([`<nav>`](/zh-hans/webfrontend/<nav>))、页脚 ([`<footer>`](/zh-hans/webfrontend/<footer>))等等。块级元素不会被嵌套进内联元素中，但可以嵌套在其它块级元素中。
- **内联元素**通常出现在块级元素中并环绕文档内容的一小部分，而不是一整个段落或者一组内容。内联元素不会导致文本换行：它通常出现在一堆文字之间例如超链接元素`<a>`或者强调元素`<em>`和`<strong>`。

## 标签 (Tag)

在HTML中，**标签**用来创建一个*元素*。HTML元素的*名称*是在**尖括号**中使用的名称，例如`<p>`用于段落（paragraph）。
注意，结束标签的名称前面有一个**斜杠字符**："`</p>`"。在*空元素*中，结束标签既不需要也不允许。
在任何情况下，如果没有提及*属性*(*attributes*)，那么将使用默认值。

!!! warn "注意"
    HTML标签**不区分大小写**。也就是说，标签既可以使用大写字母也可以使用小写字母。例如，标签`<title>`写成`<title>`、`<TITLE>`、`<Title>`、`<TiTlE>`，等等都可以正常工作。不过，从一致性、可读性等各方面来说，**最好仅使用小写字母**。

每个标签以**尖括号** **`<>`**开始和结束。

## 属性 (Attribute)

你可以使用**属性**来扩展HTML标签，提供一些附加信息，这些信息可能会影响[浏览器](/zh-hans/glossary/Web_browser)对元素的解析，例如：可改变标签行为或提供元数据。

属性总是以 **`name="value"`**的格式（属性名称后接与之相关的属性值）。

### 多属性

如果已经有一个或多个属性，就与前一个属性之间用一个**空格**隔开。

### 布尔属性

有时你会看到*没有值*的属性，它是合法的。这些属性被称为**布尔属性**，他们只能有跟它的属性名一样的属性值。例如`disabled`属性，他们可以标记表单输入使之变为不可用(变灰色)，此时用户不能向他们输入任何数据。

```html
<!-- 使用disabled属性来防止终端用户输入文本到输入框中 -->
<input type="text" disabled>

<!-- 下面这个输入框没有disabled属性，所以用户可以向其中输入 -->
<input type="text">
```

## 超链接 (Hyperlink)

**超链接**是指从一个网页指向一个目标的连接关系。这个目标可以是另一个网页或数据项。在HTML中，[`<a>`](/zh-hans/webfrontend/<a>)元素定义了网页中的一个项目（像文本，图片等）在到其他网页（甚至是同一个网页中）另一个项目的超链接。

## 超文本 (Hypertext)

**超文本**(*Hypertext*)包含了指向其他文本的链接，而不是像小说中的单一线性流。

这个术语是由*Ted Nelson*在1965年左右提出的。

## HTML5

**HTML5**是定义*HTML*标准的最新演进版本。该术语通过两个不同的概念来表现：

- 它是HTML语言的一个新版本，具有新的元素、属性和行为；
- 它有更大的技术集，允许构建更多样化和更强大的网站和应用程序。这个集合有时称为*HTML5和它的朋友们*，不过大多数时候仅缩写为一个词：*HTML5*。

HTML5技术根据其功能分为几个组：

- [**语义**](/zh-hans/webfrontend/Semantics)：能够让你更恰当地描述你的内容是什么。
    - 新的区块和段落元素: [`<section>`](/zh-hans/webfrontend/<section>),
    [`<article>`](/zh-hans/webfrontend/<article>), [`<nav>`](/zh-hans/webfrontend/<nav>), [`<header>`](/zh-hans/webfrontend/<header>),
    [`<footer>`](/zh-hans/webfrontend/<header>)和[`<aside>`](/zh-hans/webfrontend/<aside>).
    - 新的多媒体内容: [`<video>`](/zh-hans/webfrontend/<video>),
    [`<audio>`](/zh-hans/webfrontend/<audio>)元素
    - 表单的改进: 强制校验API, 一些新的属性，一些新的[`<input>`](/zh-hans/webfrontend/<input>)元素的`type`属性值, 和新的[`<output>`](/zh-hans/webfrontend/<output>)元素
    - 新的语义元素: [`<mark>`](/zh-hans/webfrontend/<mark>), [`<figure>`](/zh-hans/webfrontend/<figure>),
    [`<figcaption>`](/zh-hans/webfrontend/<figcaption>), [`<data>`](/zh-hans/webfrontend/<data>), [`<time>`](/zh-hans/webfrontend/<time>),
    [`<output>`](/zh-hans/webfrontend/<output>), [`<progress>`](/zh-hans/webfrontend/<progress>),
    or [`<meter>`](/zh-hans/webfrontend/<meter>)和[`<main>`](/zh-hans/webfrontend/<main>)等。
    - *[`<iframe>`](/zh-hans/webfrontend/<iframe>)* 的改进: 通过使用`sandbox`和`srcdoc`属性，可以精确控制[`<iframe>`](/zh-hans/webfrontend/<iframe>)元素的安全级别以及期望的渲染。
    - **MathML**: 允许直接嵌入数学公式。
- **连通性**：能够让你和服务器之间通过创新的新技术方法进行通信。
    - **[[WebSocket]]**
    - **Server-Sent Event** (**SSE**): 允许服务器向客户端推送事件，而不是仅在响应客户端请求时服务器才能发送数据的传统范式。
    - **WebRTC**: 这项即时通信技术，允许直接在浏览器中连接到其他人，控制视频会议，而不需要一个插件或是外部的应用程序。
- **离线和存储**：能够让网页在客户端本地存储数据以及更高效地离线运行。
    - **应用程序缓存** (**Application Cache**)
    - **在线和离线事件**: 可以让应用程序和扩展检测是否存在可用的网络连接，以及在连接建立和断开时能感知到。
    - **客户端会话**和**持久化存储**(即**DOM存储**): 让Web应用程序能够在客户端存储结构化数据。
    - **IndexedDB**：能够在浏览器中存储大量结构化数据，并且能够在这些数据上使用索引进行高性能检索的Web标准。
    - **文件API**（**File API**）：使Web应用程序可以访问由用户选择的本地文件。
    这包括使用`type=file`的`<input>`元素的新的`multiple`属性针对多文件选择的支持，还有`FileReader`。
- **多媒体**
    - **[`<audio>`](/zh-hans/webfrontend/<audio>)** 和 **[`<video>`](/zh-hans/webfrontend/<video>)** 元素
    - **WebRTC**
    - **摄像头API** (**Camera API**)
    - **[`<track>`](/zh-hans/webfrontend/<track>)** 和 **WebVTT**
- **2D/3D图形和特效**
    - **[`<canvas>`](/zh-hans/webfrontend/<canvas>)** 元素
    - 针对 *[`<canvas>`](/zh-hans/webfrontend/<canvas>)* 元素的 **文本API** （**Text API**）
    - **WebGL**: WebGL通过引入了一套非常地符合 **OpenGL ES 2.0**
    并且可以用在HTML5 *[`<canvas>`](/zh-hans/webfrontend/<canvas>)* 元素中的 API，给Web带来了2D/3D图像及特效功能。
    - **[[SVG]]**: 一个基于[[XML]]的可以直接嵌入到HTML中的矢量图像格式。
- **性能和集成**：提供了非常显著的性能优化和更有效的计算机硬件使用。
    - **Web Workers**: 能够把[[JavaScript]]计算委托给后台线程，通过允许这些活动以防止使交互型事件变得缓慢。
    - **`XMLHttpRequest`** level 2: 允许*异步*读取页面的某些部分，允许其显示动态内容，根据时间和用户行为而有所不同。这是在 **[[Ajax]]** 背后的技术。
    - **即时编译** (**JIT**)的[[JavaScript]]引擎
    - **History API**: 允许对浏览器历史记录进行操作。这对于那些交互地加载新信息的页面尤其有用。
    - **`contentEditable`属性**: HTML5已经把`contentEditable`属性标准化了。
    把你的网站改变成wiki！
    - **拖放API** (**Drag and Drop API**): 能够支持在网站内部和网站之间拖放项目。同时也提供了一个更简单的供扩展和应用程序使用的API。
    - **焦点管理**: 支持新的HTML5`activeElement`和`hasFocus`属性。
    - **基于Web的协议处理程序**: 你现在可以使用`navigator.registerProtocolHandler()`方法把Web应用程序注册成一个协议处理程序。
    - **requestAnimationFrame**: 允许控制动画渲染以获得更优性能。
    - **全屏API** (**Fullscreen API**)
    - **指针锁定 API** (**Pointer Lock API**): 允许锁定到内容的指针，这样游戏或者类似的应用程序在指针到达窗口限制时也不会失去焦点。
- **设备访问**：能够处理各种输入和输出设备。
    - **摄像头API** (**Camera API**)
    - **触控事件**
    - **地理位置定位**
    - **检测设备方向**: 让用户在运行浏览器的设备变更方向时能够得到信息。这可以被用作一种输入设备（例如制作能够对设备位置做出反应的游戏）或者使页面的布局跟屏幕的方向相适应（横向或纵向）。
    - **指针锁定 API** (**Pointer Lock API**): 允许锁定到内容的指针，这样游戏或者类似的应用程序在指针到达窗口限制时也不会失去焦点。

### HTML5 大纲

![HTML5元素流程图 (Dookbook Team 翻译整理)](/media/glossary__html5-element-flowchart.zh-Hans.png)

## DHTML

**DHTML**（*动态HTML*）是指不需要*Flash*或*Java*等插件的交互式网页背后的代码。DHTML聚合了HTML，[[CSS]]，[[DOM]]和[[JavaScript]]的组合功能。

DHTML不是[[W3C]]标准。它是一个营销术语，被网景公司（Netscape）和微软公司用来描述4.x代浏览器应当支持的新技术。

DHTML不是一种技术、标准或规范，只是一种将目前已有的网页技术、语言标准整合运用，制作出能在下载后仍然能实时变换页面元素效果的网页设计概念。

## HTML注释 `<!--...-->`

**`<!--...-->`** 即注释标签,用于在源代码中插入注释。注释不会显示在浏览器中。

您可使用注释对您的代码进行解释，这样做有助于您在以后的时间对代码的编辑，特别是当您编写了大量代码时尤其有用。

使用注释标签来隐藏浏览器不支持的脚本也是一个好习惯（这样就不会把脚本显示为纯文本）。

注释标签**不支持任何标准属性**。注释标签**不支持任何事件属性**。

HTML 示例:

```html
<!--这是一段注释。注释不会在浏览器中显示。-->

<p>这是一段普通的段落。</p>
```

## 了解更多

- 书籍： ***Designing With Web Standards*, Third Edition (2009)**
- [HTML - 维基百科](https://en.wikipedia.org/wiki/HTML)
- [HTML元素 - 维基百科](https://en.wikipedia.org/wiki/HTML%20element)
- [超链接 - 维基百科](https://en.wikipedia.org/wiki/Hyperlink)
- [超文本 - 维基百科](https://en.wikipedia.org/wiki/Hypertext)
- [DHTML - 维基百科](https://en.wikipedia.org/wiki/Dynamic%20HTML)
- [HTML 实时标准/规范 (WHATWG版本)](https://html.spec.whatwg.org/) (**推荐**)
- [HTML5 规范 (W3C版本)](http://www.w3.org/TR/html5/)
- [W3C HTML验证器](http://validator.w3.org/ "W3C HTML Validator")
- [W3C HTML元素表](http://www.w3.org/TR/html-markup/elements.html "W3C HTML元素表")
- [MDN HTML文档](https://developer.mozilla.org/en-US/docs/Web/html "MDN HTML文档")
