# LifeMate AI

## 專案介紹

LifeMate AI 是一個以 AI Agent 為核心的日常生活智慧助理。

本專案希望透過大型語言模型、工具與工作流程，協助使用者處理日常生活中常見的問題，例如行程規劃、天氣與外出建議、生活資訊查詢、學習安排以及待辦事項規劃等。

與一般聊天機器人不同，LifeMate AI 不只是回答問題，而是希望能根據使用者的需求判斷應採取的處理方式，並在需要時使用不同的工具取得資訊，最後整合成適合使用者的建議。

## 使用場景

1. 行程與時間規劃
2. 天氣與外出建議
3. 日常生活問題
4. 學習與待辦事項安排
5. 資訊搜尋與整理

## 未來功能

- 建立日常生活知識庫
- 串接天氣查詢工具
- 加入網路搜尋功能
- 建立不同生活情境的 Workflow
- 加入個人化偏好與記憶功能

## 使用技術與工具

- Coze
- AI Agent
- Large Language Model (LLM)
- Knowledge Base
- Workflow
- Git
- GitHub
- Markdown

## 實作進度

目前已完成 LifeMate AI Agent 的初步建置。

### 已完成功能

- 建立 LifeMate AI Agent
- 設定 Persona 與 Prompt
- 使用繁體中文回答使用者
- 協助處理日常生活問題
- 協助進行時間與任務規劃
- 測試 Agent 對即時資訊的處理方式

### Tool Calling 實驗

在測試中，我詢問 LifeMate：

> 明天台北的降雨機率是多少？我下午要出門，需要帶雨傘嗎？

由於第一版 LifeMate 尚未加入即時天氣查詢工具，因此 Agent 能夠辨識自己無法取得即時天氣資料，而沒有直接產生未經確認的降雨資訊。

下一階段預計加入 Coze Weather Plugin，透過 geocoding 將城市名稱轉換為經緯度，再使用 forecast Tool 查詢未來天氣，使 Agent 能根據即時資料提供外出建議。

## Agent 架構

目前：

User → LifeMate → LLM + Prompt → Response

未來規劃：

User → LifeMate → LLM → Tool → External Data → LLM → Response
