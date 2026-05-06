# Project Achievement Tracking Dashboard
This dashboard is designed to monitor and analyze project performance across business lines, helping stakeholders quickly identify gaps between actual performance and targets.
<br>
本儀表板用於監控與分析各事業線的專案績效，協助主管快速辨識實際表現與目標之間的差距。

## Business Requirements (From Stakeholders)
- Enable up-to-date project performance monitoring
  <br>即時監控最新的專案績效
- Support management in tracking performance against annual targets
  <br>協助管理層追蹤專案績效是否達成年度目標
- Enable deeper insights into performance across business lines
  <br>深入分析各事業線的績效表現
- Provide clear visibility into potential risks and performance issues to enable early action
  <br>以視覺化方式呈現，迅速辨識對潛在風險與績效問題，以便及早採取行動

## Design Steps

### 1. ETL Processing

#### Extract
- Extract data from OLTP systems and ingest raw data into the ODS staging layer
  <br>從 OLTP 系統擷取資料，並將原始資料暫存至 ODS
#### Transform
- Perform data cleaning and transformation
  <br>進行資料清理與轉換，處理時間格式與全形／半形字元不一致問題
#### Load
- Load processed data into the data warehouse
  <br>將處理後的資料載入資料倉儲，作為報表分析的集中資料來源
- Design reusable data marts using Star Schema and wide tables to support analytical queries
  <br>根據分析報表需求設計資料集市，透過事實表／維度表與寬表支援快速查詢

---

### 2. Dashboard Design Structures

#### What (Overview)
- Provide a high-level view of overall performance using key KPIs (Rev, GM, JHR)
  <br>透過關鍵指標快速掌握整體績效表現

#### How & Where (Trend Analysis) 
- Analyze how performance evolves over time and identify gaps between actual and target
  <br>以時間與事業線雙面向進行分析，快速找出績效落差的來源

#### Why (Drill-down Analysis)
- Enable detailed analysis across business lines to locate performance issues and risk areas
  <br>透過各事業線或專案進行深入分析，以找出績效問題的根本原因

---

### 3. Dashboard Demo  

### Overall (What)
- Evaluate whether current projects are meeting annual targets
  <br>評估是否達成年度目標 
- Monitor key KPIs such as Revenue (Rev), Gross Margin (GM), and JHR
  <br>監控關鍵績效指標
  
https://github.com/user-attachments/assets/5361865a-e492-4cbb-8905-0c92ba9df87a

### Breakdown (How & Where)
- Analyze performance across different business dimensions
  <br>分析各事業線的績效表現  
- Identify which areas contribute to performance gaps
  <br>顯示哪些月份或事業線造成績效落差

https://github.com/user-attachments/assets/eef281cc-b537-4625-84c1-bba81df15f4b

### Insight (Why)
- Highlight key drivers behind performance changes
  <br>找出影響績效變化的關鍵因素
- Support root cause analysis and decision-making
  <br>支援根本原因分析與決策制定
<img width="1439" height="850" alt="image" src="https://github.com/user-attachments/assets/71cf91fa-75a9-496e-9e28-a13b9bb74134" />

## Tools
- MSSQL (Stored Procedures for ETL processing)
- Power Query & DAX (Data transformation and KPI calculation)
- Power BI (Dashboard design and data visualization)
