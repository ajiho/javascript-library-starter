# JavaScript Library Starter

一个现代化的 JavaScript 库开发起始模板。

集成 **Rolldown、Oxlint、Oxfmt、Vitest、Size Limit、Simple Git Hooks、Release Please 和 pnpm**，开箱即用地提供从开发、测试、构建到发布的完整工具链。

## 特性

- ⚡ **Rolldown** — 高性能 JavaScript 打包
- 🔍 **Oxlint** — 极速代码检查
- ✨ **Oxfmt** — 极速代码格式化
- 🧪 **Vitest** — 单元测试与覆盖率
- 📦 **Size Limit** — 构建产物体积检测
- 🪝 **Simple Git Hooks** — 轻量 Git Hooks
- 🚀 **Release Please** — 自动化版本管理与发布
- 📦 **pnpm** — 快速、节省磁盘空间的包管理器

## 使用

### 使用 GitHub Template

推荐直接点击仓库右上角的 **Use this template** → **Create a new repository**，创建属于你的 JavaScript 库。

创建完成后克隆你的新仓库并安装依赖：

```bash
git clone https://github.com/YOUR_USERNAME/my-library.git

cd my-library

pnpm install
```

### 手动克隆

也可以直接克隆此模板：

```bash
git clone https://github.com/ajiho/javascript-library-starter.git my-library

cd my-library

pnpm install
```

然后修改 `package.json`、入口文件和源码，即可开始开发。

## 脚本

| 脚本            | 说明                          |
| --------------- | ----------------------------- |
| `pnpm fmt`      | 使用 Oxfmt 格式化代码         |
| `pnpm lint`     | 使用 Oxlint 检查代码          |
| `pnpm lint:fix` | 自动修复代码问题              |
| `pnpm test`     | 使用 Vitest 运行测试并启动 UI |
| `pnpm coverage` | 运行测试并生成覆盖率          |
| `pnpm build`    | 清理、构建并检查产物体积      |
| `pnpm size`     | 检查构建产物体积              |
| `pnpm clean`    | 清理 `dist` 目录              |
| `pnpm prepare`  | 初始化 Simple Git Hooks       |

### 构建流程

`pnpm build` 会依次执行：

```text
clean → build:base → build:min → size
```

其中：

- `build:base` — 使用 Rolldown 构建
- `build:min` — 构建生产版本
- `size` — 检查构建产物体积
