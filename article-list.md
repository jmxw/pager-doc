# 文章列表

Pager使用`pager:list`指令插入文章列表

```html
{pager:list id="listId"}
<a href= "[list:href]">[list:title]</a>
{/pager:list}
```

**文章列表的id需要在CMS中预先定义，对于未定义的文章列表id，无法生成页面。**

在`pager:list`指令内部可以使用以下占位符标签

| 占位符标签 | 说明 |
| [list:href] | 文章内容页的超链接 |
| [list:title] | 文章标题 |
| [list:cover] | 文章封面，如果没有文章封面返回空字符串 |
| [list:author] | 文章创建作者 |
| [list:lastAuthor] | 文章最后编辑作者 |
| [list:publishAt] | 文章发布时间 |
| [list:description] | 文章描述 |

以下代码展示了一个完整的，带有封面，标题，作者，发布时间以及描述的一个文章列表：

```html
{pager:list id="blog"}
<div class="col-lg-6 col-md-6">
    <div class="blog__item">
        <div class="blog__item__pic set-bg" data-setbg="[list:cover]">
            <p>By <span>[list:author] on [list:publishAt]</span></p>
        </div>
        <div class="blog__item__text">
            <h3><a href="[list:link]">[list:title]</a></h3>
            <p>[list:description]</p>
            <a href="[list:link]" class="continue-btn">Continue Reading</a>
        </div>
    </div>
</div>
{/pager:list}
```
