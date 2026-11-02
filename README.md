# 曾圣凯 · zengzi-123

**甘肃政法大学 网络空间安全学院 · 计算机科学与技术 · 2026 级**

> 目标职业：**AI 应用开发工程师（智能体工具链与效果评测方向）** —— 懂 Agent 安全的开发者

11 个开源仓库，140 次提交。做的东西只有一类：**让 AI 干活这件事，从"每次手工重来"变成"一条可重复的产线"。**

---

## 一、Agent Skill：把任务变成可复用工具

别的编程智能体读一份 `SKILL.md`，就能把一句话变成成片、变成讲解、变成 3D 闪卡。
我做的是**工具本身**，不是执行任务的人。

| 仓库 | 一句话 | 语言 |
|---|---|---|
| [RuiC-motion-reel](https://github.com/zengzi-123/RuiC-motion-reel) | 一句话 brief 生成动态图形短片。时长按 BPM×小节算，样式现场推而非从模板库挑 | Python |
| [RuiC-pixel-explainer](https://github.com/zengzi-123/RuiC-pixel-explainer) | 口播文案 → 1920×1080/30fps 像素 RPG 讲解片，**逐帧导出、逐帧可复现** | Python |
| [RuiC-card-skill](https://github.com/zengzi-123/RuiC-card-skill) | 一句话生成可拖转、会流光、带层次景深的 3D 全息闪卡网页，附可编辑 Blender 工程 | JavaScript |

**可复现是评测的前提。** 这句话是我做工具时想明白的——准备 Agent 岗面试时撞上"Agent 效果怎么评测、评测集怎么建"那道题，才发现答案早就写在代码里。

## 二、数据与标准：给 AI 生成内容做体检

AI 生图最大痛点是一致性，别人反复抽卡，我先造标准。

**[RuiC-PoseAtlas](https://github.com/zengzi-123/RuiC-PoseAtlas)** · 288 组人体姿态 × 5 视角 × **1,439 张人台线稿**，加 1,407 套无人物衣装 × 8 分类 × **86 个三语标签**。中/英/日切换、搜索筛选、键盘浏览、原图下载，纯静态零依赖。

线稿不是素材，是**可自动打分的 ground truth** —— 用来算姿态偏差与命中率。

## 三、工程纪律：把可靠性做成产品

| 仓库 | 做了什么 | 对应岗位要求 |
|---|---|---|
| [RuiC-oc-ferry](https://github.com/zengzi-123/RuiC-oc-ferry) | 隔离运行时、并发检测、判定缓存、本机 OpenAI 兼容转发口 | Tool 认证 / 授权 / 限流 / 审计日志 / 输出脱敏 |
| [RuiC-dsh-purge](https://github.com/zengzi-123/RuiC-dsh-purge) | 预检 → 快照 → 原子写入 → 冲突检测回滚 | 输出格式约束、推理路径收敛、结果一致性校验 |
| [RuiC-freebuddy](https://github.com/zengzi-123/RuiC-freebuddy) | 桌面端本机增强面板：多账号备份、Token 用量统计、会话分支迁移 | 工程化与可维护性 |
| [RuiC-FoldScreen](https://github.com/zengzi-123/RuiC-FoldScreen) | 合盖弯屏 macOS app，读翻盖角度传感器，Metal 实时折角 | 系统级、图形与传感器（Swift） |

## 四、工具与效率

- [music-geshizhuanhuan](https://github.com/zengzi-123/music-geshizhuanhuan) — 全平台加密音乐格式转换器（NCM / QMC / KGM / KWM），代码从零自研，MIT
- [RuiC-VideoGrab](https://github.com/zengzi-123/RuiC-VideoGrab) — 网页版全平台视频下载器，支持 1000+ 站点
- [dy-xuhuohua](https://github.com/zengzi-123/dy-xuhuohua) — FastAPI + Playwright + APScheduler 自动化系统

---

## 接下来的方向

**不开新项目，只把已有工具做深**：建 50 条 brief 评测集与校验层并公开评测报告 → 把 motion-reel 改造为标准 MCP Server（schema、校验、审计日志）→ 基于 1,439 张线稿做多模态评测。

**为什么是 AI 应用开发**：智能体开发需求同比 +244%，但通用型应用开发供需比已过剩、算法岗对 1 年以下经验需求 -71.43%。留给"没经验但有真东西的人"的位置在**工具链与效果评测层**——JD 都指向同一层，正是这十一个仓库所在的层。

## 说明

- 本账号 `zengzi-123` 为**主账号**；早期开发主页 `HRuiCcc` 内容同源，star / fork 计数沉淀在早期主页。
- [Awesome-Prompts](https://github.com/zengzi-123/Awesome-Prompts) 为上游 `dongshuyan/Awesome-Prompts` 的 fork，非本人原创，特此标注来源。
- [RuiC-dsh-purge](https://github.com/zengzi-123/RuiC-dsh-purge) 基于 `ZiPengWei/dsh-purge`（MIT）二次开发。
