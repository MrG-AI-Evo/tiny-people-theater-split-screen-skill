# Tiny People Theater: Split-Screen Edition｜小人剧场分屏版

A Codex Skill that turns each uploaded real photograph into one complete 3:4 split-layout editorial poster.

这是一项生成“真实照片＋趣味小人叙事”分屏海报的 Codex Skill。每张照片单独输出，不制作拼图、合集或多图网格。

## What it creates｜生成内容

- 一张完整的 3:4 竖版无边框海报。
- 上下严格 1:1 分区，各占画面高度的 50%，中间使用干净水平分界线。
- 上半部分保留原照片的主要构图、人物数量、身份、动作、空间关系、材质、色彩和自然光影。
- 下半部分提取 1–3 个原图视觉锚点，以真实材质重构编辑式故事场景。
- 加入 6–8 个各不相同的极简黑线小人物，共同完成连续的小故事。
- 自动生成一句 2–7 个英文单词的轻巧手写短句。

## Install｜安装

把下面这句话发送给 Codex：

```text
请使用 $skill-installer 安装这个公开 GitHub 仓库中的 Skill：
仓库：https://github.com/MrG-AI-Evo/tiny-people-theater-split-screen-skill
路径：.
安装名：tiny-people-theater-split-screen
```

如果你在 Codex CLI 中安装，也可以直接运行：

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo MrG-AI-Evo/tiny-people-theater-split-screen-skill \
  --path . \
  --name tiny-people-theater-split-screen
```

安装后，Skill 的调用名是：

```text
$tiny-people-theater-split-screen
```

## Use｜使用

上传一张或多张真实照片，然后说：

```text
用 $tiny-people-theater-split-screen 直接出图
```

可选口令：

```text
用 $tiny-people-theater-split-screen，先问我
用 $tiny-people-theater-split-screen，整组统一
```

默认一张照片对应一张完整海报，不会自动生成许多变体。

## Source fidelity｜忠于原图

上半部分只进行轻微、克制的摄影调色；需要适配版面时，仅自然延伸天空、墙面、地面、桌面或环境边缘，不拉伸、扭曲、重绘或替换核心主体。原图中的真实文字与标识可以保留，但不得擅自修改或新增品牌。

## File compatibility｜文件兼容

仓库包含 `scripts/normalize_photo.sh`。当 Apple Photos 导出的 `.jpeg` 实际为 MPO 或 HEIC、导致图像工具无法读取时，可在不修改原文件的前提下转换为普通 JPEG。该脚本仅在需要时使用，并依赖 ImageMagick。

Search keywords: 小人剧场分屏版 Skill, 真实照片趣味小人海报, 上下分屏海报, Codex image skill, tiny people poster, split-screen editorial photo.
