# wendui-rules

程序员与 AI 问对的基本规则

## 名词定义

- 此规则：https://raw.githubusercontent.com/os023/wendui-rules/refs/heads/main/README.md
- SFR 开源许可证：https://raw.githubusercontent.com/os023/wendui-rules/refs/heads/main/License

## 【重要】注意事项

- 【重要】所有业务代码使用中文注释
- 【重要】所有业务代码需符合各个代码语言的最佳实践规范
- 【重要】编写 API 接口时，必须避免产生明显的信息安全问题
- 【重要】禁止将密码、密钥、加密证书等信息硬编码到代码中
- 代码注释中包含`开发者说：`的文字为开发者特别说明，是代码编写生成的重要参考
- 项目中每个源码文件的行数不超过 560 行，文件大小不超过 15KB，否则进行拆分
- 在源码编写过程中要注意工具函数的复用，避免大段重复代码
- 所有测试脚本应当编写在项目目录的 `tests/` 目录下
- 所有示例代码或示例文档应当编写在项目目录的 `examples/` 目录下

## wendui 目录

在项目目录的`wendui/`路径下，有以下文件夹，如果不存在，就创建

- `wendui/plans`文件夹用于保存本项目 AI 生成的开发计划，命名为`yyyyMMDD-HHmm-[序号]-[中文主题].plan.md`
- `wendui/todos`文件夹用于保存项目开发规划，遵循原子操作原则，命名为`yyyyMMDD-HHmm-[序号]-[中文主题].todo.md`
- `wendui/finished`文件夹用于保存处理完成的`todos`的事项，命名为`yyyyMMDD-HHmm-[序号]-[中文主题].finish.md`
- `wendui/trees`文件夹用于保存项目源码的一级或二级文件目录树结构，该目录下没有子目录
- `yyyyMMDD-HHmm`为当前日期的 js 风格格式
- 只有必要、重要的程序员与大模型问对记录才保存
- 特别注意，`000000000-目录结构.md`（九个零文件）保存项目主要目录结构，此文件保持简洁，随项目更新

## web 前端（html,ts,js,vue,react,css 等）规则

- 如果涉及 html 页面编写，风格需符合中国现代化网站的最佳实践；
- html 或前端项目的自定义 css 类，以`os023-`为前缀；

### 绝对禁止项

#### 配色禁止

- 紫色、靛蓝色、蓝紫渐变
- 纯平背景色，必须有噪点纹理或渐变
- Tailwind 默认色板

#### 布局禁止

- 三卡片布局
- 完美居中对齐
- 等宽多栏（必须不对称）

### 遵守项

#### 图片系统

- 图标：使用 Iconify 图标库
- 占位图：使用 Picsum Photos
- 真实图片：使用 Pexels 搜索
- 插画：使用 unDraw

## 文案风格

### 禁止项

- 高深的专业名词和无意义的空话
- 被动语态和长句

### 遵守项

- 口语化，像朋友聊天
- 具体化，有数字和场景
- 可以幽默、自嘲、甚至挑衅
- 每句话不超过 20 个字
- 不要瞎编，多用逗号

## 创建新的开发项目

- 如果不存在项目`License`文件，默认采用`SFR开源许可证`

## http 的 json 接口格式

若无特殊说明，api（json）接口的消息体格式为：

- 成功 { code: 200, data: any, message: string }
- 失败 { code: number, data: any, message: string }

## 数据库

如无特殊说明，数据库的表主键名称规则如下：

- 整数型主键字段名称为 rid；
- 字符串型主键字段名称为 pks，长度 64；

## `.cursorrules`文件

- `.cursorrules`中 `=====` 是比 `====` 更高一级的标题，其他格式与 markdown 一致
