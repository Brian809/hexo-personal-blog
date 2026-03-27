---
title: QQ机器人部署
data: 2026-03-27
---
# QQ机器人部署
## 实用资源
1.[Napcat QQ](https://napneko.github.io/)
2.[Nonebot](https://nonebot.dev/)

## 部署步骤
Napcat QQ的文档的说明已经很详细了，如果要在Linux服务器上部署，最好禁用WebUI。
我们并不需要完全地编写机器人插件，可以试试[Nonebot插件商店](https://nonebot.dev/store/plugins)。

nonebot文档推荐使用nb-cli来添加插件，由于我不太会改`pyproject.toml`，我采用了比较粗暴的方式，使用pip安装后直接将sitepackages中对应的插件文件夹复制到项目文件夹中。这样的插件我还方便修改……

