# Elaine 的个人主页

这是我的个人主页源码，使用 Jekyll 构建，支持中英文页面。

- **个人主页**：[heyheyhazel.github.io](https://heyheyhazel.github.io/)
- **English**：[About Me](https://heyheyhazel.github.io/home/)
- **中文**：[关于我](https://heyheyhazel.github.io/zh/)

## 内容维护

| 文件或目录 | 用途 |
| --- | --- |
| `_pages/about.md` | 英文主页内容 |
| `_pages/about-zh.md` | 中文主页内容 |
| `_config.yml` | 网站标题、个人资料和全局配置 |
| `_data/navigation.yml` | 中英文导航 |
| `images/` | 头像、项目图片及其他图片资源 |

## 本地预览

安装 Ruby 和 Bundler 后，在仓库根目录运行：

```bash
bundle install
bash run_server.sh
```

在浏览器中打开 <http://127.0.0.1:4000>。修改 `_config.yml` 后需要重启预览服务。

## 发布

将更新提交并推送到 `main` 分支，在仓库的 `Settings → Pages` 中配置发布来源。仓库名为 `heyheyHazel.github.io`。

## 模板来源与许可

本网站基于 [RayeRen / AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io) 模板进行个性化修改。原模板采用 MIT License，原作者版权声明和完整许可文本保留在 [LICENSE](LICENSE) 中。

模板还使用或参考了以下项目：

- [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)：MIT License。
- [Academic Pages](https://github.com/academicpages/academicpages.github.io)：MIT License。
- [Font Awesome](https://fontawesome.com/)：相关资源采用 SIL OFL 1.1 和 MIT License。
