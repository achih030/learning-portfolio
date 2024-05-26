# 學習歷程總結工具

歡迎使用學習歷程總結工具！這個工具可以從圖片中提取文本，並使用OPEN AI模型對提取的文本進行總結，讓您輕鬆地總結學習歷程或其他文字內容。

## 如何使用

1. **安裝必要的套件**：

    開啟終端，執行以下指令以安裝所需的Python套件：

    ```bash
    !pip install openai==0.28
    !pip install google-cloud-vision
    ```

2. **設定API金鑰**：

   - 設定OpenAI API金鑰：將 `open_api_key` 替換為您的OpenAI API金鑰。
   - 設定Google Cloud Vision API服務帳戶密钥文件路径：將 `google_cloud.json` 替換為您的Google Cloud Vision API服務帳戶密钥文件的路徑。

3. **執行主程式**：

   在主程式的最後部分，執行以下指令：

    ```python
    if __name__ == "__main__":
        file_paths = upload_files()
        if not file_paths:
            print("未上傳任何文件。")
        else:
            print(f"已上傳{len(file_paths)}個文件。")
            print("正在提取文本...")
            extracted_texts = extract_texts_from_files(file_paths)
            print("正在總結學習歷程...")
            summary = summarize_texts(extracted_texts)
            print("\n學習歷程總結：")
            print(summary)
            print("正在刪除已上傳的文件...")
            delete_files(file_paths)
    ```

## 功能

- **文件上傳**：用戶可以通過文件上傳功能將要處理的圖片文件上傳到工具中。
- **文本提取**：工具會從上傳的圖片文件中提取文本信息。
- **學習歷程總結**：提取的文本將被送至OpenAI的GPT-3.5模型進行總結，生成一段大約500至1000個中文字的流暢的學習歷程與心得。
- **文件刪除**：總結完成後，上傳的文件將被自動刪除，保證用戶隱私安全。

## 注意事項

- 目前僅支持PNG、JPG和JPEG格式的圖片文件。

## 依賴套件

- [OpenAI](https://pypi.org/project/openai/)：OpenAI的GPT-3模型。
- [google-cloud-vision](https://pypi.org/project/google-cloud-vision/)：Google Cloud Vision API。

