# 🧹 Data Cleaning Project – Excel & Power BI

## 📌 Project Objective  
To clean and structure the Airbnb NYC 2019 dataset using Excel for validation and transformation. The project focused on identifying and correcting missing or misclassified data, ensuring data consistency, and preparing it for reporting. Although visualization wasn't part of the original task, a Power BI dashboard was created as a bonus.

## 🛠 Tools Used  
- **Microsoft Excel**: Data cleaning and rule-based transformations  
- **Power BI**: Used post-cleaning for visualization and validation of data structure

## 🎯 Cleaning Steps Performed  

1. **Name Column Handling**  
   - Used custom filters to identify and replace blank `name` entries with `"Unknown"`

2. **Host Name Validation**  
   - Applied `ISTEXT()` in Excel to find numeric or blank values in `host_name`  
   - Replaced non-text entries and blanks with `"Unknown"`

3. **Logical Checks for Review Columns**  
   - Used `ISBLANK()` to find and clean blanks in `last_review` and `reviews_per_month`  
   - Removed rows where `last_review` was blank or 0 (since it's a date field)  
   - Set `reviews_per_month` to 0 where missing  
   - Applied logic: if `number_of_reviews = 0` and `last_review = 0`, then `reviews_per_month` = 0, and vice versa

4. **Date Handling**  
   - Removed records where valid `last_review` dates were not available

5. **Power BI Visualization (Bonus)**  
   - Cleaned data was uploaded to Power BI  
   - Created visuals to validate cleaning steps (not part of original task)

## 📁 Files Included  
- `AB_NYC_2019.xlsx`: Original dataset  
- `steps-done.txt`: Description of manual cleaning logic applied in Excel  
- `prj2.pbix`: Power BI file with visual validation  
- `PowerBidashboard_screenshot1.0`, `PowerBidashboard_screenshot1.1`: Snapshots of dashboard  
- `README.md`: This documentation file

## 🚀 Notes  
- This project showcases strong fundamentals in data cleaning and Excel-based logic building  
- Power BI dashboard helped visually confirm the cleaning results  
