File này sẽ mô tả về bộ dữ liệu được cung cấp. 
# 1. Tổng quan:
Chúng ta sẽ có thông tin về:

- Dữ liệu thời tiết

- Dữ liệu về giá năng lượng liên quan

- Bản ghi của công suất pin mặt trời được lắp đặt (dung lượng pin mặt trời được lắp đặt).

- Sử dụng API thời tiết sẵn có

- Note: Hầu hết các biến số là giá trị **tổng** hoặc giá trị **trung bình** với **chu kỳ là 1 tiếng**. Các cột thời gian thì **luôn sử dụng chu kỳ 1 tiếng bắt đầu**. Đối với ` Dữ liệu thời tiết `, các biến như `weather` hay là `cloud cover` thì sẽ luôn sử dụng giá trị là **kết thúc 1 tiếng chu kỳ**. 

# 2. Các file:

## 2.1 `train.csv`

- `county`: ID của hạt.

> Bao nhiêu hạt? Mỗi hạt khác nhau có khác biệt như thế nào? 

- `product_type`: ID của loại hợp đồng, có 4 loại:

    - 0: Combined (Loại hợp đồng kết hợp)
    - 1: Fixed (Loại hợp đồng cố định)
    - 2: General service (Loại hợp đồng dịch vụ)
    - 3: Spot (Loại hợp đồng giao ngay)

> Ý nghĩa của từng loại hợp đồng này là gì? Các thông số khác có ảnh hưởng đến các loại hợp đồng này hay không? Các hợp đồng này có ảnh hưởng đến các chỉ số khác hay không (Cố tìm ra đặc điểm chung)? 

- `target`: Lượng năng lượng tiêu thụ hoặc sản xuất cho phân khúc của mỗi giờ. (Phân khúc được xác định bởi `county`, `is_business` và `product_type`).

> Như vậy có thể thấy rằng `target` chịu ảnh hưởng bởi 3 biến `county`, `is_business` và `product_type`

- `is_consumption`: Giá trị True/False cho biết rằng target có phải là người tiêu dùng hay là người sản xuất. 

> Các đối tượng này khác nhau ở điểm nào? Đề xuất giả thuyết, EDA để chứng minh các giả thuyết được đề ra