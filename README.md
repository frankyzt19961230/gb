# peterpans-truths.github.io

## Structure

Main points are under `content/services/section_*.md`

## Deployment

The `source` branch is our default branch. The website content and theme are saved in the `source` branch, the static content accordingly will be automatically generated after each commit to the `source` branch and save to the `master` branch.

By default, GitHub Pages settings under `Settings` tab should set the source to `branch=master`, and `folder=/ (root)`, then the static content in the `master` branch will be shown at `peterpans-truths.github.io`.

The GitHub action workflow script is saved at `.github/workflows/main.yml` in the main branch `source`.

### Temporary Placeholder

When development, you could set GitHub Pages settings to `branch=source`, and `folder=/docs`, then the page will directly show static files saved in `docs` folder in `source` branch.

## Development

To preview the website locally: 
1. Install hugo [[Link]](https://gohugo.io/getting-started/quick-start/)
2. Run `hugo server --debug` under the root directory of your local codebase

To manually generate static content:  
1. Run `hugo` in command line, then generated static website source code is saved in `public`


### 关于设置网站密码（用于测试阶段）

使用了aerobatic的密码插件，参考页面：https://www.aerobatic.com/blog/password-protect-a-hugo-site/

测试阶段网站发布的地址为 https://sore-carriage.aerobaticapp.com

网站布署: `aero deploy -d public`


### 关于modal组件

modal组件的定义位于modal.html中，其主要功能为实现图片的点击放大功能以优化排版，其接受的参数为：
- src： 图片的地址
- index： 同一页面中，每个modal组件必须使用独特的index，用于区分不同的modal组件，确保预览小图与点击后的大图内容一致
- cap：图片的字幕，出现于预览小图的下方（选填）

### 关于导航栏下拉菜单

下拉菜单的实现位于main-menu之中，需要在config.toml中建立层级关系来实现每个大标题下的小标题内容