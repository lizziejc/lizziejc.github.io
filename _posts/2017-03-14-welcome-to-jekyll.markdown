---
layout: post
title:  "Welcome to Jekyll!"
permalink: "welcome-to-jekyll.html"
date:   2017-03-14 13:24:33 +0800
---
Jekyll是一个文本转换器，它可以把`Markdown`、`Textile`转换成HTML页面。你只需要把转换好的静态页面放到自己的服务器上或者[GitHub Page](https://pages.github.com/)上，就会像这个页面一样。

### 安装jekyll   
Mac环境下: `gem install jekyll`，如果没有权限，用`sudo gem install jekyll`   

### 创建blog实例
安装后，`jekyll new blog` 创建一个新的文件夹（包括必要文件）   
对于生成的文件夹及文件的含义可以看[这里](http://jekyll.com.cn/docs/structure/)，其中最息息相关的就是`_posts`文件夹了。   
_posts文件夹中存放的是要被转换的文件，比如初始的Markdown。文件名必须是: `YEAR-MONTH-DAY-title.MARKUP`，比如`2017-03-14-welcome-to-jekyll.markdown`。   

### 编译并启动   
1. `cd blog`，在blog文件夹根目录运行`jekyll serve`，   
2. 如果提示`'cannot load such file -- bundler (LoadError)'`错误，就安装bundler：`gem install bundler`。   
3. 执行`bundler install`（如果不执行，而直接运行jekyll serve，同样会报错，因为没有依赖包）   
4. 重新运行`jekyll serve`，根据提示地址打开页面   

所以上面四步的正确顺序是，2-3-1-4，即先安装bundler工具，再安装依赖包，最后本地起一个服务。   

### 写自己的文章   
如果你已经看到了'Welcome'页面，那么接下来，需要做的就是在_posts文件夹中添加自己的文章，或者修改已经有的文件。在每个文件的开头会有一段信息如下   
```   
---
layout: post
title:  "Welcome to Jekyll!"
permalink: "welcome-to-jekyll.html"
---
```   
这段是为了设置这个文章的信息，比如模板(layout)、名称(title)、地址栏显示的地址(permalink)、标签(tags)...   
除了这部分头信息外，其他内容才是我们要展示的文章正文。比如   
```   
---
layout: post
title:  "Welcome to Jekyll!"
permalink: "welcome-to-jekyll.html"
---
Jekyll是一个文本转换器，它可以把`Markdown`、`Textile`转换成HTML页面。你只需要把转换好的静态页面放到自己的服务器上或者[GitHub Page](https://pages.github.com/)上，就会像这个页面一样。
```   
按照Jekyll自动生成的模板，在_posts里添加文章之后，就可以在首页看到相关链接，不需要自己再做设置了。

***
> http://jekyllrb.com/docs/home/

