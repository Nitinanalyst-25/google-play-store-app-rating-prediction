# Google Play Store App Rating Prediction

### **What is this project about?**
The goal of this project was to take a messy list of over 10,000 Google Play Store apps and turn it into a clean, reliable dataset. I then used this data to build a model that can predict an app's rating based on things like its category, size, and price.

---

### **The Step-by-Step Process**

#### **1. Fixing the "Messy" Data (Data Cleaning)**
When I first got the data, it was full of errors that made it impossible to do any math. I wrote Python scripts to fix these issues:
* **Standardizing Sizes:** Some app sizes were listed in Megabytes ('M') and some in Kilobytes ('k'). I converted all of them into one single numeric format.
* **Cleaning Numbers:** I removed symbols like '$', '+', and ',' from the Price and Install columns so they could be treated as numbers instead of text.
* **Removing Errors:** I found and removed ratings that were higher than 5 (which shouldn't be possible) and filled in missing information to make the dataset complete.

#### **2. Looking for Patterns (EDA)**
Before building the model, I used **Pandas** and **NumPy** to see what actually affects an app's rating:
* **What matters most?** I checked if free apps get better ratings than paid ones and which categories (like Games or Tools) are the most popular.
* **Visualizing the data:** I created simple charts to see how ratings were spread out across the whole store.

#### **3. Predicting the Ratings (Modeling)**
I used a method called **Linear Regression** to predict what an app's rating would be. 
* **Testing the Accuracy:** To make sure my predictions were actually good, I used two main checks:
    * **R-Squared:** This tells me how much of the rating "logic" my model actually understood.
    * **Mean Squared Error (MSE):** This tells me, on average, how far off my predictions were from the real ratings.

---

### **Key Results**
* Successfully cleaned and organized over **10,000 app records**.
* Fixed over **13 different types of data errors** using Python.
* Created a reliable way to predict app performance based on real market data.

### **Tools I Used**
* **Language:** Python
* **Main Libraries:** Pandas (Data handling), NumPy (Math), Scikit-learn (Prediction), Matplotlib/Seaborn (Charts)
