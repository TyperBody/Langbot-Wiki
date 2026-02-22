# [LangBot](https://github.com/langbot-app/LangBot) 官方文档

> 此仓库是 LangBot 的文档仓库，代码仓库：  
> [LangBot 代码仓库](https://github.com/langbot-app/LangBot)  
> 这是 LangBot 4.0 的文档，3.0 文档请见 `v3` 分支

## 参与编写

文档基于 [Mintlify](https://mintlify.com/) 生成，本地编写需要安装 Node.js。

Clone 本仓库，在目录下执行以下命令安装依赖：

```bash
npm install
```

完成后即可修改文档，修改完后使用以下命令本地启动预览：

```bash
npm run dev
```
或者直接使用 `mintlify` CLI (推荐)：
```bash
npx mintlify dev
```

### 使用图片

把图片放到 `images` 目录下，然后在文档中使用绝对路径引用（相对于项目根目录），如：

```markdown
![image](/images/xxx.png)
```

### 部署细节

现已迁移至 Mintlify 托管，提交至 `main` 分支后自动触发部署。

### 一些规范化标准

- 文件夹和文件的命名：**一律使用全小写，单词直接`-`隔开，如**`plugin-intro.mdx`
- 子文件（夹）的命名，**不加前缀**（即文件夹的名称），如：`deploy`文件夹下的，文件夹`langbot`，`langbot`文件夹下的`manual`文件称之为`manual.mdx`
- 文档文件格式统一使用 `.mdx` 以支持 Mintlify 组件。
- 在 `docs.json` 中配置侧边栏导航结构。

---

**[English README](README_EN.md)**
