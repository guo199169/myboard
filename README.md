# myboard

<p align="center">
  <img src="./readme/pc.png" height="300">
  <img src="./readme/mobile.png" height="300">
</p>

`myboard` 是基于 [`zashboard`](https://github.com/Zephyruso/zashboard) 修改的中文自用版本，主要针对 Mihomo / OpenClash 配置做了更清晰的策略组、节点组展示。

## 功能特点

- 将原来的 `代理` 视图重命名为 `策略组`
- 将高层策略组和地区节点组拆分为独立分页
- 支持将 `美国`、`香港`、`日本` 等地区组聚合到 `节点组`
- 新增 `兜底策略` 分组展示
- 节点组支持显示当前实际使用路径

## 仓库地址

- GitHub: [guo199169/myboard](https://github.com/guo199169/myboard)

## 本地运行

```bash
pnpm install
pnpm build
pnpm preview
```

开发模式：

```bash
pnpm dev
```

## 部署说明

构建完成后，直接部署 `dist/` 目录即可。  
可以放到任意静态站点环境中，例如：

- Nginx
- Caddy
- Cloudflare Pages
- GitHub Pages

## 当前自定义内容

- `策略组` 中展示高层策略入口
- `节点组` 中展示地区 / 底层节点分组
- 地区节点组支持聚合展示
- `兜底策略` 支持单独归类

## 使用说明

1. 打开面板后，在 `策略组` 中查看高层策略。
2. 在 `节点组` 中查看地区节点池。
3. 展开地区分组后，可以看到对应的子分组和当前路径。
4. 右键节点或节点组卡片可进行测速。

## 说明

这个仓库是个人修改版，不再保留原项目 README 中的在线地址、官方发行包、赞助说明等内容。若需查看原始项目，请前往：

- [Zephyruso/zashboard](https://github.com/Zephyruso/zashboard)
