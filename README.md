# 114-2 巨量資料與雲端運算

## 課程資訊

| 項目 | 說明 |
|------|------|
| 課程名稱 | 巨量資料與雲端運算 |
| 學期 | 114 學年度第 2 學期 |

| 實作環境 | AWS EC2 + Docker 容器、GitHub、VS Code |

## 課程說明

本課程涵蓋 Linux 作業系統操作、虛擬化技術、Docker 容器、Git 版本控制、雲端部署與 Python 大數據分析應用等主題。透過 AWS 雲端主機提供每位同學獨立的 Linux 練習環境，搭配 GitHub 進行作業繳交與版本管理。

### 課程核心主題

**Linux 與雲端基礎**：學習 Linux 系統操作、Bash Shell 指令、使用者與權限管理，並透過 AWS EC2 雲端主機進行實作，掌握雲端運算的基本架構。

**虛擬化與容器技術**：認識傳統虛擬機器、WSL、Docker 容器三種虛擬化技術的差異與應用場景，學習使用 Dockerfile 建立自訂開發與部署環境。

**版本控制與協作開發**：使用 Git 與 GitHub 進行版本控制，學習 Fork、Pull Request 等團隊協作流程，培養業界標準的開發習慣。

**Python 大數據分析應用**：使用 Python 搭配 Pandas、NumPy 等套件進行資料清洗、轉換與統計分析。透過 Jupyter Notebook 進行互動式資料探索與視覺化，並結合 Matplotlib、Seaborn 等工具將分析結果圖表化呈現。課程後期將導入機器學習基礎概念，使用 Keras 預訓練模型體驗影像辨識與自然語言處理的實際應用，並透過 Gradio 建立 AI 互動介面進行模型部署。

## 作業繳交方式

本課程採用 **Fork + Pull Request** 流程繳交作業：

1. Fork 本 Repo 到你的 GitHub 帳號
2. 在你的 Fork 中完成每週作業
3. 發 Pull Request 回本 Repo 繳交

每週作業放在對應的資料夾中，例如 `week03/`、`week04/`。

---

## Git 基本流程

### 首次設定（只需做一次）

安裝 Git 後，設定你的姓名和 Email：

```bash
git config --global user.name "你的姓名"
git config --global user.email "你的Email"
```

### Fork + Clone（每學期做一次）

1. 在老師的 Repo 頁面右上角點選 **Fork**，將 Repo 複製到你的帳號下
2. Clone 你的 Fork 到本機：

```bash
git clone https://github.com/你的帳號/114-2-BIGDATACC.git
cd 114-2-BIGDATACC
```

### 每週作業流程

```
建立作業資料夾 → 編輯檔案 → add → commit → push → 發 PR
```

Step 1：建立當週作業資料夾並完成作業

```bash
mkdir week03
cd week03
# 建立作業檔案，完成作業內容
```

Step 2：將作業加入版本控制並推送

```bash
git add .
git commit -m "完成第3週作業"
git push origin main
```

Step 3：到 GitHub 網頁發 Pull Request

1. 進入你的 Fork 頁面
2. 點選 **Contribute** > **Open pull request**
3. 確認內容後點選 **Create pull request**
4. PR 標題格式：`學號_姓名_week03`

---

## Git 基本指令

### 版本控制基礎指令

| 指令 | 功能 | 使用範例 |
|------|------|---------|
| `git clone <url>` | 複製遠端 Repo 到本機 | `git clone https://github.com/user/repo.git` |
| `git status` | 查看目前檔案狀態 | `git status` |
| `git add <file>` | 將檔案加入暫存區 | `git add week03/q1_basic.txt` |
| `git add .` | 將所有變更加入暫存區 | `git add .` |
| `git commit -m "訊息"` | 提交變更並附上說明 | `git commit -m "完成第3週作業"` |
| `git push origin main` | 將本機提交推送到 GitHub | `git push origin main` |
| `git pull origin main` | 從 GitHub 拉取最新版本 | `git pull origin main` |
| `git log` | 查看提交歷史紀錄 | `git log --oneline` |

### Fork 與 Pull Request 指令

| 指令 | 功能 | 使用範例 |
|------|------|---------|
| Fork | 在 GitHub 網頁上操作，複製老師的 Repo 到你的帳號 | 點選 Repo 右上角 Fork 按鈕 |
| Pull Request | 在 GitHub 網頁上操作，將你的作業提交回老師的 Repo | 點選 Contribute > Open pull request |

### 常用輔助指令

| 指令 | 功能 | 使用範例 |
|------|------|---------|
| `git diff` | 查看檔案變更的內容 | `git diff` |
| `git log --oneline` | 用精簡格式查看歷史紀錄 | `git log --oneline -5` |
| `git remote -v` | 查看遠端 Repo 的連結 | `git remote -v` |
| `git branch` | 查看目前所在的分支 | `git branch` |

---

## 作業資料夾結構

```
114-2-BIGDATACC/
├── README.md
├── week03/
│   ├── q1_basic.txt
│   ├── q2_fileops.txt
│   └── q3_compare.txt
├── week04/
│   └── ...
├── week05/
│   └── ...
└── ...
```

## Linux 練習環境連線資訊

| 項目 | 主機 1 | 主機 2 |
|------|--------|--------|
| IP | 54.151.244.27 | 54.255.61.68 |
| Port | 2201 | 2202 |
| 帳號 | 依帳號分配表 | 依帳號分配表 |
| 密碼 | 依帳號分配表 | 依帳號分配表 |

連線指令範例：
```bash
ssh student101@54.151.244.27 -p 2201
```

Windows 可使用 MobaXterm、PuTTY 或 PowerShell 連線。

## 注意事項

1. 首次 SSH 連線會詢問是否信任主機，請輸入 `yes`
2. 輸入密碼時畫面不會顯示任何字元，這是正常的
3. 輸入 `exit` 即可離開 Linux 環境
4. 每週作業請在截止日前發 PR 繳交
5. PR 標題請統一格式：`學號_姓名_weekXX`
