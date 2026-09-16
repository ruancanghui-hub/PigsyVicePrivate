# PigsyVicePrivate

「八戒坏习惯」公开法律与支持站点（隐私政策、用户协议、技术支持）。

主工程 [PigsyVice](https://github.com/ruancanghui-hub/PigsyVice) 通过 **git submodule** 挂载本仓库于 `docs/legal-site`。

## GitHub Pages

1. 本仓库 **Settings → Pages**
2. Source：Deploy from a branch → `main` → **`/` (root)** → Save

公开地址（启用后约 1–3 分钟生效）：

| 用途 | URL |
|------|-----|
| 首页 | https://ruancanghui-hub.github.io/PigsyVicePrivate/ |
| 隐私政策 | https://ruancanghui-hub.github.io/PigsyVicePrivate/privacy.html |
| 用户协议 | https://ruancanghui-hub.github.io/PigsyVicePrivate/terms.html |
| 技术支持 | https://ruancanghui-hub.github.io/PigsyVicePrivate/support.html |

请将上述链接填入 App Store Connect。

## 如何从主仓库同步更新

在主仓库 `PigsyVice` 中：

```bash
# 进入子模块改页面
cd docs/legal-site
# 编辑 *.html / assets/*
git add -A && git commit -m "Update legal pages"
git push origin main

# 回到主仓库记录子模块新指针
cd ../..
git add docs/legal-site
git commit -m "Bump legal-site submodule"
git push
```

或在主仓库根目录执行：`./scripts/sync-legal-site.sh`（若已添加）。
