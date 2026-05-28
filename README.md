# 🍳 Smart Recipe Recommendation System

Hệ thống gợi ý món ăn cá nhân hóa dựa trên nguyên liệu bạn có sẵn.

## 📖 Giới thiệu

Bạn mở tủ lạnh thấy có trứng, cà chua, hành — không biết nấu gì? Project này giải quyết đúng vấn đề đó.

Nhập nguyên liệu bạn có → AI gợi ý món ngon phù hợp nhất, kèm giải thích lý do và danh sách nguyên liệu còn thiếu.

## ✨ Tính năng chính

- 🔍 Gợi ý món ăn theo nguyên liệu sẵn có
- 🤖 Cá nhân hóa theo lịch sử yêu thích của user
- 💡 Giải thích lý do gợi ý (Explainable AI)
- 🎨 Khám phá món ăn theo 20 nhóm tương đồng
- ⚡ Autocomplete nguyên liệu real-time

## 🛠️ Công nghệ

**Backend:** Python, FastAPI, scikit-learn, FAISS, mlxtend, SQLite
**Frontend:** HTML, CSS, Vanilla JavaScript
**Dataset:** [Food.com - 230K recipes, 1.1M interactions](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)

## 🚀 Chạy thử

```bash
# 1. Cài thư viện
pip install -r requirements.txt

# 2. Tải dataset Kaggle vào thư mục data/raw/
#    (RAW_recipes.csv, RAW_interactions.csv, ingr_map.pkl)

# 3. Chạy lần lượt
python run_phase1_data.py      # Xử lý data + train model
python run_phase4_db_init.py   # Khởi tạo database
python run_phase3_api.py       # Khởi động server

# 4. Mở http://localhost:8000/
```

## 📄 License

MIT
