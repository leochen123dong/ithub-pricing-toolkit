# ITHub管理服务计价工具包

宜鼎（InnoDisk）ITHub 管理服务的工具集合。全部使用 HTML / CSS / JavaScript 单文件实现，无外部依赖，浏览器直接打开即可使用。

## 文件清单

| 文件 | 用途 |
|------|------|
| `index.html` | 工具导航入口页 |
| `网络维保服务蓝图_ITIL.html` | 基于 ITIL 4 服务价值体系的网络维保服务蓝图（5 阶段 × 5 泳道） |
| `网络维保计费表.html` | IT 运维服务计费表：15 大类 90+ 设备类型、类型库可在线编辑、数量/金额公式联动、CSV 导出 |
| `tenant_health.html` | 租户健康度检查工具 |

## 本地预览

任意 `.html` 文件双击在浏览器打开即可，**无需启动本地服务器、无需 `npm install`**。

> 建议：用 VS Code 或其他编辑器打开后保存，刷新浏览器即可看到效果。

## 维护指南

### 修改 / 新增工具

1. 直接编辑对应的 `.html` 文件（所有 CSS / JS 均内联在文件内）
2. 如新增工具：在 `index.html` 添加一个卡片入口，并在下方文件清单补充说明
3. 提交并推送：

```bash
git status                       # 查看变更
git add <文件名>                 # 暂存要提交的文件
git commit -m "feat: 说明修改"    # 提交
git push                         # 推送到 GitHub
```

### 设计语言（统一规范）

- 主色 `#1a237e` / `#3f51b5`，强调色 `#ff5722`，背景 `#f4f7fc`
- 中文字体栈：`'Segoe UI', 'Microsoft YaHei', sans-serif`
- 联动公式约定详见 `网络维保计费表.html` 末尾的 `formula-note` 区块

### 注意事项

- 单文件包含所有依赖，避免引入 CDN / 外部资源（保证离线可用）
- 文件名建议使用中文（与项目语境一致），避免使用空格
- 不要提交大文件（视频、PPT 等），见 `.gitignore`
- 提交前可 `git diff` 检查改动是否符合预期

## 项目信息

- **客户**：宜鼎 InnoDisk
- **项目**：FY27 服务交付
- **维护**：Richard
- **仓库**：<https://github.com/leochen123dong/ithub-pricing-toolkit>（Private）
