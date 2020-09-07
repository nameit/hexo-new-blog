## 下载

clone下来后，

```cnpm i```，

下载依赖。

## 安装主题

一般来说hexo server就能在本地预览了。

但之前下载了next主题，所以需要在github自己的fork里下载hexo-theme-next主题。进到自己项目theme目录下  

```git clone git@github.com:nameit/hexo-theme-next.git themes/next。```

只有下载了这个主题，再hexo generate才能生成public文件夹里面的css、images文件夹等。

> 如果没有全局安装hexo，可以这样引用： ./node_modules/hexo/bin/hexo

## 起服务及部署

generate后就可以通过

```./node_modules/hexo/bin/hexo server -p 4004```

 本地浏览了（有时4000端口占用可以通过-p加端口的形式另起一个端口）

具体写作参见[官网](https://hexo.io/zh-cn/docs/writing)

部署：
```./node_modules/hexo/bin/hexo d -g```

## 遇到的问题

1、fatal: unable to access 'https://github.com/nameit/nameit.github.io.git/': OpenSSL SSL_connect: SSL_ERROR_SYSCALL in connection to github.com:443

[解决办法](https://blog.csdn.net/daerzei/article/details/79528153): ```git config --global --unset http.proxy```

2、Error: fatal: in unpopulated submodule '.deploy_git'

解决方法： 把.depoy_git删除，重新运行

```hexo g```

```hexo d```



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



