# 文章列表分页

Pager使用分页条标签插入文章列表分页功能，分页条标签必须再文章列表页才可以使用，其他页面使用无效。

## 使用内置分页条

直接使用`{page:bar}`即可导入系统内置的完整分页条，示例代码如下。

```html
{pager:list id=listId}
<a href= "[list:link]">[list:title]</a>
{/pager:list}
{page:bar}
```

## 自定义分页条

如需自定义分页条，需要使用一下占位符

| 占位符标签 | 说明 |
| --- | --- |
| {page:current} | 当前页码 |
| {page:count} | 总页数 |
| {page:rows} | 总数据行数 |
| {page:index} | 首页链接 |
| {page:pre} | 前一页链接 |
| {page:next} | 下一页链接 |
| {page:last} | 尾页链接 |
