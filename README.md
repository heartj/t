
## Terminal (終端機) 的常用指令

簡單介紹 **Terminal (終端機)** 的常用指令，讓你快速上手～
(適用 macOS / Linux，如果是 Windows 也能用 PowerShell 類似概念)

---

### 🔹 1. 目前位置與導航

```bash
pwd           # 顯示目前所在目錄 (Print Working Directory)
ls            # 列出目錄下檔案 (List)
ls -l         # 詳細列表 (long format)
ls -a         # 顯示隱藏檔 (.開頭)
cd Documents  # 進入 Documents 資料夾
cd ..         # 回到上一層
cd /          # 回到根目錄
cd ~          # 回到使用者主目錄
```

---

### 🔹 2. 檔案與資料夾管理

```bash
mkdir new_folder     # 建立資料夾
touch file.txt       # 建立空檔案
cp file.txt copy.txt # 複製檔案
mv file.txt new.txt  # 移動或重新命名檔案
rm file.txt          # 刪除檔案
rm -r folder         # 刪除資料夾 (小心使用!)
```

---

### 🔹 3. 檢視檔案內容

```bash
cat file.txt     # 顯示檔案內容
less file.txt    # 分頁顯示 (用 q 離開)
head file.txt    # 顯示前10行
tail file.txt    # 顯示最後10行
tail -f file.txt # 持續監看檔案更新 (常看 log)
```

---

### 🔹 4. 系統資訊

```bash
whoami       # 顯示當前使用者
uname -a     # 顯示系統資訊
df -h        # 查看磁碟空間
du -sh *     # 查看目前目錄各檔案/資料夾大小
top          # 即時顯示系統資源使用狀況
```

---

### 🔹 5. 搜尋

```bash
find . -name "file.txt"       # 搜尋檔案
grep "keyword" file.txt       # 搜尋檔案內的文字
grep -r "keyword" /path/to/dir # 遞迴搜尋整個資料夾
```

---

### 🔹 6. 權限管理

```bash
chmod 755 file.sh    # 修改檔案權限
chown user:group file.txt  # 修改擁有者
sudo command         # 以管理員身份執行
```

---

### 🔹 7. 網路相關

```bash
ping google.com      # 測試網路連線
curl https://example.com  # 抓取網頁內容
wget https://example.com  # 下載檔案 (Linux)
```

---

### 🔹 8. 其他好用指令

```bash
history    # 顯示執行過的指令
clear      # 清空畫面
man ls     # 查看指令說明 (manual)
```

---

📌 **小結：**

* `pwd`、`ls`、`cd`：定位、移動
* `mkdir`、`touch`、`cp`、`mv`、`rm`：檔案管理
* `cat`、`less`、`head`、`tail`：檢視檔案
* `find`、`grep`：搜尋超好用
* `sudo`：用管理員權限跑指令

---

## 程式語言

### 💡 macOS 上比較容易上手的語言：

| 語言                       | 難易度 | 特點                             | 適合誰                     |
| ------------------------ | --- | ------------------------------ | ----------------------- |
| **Python**               | ⭐⭐  | 語法超簡單，資料科學、腳本、網頁開發都行           | 想快速寫小工具、學 AI、分析資料       |
| **Swift**                | ⭐⭐  | Apple 自家語言，開發 macOS、iOS App 首選 | 想開發 iPhone/iPad/Mac App |
| **Ruby**                 | ⭐⭐  | 簡單優雅，但社群活躍度略減                  | 想玩 Rails 或一些 DevOps 腳本  |
| **JavaScript (Node.js)** | ⭐⭐  | 網頁前後端通吃                        | 想做網站或網頁小工具              |
| **Shell (bash/zsh)**     | ⭐   | macOS 原生支援，用來自動化工作流程           | 想快速批量處理檔案、命令列工具         |

---

### 🔑 總結建議：

* **小工具、自動化**：建議用 **Shell** 或 **Python**
* **跨平台開發**：用 **Python**
* **App開發**：用 **Swift**
* **網頁開發**：用 **JavaScript/Node.js**

---

## Python 語法

### 🔹 1. 基本輸出與註解

```python
# 這是單行註解
print("Hello, World!")  # 印出文字
```

* `#` 開頭代表註解
* `print()` 用來輸出訊息

---

### 🔹 2. 變數與資料型別

```python
name = "Alice"     # 字串 (string)
age = 25           # 整數 (int)
height = 1.68      # 浮點數 (float)
is_student = True  # 布林值 (bool)
```

* Python 不需要事先宣告型別
* 用 `=` 指派值

---

### 🔹 3. 基本運算

```python
x = 10
y = 3
print(x + y)  # 13
print(x - y)  # 7
print(x * y)  # 30
print(x / y)  # 3.333...
print(x // y) # 3 (整數除法)
print(x % y)  # 1 (取餘數)
print(x ** y) # 1000 (次方)
```

---

### 🔹 4. 條件判斷

```python
score = 85
if score >= 90:
    print("Excellent")
elif score >= 60:
    print("Pass")
else:
    print("Fail")
```

* `if` / `elif` / `else` 控制流程
* 縮排 (4 空格) 很重要！

---

### 🔹 5. 迴圈

```python
for i in range(5):
    print(i)  # 0 1 2 3 4

count = 0
while count < 3:
    print("Hi")
    count += 1
```

---

### 🔹 6. 函式

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))
```

* 用 `def` 定義函式
* `return` 回傳結果

---

### 🔹 7. 常見資料結構

```python
# list (可變動的有序集合)
fruits = ["apple", "banana", "cherry"]

# tuple (不可變動的有序集合)
coords = (10, 20)

# dict (鍵值對)
person = {"name": "Alice", "age": 25}

# set (無序不重複集合)
numbers = {1, 2, 3, 3}
```

---

📌 **總結：**

* Python 語法簡潔、縮排重要
* 主要結構：變數、條件、迴圈、函式、資料結構
* 適合自動化腳本、資料分析、網站開發、AI 應用等

---

## Visual Studio Code (VS Code) 介紹

---

### 🔹 VS Code 是什麼？

* **開發者愛用的免費編輯器**：由 Microsoft 開發，支援 Windows、macOS、Linux。
* **多語言支援**：支援 Python、JavaScript、C++、Go、Java、Rust 等幾乎所有程式語言。
* **功能強大**：

  * 內建 Git 版本控制
  * 擴充套件（Extensions）超多，可以加強功能
  * 支援 IntelliSense 自動完成
  * Debug 工具完善
* **輕量好用**：開啟速度快，比傳統 IDE（如 PyCharm、Eclipse）更輕便。

---

### 🔹 安裝步驟

#### 🖥️ macOS 安裝

1. 打開瀏覽器，前往官方網站：[https://code.visualstudio.com](https://code.visualstudio.com)
2. 點選 **Download for macOS**，下載 `.zip` 檔。
3. 解壓縮後，把 `Visual Studio Code.app` 拖到 **應用程式資料夾**。
4. 打開 VS Code，首次開啟可能需要系統允許。
5. 建議安裝 Command Line 工具：

   * 打開 VS Code
   * `Cmd + Shift + P` → 輸入 `Shell Command: Install 'code' command in PATH` → 按下 Enter
   * 以後就可以在終端機用 `code .` 打開資料夾。

---

#### 🖥️ Windows 安裝

1. 前往 [https://code.visualstudio.com](https://code.visualstudio.com)。
2. 點 **Download for Windows**，下載 `.exe` 安裝檔。
3. 執行安裝程式：

   * 一路按「Next」
   * 建議勾選 **Add to PATH**，方便命令列啟動 VS Code。
4. 安裝完成後，從桌面或開始選單啟動。

---

#### 🐧 Linux 安裝 (以 Ubuntu 為例)

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

完成後在終端輸入 `code` 啟動 VS Code。

---

### 🔹 使用小技巧

* **安裝擴充套件**：

  * Python：程式碼補完、Debug
  * Prettier：自動格式化程式碼
  * GitLens：更好用的 Git 工具
* **快捷鍵**：

  * `Cmd/Ctrl + Shift + P`：命令面板
  * `Cmd/Ctrl + P`：快速開檔
  * `Cmd/Ctrl + Shift + O`：快速跳到函數
* **多工作區**：可以同時開啟多個資料夾，方便管理專案。


---
## Python 範例1
---

好的！這裡給你一個「完全不更動任何東西」的範例：
這段 Python 腳本只會 **列出桌面上的檔案與資料夾**，不會搬移、不會刪除，也不會修改任何檔案。

---

### 📝 Python 腳本：純列出桌面檔案

`list_desktop.py`

```python
import os

# 桌面路徑
desktop = os.path.join(os.path.expanduser("~"), "Desktop")

def list_desktop_files():
    print("📂 你的桌面檔案列表：\n")
    for item in os.listdir(desktop):
        print(item)

if __name__ == "__main__":
    list_desktop_files()
    print("\n✅ 列出完成！")
```

---

### 🚀 使用方式

1. 開啟終端機：

   ```bash
   nano list_desktop.py

   #用 vscode 編輯 
   ```
2. 貼上程式碼，按 `Ctrl+O` → `Enter` → `Ctrl+X` 儲存。
3. 執行：

   ```bash
   python3 list_desktop.py
   ```
4. 結果：終端機會顯示桌面上的所有檔案和資料夾名稱，**不會做任何變動**。

---

## Python 範例2

稍微複雜一點的 **Python 自動化範例**：
它會掃描一個資料夾下所有 `.log` 檔案，搜尋特定關鍵字，並統計出現次數，最後輸出成報表。

---

### 🔹 Python 程式：Log 分析器

`log_analyzer.py`

```python
import os
import re
import csv
from datetime import datetime

def scan_logs(directory, keyword, output_file="log_report.csv"):
    """
    掃描指定資料夾下所有 .log 檔案
    搜尋關鍵字並統計出現次數，輸出 CSV 報告
    """
    results = []
    keyword_pattern = re.compile(keyword, re.IGNORECASE)

    for root, _, files in os.walk(directory):
        for file in files:
            if file.endswith(".log"):
                filepath = os.path.join(root, file)
                count = 0
                with open(filepath, "r", encoding="utf-8", errors="ignore") as f:
                    for line in f:
                        if keyword_pattern.search(line):
                            count += 1
                results.append([file, filepath, count])

    # 寫入 CSV
    with open(output_file, "w", newline="", encoding="utf-8") as csvfile:
        writer = csv.writer(csvfile)
        writer.writerow(["檔名", "路徑", f"'{keyword}' 出現次數"])
        writer.writerows(results)

    print(f"✅ 掃描完成！結果已輸出至 {output_file}")


if __name__ == "__main__":
    folder_path = input("請輸入要掃描的資料夾路徑：").strip()
    keyword = input("請輸入要搜尋的關鍵字：").strip()
    timestamp = datetime.now().strftime("%Y%m%d_%H%M%S")
    output_filename = f"log_report_{timestamp}.csv"

    scan_logs(folder_path, keyword, output_filename)
```

---

### 🔹 這個腳本做了什麼？

1. **遍歷資料夾** (`os.walk`) 找出所有 `.log` 檔案
2. **正則搜尋** (`re`) 找出每個檔案中關鍵字的出現次數
3. **結果匯出 CSV** (`csv`) 方便用 Excel 打開分析
4. **自動加上時間戳記**，生成不重複的報表檔名

---

### 🔹 執行方式

```bash
python3 log_analyzer.py
```

然後輸入：

* 要掃描的資料夾路徑
* 想搜尋的關鍵字

---

這樣的範例適合：

* 系統管理員查看 log 檔
* 偵錯程式記錄
* 批次分析大量檔案

---

##  目標與問題

### 目標

1. 認識 Terminal (終端機) 的常用指令
2. 建立目錄 Workspaces，並建立專案目錄 (名稱自定)，並將此檔案放到專案目錄 (之後範例也是)
3. 安裝 Visual Studio Code，並用它開啟專案目錄和編輯檔案
4. 認識 Python 語法
5. 編輯並執行 Python 範例

---

### 問題

1. 此檔案的格式 (.md) 是什麼?
2. 範例1 中路徑的 `~` 是什麼意思?
3. 如何用 terminal 的指令做到 範例1 的事?
4. 如何調整 範例2 所要查找的檔案條件?
5. 如何用 terminal 的指令直接顯示 範例2 產生的檔案?
