# 股票價格相似性分析系統

## 介紹
此工具是一個股票趨勢分析系統，可從 Yahoo Finance 獲取股票歷史數據，並使用 動態時間規劃 (DTW) 或 歐幾里得距離 比較不同股票之間的趨勢相似性。此外，還支援視覺化功能來繪製股票收盤價趨勢圖表。

---

## 安裝
   ```bash
   !pip install numpy pandas yfinance dtaidistance matplotlib
   ```
   ```bash
   !pip install dtaidistance
   ```
1. **numpy**：進行數值計算
2. **pandas**：處理表格型數據
3. **scipy**：計算歐幾里得距離
4. **dtaidistance**：計算動態時間規整（DTW）距離
5. **yfinance**：從 Yahoo Finance 獲取歷史股票數據
6. **matplotlib**：繪製圖表
---

## 功能
### 資料處理函數 fetch_stock_prices(stock_code, start_date, end_date)
1. 從 Yahoo Finance 獲取指定股票的收盤價數據
2. 自動清理缺失值，返回整理後的 Pandas Series
### 趨勢比較函數
1. compare_trends(series1, series2)
- 動態時間規劃 (DTW) 方法：用於比較兩個時間序列的相似性，return DTW 距離
2. compare_trends(series1, series2)
- 歐幾里得距離方法，適用於序列長度一致的情況，return 歐幾里得距離
### 視覺化函數 plot_stock_trends(stock_data_dict)
- 輸入多支股票的收盤價數據，繪製其趨勢圖表

---

## 使用方式
### 執行主程式
```bash
python stock_analysis.py
```
根據提示輸入股票代碼和日期範圍，查看分析結果和圖表
## 範例
1. 執行程式後，輸入以下股票代碼進行分析：
```bash
輸入股票代碼：AAPL, MSFT, GOOG  
起始日期（預設 2023-01-01）：  
結束日期（預設 2023-12-31）：
 ```
2. 程式將輸出以下結果：
- 歐幾里得距離或 DTW 距離
- 股票價格的趨勢圖表
