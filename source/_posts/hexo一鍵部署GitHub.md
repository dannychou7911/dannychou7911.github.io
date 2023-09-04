---
title: hexo一鍵部署GitHub
date: 2023-09-04 11:01:58
tags: 'hexo'
---

參考官方資料與其他部落格，整理後，測試以下步驟可以成功部署至 GitHub。

**標題**

### 步驟

1. 本地端安裝 [hexo](https://hexo.io/zh-tw/docs/setup)
2. 註冊 GitHub 帳號
3. GitHub 建立專案倉庫(repository)
4. 將本地端 hexo 專案與遠端倉庫建立連結
5. 安裝一鍵部署 GitHub 套件
6. `_config.yml` 配置部署所需的設定內容

### 安裝一鍵部署 GitHub 套件

```bash
$ npm install hexo-deployer-git --save
```

### \_config.yml 配置部署內容

```yml
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
    type: git
    repo: https://github.com/<:username>/<:username>.github.io.git
    ## https://github.com/dannychou7911/dannychou7911.github.io.git
    branch: gh-pages ##可依據需求調整分支名稱 ex. main, master... and so on.
```

### 參考資源

1. [官方資料](https://hexo.io/zh-tw/docs/github-pages)
2. [如何使用 Hexo + GitHub Pages 架設個人網誌](https://hackmd.io/@Heidi-Liu/note-hexo-github#%E9%83%A8%E7%BD%B2%E5%88%B0-GitHub)
