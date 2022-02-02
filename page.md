# 文章列表分页

Pager使用分页条标签插入文章列表分页功能，分页条标签必须再文章列表页才可以使用，其他页面使用无效。

## 使用内置分页条

直接使用`[page:bar]`即可导入系统内置的完整分页条，示例代码如下。

```html
{pager:list id="listId"}
<a href= "[list:link]">[list:title]</a>
{/pager:list}
{pager:pagebar size="10"}
[page:bar]
{/pager:page}
```

## 自定义分页条

如需自定义分页条，需要使用一下占位符

| 占位符标签 | 说明 |
| --- | --- |
| [page:total] | 总页数 |
| [page:href] | 文章内容页链接 |
| [page:current] | 当前页码 |
| [page:currentClass] | 当前页码类，用来标记链接是否为当前页 |
| [page:pre] | 前一页链接 |
| [page:next] | 下一页链接 |
| [page:first] | 首页链接 |
| [page:last] | 尾页链接 |

以下一是各自定义分页条的实例代码：

```html
<div>
    <a class="pager-page-item" href="[page:first]">首页</a>
    <a class="pager-page-item" href="[page:pre]">上一页</a>
    {pager:pagelink currentClass="pager-page-item-current"}
    <a class="pager-page-item [page:currentClass]" href="[page:href]">[page:index]</a>
    {/pager:pagelink}
    <a class="pager-page-item" href="[page:next]">下一页</a>
    <a class="pager-page-item" href="[page:last]">尾页</a>
</div>
```
