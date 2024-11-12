
---

# LINE Bot Webhook Application

這是一個使用 Flask 框架開發的 LINE Bot webhook 程式，用於處理來自 LINE 的訊息事件並回應用戶訊息。

## 功能概述

此應用程式具備以下功能：
- 接收 LINE Bot 的 webhook 回調，並處理文字訊息事件。
- 根據接收到的訊息內容，自動生成回應訊息。

## 安裝步驟

1. **安裝相依套件**

    請確保已經安裝 Python，然後使用以下指令安裝所需的套件：
    ```bash
    pip install flask line-bot-sdk
    ```

2. **設置環境變數**

    在程式碼中的 `Configuration(access_token='')` 和 `WebhookHandler('')` 中填入您的 LINE Bot 頻道訪問權杖和頻道密鑰。

3. **執行應用程式**

    啟動 Flask 應用程式：
    ```bash
    python app.py
    ```

4. **使用 ngrok 進行測試**

    若您在本地端測試，需要使用 ngrok 來建立安全的 URL：
    ```bash
    ngrok http 5000
    ```

    然後將 ngrok 提供的 https 網址設定為您的 LINE Bot Webhook URL。

## 使用 ngrok 的好處

ngrok 提供一個方便的方式來公開本地服務器。特別適合測試 LINE Bot 或其他需要 webhook 支援的應用程式，無需將程式碼部署到伺服器即可立即進行調試。

## 注意事項

- 請確保您的頻道訪問權杖和密鑰保密，避免洩露。
- ngrok 提供的連接每次重新啟動後網址會改變，需要重新設定 LINE Bot 的 Webhook URL。



---
