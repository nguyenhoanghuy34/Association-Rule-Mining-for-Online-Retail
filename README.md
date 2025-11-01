# 🛒 Association Rule Mining for Online Retail

**Khai thác quy luật kết hợp sản phẩm bằng thuật toán FP-Growth**

---

## 🎯 Mục tiêu

Dự án nhằm khai thác các **quy luật kết hợp** giữa các sản phẩm trong dữ liệu bán lẻ online.  
Bằng cách áp dụng **thuật toán FP-Growth**, mô hình giúp nhận diện những sản phẩm **thường được mua cùng nhau**, phục vụ:

- 💡 **Gợi ý sản phẩm** (Recommendation System)
- 🏷️ **Bán chéo (Cross-selling)** và **bố trí trưng bày hợp lý**

---

## 📊 Dữ liệu

**Nguồn**: [Online Retail II Dataset - UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

### Các cột chính:
| Cột            | Mô tả                     |
|----------------|---------------------------|
| `Invoice`      | Mã hóa đơn                |
| `StockCode`    | Mã sản phẩm               |
| `Description`  | Tên sản phẩm              |
| `Quantity`     | Số lượng bán              |
| `InvoiceDate`  | Thời gian giao dịch       |
| `Price`        | Giá đơn vị                |
| `Customer ID`  | Mã khách hàng             |
| `Country`      | Quốc gia                  |

---

## ⚙️ Các bước thực hiện

1. **Tiền xử lý dữ liệu**  
   - Loại bỏ giá trị `null`, hóa đơn trả hàng (`Invoice` bắt đầu bằng 'C')  
   - Biến đổi dữ liệu thành **dạng giỏ hàng (basket)**

2. **Áp dụng FP-Growth**  
   - Tìm **frequent itemsets** (các tập hợp sản phẩm thường xuất hiện cùng nhau)

3. **Sinh Association Rules**  
   - Tính: `support`, `confidence`, `lift`  
   - Lọc các luật có **`lift > 1.2`** → mối quan hệ mạnh

---

## 🧩 Kết quả nổi bật

- Sản phẩm xuất hiện nhiều nhất:  
  `WHITE HANGING HEART T-LIGHT HOLDER`, `REGENCY CAKESTAND 3 TIER`
- Nhiều cặp sản phẩm có `lift > 1.2` → **xu hướng mua chung rõ rệt**

---

## 🧠 Công nghệ sử dụng

| Công cụ         | Mục đích                     |
|----------------|------------------------------|
| Python         | Xử lý dữ liệu & mô hình      |
| Pandas, NumPy  | Tiền xử lý                   |
| `mlxtend`      | FP-Growth & Association Rules|
| Matplotlib     | Trực quan hóa                |
| Jupyter/Colab  | Môi trường phát triển        |

---

## 🚀 Cách chạy dự án

### 1. Clone repository
```bash
git clone https://github.com/your-username/online-retail-fpgrowth.git
cd online-retail-fpgrowth
