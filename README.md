# 我们的 Codex 桌宠

我和女朋友的 Q 版人物桌宠：**小梅梅**与穿红黑博士袍、戴博士帽的**小博士**。

![小梅梅挥手](previews/waving.gif) ![小博士挥手](previews/phd-waving.gif)

**[下载三款合集 v1.2.0](downloads/our-codex-pets-v1.2.0.zip?raw=true)**

## 三款可选桌宠

| 桌宠 | 形象与工作动作 | 文件夹 |
| --- | --- | --- |
| 小梅梅 · 思考版 | 长黑发、眼镜、白衬衫、灰色背心裙；托腮思考 | `her-mini` |
| 小梅梅（电脑工作版） | 相同人物造型；拿笔记本、双手打字和抬头看屏幕 | `her-mini-laptop` |
| 小博士 | 短黑发、红黑博士袍、黑色博士帽和金色流苏；专注思考 | `phd-mini` |

![小梅梅思考](previews/running.gif) ![小梅梅电脑工作](previews/laptop-work.gif) ![小博士思考](previews/phd-running.gif)

安装后，在 **设置 → Pets（桌宠）** 中手动选择喜欢的形象。

## 安装

1. 下载并解压 [三款合集](downloads/our-codex-pets-v1.2.0.zip?raw=true)，得到 `her-mini`、`her-mini-laptop`、`phd-mini` 三个文件夹。
2. 将想使用的文件夹复制到对应的桌宠目录：

   | 系统 | 桌宠目录 |
   | --- | --- |
   | Windows | `%USERPROFILE%\.codex\pets\` |
   | macOS | `~/.codex/pets/` |

   如果设置了自定义 `CODEX_HOME`，使用该目录下的 `pets` 文件夹。目录不存在时可以自行新建。

3. 打开 Codex 桌面应用，在 **设置 → Pets（桌宠）** 中点击 **Refresh（刷新）**，选择 **小梅梅**、**小梅梅（电脑工作版）**或**小博士**。
4. 输入 `/pet`，或使用 **Show pet（显示桌宠）**，即可显示桌宠。

安装后的结构：

```text
.codex/
└── pets/
    ├── her-mini/
    │   ├── pet.json
    │   └── spritesheet.webp
    ├── her-mini-laptop/
    │   ├── pet.json
    │   └── spritesheet.webp
    └── phd-mini/
        ├── pet.json
        └── spritesheet.webp
```

需要支持 v2 桌宠格式的 Codex 桌面应用版本。原有 `her-mini` 标识保留，显示名为“小梅梅”。

## 工作动作的播放时长

工作状态对应 **row 7 / running**，也是内置 Codex 宠物拿电脑工作的那一行。

在本机核对的 **26.1013** 桌面应用中，这一行固定为六帧：前五帧各 120 毫秒，最后一帧 220 毫秒，每轮约 **0.82 秒**；默认播放三轮，约 **2.46 秒**后转入待机。时长和重复次数由应用控制，桌宠素材包没有可调整这些参数的字段。

电脑工作版提供更明显的手部打字和头部动作，播放时长仍遵循应用规则。一只桌宠只能配置一行工作动作，不同版本通过设置手动切换。预览 GIF 为便于观看持续循环，应用内实际播放由客户端决定。

## 动作预览

![小博士转头](previews/phd-look-directions.gif) ![小博士跳跃](previews/phd-jumping.gif)

- 小梅梅：[动作总览](previews/animation-overview.png) · [视线方向](previews/look-directions.png)
- 小梅梅电脑工作版：[动作总览](previews/laptop-animation-overview.png)
- 小博士：[形象](previews/phd-main-look.png) · [动作总览](previews/phd-animation-overview.png) · [视线方向](previews/phd-look-directions.png)

## 分享给朋友

把 [仓库链接](https://github.com/phxumy/our-codex-pets) 发给对方，下载合集并按上面的步骤安装即可。

分享包包含生成后的桌宠和预览。原始照片与本机制作记录保留在本地。

## 动画与格式

三款均包含待机眨眼、向右跑动、向左跑动、挥手、跳跃、低落、等待、工作和检查共 **9 种状态**，以及 **16 个视线方向**。

- 格式：`spriteVersionNumber: 2`
- 图集：透明 WebP，1536 × 2288 像素，8 列 × 11 行
- 每帧：192 × 208 像素
- 生成方式：内置 imagegen；结构、动作和视线方向均经过检查
- 文件校验：[SHA256SUMS.txt](downloads/SHA256SUMS.txt)

## 仓库内容

```text
her-mini/          小梅梅（思考版）
her-mini-laptop/   小梅梅（电脑工作版）
phd-mini/          小博士
downloads/        合集 ZIP、历史安装包和 SHA-256 校验值
previews/         动画 GIF、形象预览和动作总览
```

历史安装包：[小梅梅双版本 v1.1.0](downloads/xiaomeimei-v1.1.0.zip?raw=true) · [初版 v1.0.0](downloads/her-mini-v1.0.0.zip?raw=true)

应用中的选择、刷新和显示方式可参考 [OpenAI 官方 Pets 说明](https://learn.chatgpt.com/docs/pets)。
