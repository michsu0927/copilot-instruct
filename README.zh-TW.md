# copilot-instruct

[English](./README.md) | [繁體中文](./README.zh-TW.md)

這是一個用來整理 GitHub Copilot customization 檔案的 starter repository，提供一套清楚、可重用、便於團隊維護的目錄結構。

本 repo 示範如何組合使用：

- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/instructions/*.instructions.md`
- `.github/prompts/*.prompt.md`

它適合作為團隊建立 Copilot customization 規範時的起點，避免依賴未明確官方化的角色檔案慣例。

## 這個 repository 適合用來做什麼

如果你希望為團隊建立一套較有結構的 Copilot 使用方式，可以用這個 repo 作為起點，用來：

- 定義 repository-wide 的 agent 工作守則
- 建立全域 Copilot 指令
- 依檔案類型或資料夾範圍套用 scoped instructions
- 建立可重用的 prompt 入口
- 文件化團隊自己的 customization 規範

## 這個 repository 不是什麼

這個 repo：

- 不是 GitHub 官方文件鏡像
- 不保證所有 Copilot 功能在所有 IDE 中行為完全一致
- 不能取代你去查閱最新 GitHub 官方文件
- 不是以 `.github/agents/*.md` 作為官方標準前提建立的範例

## Repository 結構

```text
AGENTS.md
.github/
├── copilot-instructions.md
├── instructions/
│   ├── rust.instructions.md
│   ├── src.instructions.md
│   └── deps.instructions.md
└── prompts/
    ├── plan-change.prompt.md
    ├── implement-wrapper-change.prompt.md
    ├── review-change.prompt.md
    └── create-tests.prompt.md
docs/
└── copilot-customization-guide.md
```

## 建議工作流程

這個 repo 採用的是 prompt-based workflow，建議流程如下：

1. `/plan-change`
   - 先定義需求目標
   - 找出可能會影響的檔案
   - 規劃最小且乾淨的做法

2. `/implement-wrapper-change`
   - 實作需要的變更
   - 說明實際修改了哪些內容

3. `/review-change`
   - 檢查結構、正確性、一致性
   - 檢查是否有不精確或誤導性的描述

4. `/create-tests`
   - 補充驗證方式
   - 補充使用說明或範例檢查點

## 如何把這個範本套用到自己的專案

1. 先改寫 `AGENTS.md`，讓它符合你的 repo 工作方式
2. 改寫 `.github/copilot-instructions.md`，放入全域規範
3. 依你的專案結構，替換 `.github/instructions/*.instructions.md`
4. 依你的團隊流程，替換 `.github/prompts/*.prompt.md`
5. 更新文件，清楚說明哪些是官方支援、哪些是團隊慣例

## 建議後續優化

如果你打算把這個 repo 作為公開範本分享，建議再進一步：

- 調整 instruction 檔名，讓檔名與內容更一致
- 調整部分 prompt 名稱，避免殘留其他專案語境
- 在 GitHub repo 補上 description 與 topics
- 定期比對 GitHub 官方文件，避免內容過時

## 相關文件

可參考：

- `docs/copilot-customization-guide.md`
- `AGENTS.md`
- `.github/copilot-instructions.md`
