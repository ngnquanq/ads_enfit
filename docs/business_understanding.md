Mục tiêu của file này là để **đưa ra các câu hỏi cần trả lời** để có thể **hiểu được những gì doanh nghiệp muốn nhắm tới** và **hiểu được các tác nhân quan trọng**.

# 1. Goal

Tạo ra một mô hình **dự đoán mức tiêu thụ năng lượng** cho các nhà tiêu dùng nhằm **giảm thiểu chi phí mất cân bằng năng lượng**. 

**Mất cân bằng năng lượng**: Xuất hiện khi **lượng điện dự đoán tiêu thụ khác với lượng điện năng đo lường được**. Và các nhà tiêu dùng (vừa tiêu thụ, vừa tạo ra năng lượng) đóng góp không nhỏ vào sự mất cân bằng này. **Mặc dù chiếm tỉ số nhỏ, lượng điện tiêu thụ khó đoán của prosumers gây ra ảnh hưởng không nhỏ đối với logistics và tài chính của các công ty năng lượng.**


# 2. Giới thiệu về vấn đề đang gặp phải

Cho đến thời điểm hiện tại, Enefit đang gặ phải vấn đề là **các mô hình dự đoán của họ chưa tốt**. Nguyên nhân mà họ **dự đoán là do chưa thật sự tính hết tất cả các biến số liên quan** gây ảnh hưởng đến hành vi của prosumer. 

# 3. Thước đo đánh giá

Bài toán này sử dụng thước đo là chỉ số Mean Absolute Error (MAE) giữa năng lượng được dự đoán và năng lượng thực tế được ghi nhận. 


$$ MAE = \frac{1}{n} \sum_{i=1}^n |y_i - \hat{y}_i| $$

**Note**: Objective của bài toán không phải là để tối thiểu giá trị của thước đo này, khi một thước đo trở thành tiêu chuẩn, thước đo đó không còn là thước đo chuẩn nữa. 

# 4. Câu hỏi đặt ra
