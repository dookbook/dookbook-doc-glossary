TOPICS: HyperText Markup Language
        Hyperlink
        Element
        Tag
        Attribute

# 超文本标记语言 (HyperText Markup Language, HTML)

HTML（**HyperText Markup Language**，*超文本标记语言*）是用来定义网页结构的一种描述语言。

## 发展简史

1990年，由于对 [Web](/zh-hans/glossary/World_Wide_Web) 未来发展的远见，*Tim Berners-Lee*提出了
**[超文本](/zh-hans/glossary/Hypertext)** 的概念，并在第二年在*SGML*的基础上将其正式定义为一个标记语言。
[[IETF]]于1993年正式开始制定HTML规范，并在经历了几个版本的草案后于1995年发布了
*HTML 2.0*版本。1994年，*Berners-Lee*为了Web发展而成立了**[[W3C]]**。
1996年，W3C接管了HTML的标准化工作，并在1年后发布了*HTML 3.2*推荐标准。1999年，*HTML 4.0*发布，并在2000年成为[[ISO]]标准。

自那以后，W3C几乎放弃了HTML而转向*[[XHTML]]*，并于2004年成立了另一个独立的小组**[[WHATWG]]**。幸运的是，WHATWG后来又转回来参与了*HTML5*标准的制定，
两个组织（即[[W3C]]和[[WHATWG]]）在2008年发布了第一份草案，并在2014年发布了HTML5标准的最终版。

## 概念和语法

HTML文档是包含多个HTML**元素**的文本文档。

![HTML元素的结构剖析](/media/glossary__anatomy-of-an-html-element.png)

HTML文件通常会以`.htm` 或 `.html`为扩展名。用户可以从Web服务器中下载，并使用任一[Web浏览器](/zh-hans/glossary/Web_browser)来解析和显示。

### 元素 (Element)

每个典型的**元素**都包含一个*开始标签*，一些*属性*，包含的*文本内容*，和一个*结束标签*。

也有一部分标签中不需要包含文本，这些标签称为*空标签*，如 `<img>`。

### 标签 (Tag)

在HTML中，**tag**用来创建一个*element*。HTML*元素*的**名称**是在尖括号中使用的名称，例如`<p>`用于段落（paragraph）。
注意，*结束*标记的名称前面有一个斜杠字符"`</p>`"。在*空元素*中，结束标记既不需要也不允许。
在任何情况下，如果没有提及*属性*(*attributes*)，那么将使用默认值。

每个标签以尖括号`<>`开始和结束。

### 属性 (Attribute)

你可以使用**属性**来扩展HTML*标签*。属性用来提供一些附加信息，这些信息可能会影响[浏览器](/zh-hans/glossary/Web_browser)对元素的解析。

标签**属性** (**Attribute**）用于拓展HTML*标签*，可改变标签行为或提供元数据，属性总是以`name = value`的格式（属性的识别码后接与之相关的值）。

### 超链接 (Hyperlink)

**超链接**简单来讲，就是指按内容链接。超级链接在本质上属于一个网页的一部分，它是一种允许我们同其他网页或站点之间进行连接的元素。
各个网页链接在一起后，才能真正构成一个网站。所谓的超链接是指从一个网页指向一个目标的连接关系，这个目标可以是另一个网页，
也可以是相同网页上的不同位置，还可以是一个图片，一个电子邮件地址，一个文件，甚至是一个应用程序。而在一个网页中用来超链接的对象，
可以是一段文本或者是一个图片。当浏览者单击已经链接的文字或图片后，链接目标将显示在浏览器上，并且根据目标的类型来打开或运行。

### 超文本 (Hypertext)

**超文本**(*Hypertext*)包含了指向其他文本的链接，而不是像小说中的单一线性流。

这个术语是由*Ted Nelson*在1965年左右提出的。

## HTML5

HTML的最新稳定版本, **HTML5**将HTML从用于构造一个文档的一个简单标记，到一个完整的应用程序开发平台。除其他功能外,
HTML5还包括新元素和用于增强存储、多媒体和硬件访问的JavaScript APIs。

## DHTML

**DHTML**（*动态HTML*）是指不需要*Flash*或*Java*等插件的交互式网页背后的代码。DHTML聚合了HTML，CSS，[[DOM]]和[[JavaScript]]的组合功能。

DHTML不是[[W3C]]标准。它是一个营销术语，被网景公司（Netscape）和微软公司用来描述4.x代浏览器应当支持的新技术。

DHTML不是一种技术、标准或规范，只是一种将目前已有的网页技术、语言标准整合运用，制作出能在下载后仍然能实时变换页面元素效果的网页设计概念。

## 了解更多

- [HTML维基百科](https://en.wikipedia.org/wiki/HTML)
- [HTML元素维基百科](https://en.wikipedia.org/wiki/HTML%20element)
- [超链接维基百科](https://en.wikipedia.org/wiki/Hyperlink)
- [超文本维基百科](https://en.wikipedia.org/wiki/Hypertext)
- [DHTML维基百科](https://en.wikipedia.org/wiki/Dynamic%20HTML)
- [HTML规范](http://www.w3.org/TR/html5/)
