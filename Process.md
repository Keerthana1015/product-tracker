# Process Documentation: Product Pricing Insights Tool

## **Introduction**
This project is designed to help small business owners track product pricing and adjust to market conditions. I have processed the provided CSV data, fetched real-time external data, and generated an easy insights with visual aids.

## **Steps I Followed**

### **1. Cleaning the Data**
I noticed that the CSV file had some issues like:
- Extra columns that weren't needed.
- Prices formatted with currency symbols (e.g., `$12.99`).
- Missing values in some fields.

#### **What I Did:**
- Removed unnecessary columns.
- Cleaned price fields to remove `$` and converted them to numbers.
- Replaced missing values with `0` so everything worked smoothly.
- Standardized names to lowercase for consistency.

---

### **2. Adding External Data**
#### **Why This API?**
I have used the [ExchangeRate-API](https://www.exchangerate-api.com/) because:
- It provides real-time exchange rates (e.g., USD to EUR).
- It’s simple and free to use for small-scale projects.

#### **How I Have Integrated It:**
- Managed the API key securely using a `.env` file.
- Retrieved the latest exchange rates and calculated product prices in EUR.

---

### **3. Generating Insights**
I have created meaningful insights by analyzing the cleaned data combined with external exchange rates.

#### **Key Insights:**
- Identified the most expensive product: `Organic Coffee Beans (1lb)` (€14.39).
- Found the cheapest product: `Hot Chocolate Mix (1lb)` (€7.67).
- Calculated the average product price in EUR: €10.55.

#### **What I Would Recommended:**
- Monitor exchange rates regularly to adjust prices as needed.
- Focus on products with high demand and competitive pricing.
- Explore pricing strategies for low-margin items.

---

### **4. Adding Visuals**
To make the insights easier to understand, I have created a bar chart showing product prices in EUR.

#### **Steps I Have Taken:**
- Used the `matplotlib` library to generate a bar chart.
- Saved the chart as `price_chart.png`.
- Linked the chart in the report for quick reference.

---

### **5. Testing Everything**
- **Testing the CSV:** I tried the script with different types of CSV files to ensure it handled errors (like missing or malformed data) gracefully.
- **API Key Handling:** Verified that the script warned users if the API key wasn’t provided.
- **Final Output:** Confirmed the report (`report.md`) and the chart (`price_chart.png`) were generated correctly.

---

## **How the Files Are Organized**
```
├── README.md          # Quick setup instructions
├── Process.md         # This file: explains the workflow
├── data/              # Folder containing the CSV file
├── src/               # Folder with scripts for analysis
│   ├── analysis.py    # Main script
│   └── utils.py       # Helper functions
├── requirements.txt   # List of required libraries
├── report.md          # Insights and recommendations
├── .env.example       # Template for environment variables
└── price_chart.png    # Generated bar chart
```

---

## **Reflections**
### **What Went Well:**
- Successfully cleaned and processed messy data.
- Integrated real-time external data effectively.
- Delivered insights that are both actionable and visually appealing.

### **What Could Be Improved:**
- Automate tests to handle even more CSV issues.
- Optimize performance for very large datasets.
- Add support for more external data sources, like competitor pricing.

---

## **Time Spent**
- Cleaning the data: ~30 minutes
- Adding external data: ~40 minutes
- Generating insights: ~30 minutes
- Creating visuals: ~20 minutes

