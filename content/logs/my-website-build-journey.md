
# 建站技术日志 (Build Log)

### 1. 项目概况 (Project Overview)

* **框架**：基于 Go 语言的静态网站生成器 Hugo。
* **主题**：PaperMod。
* **部署架构**：GitHub Pages (主站) + Vercel (OAuth 中转)。
* **目标**：构建具有“工程蓝图”质感的个人技术空间，集成 CS50 与 STM32 学习笔记。

---

### 2. 执行流程记录 (Execution Pipeline)

| 阶段 | 核心任务 | 状态 |
| --- | --- | --- |
| **基础搭建** | 配置 `hugo.yml`，初始化 PaperMod 主题，设置 GitHub 仓库。 | 已完成 |
| **视觉定制** | 编写 `custom.css`，实现网格背景、硬质投影卡片、衬线标题与思源宋体描述。 | 已完成 |
| **CI/CD 配置** | 编写 `.github/workflows/hugo.yml`，配置 GitHub Actions 自动化构建脚本。 | 已完成 |
| **后台集成** | 在 GitHub 申请 OAuth App，使用 Vercel 部署 `oauth-provider`。 | 已完成 |
| **CMS 联调** | 配置 `config.yml` 中的 `base_url`，打通后台登录权限。 | 已完成 |

---

### 3. 技术坑位与解决方案 (Pitfalls & Solutions)

#### A. 站点渲染与部署 (GitHub Actions)

* **坑位 1：主页“裸奔”（Naked Site）**
* **现象**：网页仅显示原始 HTML 文字，无 CSS 样式加载。
* **原因**：GitHub Actions 构建失败（红叉），未生成样式文件；或 `baseURL` 配置错误。
* **解决**：在 Actions 脚本中添加 `submodules: recursive` 确保主题拉取完整，并开启 `extended: true` 以支持 Hugo 扩展版编译。


* **坑位 2：Actions 持续报错**
* **原因**：`hugo.yml` 中的 `baseURL` 缺少末尾斜杠 `/` 或协议头不匹配。
* **解决**：修正 `baseURL` 为 `https://heyiweine729.github.io/`。



#### B. 后台管理系统 (Vercel & OAuth)

* **坑位 3：Vercel 部署“No Results”**
* **现象**：Vercel 项目列表为空，未感知到代码变动。
* **原因**：GitHub 仓库为空（未初始化 README）或 Webhook 链路断裂。
* **解决**：通过 Fork 官方模板仓库手动搬运代码，重新 Import 至 Vercel。


* **坑位 4：OAuth 登录失效**
* **原因**：GitHub OAuth App 中的 `Authorization callback URL` 填写不规范。
* **解决**：确保回调地址格式为 `https://[你的Vercel地址].vercel.app/callback`（必须包含后缀）。


* **坑位 5：环境变量未读取**
* **现象**：部署后登录提示 Client 错误。
* **原因**：未在 Vercel Settings 中配置 `OAUTH_CLIENT_ID` 与 `OAUTH_CLIENT_SECRET`。
* **解决**：在 Vercel 后台手动补录 Environment Variables 并执行 Redeploy。



---

### 4. 维护指令集 (Maintenance Commands)

* **同步内容**：git add .
git commit -m ""
git push origin main。
* **强制重置主题**：`git submodule add --force [URL] themes/PaperMod`。

---
```
git add .
git commit -m "update 2.23"
git push
```