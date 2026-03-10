# GitHub组织配置

## 目录结构

```
.github/
├── profile/
│   └── README.md    # 组织首页介绍
├── workflows/       # GitHub Actions 工作流（可选）
└── .gitignore
```

## 说明

- `profile/README.md` - 此文件会显示在组织首页
- `workflows/` - 存放 GitHub Actions 工作流配置

## 上传到GitHub

```bash
cd /Users/chenpan/dev/source_code/chirspan/daas/new/.github

# 初始化仓库
git init
git checkout -b main
git add -A
git commit -m "Initial commit: Organization profile"

# 创建组织仓库并推送
gh repo create healthcaredaas/.github --public --source=. --remote=origin --push
```