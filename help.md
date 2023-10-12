## 安装过程：
1. 通过镜像的方式 [仓库](https://github.com/BretFisher/jekyll-serve/tree/main)
1. 使用容器本地调试你的博客网站:
    ```
    cd your-dir
    docker run -v $(pwd):/site bretfisher/jekyll new .
    docker run -p 4000:4000 -v $(pwd):/site bretfisher/jekyll-serve
    ```

1. 使用主题
    [主题](https://github.com/sighingnow/jekyll-gitbook)
    git clone 该仓库，然后修改其
    - _sites/index.html
        - 删除
    - _includes/toc-date.html
        - 修改 Fork it Now 这一 \<li\> 标签中的内容
    - _includes
        - 静态页面的组织方式，template语法文件，修改页面的可以修改这个文件夹下面的模板文件

官方网站： 
[jekyll 中文官网](https://www.jekyll.com.cn/docs/)
[jekyll 官网](https://jekyllrb.com/docs/)
[github pages docs](https://docs.github.com/pages)

## 其他情况
docker 空间不够：docker system prune --all --volumes