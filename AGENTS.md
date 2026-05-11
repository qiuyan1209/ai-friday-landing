# AI星期五宣传落地页 - 需求拆解文档

## 产品概述

- **产品类型**: 品牌宣传落地页 (Landing Page)
- **场景类型**: <scene_type>prototype-app</scene_type>
- **目标用户**: 杭州滨江及周边中小企业老板、团队负责人、对 AI 转型感兴趣的传统行业从业者
- **核心价值**: 传递“AI星期五”真实、接地气、不装专家的品牌调性，吸引潜在参与者围观并加入社群
- **界面语言**: 中文
- **主题偏好**: user_specified (青蓝色+明黄撞色，科技感与活力感并存)
- **导航模式**: 锚点导航
- **导航布局**: Topbar（顶部透明/吸顶固定）

---

## 页面结构总览

> **说明**：落地页为单页应用，通过锚点实现平滑滚动跳转。

**页面文件**: `HomePage.tsx`

| 区块名称 | 锚点 | 区块说明 |
|---------|------|---------|
| Hero 首屏 | `#hero` | 品牌名、核心口号、主视觉氛围、CTA按钮 |
| AI星期五是什么 | `#about` | 一句话定义、品牌定位说明（非专家培训，而是真实探索） |
| 我们做什么 | `#services` | 5类核心服务内容卡片展示 |
| 超级金句墙 | `#quotes` | 3条品牌超级金句集中大字报展示 |
| 先围观，再入局 | `#philosophy` | 参与理念说明，解释为何要先围观后加入 |
| 往期回顾 | `#review` | 第1期沙龙内容摘要、亮点与真实反馈展示 |
| 联系我们 | `#contact` | 扫码入群入口、微信添加指引、联系方式 |

---

## 导航配置

> **说明**：此表为导航生成的数据源，路由需与页面结构总览一致

- **导航布局**: Topbar（顶部固定，滚动时背景渐变/毛玻璃效果）
- **导航项**:
  | 导航文字 | 锚点 |
  |---------|------|
  | 品牌介绍 | `#about` |
  | 服务内容 | `#services` |
  | 超级金句 | `#quotes` |
  | 往期回顾 | `#review` |
  | 联系我们 | `#contact` |

---

## 功能列表

> **说明**：每个区块的功能点，供页面生成使用

- **区块: Hero 首屏 (`#hero`)**
  - **页面目标**: 第一眼建立品牌认知，传递核心口号，吸引用户继续浏览
  - **功能点**:
    - **品牌标识展示**: 左上角放置“AI+5”融合 Logo，强化星期五与 AI 的关联
    - **核心口号排版**: 突出显示“先围观，再入局”等核心标语，采用阶梯式大字重排版
    - **主视觉背景**: 使用青蓝渐变底色搭配半透明流线型抽象曲线，营造科技流动感
    - **CTA 行动按钮**: “立即围观”或“扫码入群”按钮，点击平滑滚动至 `#contact` 区块

- **区块: AI星期五是什么 (`#about`)**
  - **页面目标**: 清晰定义品牌定位，打破“专家培训”的刻板印象
  - **功能点**:
    - **一句话定义高亮**: 居中或左对齐展示品牌定义，使用引用块或高亮背景强调
    - **定位对比说明**: 采用“不是…而是…”的对比排版，突出“小白探索+真实公开过程”
    - **活动时间地点**: 醒目展示“每周五下午4点 | 杭州滨江·中恒世纪”
    - **视觉辅助**: 配合沙龙现场氛围图或简约插画，增强真实感

- **区块: 我们做什么 (`#services`)**
  - **页面目标**: 清晰呈现5类服务价值，让用户快速了解参与收益
  - **功能点**:
    - **服务卡片网格**: 采用 2x3 或响应式网格布局展示5项服务，保持视觉整齐
    - **图标/数字标识**: 每项服务搭配对应图标或序号，提升可读性
    - **内容摘要展示**: 卡片内展示服务标题与简短说明（如“真实试错复盘”、“数字资产指导”等）
    - **Hover 交互反馈**: 鼠标悬停时卡片轻微上浮或边框高亮，增强科技感交互

- **区块: 超级金句墙 (`#quotes`)**
  - **页面目标**: 集中传递品牌精神，强化情感共鸣
  - **功能点**:
    - **金句大字报排版**: 3条金句采用超大字号、粗体无衬线字体，错落有致排布
    - **撞色背景衬托**: 使用黄蓝撞色几何色块或渐变背景，突出文字视觉冲击力
    - **引用样式设计**: 添加引号装饰或作者/场景标注，增强语录感
    - **移动端自适应**: 在小屏幕下自动切换为垂直堆叠布局，保证字号可读性

- **区块: 先围观，再入局 (`#philosophy`)**
  - **页面目标**: 降低参与门槛，解释“围观”的价值与必要性
  - **功能点**:
    - **理念图文阐述**: 左侧文字说明（为什么可以慢慢学但不能不在场），右侧配图
    - **分点优势罗列**: 列出“零压力旁听”、“真实案例拆解”、“无推销纯交流”等核心优势
    - **引导性排版**: 使用箭头或进度条视觉元素，暗示“围观→了解→入局”的路径
    - **行动提示**: 底部附带“点击了解往期内容”链接，跳转至 `#review`

- **区块: 往期回顾 (`#review`)**
  - **页面目标**: 用真实过往内容证明沙龙价值，建立信任
  - **功能点**:
    - **第1期内容摘要**: 展示“AI星期五第1期”主题、核心讨论点与关键结论
    - **亮点数据/反馈提取**: 提炼参与人数、讨论热度或典型用户反馈语录
    - **图文混排展示**: 结合现场照片、PPT截图或思维导图，还原真实沙龙氛围
    - **查看更多入口**: 提供“查看完整复盘”或“公众号文章链接”占位按钮

- **区块: 联系我们 (`#contact`)**
  - **页面目标**: 提供明确的转化路径，促成用户扫码或添加微信
  - **功能点**:
    - **二维码展示区域**: 预留微信群/个人微信二维码占位图，带圆角边框
    - **扫码操作指引**: 添加“长按识别”或“扫码添加小助手”等引导文案
    - **备用联系方式**: 展示邮箱、电话或企业微信链接，作为二维码失效的备选
    - **底部版权信息**: 展示“杭州中恒世纪科技实业有限公司”及备案号等基础信息

-------

# UI 设计指南

> **场景类型**: <scene_type>prototype-app</scene_type>（应用架构设计）
> **确认检查**: 本指南适用于可交互的宣传落地页/单页应用。如果产出物是静态报告或带进度的教程，请使用对应场景的模板。

> ℹ️ Section 1-2 为设计意图与决策上下文。Code agent 实现时以 Section 3 及之后的具体参数为准。

## 1. Design Archetype (设计原型)

### 1.1 内容理解
- **目标用户**: 杭州滨江及周边中小企业老板、团队负责人、对 AI 转型感兴趣的传统行业从业者。心理预期：反感“AI神话”与过度包装，渴望真实、可落地的试错经验。
- **核心目的**: 传递“真实探索、不装专家”的品牌定位，降低参与心理门槛，引导扫码入群/报名。
- **期望情绪**: 信任、接地气、科技活力、行动欲。
- **需避免的感受**: 焦虑、廉价营销感、过度技术化导致的冰冷感、信息堆砌。

### 1.2 设计语言
- **Aesthetic Direction**: 「科技纪实风」——以高对比青蓝/明黄撞色建立视觉记忆，配合流动抽象曲线营造科技氛围；排版采用大字重阶梯式层级，信息区块保持干净留白，拒绝过度装饰。
- **Visual Signature**: 
  1. 青蓝 (`#16A8EB`) 与明黄 (`#F7D038`) 几何色块碰撞
  2. `font-black` / `font-extrabold` 无衬线大字标题
  3. 半透明 SVG 流线型背景装饰（营造流动科技感）
  4. 卡片 `rounded-xl` 与金句区块 `sharp` 圆角形成对比节奏
- **Emotional Tone**: 真诚接地气 (Sincere & Grounded) + 科技活力 (Tech & Energetic)
- **Design Style**: `Bauhaus 包豪斯` (主：强撞色、几何排版、大字重) + `Rounded 圆润几何` (辅：现代卡片容器、Pill 按钮，平衡包豪斯的硬朗感)
- **Application Type**: Landing Page (SPA with anchor nav) - 决定后续布局策略为顶部固定导航 + 锚点平滑滚动 + 全宽流式内容区。

## 2. Design Principles (设计理念)
1. **去神话化，重真实**：视觉不追求“未来科幻感”，而是用清晰的排版、真实的现场留白、克制的装饰传递“我们在一线试”的诚恳。
2. **撞色即行动**：黄色仅用于核心 CTA、金句强调、视觉锚点；青蓝色作为品牌基底与交互主色。避免色彩平均分布。
3. **呼吸感排版**：大标题与正文保持 ≥ 1.5x 字号比，区块间距 ≥ `space-y-24`，让老板们能“扫读”而非“苦读”。
4. **动效服务于节奏**：滚动揭示采用短促淡入+微上移，卡片 Hover 轻微上浮。不炫技，只强化信息层级与可点击反馈。

## 3. Color System (色彩系统)

> 基于内容理解推导配色方案，确保整体协调。
> **⚠️ App 场景配色规则**：App 子场景**禁止使用**共用预设配色方案库中的 7 个方案。App 必须根据产品定位、品牌特征和目标用户自主设计完整配色体系，参考「配色基础原则」中的衍生规则从基础色推导。

**配色设计理由**：参考 VI 海报与 PPT 素材，提取「青蓝+明黄」作为品牌核心标识色。青蓝传递科技与专业信任，明黄提供活力与视觉警示（用于 CTA/金句）。背景采用极浅冷灰降低视觉疲劳，深色 Topbar 与 Hero 形成明确分区。

### 3.1 主题颜色

> **App 场景约束**：当 Application Type = App 时，`primary` 与 `accent` 必须遵循「App 场景 Primary / Accent 映射规则」及差异阈值要求，避免主色与强调色过于接近。

| 角色 | CSS 变量 | Tailwind Class | HSL 值 | 设计说明 |
|-----|---------|----------------|--------|---------|
| bg | `--background` | `bg-background` | `hsl(210 20% 98%)` | 极浅冷灰，减少视觉干扰，衬托内容容器 |
| surface | `--card` | `bg-card` | `hsl(0 0% 100%)` | 纯白卡片背景，与 bg 形成微层次 |
| text | `--foreground` | `text-foreground` | `hsl(222 47% 11%)` | 深海军蓝黑，比纯黑更柔和，保证正文对比度 ≥ 7:1 |
| textMuted | `--muted-foreground` | `text-muted-foreground` | `hsl(215 16% 47%)` | 中灰蓝，用于辅助说明、标签、次要信息 |
| primary | `--primary` | `bg-primary` | `hsl(196 80% 45%)` | 品牌青蓝，用于主按钮、链接、激活态 |
| primary-foreground | `--primary-foreground` | `text-primary-foreground` | `hsl(0 0% 100%)` | 主交互文字色，确保在青蓝背景上清晰可读 |
| accent | `--accent` | `bg-accent` | `hsl(48 90% 55%)` | 品牌明黄，用于 CTA、金句背景、Hover 反馈 |
| accent-foreground | `--accent-foreground` | `text-accent-foreground` | `hsl(222 47% 11%)` | 明黄区域文字色，深色保证对比度 ≥ 4.5:1 |
| border | `--border` | `border-border` | `hsl(214 32% 91%)` | 浅灰蓝边框，用于卡片分隔、输入框 |

> **Color Token 语义速查（供 code agent 参考）**:
> - `primary` → 主行动：按钮填充、激活态高亮、关键操作 CTA
> - `accent` → 状态反馈：Ghost/Outline 按钮 hover、DropdownMenu focus、Toggle 激活、Skeleton 占位背景
> - `muted` → 静态非交互：禁用态背景、次级说明背景、占位文字色（`text-muted-foreground`）
> - **选择原则**：用户"可以点击" → primary；交互"正在发生" → accent；内容"不可操作" → muted

### 3.2.1 Topbar 颜色（仅当使用 Topbar 导航时参考）

> **重要**：shadcn/ui 没有 Topbar 组件，**不存在** `--topbar-*`、`--header`、`--navbar-*` 等内置 CSS 变量。请勿编造这些变量名。

**正确做法**：
- Topbar 背景使用配色方案中 `header` 角色的 HSL 值，直接写入组件样式，例如 `bg-[hsl(222_47%_11%)]`；或在 CSS 中自行声明变量（如 `--topbar-bg`）后通过 Tailwind 引用
- 文字色需根据 `header` 背景明度选择 `foreground` 或 `white`/`black`，确保对比度 ≥ 4.5:1
- 当 `header` 色与 `bg`（页面背景）相同时，需为 Topbar 添加底部边框（`border-b border-border`）以区分导航区与内容区

**Topbar 实际色值**：`bg-[hsl(222_47%_11%)]`，文字 `text-white`，滚动激活态叠加 `backdrop-blur-md bg-[hsl(222_47%_11%)]/90`。

### 3.3 语义颜色（可选）

| 用途 | HSL 值 | 衍生说明 |
|-----|--------|---------|
| 成功/正向反馈 | `hsl(142 71% 45%)` | 固定语义色，用于数据上升、完成状态 |
| 警告/风险提示 | `hsl(38 92% 50%)` | 偏深橙黄，保证 4.5:1 对比度，用于试错卡点提示 |
| 错误/下降 | `hsl(0 72% 51%)` | 固定语义色，用于失败状态、负向指标 |

## 4. Typography (字体排版)
- **Heading**: `system-ui, -apple-system, "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif` + `font-extrabold` / `font-black`
- **Body**: `system-ui, -apple-system, "Noto Sans SC", "PingFang SC", sans-serif` + `font-normal` / `font-medium`
- **字体导入**: 使用系统字体栈，禁止引入 Google Fonts。确保多端渲染一致且加载零延迟。
- **层级规范**: H1 ≥ `text-4xl md:text-6xl` (Hero), H2 `text-3xl`, H3 `text-2xl`, Body `text-base md:text-lg`。标题与正文比例 ≥ 1.5x。

## 5. Global Layout Structure (全局布局结构)

### 5.1 Page Content Zones (页面区块配置)

> ⚠️ **全局统一规则**：以下参数为所有页面共享的**唯一**内容区定义。禁止按页面拆分、禁止为不同页面定义不同的 max-w。

**Standard Content Zone（全页面统一）**:
- **Maximum Width**: `max-w-6xl`（落地页需兼顾宽屏视觉冲击与阅读舒适度）
- **Padding**: `px-4 md:px-6 lg:px-8 py-16 md:py-24`（区块垂直间距充足，保持呼吸感）
- **Alignment**: `mx-auto`
- **Vertical Spacing**: 区块间 `space-y-24`，网格内 `gap-6` / `gap-8`

**宽内容溢出策略**：当页面内某个组件（如多列表格、甘特图）超出 Standard Content Zone 宽度时，在该组件外层使用 `overflow-x-auto` 实现横向滚动，禁止为此放大容器 max-w。

**Hero/Banner 区块**（如适用）:
- **Width**: `w-full`（仅背景可全宽，内部文字内容仍受 Standard Content Zone 的 max-w 约束）
- **Padding**: `0`
- **Background**: `bg-gradient-to-br from-[hsl(222_47%_11%)] to-[hsl(210_30%_15%)]` 叠加半透明青蓝/明黄流线 SVG

## 6. Visual Effects & Motion (视觉效果与动效)

- **Header/Hero 视觉方案**: Hero 区使用深蓝渐变底色，叠加 2-3 条低透明度 (`opacity-15~20`) 的抽象流线 SVG 曲线（青蓝与明黄渐变填充），营造科技流动感但不干扰文字。
- **装饰手法**: 金句墙使用明黄/青蓝几何色块 (`absolute inset-0`) 做错位背景；服务卡片使用 `border-l-4 border-primary` 左侧强调条。
- **圆角**: 按钮 `rounded-full` (Pill)，内容卡片 `rounded-xl`，金句/引用块 `rounded-none` (Sharp Bauhaus)，输入框 `rounded-lg`。
- **阴影**: 卡片默认 `shadow-sm`，Hover `shadow-lg`，Hero 文字投影 `drop-shadow-md` 增强可读性。
- **复杂背景文字处理**:
  - 渐变背景: Hero 标题使用纯白 `text-white`，辅以 `drop-shadow-lg` 确保在复杂曲线背景上对比度 ≥ 4.5:1
  - 图片背景: 预留位加 `bg-black/40` 遮罩
  - 有色背景: 明确指定 HSL 值，如明黄背景上强制使用 `text-[hsl(222_47%_11%)]`

### 6.1 动效意图

> 本节只声明动效意图（what / why），不提供实现细节（how）；禁止输出 `@keyframes` / cubic-bezier 字符串 / 完整 CSS 声明 / 具体实现技术选型。

- **整体动效风格**: 克制、流畅、以微位移与透明度变化为主，服务于“真实、不浮夸”的品牌调性。
- **页面入场**: 首屏 Hero 内容以轻微上移淡入（约 300ms），营造沉稳落地感。
- **滚动揭示**: 各 Section 随视口进入时，标题先入场，正文/卡片依次 stagger 错峰浮现（节奏从容，非快速弹跳）。
- **列表项动效 · 变更模式**: `无`（静态落地页无动态列表）
- **列表项动效 · 意图**: 无
- **对话框/弹层**: 无（落地页无 Modal 交互）
- **关键交互微动效**: 卡片 Hover 轻微上浮 (`translate-y-[-4px]`) + 阴影加深；CTA 按钮 Hover 背景色明度微调 + 光标变化；锚点点击平滑滚动（`scroll-behavior: smooth`）。

## 7. Components (组件指南)

> **必须引用 Color System 中的颜色角色**（如 `primary`、`accent`、`border`）
> 每个组件需定义 Default/Hover/Active/Focus/Disabled 状态

### Buttons
- **Primary**: 背景 `bg-primary` / 文字 `text-primary-foreground` / Hover `bg-[hsl(196_80%_40%)]` / Active `scale-[0.98]` / Focus `ring-2 ring-primary/50 ring-offset-2` / Disabled `opacity-50 cursor-not-allowed`
- **Secondary (Accent CTA)**: 背景 `bg-accent` / 文字 `text-accent-foreground` / Hover `bg-[hsl(48_90%_50%)]` / Active `scale-[0.98]` / Focus `ring-2 ring-accent/50`
- **Ghost**: 背景 透明 / 文字 `text-foreground` / Hover `bg-accent/10 text-accent-foreground`
- **Outline**: 背景 透明 / 边框 `border border-border` / 文字 `text-foreground` / Hover `bg-accent text-accent-foreground border-accent`

### Form Elements
- **输入框**: 背景 `bg-card` / 边框 `border border-border` / Focus `ring-2 ring-primary/50 border-primary` / Placeholder `text-muted-foreground`
- **文本域**: 同上，`min-h-[120px]`，`resize-y`

### Cards (服务/回顾)
- 背景 `bg-card` / 边框 `border border-border` / 圆角 `rounded-xl` / 内边距 `p-6` / 阴影 `shadow-sm` / Hover `shadow-lg translate-y-[-4px] transition-all duration-300`

### Menu / Dropdown (Topbar 移动端)
- **菜单项 Focus/Hover**: `bg-accent/10 text-accent-foreground`
- **激活态**: `text-primary font-medium`

### Skeleton
- **加载占位**: `bg-muted animate-pulse rounded-md`

### Navigation (Topbar)
- 背景 `bg-[hsl(222_47%_11%)]` / 文字 `text-white/80` / Hover `text-white` / 激活锚点 `text-accent border-b-2 border-accent` / 滚动状态 `backdrop-blur-md bg-[hsl(222_47%_11%)]/90`

## 8. Flexibility Note (灵活性说明)

> **一致性优先原则**：多页应用（MPA）中，所有页面必须使用相同的核心参数（最大宽度、容器边距、圆角、阴影等），确保整体设计语言统一。
>
> **允许的微调范围**（code agent 可自行判断）：
> - 响应式断点适配（如移动端 Hero 字号缩小、网格改为单列、Topbar 转为汉堡菜单）
> - 页面内部的局部间距（如卡片内边距 `p-5`~`p-6`）
> - 单页组件（如 Modal）的独立样式
>
> **禁止的随意变更**：
> - ❌ 不同区块使用不同的最大宽度
> - ❌ 不同区块使用不同的圆角/阴影风格
> - ❌ 不同区块使用不同的主色调（青蓝+明黄必须贯穿始终）
> - ❌ 使用 Tailwind 预设色板（如 `bg-blue-500`）替代设计系统颜色

## 9. Signature & Constraints (设计签名与禁区)

### DO (视觉签名)
1. **青黄撞色几何锚点**: 使用 `bg-[hsl(196_80%_45%)]` 与 `bg-[hsl(48_90%_55%)]` 的矩形/流线色块作为视觉分隔，强化“科技+活力”记忆点。
2. **阶梯式大字重排版**: Hero 与金句墙严格使用 `font-black` / `font-extrabold`，配合 `tracking-tight`，形成强烈视觉冲击。
3. **玻璃态固定导航**: Topbar 默认深色实底，滚动后叠加 `backdrop-blur-md` 与 `90%` 透明度，保持现代感且不遮挡内容。
4. **左侧强调线卡片**: 服务/回顾卡片统一采用 `border-l-4 border-primary`，替代传统全包围边框，提升信息扫描效率。

### DON'T (禁止做法)
> 通用约束参见「通用约束」。以下为 Prototype 特有：
- ❌ 使用紫色渐变、霓虹光效或“AI 默认蓝”等陈词滥调配色
- ❌ 在落地页添加 Sidebar、Footer 导航链接或复杂的步骤指示器
- ❌ 将金句放入圆角卡片或添加多余阴影（金句必须靠排版与色块支撑，保持 sharp 锐利感）
- ❌ 捏造往期数据、虚构参与人数或使用 `Math.random()` 生成内容，所有文案必须基于用户提供的真实素材