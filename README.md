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

## 安装部署

### 方式一：Docker 一键部署（推荐）

```bash
docker run -d -p 8080:80 ghcr.io/zephyruso/zashboard:latest
```

然后访问 `http://your-ip:8080`

### 方式二：下载预构建包

直接下载并解压部署：

```bash
# 下载最新版
wget https://github.com/guo199169/myboard/releases/latest/download/dist.zip
unzip dist.zip
```

然后将 `dist` 目录部署到任意 Web 服务器（Nginx、Caddy 等）。

### 方式三：源码构建

```bash
# 克隆仓库
git clone git@github.com:guo199169/myboard.git
cd myboard

# 安装依赖
pnpm install

# 构建
pnpm build

# 预览
pnpm preview
```

## 配置使用

部署完成后，访问面板时需要在 URL 中填写 Clash API 的连接信息：

```
http://your-ip:port/#/setup?hostname=你的IP&port=9090&secret=你的密码
```

参数说明：
- `hostname` - Clash API 的 IP 或域名
- `port` - Clash API 端口（默认 9090）
- `secret` - Clash API 密码（可选）

## 部署环境

构建后的 `dist/` 是纯静态文件，可部署到：

- Nginx / Caddy
- Docker
- Cloudflare Pages
- GitHub Pages
- Vercel
- 任意 Web 服务器

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
