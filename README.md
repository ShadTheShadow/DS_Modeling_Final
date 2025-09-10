# Titanic Survival and Passenger Fare Analysis
## Data Science Modeling Final

## 📖 Introduction
When people think about the Titanic, they usually focus on the sinking or the enormous casualty numbers.  
Our group explored a deeper story: **Did higher ticket fares increase the chances of survival?**

**Research Question:**  
_Is there a positive difference in mean passenger fare between those who survived and those who died in the Titanic disaster?_

**Summary of Findings:**  
We found strong evidence that the average passenger fare was higher for survivors compared to non-survivors.

---

## 📊 Background
- **Dataset Source:** Organized by Will Cukierski, based on Titanic search and rescue team data.  
- **Key Variables:**
  - `Survived`: Indicates whether a passenger survived (1) or died (0).  
  - `Fare`: Passenger ticket price.  
- **Sample Size:** 891 passengers (subset of Titanic population).  
- **Historical Context:**  
  - The Titanic sank in 1912 despite its “unsinkable” reputation.  
  - It hosted a diverse group of passengers across class structures, leading to wide variation in fares.

---

## 🧹 Data Cleaning & Preparation
- Removed outliers using median ± 1.5×IQR method.  
- Focused on `Survived` and `Fare` variables.  
- Produced histograms of fare distribution by survival status.

cleaned_data <- data %>%
  filter(Fare > med - 1.5*IQR, Fare < med + 1.5*IQR)
