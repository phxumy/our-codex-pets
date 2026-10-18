# 小梅梅 · Codex 桌宠

基于照片制作的 Q 版人物桌宠：长黑发、眼镜、白衬衫和灰色背心裙。

![挥手](previews/waving.gif) ![转头](previews/look-directions.gif) ![跳跃](previews/jumping.gif)

**[下载双版本安装包 v1.1.0](downloads/xiaomeimei-v1.1.0.zip?raw=true)**

## 两个可切换的版本

| 小梅梅 · 思考版 | 小梅梅（电脑工作版） |
| --- | --- |
| 原版托腮思考动作 | 新增拿笔记本、双手打字和抬头看屏幕的动作 |
| ![思考版工作动画](previews/running.gif) | ![电脑工作版动画](previews/laptop-work.gif) |
| 文件夹：`her-mini` | 文件夹：`her-mini-laptop` |

两版保留相同的人物形象、服装和其他动作。安装两版后，在 **设置 → Pets（桌宠）** 中手动选择使用哪一版。

## 安装

1. 下载上面的压缩包并解压，得到 `her-mini` 和 `her-mini-laptop` 两个文件夹。
2. 将这两个文件夹复制到下面对应的目录中：

   | 系统 | 桌宠目录 |
   | --- | --- |
   | Windows | `%USERPROFILE%\.codex\pets\` |
   | macOS | `~/.codex/pets/` |

   如果设置了自定义 `CODEX_HOME`，使用该目录下的 `pets` 文件夹。目录不存在时可以自行新建。

3. 打开 Codex 桌面应用，在 **设置 → Pets（桌宠）** 中点击 **Refresh（刷新）**，选择 **小梅梅** 或 **小梅梅（电脑工作版）**。
4. 输入 `/pet`，或使用 **Show pet（显示桌宠）**，即可显示桌宠。

安装后的结构应为：

```text
.codex/
└── pets/
    ├── her-mini/
    │   ├── pet.json
    │   └── spritesheet.webp
    └── her-mini-laptop/
        ├── pet.json
        └── spritesheet.webp
```

旧版的 `her-mini` 标识保留不变，更新后显示名改为“小梅梅”。需要支持 v2 桌宠格式的桌面应用版本。

## 工作动作为什么只播放一小段？

工作状态对应 **row 7 / running**，也是内置 Codex 宠物拿电脑工作的那一行。

在本机核对的 **26.1013** 桌面应用中，这一行固定为六帧：前五帧各 120 毫秒，最后一帧 220 毫秒，每轮约 **0.82 秒**；默认播放三轮，约 **2.46 秒**后转入待机。时长和重复次数由应用控制，桌宠素材包没有可调整这些参数的字段。

电脑工作版增加了更明显的手部打字和头部动作，播放时长仍遵循应用规则。一只桌宠只能配置一行工作动作；这里提供的是两个可手动切换的版本。预览 GIF 为便于观看持续循环，应用内的实际播放由客户端决定。

## 分享给朋友

把 [这个仓库链接](https://github.com/phxumy/my-girlfriend-codex-pet) 发给对方，让对方下载双版本压缩包并按上面的步骤安装即可。

分享包包含生成后的桌宠和预览，原始照片与本机制作记录保留在本地。

## 动画与格式

两版均包含待机眨眼、向右跑动、向左跑动、挥手、跳跃、低落、等待、工作和检查共 **9 种状态**，以及 **16 个视线方向**。

- 格式：`spriteVersionNumber: 2`
- 图集：透明 WebP，1536 × 2288 像素，8 列 × 11 行
- 每帧：192 × 208 像素
- 生成方式：内置 imagegen；结构、动作与方向均经过检查
- 文件校验：[SHA256SUMS.txt](downloads/SHA256SUMS.txt)

[思考版动作总览](previews/animation-overview.png) · [电脑工作版动作总览](previews/laptop-animation-overview.png) · [视线方向](previews/look-directions.png)

## 仓库内容

```text
her-mini/          小梅梅（思考版）
her-mini-laptop/   小梅梅（电脑工作版）
downloads/         双版本 ZIP 安装包与 SHA-256 校验值
previews/          动画 GIF、形象预览和动作总览
```

应用中的选择、刷新和显示方式可参考 [OpenAI 官方 Pets 说明](https://learn.chatgpt.com/docs/pets)。
