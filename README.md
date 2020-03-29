<h1 align="center"><a href="https://github.com/halo-dev" target="_blank">Halo theme develop Snippets</a></h1>
> Halo theme develop Snippets 是 [Halo](https://github.com/halo-dev/halo) 在 VS Code 上开发的一款主题开发的代码片段插件。

<p align="center">
<a href="https://marketplace.visualstudio.com/items?itemName=halo-dev.halo-theme-dev-snippets-for-vs-code"><img alt="Visual Studio Marketplace Version" src="https://img.shields.io/visual-studio-marketplace/v/halo-dev.halo-theme-dev-snippets-for-vs-code"></a>
<a href="https://marketplace.visualstudio.com/items?itemName=halo-dev.halo-theme-dev-snippets-for-vs-code"><img alt="Visual Studio Marketplace Downloads" src="https://img.shields.io/visual-studio-marketplace/d/halo-dev.halo-theme-dev-snippets-for-vs-code"></a>
</p>

------------------------------

## Snippets

### theme.yaml

前缀:

```
!th.template
```

输出:

```
id: id
name: name
author:
  name: author_name
  website: author_website
description: description
logo: logo
website: website
repo: repo
version: version
require: require
```

### settings.yaml

| 前缀                     | 输出内容                           |
| ------------------------ | ---------------------------------- |
| !set.new.group           | 输出一个新的分组                   |
| !set.new.text.item       | 输出一个为 text 类型的设置项       |
| !set.new.color.item      | 输出一个为 color 类型的设置项      |
| !set.new.attachment.item | 输出一个为 attachment 类型的设置项 |
| !set.new.textarea.item   | 输出一个为 textarea 类型的设置项   |
| !set.new.radio.item      | 输出一个为 radio 类型的设置项      |
| !set.new.select.item     | 输出一个为 select 类型的设置项     |

### category tag

| 前缀                | 说明                                                     |
| ------------------- | -------------------------------------------------------- |
| @tag.category.list  | 遍历所有分类                                             |
| @tag.category.count | `<@categoryTag method="count">${count!0}</@categoryTag>` |

### global tag

| 前缀                 | 说明                                |
| -------------------- | ----------------------------------- |
| @tag.global.head     | `<@global.head />`                  |
| @tag.global.footer   | `<@global.footer />`                |
| @tag.global.timeline | `<@global.timeline datetime="" />`  |
| @tag.global.comment  | `<@global.comment target= type= />` |

### menu tag

| 前缀           | 说明         |
| -------------- | ------------ |
| @tag.menu.list | 遍历所有菜单 |

### pagination tag

| 前缀                           | 说明                     |
| ------------------------------ | ------------------------ |
| @tag.index.pagination          | 首页分页标签的结构       |
| @tag.archives.pagination       | 归档页分页标签的结构     |
| @tag.search.pagination         | 搜索页分页标签的结构     |
| @tag.category.posts.pagination | 分类下文章分页标签的结构 |
| @tag.tag.posts.pagination      | 标签下文章分页标签的结构 |
| @tag.photos.pagination         | 相册页分页标签的结构     |
| @tag.journals.pagination       | 日志页分页标签的结构     |

### tag tag

| 前缀           | 说明                                           |
| -------------- | ---------------------------------------------- |
| @tag.tag.list  | 遍历所有标签                                   |
| @tag.tag.count | `<@tagTag method="count">${count!0}</@tagTag>` |

### list

| 前缀                 | 说明                                          |
| -------------------- | --------------------------------------------- |
| \#list.post.page     | `<#list posts.content as post></#list>`       |
| \#list.post.archives | 输出归档标签                                  |
| \#list.post          | `<#list posts as post></#list>`               |
| \#list.category      | `<#list categories as category></#list>`      |
| \#list.post.category | `<#list post.categories as category></#list>` |
| \#list.tag           | `<#list tags as tag></#list>`                 |
| \#list.post.tag      | `<#list post.tags as tag></#list>`            |

### category model

| 前缀           | 说明                                          |
| -------------- | --------------------------------------------- |
| $c.id          | `${category.id?c}`                            |
| $c.name        | `${category.name!}`                           |
| $c.slug        | `${category.slug!}`                           |
| $c.fullPath    | `${category.fullPath!}`                       |
| $c.description | `${category.description!}`                    |
| $c.thumbnail   | `${category.thumbnail!}`                      |
| $c.parentId    | `${category.parentId?c}`                      |
| $c.createTime  | `${category.createTime?string('yyyy-MM-dd')}` |
| $c.updateTime  | `${category.updateTime?string('yyyy-MM-dd')}` |

### global model

| 前缀                | 说明                                      |
| ------------------- | ----------------------------------------- |
| $g.blog_url         | `${blog_url!}`                            |
| $g.context          | `${context!}`                             |
| $g.theme_base       | `${theme_base!}`                          |
| $g.theme.name       | `${theme.name!}`                          |
| $g.theme.repo       | `${theme.repo!}`                          |
| $g.theme.version    | `${theme.version!}`                       |
| $g.blog_title       | `${blog_title!}`                          |
| $g.blog_logo        | `${blog_logo!}`                           |
| $g.version          | `${version!}`                             |
| $g.user.nickname    | `${user.nickname!}`                       |
| $g.user.email       | `${user.email!}`                          |
| $g.user.description | `${user.description!}`                    |
| $g.user.avatar      | `${user.avatar!}`                         |
| $g.user.expireTime  | `${user.expireTime?string('yyyy-MM-dd')}` |
| $g.meta_keywords    | `${meta_keywords!}`                       |
| $g.meta_description | `${meta_description!}`                    |
| $g.rss_url          | `${rss_url!}`                             |
| $g.atom_url         | `${atom_url!}`                            |
| $g.sitemap_xml_url  | `${sitemap_xml_url!}`                     |
| $g.sitemap_html_url | `${sitemap_html_url!}`                    |
| $g.links_url        | `${links_url!}`                           |
| $g.photos_url       | `${photos_url!}`                          |
| $g.journals_url     | `${journals_url!}`                        |
| $g.archives_url     | `${archives_url!}`                        |
| $g.categories_url   | `${categories_url!}`                      |
| $g.tags_url         | `${tags_url!}`                            |

### journal model

| 前缀          | 说明                                         |
| ------------- | -------------------------------------------- |
| $j.id         | `${journal.id?c}`                            |
| $j.content    | `${journal.content!}`                        |
| $j.likes      | `${journal.likes?c}`                         |
| $j.createTime | `${journal.createTime?string('yyyy-MM-dd')}` |
| $j.updateTime | `${journal.updateTime?string('yyyy-MM-dd')}` |

### link model

| 前缀           | 说明                                      |
| -------------- | ----------------------------------------- |
| $l.id          | `${link.id?c}`                            |
| $l.name        | `${link.name!}`                           |
| $l.url         | `${link.url!}`                            |
| $l.logo        | `${link.logo!}`                           |
| $l.description | `${link.description!}`                    |
| $l.team        | `${link.team!}`                           |
| $l.createTime  | `${link.createTime?string('yyyy-MM-dd')}` |
| $l.updateTime  | `${link.updateTime?string('yyyy-MM-dd')}` |

### menu model

| 前缀        | 说明                |
| ----------- | ------------------- |
| $m.id       | `${menu.id?c}`      |
| $m.name     | `${menu.name!}`     |
| $m.url      | `${menu.url!}`      |
| $m.priority | `${menu.priority!}` |
| $m.target   | `${menu.target!}`   |
| $m.icon     | `${menu.icon!}`     |
| $m.parentId | `${menu.parentId!}` |
| $m.team     | `${menu.team!}`     |

### photo model

| 前缀            | 说明                                       |
| --------------- | ------------------------------------------ |
| $ph.id          | `${photo.id?c}`                            |
| $ph.name        | `${photo.name!}`                           |
| $ph.description | `${photo.description!}`                    |
| $ph.takeTime    | `${photo.takeTime!}`                       |
| $ph.location    | `${photo.location!}`                       |
| $ph.thumbnail   | `${photo.thumbnail!}`                      |
| $ph.url         | `${photo.url!}`                            |
| $ph.team        | `${photo.team!}`                           |
| $ph.createTime  | `${photo.createTime?string('yyyy-MM-dd')}` |
| $ph.updateTime  | `${photo.updateTime?string('yyyy-MM-dd')}` |

### post model

| 前缀             | 说明                                      |
| ---------------- | ----------------------------------------- |
| $p.id            | `${post.id?c}`                            |
| $p.title         | `${post.title!}`                          |
| $p.slug          | `${post.slug!}`                           |
| $p.fullPath      | `${post.fullPath!}`                       |
| $p.formatContent | `${post.formatContent!}`                  |
| $p.summary       | `${post.summary!}`                        |
| $p.thumbnail     | `${post.thumbnail!}`                      |
| $p.visits        | `${post.visits?c}`                        |
| $p.likes         | `${post.likes?c}`                         |
| $p.editTime      | `${post.editTime?string('yyyy-MM-dd')}`   |
| $p.createTime    | `${post.createTime?string('yyyy-MM-dd')}` |
| $p.updateTime    | `${post.updateTime?string('yyyy-MM-dd')}` |

### sheet model

| 前缀             | 说明                                       |
| ---------------- | ------------------------------------------ |
| $s.id            | `${sheet.id?c}`                            |
| $s.title         | `${sheet.title!}`                          |
| $s.slug          | `${sheet.slug!}`                           |
| $s.fullPath      | `${sheet.fullPath!}`                       |
| $s.formatContent | `${sheet.formatContent!}`                  |
| $s.summary       | `${sheet.summary!}`                        |
| $s.thumbnail     | `${sheet.thumbnail!}`                      |
| $s.visits        | `${sheet.visits?c}`                        |
| $s.likes         | `${sheet.likes?c}`                         |
| $s.editTime      | `${sheet.editTime?string('yyyy-MM-dd')}`   |
| $s.createTime    | `${sheet.createTime?string('yyyy-MM-dd')}` |
| $s.updateTime    | `${sheet.updateTime?string('yyyy-MM-dd')}` |

### tag model

| 前缀          | 说明                                     |
| ------------- | ---------------------------------------- |
| $t.id         | `${tag.id?c}`                            |
| $t.name       | `${tag.name!}`                           |
| $t.slug       | `${tag.slug!}`                           |
| $t.fullPath   | `${tag.fullPath!}`                       |
| $t.thumbnail  | `${tag.thumbnail!}`                      |
| $t.createTime | `${tag.createTime?string('yyyy-MM-dd')}` |
| $t.updateTime | `${tag.updateTime?string('yyyy-MM-dd')}` |

