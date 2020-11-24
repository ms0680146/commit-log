# commit-log
替專案導入 Commit Log 規範，讓我們更好追蹤程式碼

# 範例
```
{type}: {subject}

{description}
{issue reference}
```
* 第 1 行：Commit類型，主旨
* 第 2 行：空白
* 第 3~N 行：說明
* 最後一行：issue number
* 精神：
    * 讓三個月後的自己知道這個commit的
        * 種類
        * 在解決什麼問題
        * 怎麼解決的
    * 讓git log像是程式的日記一樣


# 規格
## Commit類型
* feat: 新增/修改功能 (feature)。
* fix: 修補 bug (bug fix)。
* docs: 文件 (documentation)，像是README.MD/修改註解/移除console.log。
* style: 格式 (不影響程式碼運行的變動 white-space, formatting, missing semi colons, etc) 或文案調整。
* refactor: 重構 (既不是新增功能，也不是修補 bug 的程式碼變動)。
* perf: 改善效能。
* test: 增加/修改測試。
* chore: 建構程序或輔助工具的變動。
* revert: 撤銷回覆先前的 commit 例如：revert: type(scope): subject (回覆版本：xxxx)。

## 主旨
* 一句話說明你做了什麼
* 在50字以內

## 說明
* 簡介一下為什麼要做這件事、你怎麼解決的。
* 盡可能在100字以內

## Issue Number
* 當你的commit是針對某個issue作的，要加上issue number
* 格式：`Ref: {Project Name Chain}#{number}`

## 範例
```
feat: Backend_Alert Email 內夾帶 PDF

1. AlertController 新增夾帶PDF.
2. 新增PdfService, 用於產生PDF及儲存於storage.
3. AlertSurvey Mail 新增attach附檔.
4. 修改SurveyResult blade PDF內容.

Ref: PM_XXXX#9527
```

```
fix: meta api 新增 reporting key

1. PM先將config檔打importJson api，寫進sn_mapping table.
2. 修改meta api，多新增reporting key.

Ref: PM_Voice2020_reporting#227
```

## 參考資料
[Git Commit Message 這樣寫會更好，替專案引入規範與範例](https://wadehuanglearning.blogspot.com/2019/05/commit-commit-commit-why-what-commit.html?m=1)
