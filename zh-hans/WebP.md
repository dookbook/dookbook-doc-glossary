TOPIC: WebP

# WebP

**WebP**是由 *Google*开发的*开源*的*图像格式*，与 *[[JPEG]]* 和 *[[PNG]]*格式相比，它保证生成的图像尺寸**更小**，同时生成“**更好看**”的图像。

**WebP**同时支持**无损**和**有损压缩**。

**WebP**支持**透明度**，就像 *[[PNG]]*和 *[[GIF]]*图像。

**WebP**支持**动画**，就像 *[[GIF]]*图像。

而且，使用**WebP**可以设置图像的“**质量比**”，以便决定要获得更好的质量还是缩小尺寸（就像在 *[[JPEG]]*图像一样）。

因此，WebP可以用一种格式完成所有GIF，JPEG和PNG图像可以完成的操作，并生成较小的图像。
听起来不错。

## 尺寸小多少

生成较小图像的前提是非常意思的，尤其是当您考虑到大多数Web页面的大小取决于用户应下载的图像资产的数量和大小时。

Google发布了一百万张图像比较研究的结果，如下：

> **WebP**的总体压缩率比 *[[JPEG]]*或 *JPEG 2000*高。对于较小的图像而言，最小化文件大小的收益特别高，而较小的图像是Web上最常见的图像。

与 *[[PNG]]*相比，无损压缩可生成 **WebP**图像小50％。*PNG*仅在使用有损压缩时才能达到该文件大小。

## 生成WebP图像

所有现代的图形和图像编辑工具都可让您导出到 **`.webp`**文件。

**`cwebp`**是主流的命令行实用程序，可将任何图像转换为`.webp`，使用如下：

```sh
cwebp image.png -o image.webp
```

查看该命令行所有选项及用法请使用`cwebp -longhelp`。

## 浏览器支持

WebP当前被这些浏览器支持：

- [Chrome](/zh-hans/glossary/Google_Chrome)
- Firefox 65+ (Jan 2019)
- Edge 18+
- Opera
- Opera Mini
- UC浏览器

*[Safari](/zh-hans/glossary/Apple_Safari)*和IE根本不支持WebP，并且两者都没有任何即将实现WebP的迹象。

## 如何使用

最方便，且对您和您的网页完全透明的方法：当 **`HTTP_ACCEPT`** 请求头部包含 **`image/webp`**时，可以使用服务器级机制来提供*WebP*图像，而不是JPEG和PNG。

另一种选择是使用**Modernizr**并检查*`Modernizr.webp`*设置。

如果不需要支持Internet Explorer，一种非常方便的方法是使用 **[`<picture>`](/zh-hans/webfrontend/<picture>)** 标签 --
除Opera Mini和IE（所有版本），其他所有主流浏览器现在都支持。

```html
<picture>
  <source type="image/webp" srcset="image.webp">
  <img src="image.jpg" alt="图片">
</picture>
```

## 更多

- [WebP - 维基百科](https://en.wikipedia.org/wiki/WebP)
