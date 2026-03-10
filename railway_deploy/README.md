# 🚂 TAPD监控仪表盘 - Railway部署方案

## 🎯 一键部署到 Railway

### **方法1：GitHub导入（推荐）**
1. 访问 [Railway.app](https://railway.app)
2. 点击 "New Project"
3. 选择 "Deploy from GitHub repo"
4. 粘贴GitHub仓库URL 或 选择 "Deploy from GitHub template"
5. Railway自动部署，等待2-3分钟

### **方法2：快速启动（无需GitHub）**
```bash
# 安装Railway CLI
npm i -g @railway/cli

# 登录
railway login

# 创建项目
railway init

# 部署当前目录
railway up
```

### **方法3：网页上传**
1. 访问 https://railway.app/new
2. 选择 "Deploy from code" → "Public Git URL" 或直接上传ZIP
3. 或使用: `Deploy on Railway` 按钮

## 📁 文件结构
```
railway_deploy/
├── app.py              # 主应用
├── requirements.txt    # Python依赖
├── railway.json        # Railway配置
├── README.md          # 本文件
└── templates/         # HTML模板
    └── index.html     # 仪表盘页面
```

## ⚡ Railway优势
- **一键部署** - 2分钟完成
- **全球网络** - 自动选择最佳节点
- **自动SSL** - 免费HTTPS证书
- **数据库集成** - 可轻松添加数据库
- **完全免费** - 足够个人使用
- **自动扩展** - 根据流量调整

## 🔗 部署后地址
成功部署后，获得：
- **主页面**: `https://tapd-dashboard.up.railway.app`
- **API接口**: `https://tapd-dashboard.up.railway.app/api/data`
- **健康检查**: `https://tapd-dashboard.up.railway.app/api/health`

## 📊 功能特性
- ✅ 实时缺陷监控
- ✅ 动态数据更新
- ✅ 趋势图表分析
- ✅ 关键词提取
- ✅ 移动端适配
- ✅ 自动刷新

## 🛠️ 本地测试
```bash
# 创建虚拟环境
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 安装依赖
pip install -r requirements.txt

# 运行应用
python app.py

# 访问 http://localhost:8000
```

## 🔧 环境变量（可选）
```bash
PORT=8000
FLASK_ENV=production
TAPD_PROJECT_NAME="GR_发行活动"
TAPD_WORKSPACE_ID=70170179
```

## 🚨 故障排除
1. **部署失败** - 检查 `requirements.txt` 是否正确
2. **应用无法启动** - 查看Railway控制台的Logs
3. **访问超时** - 免费版可能进入休眠，首次访问稍等

## 📈 升级扩展
1. **添加数据库** - Railway提供PostgreSQL、MySQL、MongoDB
2. **添加域名** - Railway控制台 → Settings → Domains
3. **添加监控** - Railway控制台 → Metrics

## 📞 支持
- Railway官方文档: https://docs.railway.app
- GitHub Issues: 报告问题
- 项目维护: 持续更新

---

**🚀 立即部署**: [Railway.app](https://railway.app)
**📅 部署时间**: {{现在时间}}
**🏷️ 版本**: v1.0-railway
**🎯 状态**: 生产就绪