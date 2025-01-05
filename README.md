# POWER-BI-ASSIGNMENT-2

### **Step-by-Step Guide to Creating the Interactive Sales Report in Power BI**

### **Step 1: Import Data into Power BI**
1. **Open Power BI Desktop**.
2. **Import Data**: Click on `Home` → `Get Data`. Select the data source type (Excel, SQL Server, CSV, etc.) based on your dataset format.
3. **Load the Dataset**: Once the data is loaded, you’ll see the tables on the right side of the Power BI window under the "Fields" pane.

### **Step 2: Data Preparation (Optional)**
Before creating visualizations, you may need to prepare and clean your data. This can be done in Power BI's **Power Query Editor**.
1. **Remove duplicates**: In the "Transform Data" section, select `Remove Duplicates` to ensure unique rows.
2. **Handle missing values**: Identify and fill in or remove rows with missing data where necessary.
3. **Format columns**: Ensure that fields like `Sales`, `Order Date`, `Country`, `Region`, `Ship Mode`, etc., are correctly formatted (e.g., currency, date, text).
4. **Create calculated columns or measures**: If needed, create new columns or measures, such as the percentage of shipping

  percentage of shipping = DIVIDE(SUM(Orders[Shipping Cost]),CALCULATE(SUM(Orders[Shipping Cost]),ALL(Orders[Ship Mode])))

### **Step 3: Create Visualizations**
#### **Visualization 1: shipping percentage based on ship mode**
1. **Donut chart**: Drag `Country` to the `legend` and `% of shipping` to the `Values`.
   - This will show a shipping percentage base on ship mode

#### **Visualization 2: Sales by City**
1. **Column chart**: Drag `city` to the `Axis` and `sum of sales` to the `Values`.
2.' top n filter'function used this and get top 5 cities
  -also create tables sales by cities,sort it.
   

#### **Visualization 3: Sales by region**
1. **Map**: Drag `Region` to the `Location` and `sumof sales` to the `bubbles`.
   -This will show a geographical map where the size or color intensity represents the sales volume in each location.
   -also create tables,and sort it.

#### **Visualization 5: Sales by market&State (*bar chart*)
1. **Bar chart**: in this we will show sales by market&state by drill down&drill up.
2. create hierarchy state&market.Drag 'hierarchy' to the y axis and 'sum of sales' in  x axis.
3. also create tables and sort it.this will  each market &state trends




