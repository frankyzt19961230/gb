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