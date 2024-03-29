# my template r

## Usage 
- Create a new repo based on this, choose one of these methods
    - （推荐） `use this template` -> `create a new repository`
    - fork
        - 设置fork repo名为project名
        - clone 到本地
    - clone and manually set remote
        - github 创建新的空repo，新repo名为project名，不要添加readme或者gitignore
        - 在本地先clone模板repo，再 `remote set-url origin <new url>` （注意，需要把github提示的commands中的 `add origin` 改成 `set-url origin` ，例如
            
            ```bash
            git remote set-url origin https://github.com/mangost/<new repo name>.git
            git branch -M main
            git push -u origin main
            ```
            
- 几处名称更改
    - 更改项目文件夹为project名
    - 更改 `.Rproj` 为project名，使用 `git mv`
    - 修改 `README.md` 的标题
    - 修改 `_site.yml` 中的 `name` 和 `title` 为新项目名，修改 `href` 为新repo地址
    - 必要时，修改 `.Rprofile` 和 `renv.lock` 中的 CRAN 的 URL
- 启动 DevContainer 或者 切换 folder（一般需要40s，第一次启动除外）
- 安装R包（一般需要3分钟）
    - `renv::restore()`
    - 如果有新代码要求新的包： `renv::snapshot()`
- 重建分析和网站
    - `wflow_build(republish = T)`
    - live server 检查 网站名称、past versions、超链接
    - 在github主页上添加链接（public repo 可访问）`https://htmlpreview.github.io/?https://raw.githubusercontent.com/mangost/<new repo name>/main/docs/index.html`
- git add and commit


## Attributes

- [workflowr][]
- rocker
- posit
- vscode and many extensions (see `.devcontainer/devcontainer.json`)

[workflowr]: https://github.com/workflowr/workflowr