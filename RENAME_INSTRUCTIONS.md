# 仓库重命名说明

要将仓库从 `hxtmoldbot` 重命名为 `hxtskills`，您需要在GitHub网站上执行以下步骤：

## 在GitHub网站上重命名仓库：

1. 访问仓库页面：https://github.com/zjsailor/hxtmoldbot
2. 点击 "Settings" 标签页（在仓库页面的右侧）
3. 向下滚动到 "Danger Zone" 部分
4. 在 "Repository name" 字段中，将 "hxtmoldbot" 更改为 "hxtskills"
5. 点击 "Rename" 按钮

## 重命名后的本地配置更新：

仓库重命名后，您需要更新本地仓库的远程URL：

```bash
git remote set-url origin https://github.com/zjsailor/hxtskills.git
```

或者使用SSH方式：

```bash
git remote set-url origin git@github.com:zjsailor/hxtskills.git
```

## 重要提示：

- 重命名后，旧的仓库URL将重定向到新URL，但建议尽快更新所有引用
- 如果有其他协作者，请通知他们更新他们的本地仓库远程URL
- 任何使用此仓库URL的服务或脚本也需要相应更新