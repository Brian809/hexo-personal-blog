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

## 2026.3.29 小记
由于我发现nonebot的llm支持严重依赖插件，agent和mcp支持不够完善，我打算换成astrbot了，我入门了astrbot插件开发（当然用了AI vibe coding来辅助），项目在[这里](https://github.com/Brian809/astrbot-plugin-aliyun-qwen-generator)。可参考一下，是一个调用阿里云百炼平台的图片生成插件。

效果如下：
![效果](/images/QQ机器人部署/image.png)
