# 🎬 AI视频提示词生成器

> 一个智能化的AI视频提示词工具，专为创作者设计。通过引导式提问，帮助您将脑海中的场景转化为精准的AI视频生成提示词，支持智能优化、版本对比和模板复用。

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.9+-blue)
![Vue](https://img.shields.io/badge/vue-3.0+-green)

## ✨ 核心功能

### 🎯 智能引导生成
- **多维度引导问卷**: 通过AI驱动的自适应问卷系统，逐步挖掘场景细节
  - 视觉元素（风格、光线、色彩、构图）
  - 时空设置（场景、季节、天气、时间）
  - 角色动作（人物、姿态、表情、动作）
  - 音效氛围（背景音乐、音效、节奏）
  - 情感基调（主题、情绪、节奏感）

- **智能追问算法**: 根据用户回答动态生成后续问题，避免冗余
- **场景可视化**: 实时生成场景描述和概念图
- **上下文记忆**: 保留对话历史，支持返回编辑

### 🚀 AI提示词优化
- **多层级优化**:
  - 语法规范化
  - 结构优化（按重要性排序）
  - 关键词增强
  - 质量评分

- **版本对比系统**:
  - 并排对比展示
  - 变更高亮标记
  - 详细变更说明
  - 优化建议文本解释

- **可配置优化参数**:
  - 优化强度（轻微/中等/激进）
  - 风格倾向（详细/简洁/创意）
  - 目标模型（Runway/Pika/通用）

### 💾 智能模板管理
- **自动模板提取**:
  - 完成提示词后，AI自动识别可复用片段
  - 智能分类（场景模板、风格模板、效果模板）
  - 使用频率统计

- **交互式保存**:
  - 推荐保存的模板片段
  - 创作者确认是否保存
  - 自定义模板名称和描述
  - 标签管理和分类

- **模板库功能**:
  - 模板预览和使用统计
  - 快速搜索和过滤
  - 模板评分和评论
  - 导出和分享

### 📚 创意库与版本控制
- **完整的提示词管理**:
  - 保存完整的提示词作品
  - 版本历史追踪
  - 自动生成变更日志
  - 支持回滚到任意版本

- **高级搜索**:
  - 关键词搜索
  - 标签过滤
  - 日期范围筛选
  - 模型和风格分类

- **数据分析**:
  - 创作统计（总数、日均、热门模板）
  - 优化效果分析
  - 提示词质量评分
  - 创意灵感推荐

### 🔄 工作流优化
- **快捷操作**:
  - 一键复制提示词
  - 快速应用模板
  - 批量操作
  - 快捷键支持

- **效率工具**:
  - 提示词导入导出（JSON/CSV）
  - 批量优化
  - 模板批量创建
  - API集成

## 📁 项目结构

```
ai-video-prompt-generator/
├── frontend/                          # Vue 3 前端应用
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Header.vue
│   │   │   │   ├── Sidebar.vue
│   │   │   │   └── Footer.vue
│   │   │   ├── generator/
│   │   │   │   ├── GuidedGenerator.vue         # 智能引导生成
│   │   │   │   ├── QuestionPanel.vue           # 问卷面板
│   │   │   │   ├── PromptPreview.vue           # 实时预览
│   │   │   │   └── InteractiveGuide.vue        # 交互式场景描述
│   │   │   ├── optimizer/
│   │   │   │   ├── PromptOptimizer.vue         # 优化界面
│   │   │   │   ├── PromptComparison.vue        # 并排对比展示
│   │   │   │   ├── ComparisonHighlight.vue     # 变更高亮
│   │   │   │   └── OptimizationExplainer.vue   # 优化说明
│   │   │   ├── template/
│   │   │   │   ├── TemplateExtractor.vue       # 模板自动提取
│   │   │   │   ├── TemplateSaveDialog.vue      # 保存确认
│   │   │   │   ├── TemplateLibrary.vue         # 模板库浏览
│   │   │   │   └── TemplatePreview.vue         # 模板预览
│   │   │   └── library/
│   │   │       ├── LibraryManager.vue           # 创意库管理
│   │   │       ├── VersionHistory.vue           # 版本历史
│   │   │       ├── PromptStatistics.vue         # 统计分析
│   │   │       └── SearchAndFilter.vue          # 搜索过滤
│   │   ├── pages/
│   │   │   ├── Dashboard.vue          # 仪表板
│   │   │   ├── Generator.vue          # 生成器主页
│   │   │   ├── Library.vue            # 创意库
│   │   │   ├── Templates.vue          # 模板库
│   │   │   ├── Settings.vue           # 设置
│   │   │   └── Help.vue               # 帮助
│   │   ├── stores/
│   │   │   ├── promptStore.js         # 提示词状态管理
│   │   │   ├── templateStore.js       # 模板状态管理
│   │   │   ├── userStore.js           # 用户状态管理
│   │   │   └── uiStore.js             # UI状态管理
│   │   ├── services/
│   │   │   ├── api.js                 # API客户端
│   │   │   ├── promptService.js       # 提示词服务
│   │   │   ├── templateService.js     # 模板服务
│   │   │   └── analyticsService.js    # 分析服务
│   │   ├── utils/
│   │   │   ├── formatters.js          # 格式化工具
│   │   │   ├── validators.js          # 验证工具
│   │   │   ├── diffUtils.js           # 差异对比工具
│   │   │   └── helpers.js             # 通用帮助函数
│   │   ├── App.vue
│   │   └── main.js
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   ├── tailwind.config.js
│   └── .env.example
│
├── backend/                           # Python Flask 后端
│   ├── app.py                         # 应用入口
│   ├── config.py                      # 配置管理
│   ├── requirements.txt               # Python依赖
│   ├── models/
│   │   ├── __init__.py
│   │   ├── user.py                    # 用户模型
│   │   ├── prompt.py                  # 提示词模型
│   │   ├── template.py                # 模板模型
│   │   ├── comparison.py              # 对比记录模型
│   │   └── session.py                 # 会话模型
│   ├── services/
│   │   ├── __init__.py
│   │   ├── ai_guide.py                # AI引导服务
│   │   ├── prompt_optimizer.py        # 优化服务
│   │   ├── template_extractor.py      # 模板提取服务
│   │   ├── diff_analyzer.py           # 差异分析服务
│   │   ├── analytics_service.py       # 分析服务
│   │   └── openai_service.py          # OpenAI集成
│   ├── routes/
│   │   ├── __init__.py
│   │   ├── auth.py                    # 认证路由
│   │   ├── prompts.py                 # 提示词路由
│   │   ├── templates.py               # 模板路由
│   │   ├── comparisons.py             # 对比路由
│   │   ├── guide.py                   # 引导路由
│   │   └── analytics.py               # 分析路由
│   ├── middleware/
│   │   ├── __init__.py
│   │   ├── auth_middleware.py         # 认证中间件
│   │   ├── rate_limit.py              # 限流中间件
│   │   └── error_handler.py           # 错误处理
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── validators.py              # 验证工具
│   │   ├── formatters.py              # 格式化工具
│   │   └── helpers.py                 # 帮助函数
│   └── tests/
│       ├── test_services.py
│       ├── test_routes.py
│       └── test_integration.py
│
├── database/
│   ├── schema.sql                     # 数据库架构
│   ├── init_db.py                     # 数据库初始化
│   └── migrations/
│       └── 001_initial_schema.sql
│
├── docs/
│   ├── API.md                         # API文档
│   ├── USER_GUIDE.md                  # 用户指南
│   ├── ARCHITECTURE.md                # 架构设计
│   ├── INSTALLATION.md                # 安装指南
│   └── CONTRIBUTING.md                # 贡献指南
│
├── docker/
│   ├── Dockerfile.frontend
│   ├── Dockerfile.backend
│   └── docker-compose.yml
│
├── .github/
│   └── workflows/
│       ├── ci.yml
│       └── cd.yml
│
├── .gitignore
├── .env.example
├── LICENSE
└── PROJECT_PLAN.md                    # 项目计划
```

## 🚀 快速开始

### 前置要求
- Python 3.9+
- Node.js 16+
- PostgreSQL 12+ (生产环境) 或 SQLite (开发环境)
- pip 和 npm

### 开发环境安装

#### 1. 克隆项目
```bash
git clone https://github.com/nvndfvx/ai-video-prompt-generator.git
cd ai-video-prompt-generator
```

#### 2. 后端设置
```bash
cd backend

# 创建虚拟环境
python -m venv venv
source venv/bin/activate          # Linux/Mac
# 或
venv\Scripts\activate             # Windows

# 安装依赖
pip install -r requirements.txt

# 配置环境变量
cp .env.example .env
# 编辑 .env 文件填入你的API密钥和数据库配置

# 初始化数据库
python init_db.py

# 启动后端服务
python app.py
```

后端将运行在 `http://localhost:5000`

#### 3. 前端设置
```bash
cd frontend

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

前端将运行在 `http://localhost:5173`

### Docker 快速启动
```bash
docker-compose up -d
```

## 💡 使用流程

### 第一步：创建新提示词
1. 点击「新建提示词」按钮
2. 为你的创作给个标题和简短描述
3. 选择目标AI模型（Runway/Pika/通用）

### 第二步：智能引导问卷
1. AI会根据你的选择提出精准的问题
2. 每个回答都会更新实时预览的提示词
3. 可以返回上一步调整之前的答案
4. 问卷包括5个核心维度：
   - 📐 **视觉风格** - 镜头语言、构图、光影
   - 🌍 **场景设置** - 时间、地点、天气、季节
   - 👥 **角色动作** - 人物描述、姿态、表情、动作
   - 🎵 **音效氛围** - 背景音、节奏、情感基调
   - ✨ **特效效果** - 转场、特效、字幕

### 第三步：查看优化建议
1. 完成所有问题后，点击「优化提示词"
2. 系统自动进行多层级优化：
   - 语法和结构优化
   - 关键词增强
   - 质量评分
3. 系统给出具体的优化说明

### 第四步：对比优化效果
1. 并排查看优化前后的版本
2. 变更部分用颜色高亮
3. 点击「查看详情」了解每项优化的原因
4. 可选择「接受全部」或「选择性接受"

### 第五步：模板提取与保存
1. 系统自动分析完成的提示词
2. 识别可重复使用的片段并推荐
3. 选择是否保存为模板（支持多选）
4. 为模板添加名称、描述和标签
5. 选择是否保存完整提示词到创意库

### 第六步：管理与复用
- 在「创意库」中浏览所有保存的提示词
- 在「模板库」中快速找到常用片段
- 创建新提示词时一键应用模板
- 查看使用统计和创作趋势

## 🔧 技术栈

### 前端
| 技术 | 版本 | 说明 |
|------|------|------|
| Vue | 3.3+ | 渐进式JS框架 |
| Vite | 4.0+ | 新一代构建工具 |
| Tailwind CSS | 3.0+ | 原子化CSS框架 |
| Pinia | 2.0+ | Vue状态管理 |
| Axios | 1.0+ | HTTP客户端 |
| Highlight.js | 11.0+ | 代码高亮 |

### 后端
| 技术 | 版本 | 说明 |
|------|------|------|
| Flask | 2.3+ | Web框架 |
| SQLAlchemy | 2.0+ | ORM |
| OpenAI API | 最新 | AI优化和引导 |
| Redis | 7.0+ | 缓存和会话 |
| Celery | 5.0+ | 任务队列 |
| JWT | - | 身份认证 |

### 数据库
- **SQLite**: 开发环境
- **PostgreSQL**: 生产环境

## 📊 核心数据模型

### Prompt（提示词）
```
- id: UUID
- user_id: 用户ID
- title: 标题
- description: 描述
- original_content: 原始内容
- optimized_content: 优化后内容
- target_model: 目标模型
- status: 状态（草稿/已优化/已发布）
- quality_score: 质量评分
- tags: 标签
- created_at: 创建时间
- updated_at: 更新时间
```

### Template（模板）
```
- id: UUID
- user_id: 用户ID
- category: 分类
- name: 名称
- content: 内容
- description: 描述
- usage_count: 使用次数
- tags: 标签
- created_at: 创建时间
```

### Comparison（对比记录）
```
- id: UUID
- prompt_id: 提示词ID
- original: 原始版本
- optimized: 优化版本
- changes: 变更详情
- created_at: 创建时间
```

## 🔐 认证与授权
- JWT Token认证
- 用户权限管理
- API密钥管理
- 审计日志

## 📈 性能优化
- 前端：代码分割、懒加载、CDN加速
- 后端：数据库查询优化、缓存策略、异步任务处理
- 通过Redis缓存热数据
- 使用Celery处理耗时操作

## 🌐 API 端点概览

### 认证
- `POST /api/auth/register` - 注册
- `POST /api/auth/login` - 登录
- `POST /api/auth/refresh` - 刷新令牌

### 提示词
- `POST /api/prompts` - 创建提示词
- `GET /api/prompts` - 获取列表
- `GET /api/prompts/:id` - 获取详情
- `PUT /api/prompts/:id` - 更新提示词
- `DELETE /api/prompts/:id` - 删除

### 优化
- `POST /api/optimize` - 优化提示词
- `GET /api/comparisons/:id` - 获取对比记录

### 模板
- `POST /api/templates` - 创建模板
- `GET /api/templates` - 获取模板列表
- `POST /api/extract-templates` - 自动提取模板

### 引导
- `POST /api/guide/start` - 开始引导
- `POST /api/guide/next-question` - 获取下一个问题
- `POST /api/guide/update-preview` - 更新预览

### 分析
- `GET /api/analytics/stats` - 统计数据
- `GET /api/analytics/trends` - 趋势分析

## 📝 文档
- [完整API文档](./docs/API.md)
- [用户指南](./docs/USER_GUIDE.md)
- [架构设计](./docs/ARCHITECTURE.md)
- [开发指南](./docs/CONTRIBUTING.md)

## 🎯 Roadmap

### V1.0（当前版本）
- ✅ 智能引导问卷
- ✅ AI提示词优化
- ✅ 版本对比
- ✅ 模板提取和管理
- ✅ 创意库管理

### V1.1（计划中）
- 🔄 多语言支持
- 🔄 社区提示词共享
- 🔄 提示词评分系统
- 🔄 批量优化工具

### V2.0（未来）
- 🔄 AI模型集成（直接调用生成视频）
- 🔄 视频预览功能
- 🔄 团队协作功能
- 🔄 高级分析报表
- 🔄 Mobile应用

## 💬 支持与反馈
- 📧 Email: support@example.com
- 💬 GitHub Issues: 报告问题
- 💡 Discussions: 分享想法
- 📱 社区论坛: 交流讨论

## 🤝 贡献指南

我们欢迎各种形式的贡献！包括：
- 🐛 报告Bug
- ✨ 提议新功能
- 📝 改进文档
- 🔧 提交代码

[详细贡献指南](./docs/CONTRIBUTING.md)

## 📄 许可证

MIT License - 详见 [LICENSE](./LICENSE) 文件

---

<div align="center">

**让每位创作者都能用AI创意创作出惊人的视频！** 🎬✨

[网站](https://example.com) • [文档](./docs) • [反馈](https://github.com/nvndfvx/ai-video-prompt-generator/issues) • [讨论](https://github.com/nvndfvx/ai-video-prompt-generator/discussions)

</div>