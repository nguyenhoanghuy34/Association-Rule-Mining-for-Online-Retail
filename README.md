🛒 Association Rule Mining for Online Retail
🎯 Mục tiêu

Dự án nhằm khai thác các quy luật kết hợp giữa các sản phẩm trong dữ liệu bán lẻ online.
Bằng cách áp dụng thuật toán FP-Growth, mô hình giúp nhận diện những sản phẩm thường được mua cùng nhau, phục vụ:

💡 Gợi ý sản phẩm (recommendation).

🏷️ Bán chéo (cross-selling) và bố trí trưng bày hợp lý.

📊 Dữ liệu

Nguồn: Online Retail II Dataset (UCI Machine Learning Repository)

Các cột chính:

Invoice: Mã hóa đơn.

StockCode: Mã sản phẩm.

Description: Tên sản phẩm.

Quantity: Số lượng bán.

InvoiceDate: Thời gian giao dịch.

Price: Giá đơn vị.

Customer ID: Mã khách hàng.

Country: Quốc gia.

⚙️ Các bước thực hiện

🧹 Tiền xử lý dữ liệu

Loại bỏ giá trị null và hóa đơn trả hàng.

Biến đổi dữ liệu thành dạng giỏ hàng (basket).

🔍 Áp dụng thuật toán FP-Growth

Phát hiện các frequent itemsets – nhóm mặt hàng thường được mua cùng nhau.

📈 Sinh luật kết hợp (Association Rules)

Tính các chỉ số: support, confidence, lift.

Giữ lại các luật có lift > 1.2 để xác định mối liên hệ mạnh nhất.

🧩 Kết quả

Sản phẩm “WHITE HANGING HEART T-LIGHT HOLDER” và “REGENCY CAKESTAND 3 TIER” có tần suất xuất hiện cao nhất.

Nhiều cặp sản phẩm đạt lift > 1.2, cho thấy khả năng được mua cùng nhau rất lớn.

🧠 Công nghệ sử dụng

Python: Pandas, NumPy, mlxtend, Matplotlib

Môi trường: Jupyter Notebook / Google Colab

💬 Ý nghĩa

Phân tích giúp doanh nghiệp hiểu hành vi mua sắm, tối ưu gợi ý sản phẩm, và tăng doanh thu qua bán chéo.
