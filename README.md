## **Mouse Size vs Weight Regression in R 🐭📊**  

This repository contains an R script that performs **linear regression** on a dataset of mouse **weights and sizes**. The goal is to analyze the relationship between a mouse's weight and its size using **simple linear regression** and visualize the results.

---

### **📌 Overview**  
The script:  
1. **Creates a dataset** of mouse weights and sizes.  
2. **Plots** the data to visualize the relationship.  
3. **Fits a linear regression model** (`lm()`) to predict size based on weight.  
4. **Summarizes** the regression results.  
5. **Plots the regression line** using `abline()`.

---

### **📜 Code Explanation**  

#### **1️⃣ Create a Data Frame**  
```r
mouse.data <- data.frame(
  weight = c(0.9,1.8,2.4,3.5,3.9,4.4,5.1,5.6,6.3),
  size = c(1.4,2.6,1.0,3.7,5.5,3.2,3.0,4.9,6.3)
)
```
- Defines `mouse.data`, a **data frame** with two columns:  
  - `weight` → Mouse weight  
  - `size` → Mouse size  

#### **2️⃣ Visualize the Data**  
```r
plot(mouse.data$weight, mouse.data$size)
```
- Creates a **scatter plot** of `size` vs. `weight`.  
- Helps visualize the trend between weight and size.

#### **3️⃣ Fit a Linear Regression Model**  
```r
mouse.regression <- lm(size ~ weight, data=mouse.data)
summary(mouse.regression)
```
- `lm(size ~ weight, data=mouse.data)` → Fits a **linear regression** model.  
- `summary(mouse.regression)` → Displays model statistics (coefficients, R², p-values).  

#### **4️⃣ Add the Regression Line to the Plot**  
```r
abline(mouse.regression, col = "blue")
```
- **Draws the best-fit line** from the regression model onto the scatter plot.  
- `col = "blue"` makes the line **blue** for visibility.

---

### **📊 Example Output**  
After running the script, you’ll get:  
✅ A **scatter plot** of weight vs. size.  
✅ A **regression line** showing the trend.  
✅ A **summary** of the model with coefficients, R², and statistical significance.

---
