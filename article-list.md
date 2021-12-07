# 文章列表

Pager使用`pager:list`指令插入文章列表

```html
{pager:list id=listId}
<a href= "[list:link]">[list:title]</a>
{/pager:list}
```

关于以上代码的说明：
- 文章列表的id需要在CMS中预先定义，对于未定义的文章列表id，无法生成页面。
- [list:link] 是该链接的url，用于替换掉静态页面中的url
- [list:title] 是该链接的标题，用于替换掉静态页面中的标题
