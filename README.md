# 网站内容编辑说明

## 📝 如何编辑网站内容

现在您可以通过编辑 `config.js` 文件来修改网站内容，无需修改 HTML 代码！

## 🎯 编辑步骤

### 1. 打开配置文件
编辑 `config.js` 文件，所有可配置的内容都在这里。

### 2. 修改基本信息
在 `siteInfo` 部分修改网站基本信息：

```javascript
siteInfo: {
  title: "您的网站标题",              // 修改网站标题
  language: "zh-CN"                  // 修改语言设置
}
```

### 3. 修改个人信息
在 `dayMode` 和 `nightMode` 部分修改您的个人信息：

```javascript
dayMode: {
  name: "您的姓名 / 学业形态",           // 修改姓名
  nickname: "您的昵称",                 // 修改昵称
  tagline: "您的个人简介",              // 修改简介
  avatar: "./您的头像图片.jpg",         // 修改头像路径
  // ... 其他内容
}
```

### 4. 修改自定义链接（可选项）
在 `customLinks` 数组中修改您的社交媒体链接：

```javascript
customLinks: [
  { text: "GitHub", url: "https://github.com/您的用户名" },
  { text: "知乎", url: "https://zhihu.com/people/您的用户名" },
  { text: "微博", url: "https://weibo.com/您的用户名" },
  { text: "B站", url: "https://space.bilibili.com/您的用户ID" }
]
```

### 5. 修改内容模块
使用 `modules` 结构来组织内容，每个模块可以包含：

#### 5.1 分组标题 (groupTitle)
```javascript
{
  groupTitle: "教育背景",              // 添加分组标题（非必须）
  sections: [
    // 具体内容
  ]
}
```

#### 5.2 内容板块 (sections)
```javascript
sections: [
  {
    title: "板块标题",                  // 简单标题
    items: [
      "项目1",                         // 简单项目
      "项目2"
    ]
  },
  {
    title: {                           // 带右侧信息的标题
      text: "板块标题",
      right: "右侧信息（如时间、技能等）"
    },
    items: [
      "项目1",
      "项目2"
    ]
  }
]
```

#### 5.3 项目内容 (items)
项目内容支持两种格式：

**简单文本：**
```javascript
items: [
  "项目描述1",
  "项目描述2"
]
```

**带右侧信息的项目：**
```javascript
items: [
  {
    text: "项目描述",
    right: "右侧信息（如时间、技术栈等）"
  }
]
```

### 6. 修改页脚信息
在 `footer` 部分修改版权信息：

```javascript
footer: "© 2025 您的姓名"
```

### 7. 修改主题配色
在 `themes` 部分修改颜色：

```javascript
themes: {
  day: {
    grad1: '#f9e8ea',                 // 顶部渐变色
    grad2: '#ffffff',                 // 底部渐变色
    text: '#1f2937',                  // 主要文字颜色
    muted: '#6b7280',                 // 次要文字颜色
    card: '#ffffff',                  // 卡片背景色
    accent: '#ef4444'                 // 强调色
  },
  night: {
    grad1: '#e8f0fb',                 // 夜间模式顶部渐变色
    grad2: '#ffffff',                 // 夜间模式底部渐变色
    text: '#1f2735',                  // 夜间模式主要文字颜色
    muted: '#5b6472',                 // 夜间模式次要文字颜色
    card: '#ffffff',                  // 夜间模式卡片背景色
    accent: '#3b82f6'                 // 夜间模式强调色
  }
}
```

## 🔧 常用修改示例

### 添加带分组的内容模块
```javascript
{
  groupTitle: "工作经历",
  sections: [
    {
      title: {
        text: "公司名称",
        right: "2020-2024"
      },
      items: [
        {
          text: "职位描述",
          right: "使用的技术"
        },
        "项目成果1",
        "项目成果2"
      ]
    }
  ]
}
```

### 修改头像
```javascript
avatar: "./my_avatar.jpg"  // 确保图片文件存在
```


## ⚠️ 注意事项

1. **保存文件**：修改后记得保存 `config.js` 文件
2. **图片路径**：确保头像图片文件存在于正确路径
3. **语法正确**：保持 JavaScript 语法正确，特别是逗号、引号和括号
4. **刷新页面**：修改后刷新浏览器页面查看效果


## 🎨 自定义建议

- **颜色搭配**：可以使用在线配色工具选择和谐的颜色
- **内容组织**：使用 `groupTitle` 对相关内容进行分组，让页面更有层次
- **个性化**：添加您的兴趣爱好、技能特长、项目经验等
- **链接管理**：保持社交媒体链接的更新，让访客能够找到您

## 📁 文件结构

```
Personal-homepage-template/
├── index.html          # 主页面（无需修改）
├── config.js           # 配置文件（在这里编辑内容）
├── avatar_study.jpg    # 形态头像1
└── avatar_inner.jpg    # 形态头像2
```

## 🔄 配置结构总结

完整的配置结构包括：
- `siteInfo`: 网站基本信息
- `dayMode`/`nightMode`: 两种形态的配置
  - `name`: 姓名
  - `nickname`: 昵称
  - `tagline`: 个人简介
  - `avatar`: 头像
  - `customLinks`: 自定义链接
  - `modules`: 内容模块（包含 `groupTitle` 和 `sections`）
  - `footer`: 页脚信息
- `themes`: 主题配色

现在您只需要编辑 `config.js` 文件，网站内容就会自动更新！🎉
