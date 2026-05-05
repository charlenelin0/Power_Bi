# Project Achievement Tracking Dashboard
This dashboard is designed to monitor and analyze project performance across business lines, helping stakeholders quickly identify gaps between actual performance and targets.
<br><br>
本儀表板用於監控與分析各業務線的專案績效，協助主管快速辨識實際表現與目標之間的差距。

## Business Requirements (From Stakeholders)
- Enable up-to-date project performance monitoring
  <br>即時監控最新的專案績效
- Support management in tracking performance against annual targets
  <br>協助管理層追蹤專案績效是否達成年度目標
- Enable deeper insights into performance across business lines
  <br>深入分析各業務線的績效表現
- Provide clear visibility into potential risks and performance issues to enable early action
  <br>提供對潛在風險與績效問題的清晰可視性，以便及早採取行動

## Design Steps

### 1. ETL Processing (SQL Stored Procedures)

#### Extract
- Extract data from OLTP systems (multiple data sources)
  <br>從 OLTP 系統（多個資料來源）擷取資料
- Ingest raw data into the ODS (staging layer)
  <br>將原始資料匯入 ODS（暫存層）

#### Transform
- Perform data cleaning, transformation, and validation
  <br>進行資料清理、轉換與驗證
- Standardize data formats and ensure data consistency
  <br>標準化資料格式並確保資料一致性  

#### Load
- Load processed data into the data warehouse
  <br>將處理後的資料載入資料倉儲 
- Design reusable data marts based on business requirements
  <br>根據業務需求設計可重複使用的資料集市
- Flatten dimensional data into wide tables to support analytical queries
  <br>將維度模型資料展平成大寬表，以支援分析查詢

---

### 2. Dashboard Design

#### What (Overview)
- Provide a high-level view of overall performance using key KPIs (Rev, GM, JHR)
  <br>透過關鍵指標（Rev、GM、JHR）提供整體績效的高層次視圖

#### How (Trend Analysis) 
- Analyze how performance evolves over time and identify gaps between actual and target
  <br>分析績效隨時間的變化，並找出實際表現與目標之間的落差

#### Where (Drill-down Analysis)
- Enable detailed analysis across business lines to locate performance issues and risk areas
  <br>透過各業務線進行細部分析，以定位績效問題與潛在風險區域

---

### 3. Dashboard Preview  

### Overall (What)
- Evaluate whether current projects are meeting annual targets
  <br>評估是否達成年度目標 
- Monitor key KPIs such as Revenue (Rev), Gross Margin (GM), and JHR
  <br>監控關鍵績效指標 
<img width="1414" height="836" alt="image" src="https://github.com/user-attachments/assets/bfec9f15-e519-4c11-8dd8-b06943f92c83" />

### Breakdown (How)
- Analyze performance across different business dimensions
  <br>分析各事業線的績效表現  
- Identify which areas contribute to performance gaps
  <br>識別哪些月份/事業線造成績效落差
<img width="1428" height="842" alt="image" src="https://github.com/user-attachments/assets/82b60d6d-0acd-4ebf-86a3-f200b9e7d53c" />

### Insight (Why)
- Highlight key drivers behind performance changes
  <br>找出影響績效變化的關鍵因素
- Support root cause analysis and decision-making
  <br>支援根本原因分析與決策制定
<img width="1439" height="850" alt="image" src="https://github.com/user-attachments/assets/71cf91fa-75a9-496e-9e28-a13b9bb74134" />
