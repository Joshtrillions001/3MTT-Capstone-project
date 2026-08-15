 # Localized NAFDAC Drug Counterfeit Checker (MVP)

An accountability-driven Machine Learning prototype built as a Capstone Project for the 3MTT NextGen cohort. This system helps protect patients in Nigeria by identifying suspicious or altered NAFDAC drug registration entries.

## 📌 Problem Statement
Counterfeit pharmaceuticals with forged NAFDAC numbers present a critical threat to healthcare safety across Nigeria. This project provides a functional Minimum Viable Product (MVP) that leverages data-driven validation to instantly flag suspicious product entries.

## ⚙️ Core Technical Features
- **Real-World Foundation:** Scaled entirely using an authentic dataset containing **18,110 official NAFDAC drug records**.
- **Machine Learning Integration:** Uses `TfidfVectorizer` and a `MultinomialNB` (Naive Bayes) classification pipeline via Scikit-Learn.
- **Hybrid Verification:** Combines statistical AI text pattern recognition with a deterministic database cross-reference scanner to maximize accuracy.
- **Zero Ambiguity:** Returns clean, direct results: **Genuine** or **Suspicious**.

## 🛠️ Project Workspace Layout
The code is divided logically into 3 distinct operational cells within Google Colab:
1. **Cell 1 (Data Prep):** Loads, strips, and cleans the NAFDAC dataset while injecting balanced synthetic anomalies for model training.
2. **Cell 2 (ML Engine):** Converts text profiles into mathematical feature vectors and trains the classifier.
3. **Cell 3 (Verification Dashboard):** Houses the primary execution function along with a 10-batch simulation loop for live demonstrations.

## 🚀 How to Run the Prototype
1. Open Google Colab and upload the `nafdac_drugs.csv` file to your session storage.
2. Execute the three cells sequentially.
3. Query any text profile using the test function:
   ```python
   check_my_drug("#Accu-Chek A3-100882") # Returns: Genuine
   check_my_drug("Fidson Healthcare Amoxicillin 250mg ERROR-23") # Returns: Suspicious
   ```

---
*Built with discipline and shipped in public for the 3MTT Graduation Requirement.*
