.deploy_git就是发布到name.github.io的内容，就是name.github.io仓库的内容



### Hexo打不开标签和分类

是因为在对应的主题文件夹(比如next)下的yml文件里没有把tags: /tags/ || tags前面的注释井号去掉，

去掉后还要运行` hexo new page “tags"`

还差最后一步，打开各页面对应的index.md文件D:\hexo\blog\source\tags\index.md改为：

```js
title: tags

date: 2020-09-04 12:13:14

type: "tags"

---

```



