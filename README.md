# 她的小分身 · Codex 桌宠

基于照片制作的 Q 版人物桌宠：长黑发、眼镜、白衬衫和灰色背心裙。

![挥手](previews/waving.gif) ![转头](previews/look-directions.gif) ![跳跃](previews/jumping.gif)

**[下载桌宠安装包 v1.0.0](downloads/her-mini-v1.0.0.zip?raw=true)**

## 安装

1. 下载上面的压缩包并解压，得到 `her-mini` 文件夹。
2. 把整个 `her-mini` 文件夹复制到下面对应的目录中：

   | 系统 | 桌宠目录 |
   | --- | --- |
   | Windows | `%USERPROFILE%\.codex\pets\` |
   | macOS | `~/.codex/pets/` |

   如果设置了自定义 `CODEX_HOME`，使用该目录下的 `pets` 文件夹。目录不存在时可以自行新建。

3. 打开 Codex 桌面应用，在 **设置 → Pets（桌宠）** 中点击 **Refresh（刷新）**，选择 **她的小分身**。
4. 输入 `/pet`，或使用 **Show pet（显示桌宠）**，即可显示桌宠。

安装后的结构应为：

```text
.codex/
└── pets/
    └── her-mini/
        ├── pet.json
        └── spritesheet.webp
```

需要支持 v2 桌宠格式的桌面应用版本。如果刷新后没有出现，先确认 `pet.json` 和 `spritesheet.webp` 位于同一个 `her-mini` 文件夹，再尝试重启应用。

## 分享给朋友

把 [这个仓库链接](https://github.com/phxumy/my-girlfriend-codex-pet) 发给对方，让对方下载压缩包并按上面的步骤安装即可。

这个分享包包含生成后的桌宠和预览，原始照片与本机制作记录保留在本地。

## 动画与格式

包含待机眨眼、向右跑动、向左跑动、挥手、跳跃、低落、等待、思考和检查共 **9 种状态**，以及 **16 个视线方向**。

- 桌宠名：她的小分身
- 标识：`her-mini`
- 格式：`spriteVersionNumber: 2`
- 图集：透明 WebP，1536 × 2288 像素，8 列 × 11 行
- 每帧：192 × 208 像素
- 生成方式：内置 imagegen；已完成结构、动作与方向检查
- 文件校验：[SHA256SUMS.txt](downloads/SHA256SUMS.txt)

[查看全部动作](previews/animation-overview.png) · [查看视线方向](previews/look-directions.png)

## 仓库内容

```text
her-mini/       桌宠本体，包含 pet.json 和 spritesheet.webp
downloads/      可分享的 ZIP 安装包与 SHA-256 校验值
previews/       动画 GIF、形象预览和动作总览
```

应用中的选择、刷新和显示方式可参考 [OpenAI 官方 Pets 说明](https://learn.chatgpt.com/docs/pets)。
