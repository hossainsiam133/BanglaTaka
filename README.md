# [BanglaTaka 🇧🇩💴](https://colab.research.google.com/github/hossainsiam133/BanglaTaka/blob/main/Code/BanglaTaka_Siam.ipynb)

*A Dataset for Classification of Bangladeshi Banknotes*

BanglaTaka is a curated image dataset and machine learning project focused on the **classification of Bangladeshi banknotes** using computer vision and deep learning techniques.  
The dataset and methodology are inspired by the work of **Md. Naimul Islam Nuhash and Sadia Akter (2025)** and are designed to support research in **financial automation, currency recognition, and fraud prevention**.

---

## 📌 Introduction
Automated banknote classification is critical for modern financial systems such as ATMs, vending machines, and currency authentication platforms. Manual verification is time-consuming and prone to human error.

The **BanglaTaka dataset** provides high-quality images of Bangladeshi currency notes captured under diverse conditions, enabling robust supervised machine learning and deep learning–based classification models. 
---

## 💵 Supported Denominations
The dataset includes **9 Bangladeshi banknote denominations**:

- 2 taka  
- 5 taka  
- 10 taka  
- 20 taka  
- 50 taka  
- 100 taka  
- 200 taka  
- 500 taka  
- 1000 taka  

---

## [📊 Dataset Overview](https://drive.google.com/drive/folders/13P5Soos4thSeu9Su62lHVENzrSF3kxCA?brid=_lZkcYae4gXRQ2ufJUg74w)
- **Total Images:** 5,073 (JPG format)  
- **Collection Locations:** Dhaka, Rajshahi, Khulna, Sylhet, and other regions  
- **Capture Conditions:**  
  - Different lighting environments  
  - Multiple camera angles  
- **Devices Used:**  
  - iPhone 12 Pro  
  - Samsung M31  
  - Realme C25s  
  - Redmi Note 13  

The dataset includes **new, old, worn, and damaged banknotes**, ensuring real-world applicability.
---

## 🧪 Data Preprocessing & Enhancement
Each image undergoes several preprocessing steps to ensure consistency and quality:

- Cropping to extract the clean banknote region  
- Contrast and brightness adjustment  
- Orientation normalization  
- Color correction  
- Removal of blurred, duplicated, or low-quality images  

These steps improve robustness for machine learning model training and evaluation.

---

## 🧠 Methodology
- Images collected from shops, banks, markets, and homes  
- Each image labeled according to denomination  
- Images categorized into **9 classes**  
- Quality control applied to ensure dataset reliability  
- Dataset structured for direct use in ML and DL pipelines  

---

## ⭐ Key Contributions
- First large-scale, publicly usable dataset for Bangladeshi banknotes  
- High-quality, background-free images  
- Multiple capture devices for diversity  
- Suitable for:
  - Currency classification  
  - Financial automation  
  - Counterfeit detection research  
  - Computer vision benchmarking  


---

## 🧩 Applications
- Automated banknote recognition systems  
- ATM and cash-handling automation  
- Fraud and counterfeit detection research  
- Deep learning–based currency classification  
- FinTech and AI research in developing economies  

---

## 🔗 Connection to Machine Learning Concepts
This project demonstrates:
- Supervised image classification  
- Data preprocessing and normalization  
- Multi-class classification problems  
- Applicability of:
  - CNN  
  - EfficientNet  
  - Vision Transformers (ViT)  

---

## ⚠️ Limitations
- Mostly controlled environment images  
- Unequal representation across denominations  
- No counterfeit banknotes included  
- Limited to Bangladeshi currency only  

**Future Work:**
- Inclusion of forged and counterfeit samples  
- UV and infrared imaging  
- Cross-country currency classification  
- Real-time detection systems  

---

## 📁 Dataset Structure
drive/MyDrive/dataset  <br>
│── 2/ <br>
│── 5/  <br>
│── 10/  <br>
│── 20/  <br>
│── 50/  <br>
│── 100/  <br>
│── 200/  <br>
│── 500/  <br>
│── 1000/  <br>

Each denomination initially contains a limited number of images, which are expanded using augmentation techniques.

---

## 👨‍🎓 Academic Context
**Presented by:** 
- Md. Siam Hossain (23100084)  
- Md. Talha Mahmud (23100069)  
- Asif Manowar (23100016) <br>

**Course:** Machine Learning Lab  
**Instructor:** Md. Safaet Ullah, Lecturer, CSE, RPSU  

---

## 📚 References
1. Md. Naimul Islam Nuhash, Sadia Akter (2025). *BanglaTaka: A Dataset for Classification of Bangladeshi Banknotes*. ScienceDirect. :contentReference[oaicite:6]{index=6}  
2. NSTU-BDTAKA: An Open Dataset for Bangladeshi Paper Currency Detection (2024)  
3. CNN-Based Bangladeshi Currency Detection with Mobile App Integration  
4. Efficient Currency Recognition Systems Using Deep Learning  

---

## 📜 License
This project is intended for **academic and research purposes only**.
