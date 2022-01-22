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

如需自定义分页条
