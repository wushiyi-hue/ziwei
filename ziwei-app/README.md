# 紫微斗数命盘推算

基于紫微斗数三层叠加模型，输入生辰推算流年运势。

## 部署到 Vercel（5分钟完成）

### 第一步：上传到 GitHub

1. 打开 [github.com](https://github.com) 并登录（没有账号就注册一个）
2. 点击右上角 **+** → **New repository**
3. 仓库名填 `ziwei-app`，选 **Public**，点 **Create repository**
4. 把这个项目文件夹里的所有文件上传上去（拖拽即可）

### 第二步：部署到 Vercel

1. 打开 [vercel.com](https://vercel.com) 并用 GitHub 账号登录
2. 点击 **Add New → Project**
3. 找到你刚创建的 `ziwei-app` 仓库，点 **Import**
4. **Framework Preset** 选 **Other**
5. **Root Directory** 填 `public`（重要！）
6. 点击 **Environment Variables**，添加一条：
   - Key: `ANTHROPIC_API_KEY`
   - Value: 你的 Anthropic API Key（去 console.anthropic.com 获取）
7. 点击 **Deploy**

### 第三步：获取链接

部署完成后，Vercel 会给你一个链接，类似：
`https://ziwei-app-xxx.vercel.app`

把这个链接分享给任何人，他们直接打开就能用。

---

## 项目结构

```
ziwei-app/
├── public/
│   └── index.html      # 前端页面
├── api/
│   └── chat.js         # 后端接口（保护 API Key）
├── vercel.json         # Vercel 配置
└── README.md
```

## 注意事项

- API Key 只存在 Vercel 环境变量里，用户看不到
- 每次推算会消耗约 0.01–0.02 美元的 API 费用
- 建议在 Anthropic 控制台设置月度消费上限，防止超额
