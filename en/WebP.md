TOPIC: WebP

# WebP

**WebP** is an *Open Source* *image format* developed at *Google*, which promises to generate images
**smaller in size** compared to *[[JPEG]]* and *[[PNG]]* formats, while generating **better looking**
images.

**WebP** supports both **lossless** and **lossy** **compression**.

**WebP** supports **transparency**, like *[[PNG]]* and *[[GIF]]* images.

**WebP** supports **animations**, like *[[GIF]]* images.

And, using **WebP** you can set the **quality ratio** of your images, so you decide if you want to get
better quality or a smaller size (like it happens in *[[JPEG]]* images).

So WebP can do all GIF, JPEG and PNG images can do, in a single format, and generate smaller images.
Sounds like a deal.

## How Much Smaller

The premise of generating smaller images is very interesting, especially when you consider than most
of a Web page size is determined by the amount and size of the image assets the user should download.

Google published a [comparative study](https://developers.google.com/speed/webp/docs/c_study) on the
results of 1 million images with this result:

> **WebP** achieves overall higher compression than either *[[JPEG]]* or *JPEG 2000*. Gains in file size
> minimization are particularly high for smaller images which are the most common ones found on the Web.

Lossless compression compared to *[[PNG]]* generates **WebP** images 50% smaller. *PNG* reaches that
file sizes only when using lossy compression.

## Generating WebP Images

All modern graphical and image editing tools let you export to **`.webp`** files.

**`cwebp`** is the main command line utility to convert any image to `.webp`, use it with

```sh
cwebp image.png -o image.webp
```

Check out all the options using `cwebp -longhelp`.

## Browsers Support

WebP is currently supported by

- [Chrome](/en/glossary/Google_Chrome)
- Firefox 65+ (Jan 2019)
- Edge 18+
- Opera
- Opera Mini
- UC Browser

*[Safari](/en/glossary/Apple_Safari)* and IE do not support WebP at all, and there are no signs of
WebP being implemented any time soon in those browsers.

## How To Use

The most convenient way, as completely transparent to you and to your web pages: You can
use a server-level mechanism that serves *WebP* images instead of JPEG and PNG when the
**`HTTP_ACCEPT`** request header contains **`image/webp`**.

Another option is to use **Modernizr** and check the *`Modernizr.webp`* setting.

If you don’t need to support Internet Explorer, a very convenient way is to use the
**[`<picture>`](/en/webfrontend/<picture>)** tag, which is now supported by all the major browsers except
Opera Mini and IE (all versions):

```html
<picture>
  <source type="image/webp" srcset="image.webp">
  <img src="image.jpg" alt="An image">
</picture>
```

## Learn More

- [WebP on Wikipedia](https://en.wikipedia.org/wiki/WebP)
