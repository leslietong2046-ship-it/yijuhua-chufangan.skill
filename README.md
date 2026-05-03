# 一句话出方案

> **你有没有花3小时憋一个方案框架，最后发现方向全错？**
> 
> 别慌，现在你只需要说一句话，我来帮你搞定完整方案文档。

---

## 🆕 v2. 重大升级：从框架变工具

**升级前**：5步思考框架 → **升级后**：一句话进，完整方案文档出

- 加了输出协议 → 方案结构标准化
- 加了直接输出模式 → 不用引导，直接出完整方案
- 加了自动场景匹配 → 政务/商业/技术自动识别
- 加了Python方案生成器CLI → `demo.py` 可离线生成方案

---

## 功能特性

- **一句话输入**：只需描述你的需求，如"建设智慧城市平台"
- **智能场景识别**：自动识别政务/商业/技术场景
- **模板自动匹配**：根据场景选择最合适的方案模板
- **完整方案输出**：生成可直接使用的Markdown方案文档

---

## 快速开始

### Coze Skill 使用
```markdown
激活后，直接说需求，如"建设智慧城市平台"
```

### CLI 方案生成器（新增！）
```bash
# 安装依赖
pip install -r requirements.txt

# 基本用法
python demo.py "建设智慧城市平台"

# 保存到文件
python demo.py "新产品上市方案" --output ./方案.md

# 指定场景
python demo.py "电商系统升级" --scenario tech

# 预览模式
python demo.py "技术架构升级" --preview

# 查看帮助
python demo.py --help
```

---

## CLI 使用示例

```bash
$ python demo.py "智慧政务平台"

 场景识别：政务场景 (gov.md)
 正在生成方案...
 方案已生成！

# 【智慧政务平台建设方案】

## 一、背景
（基于政务场景自动填充...）
...
```

---

## 项目结构

```
一句话出方案/
├── SKILL.md # Coze Skill 定义（输出协议+直接输出模式）
├── demo.py # Python 方案生成器 CLI（828行）
├── requirements.txt # 依赖列表
├── README.md # 本文件
└── templates/ # 方案模板
 ├── gov.md # 政务方案模板（65行）
 ├── biz.md # 商业方案模板（89行）
 └── tech.md # 技术方案模板（118行）
```

---

## 场景自动识别

| 关键词示例 | 识别场景 | 生成模板 |
|-----------|---------|---------|
| 政务、服务大厅、街道、局委办、智慧城市 | 政务 | gov.md |
| 营销、推广、运营、上市、商业化、市场 | 商业 | biz.md |
| 系统、平台、架构、技术、API、中台、数据 | 技术 | tech.md |

---

## 模板定制

### 修改模板

编辑 `templates/` 目录下的模板文件，使用 `{{变量名}}` 占位符：

```markdown
# 【{{title}}智慧城市平台建设方案】

## 一、背景
{{background_content}}
```

### 变量说明

| 变量 | 说明 | 示例 |
|-----|------|------|
| `{{title}}` | 方案标题 | 智慧城市平台 |
| `{{area}}` | 区域名称 | XX区 |
| `{{year}}` | 目标年份 | 227 |
| `{{total_budget}}` | 总预算 | 12 |
| ... | ... | ... |

---

## 输出协议

Agent 执行时必须遵循以下输出格式：

```markdown
# 【方案标题】

## 一、背景
（2-3句话：为什么现在要做这事）

## 二、目标
（量化指标：到XX年，XX从X%提升至X%）

## 三、举措
### （一）[举措名称]
- **动作**：[具体做什么]
- **对象**：[面向谁]
- **效果**：[预期成果]

## 四、保障
- **组织**：谁来牵头
- **资金**：预算多少
- **考核**：如何评估

## 五、预期成效
- **直接成效**：可量化的指标
- **间接效益**：长期价值
```

---

## 使用口诀

> **"一句话进，自动识别场景，完整方案出来"**

---

## ⭐ 给我Star

开源不易，如果对你有用：
[![Star](https://img.shields.io/github/stars/leslietong246-ship-it/yijuhua-chufangan.skill?style=social)](https://github.com/leslietong246-ship-it/yijuhua-chufangan.skill)

---

## 更多资源

- [虾评Skill详情](https://xiaping.coze.site/skill/a632ef-85-4475-9c4c-3c138af8d6?ref=8fa389-2274-441a-ac3-b2bd9aabf8c)
- [GitHub开源](https://github.com/leslietong246-ship-it/yijuhua-chufangan.skill)

---

## Changelog

### v2. (224-5-2)
- 加了输出协议（方案结构标准化）
- 加了直接输出模式（不用引导，直接出方案）
- 加了自动场景匹配（政务/商业/技术）
- 加了 `demo.py` Python方案生成器CLI
- 加了3个场景模板（gov.md/biz.md/tech.md）

### v1. (224-4-1)
- 初始版本
- 5步思考框架

---

> 由 [一句话出方案] Skill 生成器 v2.. 提供支持

## Install

```bash
# Clone and copy to your OpenClaw skills directory
git clone https://github.com/leslietong2046-ship-it/yijuhua-chufangan.skill.git
cp -r yijuhua-chufangan.skill ~/.openclaw/skills/

# Or just paste the repo URL in your OpenClaw chat
```

## More Skills

- [kaiqiao](https://github.com/leslietong2046-ship-it/kaiqiao.skill) - Agent什么时候该问/该拦/该闭嘴干
- [一句话出方案](https://github.com/leslietong2046-ship-it/yijuhua-chufangan.skill) - 一句话输入5步出完整方案
- [锐评](https://github.com/leslietong2046-ship-it/ruiping.skill) - 追观点不追热点
- [奇门遁甲](https://github.com/leslietong2046-ship-it/qimen-dunjia.skill) - 一句话直断九宫排盘
- [黄大仙灵签](https://github.com/leslietong2046-ship-it/huangdaxian-lingqian.skill) - 抽签解签心诚则灵

