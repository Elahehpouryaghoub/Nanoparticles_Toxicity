# Nanoparticles_Toxicity
### **🔹 Introduction**

This project explores **nanoparticle toxicity classification** using a dataset containing various nanoparticles and their physicochemical properties. The dataset includes features such as **core size, hydrosize(hydrodynamic size of the NPs), surface charge, surface area, Ec (electric charge), exposure time, e (energy related feature possibly Electron Affinity or Energy Dissipation), dosage, and number of oxygen atoms**. The final column represents toxicity, where **1 indicates toxic** and **0 indicates non-toxic**.

---

### **🔹 Methods**

After loading the dataset, **preprocessing** was performed to ensure compatibility with machine learning models.

1️⃣ **One-Hot Encoding** was applied to transform the categorical **nanoparticle (NPs) column** into a numerical format, making it suitable for machine learning. Since One-Hot Encoding produces only **0s and 1s**, these values remained unchanged even after normalization.

2️⃣ **A correlation heatmap** was generated to visually assess the linear relationships between all features and the target class (toxicity). This helped identify features with strong positive or negative correlations to toxicity, such as NOxygen,NPs_TiO2, and NPs_ZnO providing early insights into which variables might be influential in predicting nanoparticle toxicity. 

3️⃣ The **target column (toxicity label)** was separated from the feature set, and the dataset was split into **training (80%) and testing (20%) sets**.

4️⃣ **Feature Normalization** was applied to scale all numerical features between **0 and 1**, ensuring models learn effectively without bias toward larger values. The processed data was then converted back into a dataframe.

5️⃣ A **custom evaluation function** was implemented to compute **accuracy, recall, precision, and F1-score** for performance comparison.

6️⃣ Machine learning models including **XGBoost, SVM, Random Forest, Decision Tree, Logistic Regression, and ANN (Artificial Neural Network)** were trained and evaluated.

---

### **🔹 Results and Findings**

The **Model Performance Heatmap** indicates that **no major overfitting** was observed. Most models exhibited **similar Train and Test F1-Scores**, demonstrating good generalization to new data. While **XGBoost and Random Forest showed slight overfitting** (Train ≈ 0.99 vs. Test ≈ 0.96), the gap was minimal and **not concerning**. Other models, such as **Decision Tree, SVM, ANN, and Logistic Regression**, performed well without signs of memorization, suggesting a strong balance between learning and generalization.

The **Confusion Matrix** provided insight into False Negatives (FN), False Positives (FP), True Positives (TP), and True Negatives (TN) for each model. **XGBoost, Random Forest, and ANN performed best**, with **0 or 1 FN cases**, indicating high reliability in detecting toxic nanoparticles. While **Logistic Regression** showed only one FN, its high FP count (32) reduced its reliability for accurate predictions. SVM, in contrast, demonstrated weaker performance, failing to minimize both FN and FP errors compared to other models.

Finally, a **Feature Importance Plot** was generated for tree-based models (**XGBoost, Random Forest, and Decision Tree**), as **SVM and ANN** do not provide direct feature importance scores. This analysis revealed that **Number of Oxygen atoms and Dosage** were the most influential features affecting toxicity. Additionally, models such as Random Forest, XGBoost, and Logistic Regression indicated that the **TiO₂ nanoparticle contributes with toxicity**.

---

### **🔹 Conclusion**

The results suggest that **XGBoost, Random Forest, and ANN are the most effective models for nanoparticle toxicity classification** due to their ability to **minimize False Negatives while maintaining high accuracy**. The findings highlight that **dosage and oxygen content** play a crucial role in determining toxicity, making them key factors for future research and regulatory assessments.

## ✉ Contact
If you have any questions or feedback, feel free to reach out!
- **LinkedIn:** www.linkedin.com/in/elaheh-p-9918432a6

 **If you find this project useful, please ⭐ star the repository!** ⭐
