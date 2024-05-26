# 學習歷程總結工具

歡迎使用學習歷程總結工具！這個工具使用了 Google Cloud Vision API 和 OpenAI 的 GPT-3.5-Turbo 模型，可以從圖片中提取文本並生成學習歷程的摘要。

## 如何使用

1. 安裝必要的 Python 套件：

    ```bash
    !pip install pillow pytesseract tk
    !pip install openai==0.28
    !pip install google-cloud-vision
    ```

2. 在 `main.py` 文件中設置 OpenAI API 密鑰和 Google Cloud Vision API 服務賬戶密鑰文件路徑。

3. 上傳要處理的圖片文件，工具會自動提取文本並生成學習歷程的摘要。

4. 摘要將以中文文字返回，並且可以根據提取的文本自動調整長度。

## 文件結構

- `main.py`: 包含主要的程式碼，用於上傳、提取文本和生成摘要。
- `primeval-shadow-424504-f0-65ca56cd6716.json`: Google Cloud Vision API 服務賬戶密鑰文件。
- `README.md`: 這個文件，提供了使用說明和相關信息。

## 依賴套件

- `pillow`: Python Imaging Library，用於圖片處理。
- `pytesseract`: 用於 OCR 文字識別。
- `tk`: Python 的圖形使用者介面工具包。
- `openai==0.28`: OpenAI Python 套件，用於使用 GPT-3 模型。
- `google-cloud-vision`: Google Cloud Vision API Python 客戶端套件。

## 注意事項

- 請確保你的 Google Cloud Vision API 服務賬戶密鑰文件有效並設置正確的路徑。
- 目前此工具設計為在 Google Colab 上運行，如果在其他環境中運行，請注意可能需要進行相應的修改。
