# 付饼 · AAAA 万能大饼

这是一个可直接导入 Codex 的 v2 动态宠物。它包含 9 种常用动作和 16 个视线方向。

动作由 Codex 根据当前状态自动选择，不是 9 个独立的 GIF 文件。对应关系如下：

- 待机：idle
- 向右移动：running-right
- 向左移动：running-left
- 打招呼：waving
- 跳跃：jumping
- 失败/出错：failed
- 等待确认或输入：waiting
- 工作/处理中：running
- 检查结果：review

16 个视线方向用于鼠标指针方向跟随；指针位于正前方时会回到待机动画。因此平时主要看到待机，只有 Codex 进入相应状态或鼠标移动到不同方向时，其他动态才会出现。

![付饼预览](preview.png)

## 文件说明

- `pet.json`：宠物名称、介绍和版本配置。
- `spritesheet.webp`：宠物的完整动画图集；必须与 `pet.json` 保持同一目录。

## 导入到另一台电脑

1. 下载或克隆此仓库。
2. 在目标电脑创建宠物目录：

   ```text
   ~/.codex/pets/fubing/
   ```

3. 将本仓库中的 `pet.json` 和 `spritesheet.webp` 一起复制到该目录。
4. 刷新或重新打开 Codex；宠物列表中会显示“付饼”。

导入后的目录应为：

```text
~/.codex/pets/fubing/
├── pet.json
└── spritesheet.webp
```

## 配置

此宠物使用 `spriteVersionNumber: 2`，因此图集为 8 列 × 11 行。请勿单独替换其中一个文件，或修改图集尺寸。
