```markdown
# 🔖 书签HTML转JSON转换器

一个纯前端实现的浏览器书签转换工具，可将Chrome、Firefox、Edge等浏览器导出的HTML书签文件无损转换为JSON格式。

## 📋 项目简介

这个工具解决了浏览器书签导出的HTML文件难以直接用于其他应用的问题。通过将书签转换为结构化的JSON格式，你可以：
- 轻松导入到其他书签管理工具
- 进行数据分析或备份
- 开发自己的书签管理应用
- 实现书签的迁移和同步

## 🚀 使用方法

### 在线使用
1. 访问GitHub Pages链接：[https://你的用户名.github.io/bookmark-converter/](https://你的用户名.github.io/bookmark-converter/)
2. 上传从浏览器导出的HTML书签文件
3. 点击“转换为JSON”
4. 下载或复制生成的JSON文件

### 本地使用
1. 将 `index.html` 文件下载到本地
2. 用浏览器直接打开该文件
3. 按照上述步骤操作

## 📥 如何导出浏览器书签

### Chrome / Edge
1. 打开书签管理器：`Ctrl + Shift + O`
2. 点击右上角"⋮"菜单
3. 选择"导出书签"
4. 保存HTML文件

### Firefox
1. 打开书签管理器：`Ctrl + Shift + O`
2. 点击"导入和备份"菜单
3. 选择"导出书签到HTML"
4. 保存HTML文件

### Safari
1. 点击"文件"菜单
2. 选择"导出书签"
3. 保存HTML文件

## ⚙️ 快速部署你自己的版本

想拥有专属的书签转换工具？只需2分钟，Fork本仓库即可！

### 步骤1：Fork本仓库
点击右上角的 **"Fork"** 按钮，选择你的账号，创建副本。

### 步骤2：启用GitHub Pages
1. 进入你Fork后的仓库
2. 点击 **Settings** → **Pages**
3. 在“Source”部分：
   - Branch: 选择 `main`
   - Folder: 选择 `/(root)`
   - 点击 **Save**

### 步骤3：等待部署
- GitHub会自动部署，通常1-2分钟完成
- 部署成功后，访问：`https://你的用户名.github.io/仓库名/`

### 步骤4：开始使用
- 将链接收藏或设为浏览器书签
- 随时随地转换你的书签文件！

## 📄 文件结构

```
bookmark-converter/
├── index.html          # 主程序文件（完整功能）
├── README.md           # 项目说明文档
└── bookmarks.html      # 示例书签文件（可选）
```

## 🔧 自定义配置

### 修改默认选项
编辑 `index.html` 中的以下代码，可以修改默认勾选状态：

```javascript
// 在initEventListeners方法中修改
document.getElementById('includeMetadata').checked = true;    // true/false
document.getElementById('preserveStructure').checked = true;  // true/false
document.getElementById('includeIcons').checked = true;       // true/false
```

### 修改输出文件名
在 `downloadJson` 方法中修改：

```javascript
a.download = `bookmarks_${new Date().getTime()}.json`;  // 自定义文件名
```

## ⚠️ 注意事项

1. **文件大小限制**：建议处理10MB以内的书签文件
2. **编码格式**：确保HTML文件为UTF-8编码
3. **隐私保护**：所有处理在本地完成，无需担心数据泄露
4. **浏览器安全**：部分浏览器可能限制本地文件的某些功能

## 🐛 常见问题

**Q: 转换后的JSON文件太大？**
A: 取消勾选"包含网站图标数据"选项，图标数据通常占文件大部分体积

**Q: 书签结构显示不正确？**
A: 检查原始HTML文件是否完整，某些浏览器导出的格式可能略有差异

**Q: 可以批量转换吗？**
A: 当前版本为单次转换。

## 🔄 更新日志

### v1.0.1 (2024-12-06)
- 修复预览后无法返回结果页面的问题
- 添加"返回结果"按钮，改善用户体验
- 优化树形结构预览的交互

### v1.0.0 (2024-12-05)
- 初始版本发布
- 支持主流浏览器书签格式
- 完整保留文件夹层级结构
- 提供多种输出选项

## 💡 使用场景建议

1. **书签备份**：定期将书签转换为JSON备份
2. **数据迁移**：在不同书签管理工具间迁移
3. **数据分析**：分析书签的域名、分类等统计信息
4. **二次开发**：作为自己项目的书签处理模块

---

**如果这个项目对你有帮助，欢迎Star支持！** ⭐
