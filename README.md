## Blog
这是我的个人记事本，使用Jekyll生成，采用默认主题，托管于Github Pages上面。

### 介绍
1. 非_site文件托管在bitbucket.org中的私有库中。
2. 并非所有.md文件是公开的，_posts中包含私人文档和允许公开的文档。
3. 允许公开的文档，大都以2018-09-01文件名开头，会被jekyll build并生成html放置_site中。
4. 私有文档不符合jekyll生成规则就行。

### 结构
- .gitignore
- 404.html
- Gemfile
- Gemfile.lock
- _config.yml
- _posts
- about.md
- index.md
- _site -> wangkaimin.github.io

### 一般流程
```shell
jekyll new my.site
cd my.site
git init .
git remote add origin git@bitbucket.org:xxx/xxx.git
# submodule 需要重命名为 _site
# 因为jekyll默认生成的html目录为_site
git submodule add git@github.com:yyy/yyy.github.io.git _site
git add .
git commit -m "init"
git push origin master
cd _site
git add .
git commit -m "init"
git push origin master
```

