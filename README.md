# 🍯 Shopper Spectrum ML Dashboard

An end-to-end **Streamlit** web app for:

* 🌟 **Product Recommendation** using Item-Based Collaborative Filtering
* 🔍 **Customer Segmentation** using the RFM Model and KMeans Clustering

Built using Python, Machine Learning, Data Preprocessing, and Visual Analytics.

---

## 🔹 Features

### 🎯 Product Recommendation

* Uses **item-item cosine similarity** from purchase history
* Input a `StockCode` and get **Top 5 similar products**
* Returns product names using a product lookup table

### 🔍 Customer Segmentation

* Takes **Recency, Frequency, Monetary** values from user input
* Uses a **pre-trained KMeans model** to predict cluster
* Maps clusters to segments:

  * `0`: At-Risk
  * `1`: High-Value
  * `2`: Regular
  * `3`: Occasional

---

## 📊 Dataset Files Used

| Filename                        | Description                               |
| ------------------------------- | ----------------------------------------- |
| `rfm_segmented.csv`             | RFM scores and cluster labels             |
| `pivot_table.csv`               | Customer vs. Product matrix for filtering |
| `product_similarity_matrix.csv` | Cosine similarity matrix of products      |
| `product_lookup.csv`            | Maps StockCode to product names           |
| `rfm_kmeans_model.pkl`          | Trained KMeans clustering model           |
| `rfm_scaler.pkl`                | StandardScaler used during model training |

---

## 📁 Project Structure

```bash
shopper_spectrum_app/
├── app.py                          # Main Streamlit app
├── rfm_kmeans_model.pkl            # KMeans model
├── rfm_scaler.pkl                  # Scaler for RFM values
├── rfm_segmented.csv               # Customer segments
├── pivot_table.csv                 # Purchase matrix
├── product_similarity_matrix.csv   # Similarity matrix
├── product_lookup.csv              # StockCode to name mapping
├── README.md                       # This file
```

---

## 🚀 How to Run This Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Aswani-2073/shopper-spectrum-ml-dashboard.git
cd shopper-spectrum-ml-dashboard
```

### 2. Install Required Packages

```bash
pip install -r requirements.txt
```

### 3. Start the Streamlit App

```bash
streamlit run app.py
```

---

## 📈 Sample Outputs

### Product Recommendation:

* Input: `85123A`
* Output: Top 5 similar products (e.g., `47556B - TEA TIME TEA TOWELS`)

### Customer Segmentation:

* Input: Recency = 20, Frequency = 15, Monetary = 500
* Output: Segment = `At-Risk`

---

## 📊 Tech Stack

* **Frontend**: Streamlit
* **ML Models**: Scikit-learn (KMeans, StandardScaler)
* **Similarity**: Cosine Similarity (Item-Item)
* **Backend**: Python, Pandas, NumPy, Joblib

---

## 📄 GitHub Push Commands

If you've initialized the project locally:

```bash
git init
git remote add origin https://github.com/Aswani-2073/shopper-spectrum-ml-dashboard.git
git add .
git commit -m "Initial commit with app, models, data, and README"
git push -u origin main
```

---

## 🙋️ Author

**Aswani Kasireddy**
Email: [aswani.kasireddy5@gmail.com](mailto:aswani.kasireddy5@gmail.com)
GitHub: [Aswani-2073](https://github.com/Aswani-2073)

---

