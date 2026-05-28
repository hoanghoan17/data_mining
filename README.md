# 🍳 Smart Recipe Recommendation System

Hệ thống gợi ý món ăn cá nhân hóa dựa trên nguyên liệu có sẵn, sử dụng Content-Based Filtering + FP-Growth + KMeans.

## 🎯 Tính năng

- 🔍 Gợi ý món ăn từ nguyên liệu người dùng có sẵn
- 🤖 Cá nhân hóa theo lịch sử "thích" của user (User History Vector)
- 💡 Giải thích lý do gợi ý (Explainable AI với FP-Growth rules)
- 🎨 Phân cụm món ăn (KMeans) để khám phá theo nhóm
- ⚡ Tìm kiếm tốc độ cao bằng FAISS
- 📊 Autocomplete nguyên liệu real-time

## 🏗️ Kiến trúc
- Frontend (HTML/CSS/JS)
- HTTP Backend (FastAPI)
- Recommendation Engine (TF-IDF + SVD + FAISS + FP-Growth + KMeans)
- SQLite Database (User, Interactions, Logs)


## 🛠️ Công nghệ

- **Backend:** Python, FastAPI, Uvicorn, Pydantic
- **ML/Data:** pandas, scikit-learn, mlxtend, FAISS, numpy
- **Database:** SQLite (SQLAlchemy ORM)
- **Frontend:** HTML5, CSS3, Vanilla JavaScript

## 📦 Cài đặt

### Yêu cầu
- Python 3.10+
- 4GB RAM (để load model)

### Bước 1: Clone repo
```bash
git clone https://github.com/YOUR_USERNAME/recipe-recsys.git
cd recipe-recsys
```
### Bước 2: Cài thư viện
```bash
pip install -r requirements.txt
```
### Bước 3: Tải dataset Kaggle
Tải 3 file từ Food.com Dataset và đặt vào data/raw/:
- RAW_recipes.csv
- RAW_interactions.csv
- ingr_map.pkl

### Bước 4: Chạy các phase theo thứ tự
# Phase 1: Xử lý data và train model (~10 phút)
python run_phase1_data.py

# Phase 4: Khởi tạo database
python run_phase4_db_init.py

# Phase 3: Chạy API server
python run_phase3_api.py

### Bước 5: Mở trình duyệt
Truy cập: http://localhost:8000/
