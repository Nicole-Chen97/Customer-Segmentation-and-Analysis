## 專案：

目的：本專案針對賣場銷售資料進行分析，以了解不同群族客戶的特徵與消費偏好。透過對客戶基本資料（如年齡、收入、家庭狀況等）及消費行為（如購買金額、購買頻率等）的深入研究，協助企業制定更精準的行銷策略，提升顧客滿意度與忠誠度。

方法：為了有效地對客戶進行群組劃分，本專案採用了 KMeans 分群演算法，分析客戶之間的相似性並將其分成不同群組。藉此，能更清晰地了解各群客戶的特徵與需求，為後續的市場行銷提供支持。

資料來源： kaggle https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis

---
## 使用之資料說明：

客戶基本資料：

ID: Customer's unique identifier

Year_Birth: Customer's birth year

Education: Customer's education level

Marital_Status: Customer's marital status

Income: Customer's yearly household income

Kidhome: Number of children in customer's household

Teenhome: Number of teenagers in customer's household

Dt_Customer: Date of customer's enrollment with the company

Recency: Number of days since customer's last purchase

Complain: 1 if the customer complained in the last 2 years, 0 otherwise

產品消費金額：
MntWines: Amount spent on wine in last 2 years

MntFruits: Amount spent on fruits in last 2 years

MntMeatProducts: Amount spent on meat in last 2 years

MntFishProducts: Amount spent on fish in last 2 years

MntSweetProducts: Amount spent on sweets in last 2 years

MntGoldProds: Amount spent on gold in last 2 years

購物通路之次數：
NumWebPurchases: Number of purchases made through the company’s website

NumCatalogPurchases: Number of purchases made using a catalogue

NumStorePurchases: Number of purchases made directly in stores

NumWebVisitsMonth: Number of visits to company’s website in the last month 


## 結論：
分別使用人工分群和Kmeans分群，並針對分群結果以觀察客戶基本特徵、消費篇好管道、資金分配比例 

##### KMeans 分析結果：
#### **總體分析：**
分為兩群，cluster_0 為887 人（佔比40.2%)，其總消費額為1,098,169 (佔比80%)

cluster_1 為1319人（佔比59.8%)，其總消費額為245,083 (佔比20%)

顯示雖然cluster_0人數僅有四成，但其貢獻金額為佔整體的八成，可針對該群擬定詳細的策略規劃，以增進總消費額

---

#### **群組特點：**
1. **cluster_0 (藍色點)：**
   - **收入與消費額偏高：** 該群組的收入範圍多集中於4000-10,000中高區間，且總消費額（Total_Mnt_Spent）相對較高，落在500-2000，消費額與收入呈現較強的正相關，顯示收入驅動了該群體的消費能力。
   - **產品：** 在資金支配上，該群體可能偏好高單價商品，酒類和肉品消費範圍較廣，其消費支出多集中於此，對其他類別的消費比例較為平均（4-6%)
   - **消費管道：** 以實體為主，但也會使用網路和目錄消費 

2. **cluster_1  (橙色點)：**
   - **收入與消費額偏低：** 該群組的收入範圍主要集中於低收入區間（0~8000)，且總消費額相對較低(1000以下）。
   - **小孩數量影響：** 這些客戶大多有小孩，支出受家庭經濟壓力影響更大。
   - **消費行為分散：** 群組的消費次數相對較低（集中於5-10)，但瀏覽網站次數集中於5-7次，顯示該群體在低收入背景下的支出模式較不穩定。
   - **產品：** 在資金分配上，偏好購買酒類、肉品和黃金類產品，但其金額比cluster_0消費來得低些，多集中在左邊
   - **消費管道：** 以實體為主，但也會使用網路，目錄消費的比例低
   - **網路瀏覽與折價購物次數：** 相較cluster_0 ，此群會使用折價券，其網路瀏覽次數較廣，多集中在5-7次

---

#### **策略建議：**

1. **cluster_0  (高收入群體)：**
   - **推廣高端產品：** 提供專屬的高價商品組合或高端會員優惠，進一步吸引其消費。

2. **cluster_1  (低收入群體)：**
   - **價格敏感性促銷：** 推出更多價格友好的促銷活動（例如折扣和積分兌換），滿足該群體的消費需求。
   - **家庭型產品優惠：** 提供家庭套餐或針對多孩家庭的促銷活動，吸引該群體增加單次消費金額。
   - **數位化購物體驗：** 該群體可能偏好性價比高的商品，應優化網路購物界面，推廣在線購物折扣。




