# 文章内容

在一个文章内容页里面，需要使用一些占位符去替换文章内容模板中的字符串。
下面举一个简单的例子

```html
<html>
  <head>
    <title>{content:title}</title>
  </head>
  <body>
    作者：{content:author}
    创建时间：{content:createdAt}
    更新时间: {content:updatedAt}
    正文内容：{content:content}
  </body>
</html>
```
