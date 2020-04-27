# Install
## Install gem & bundle
See:[使用Bunlder搭建Jekyll(Github-pages)服务](https://cndaqiang.github.io//2020/04/18/ruby/)
## Install the dependencies with [Bundler](http://bundler.io/):
~~~bash
$ bundle install
~~~
The Gemfile in this dir is
```
source 'https://mirrors.tuna.tsinghua.edu.cn/rubygems'
#https://rubygems.org'

gem 'jekyll', '3.8.4'

group :jekyll_plugins do
  gem 'jekyll-feed', '0.11.0'
  gem 'jekyll-seo-tag', '2.5.0'
  gem 'jekyll-sitemap', '1.2.0'
end
```
## Run

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
nohup bundle exec jekyll serve -P 3000 > /tmp/outout.log
~~~

# help


该主题用于以后的软件Manual的主题.
> 示例网页[Manual-Theme](https://cndaqiang.github.io/Manual-Theme/) , 安装方法[使用Bunlder搭建Jekyll(Github-pages)服务](https://cndaqiang.github.io//2020/04/18/ruby/)

## 文件框架
- `index.md`主页的内容,使用`_layouts/default.html`模板
- `_config.yml`网站配置文件
- `_layouts/` 模板文件
<br> 目前仅有`_layouts/default.html`,包含了左侧目录和右侧正文
<br>控制了整个网站的布局:主页、搜索、目录、News.
- `_docs`文件夹及其子文件夹下面的所有md文件，都会被收录整理到左侧目录<br>
文件开头格式
```markdown
---
title: input.in
category: Input
order: 2
---
```

    - `title` 显示标题
    - `category`一级分类，按照category进行分类，分类的顺序由子文件夹名称决定
    - `category`二级分类下面的排序，就是文章的顺序
- `search.html`检索`_docs`目录下的文章
- `news.html`，把`_posts/`中的文件进行检索，排列展示
- `404.md`,连接无效页面



## 语法
markdown
## 公式
在`_layouts/default.html`中添加
```html
<script type="text/javascript"
src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
```
然后使用`$$y=\sin(x)$$`插入公式，如$$y=\sin(x)$$

## 代码高亮
在第一个\`\`\`或\~\~\~后面写上代码

## 标题展示
```markdown
# 一级标题
## 二级标题
### 三级标题
```
示例
# 一级标题
## 二级标题
### 三级标题
#### 四级
##### 五级
###### 六级

<br><br><br><br>
