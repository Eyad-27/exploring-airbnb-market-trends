# 🏙️ Exploring Airbnb Market Trends  

![NYC Skyline](nyc.jpg)  

New York City is one of the most-visited cities in the world, with a booming Airbnb market that offers a wide range of rental options. In this project, I explored Airbnb listings from multiple datasets (CSV, Excel, and TSV formats) to analyze pricing, room types, and review activity.  

The goal was to **merge diverse data sources** and uncover insights about private room availability, average pricing, and review patterns in the NYC market.  

---

## 📌 Guiding Questions  
- What are the dates of the **earliest and most recent reviews**?  
- How many of the listings are **private rooms**?  
- What is the **average listing price**?  
- Can we combine these insights into a single, clean **DataFrame** for analysis?  

---

## 📂 The Data  

### **airbnb_price.csv**  
| Column       | Description                                          |  
|--------------|------------------------------------------------------|  
| `listing_id` | Unique identifier of listing                         |  
| `price`      | Nightly listing price in USD                         |  
| `nbhood_full`| Borough and neighborhood where listing is located    |  

### **airbnb_room_type.xlsx**  
| Column       | Description                                          |  
|--------------|------------------------------------------------------|  
| `listing_id` | Unique identifier of listing                         |  
| `description`| Listing description                                  |  
| `room_type`  | Room type: shared, private, or entire home/apartment |  

### **airbnb_last_review.tsv**  
| Column       | Description                                          |  
|--------------|------------------------------------------------------|  
| `listing_id` | Unique identifier of listing                         |  
| `host_name`  | Name of listing host                                 |  
| `last_review`| Date when the listing was last reviewed              |  

---

## 🛠️ How I Approached the Project  

1. **Loading the Data**  
   - Imported `.csv`, `.tsv`, and `.xlsx` files into pandas DataFrames.  

2. **Merging DataFrames**  
   - Combined all three DataFrames on the `listing_id` column for a unified dataset.  

3. **Handling Review Dates**  
   - Converted review date column into datetime format.  
   - Extracted earliest and most recent review dates.  

4. **Analyzing Room Types**  
   - Standardized text capitalization for consistency.  
   - Counted the number of private room listings.  

5. **Analyzing Prices**  
   - Converted `price` column into numeric type.  
   - Calculated average listing price (rounded to 2 decimals).  

6. **Creating a Summary DataFrame**  
   - Built a one-row DataFrame (`review_dates`) with:  
     `first_reviewed`, `last_reviewed`, `nb_private_rooms`, `avg_price`.  

---

## ✅ Key Deliverables  
- Imported and merged multi-format datasets (`CSV`, `Excel`, `TSV`).  
- Cleaned and standardized categorical variables (room types).  
- Analyzed **review trends** and room availability.  
- Calculated **average Airbnb prices** across NYC.  
- Produced a consolidated DataFrame summarizing all insights.  

---

## 🧰 Skills Used  
- Python (`pandas`)  
- Data wrangling and merging  
- Handling multi-format datasets  
- Data cleaning and transformation  
- Exploratory Data Analysis (EDA)  
