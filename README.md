# mzh-RW.github.io
# mzh — 个人主页

一个纯静态的个人主页，用于 GitHub Pages。整个站点只有三个文件，没有构建步骤、没有依赖。

## 文件结构

```
.
├── index.html          # 页面本体（根目录入口，GitHub Pages 默认读取）
├── assets/
│   ├── style.css       # 样式
│   └── favicon.svg     # 站点图标（内联 SVG，无外部请求）
└── README.md
```

## 本地预览

任选一种方式，在项目根目录（即本文件所在目录）执行：

**Python 3（多数系统已自带）**

```powershell
python -m http.server 8000
```

macOS / Linux 上如果 `python` 不存在，用 `python3 -m http.server 8000`。

**Node.js**

```bash
npx serve .
```

**VS Code**

安装 Live Server 扩展，右键 `index.html` → *Open with Live Server*。

然后用浏览器打开 <http://localhost:8000>。请通过本地服务器访问，不要直接双击 `index.html`——用 `file://` 打开时相对路径资源的行为和上线后不一致。

按 `Ctrl+C` 停止服务器。

## 发布到 GitHub Pages

1. 新建一个公开仓库，把本目录下的文件提交并推送到 `main` 分支（`index.html` 必须位于仓库根目录）。
2. 打开仓库 **Settings → Pages**。
3. 在 *Build and deployment* 里选择 **Deploy from a branch**，分支选 `main`、目录选 `/ (root)`，保存。
4. 等一两分钟，页面会发布在 `https://<你的用户名>.github.io/<仓库名>/`；若仓库名就是 `<你的用户名>.github.io`，地址则是 `https://<你的用户名>.github.io/`。

## 隐私与依赖说明

- 没有外部字体、CDN、图片、统计或追踪脚本，页面只加载同目录下的 `assets/` 文件，不产生第三方请求。
- 仓库内不含学号、真实姓名、作业内容、密钥或令牌。
- 修改展示内容只需编辑 `index.html` 里的昵称与介绍文字；整体配色在 `assets/style.css` 顶部的 `:root` 变量里调整。
