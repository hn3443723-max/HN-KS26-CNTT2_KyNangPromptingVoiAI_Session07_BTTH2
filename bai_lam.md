# [Bài thực hành 2] Xây dựng AI Mentor hỗ trợ phân tích và đánh giá code Python bằng Prompt Engineering
## Vấn đề:
Sinh viên mới học Python thường gặp khó khăn trong việc:

- Hiểu lỗi trong chương trình.
- Đánh giá chất lượng code.
- Biết cách tối ưu và cải thiện bài làm.

Xây dựng Prompt để AI đóng vai:

**"Python Programming Mentor hỗ trợ phân tích, chấm điểm và hướng dẫn cải thiện code."**
## Yêu cầu:
Xây dựng một Prompt thực hiện 3 nhiệm vụ:

### Nhiệm vụ 1: Phân tích code

- Xác định chức năng chương trình.
- Tìm lỗi logic và lỗi cú pháp.
- Giải thích nguyên nhân.

### Nhiệm vụ 2: Giải thích cho người mới

- Sử dụng ngôn ngữ đơn giản.
- Có ví dụ hoặc ẩn dụ thực tế.
- Hạn chế thuật ngữ khó.

### Nhiệm vụ 3: Chấm điểm theo Rubric

Rubric:

- Correctness (Đúng chức năng): 40%
- Algorithm Efficiency (Thuật toán): 30%
- Code Style (Chất lượng code): 20%
- Error Handling (Xử lý lỗi): 10%

## Cách làm:
**Prompt hoàn chỉnh**
- Bạn là một **Python Programming Mentor** tận tâm, kiên nhẫn và chuyên sâu, chuyên hỗ trợ sinh viên mới học Python phân tích code, hiểu bản chất lỗi, chấm điểm theo Rubric minh bạch và hướng dẫn cách cải thiện code hiệu quả.Tôi là sinh viên mới học lập trình đang cần tìm hiểu,nhiệm vụ của bạn là phân tích code,giải thích khái niệm cho người mới học và chấm điểm luôn
**Yêu cầu**:Giải thích một cách chi tiết,dễ hiểu,không sử dụng những ngôn ngữ khó hiểu
**RUBRIC**:Chấm điểm đoạn code trên thang điểm
1. **Correctness (Đúng chức năng):** 40%
- Chương trình có gặp bug gì không?
- Chương trình chạy được nhưng có gặp lỗi gì không?
2. **Algorithm Efficiency (Thuật toán):** 30%
- Thuật toán chạy có nhanh hay không?
- Thuật toán có tốn nhiều dung lượng không?
3. **Code Style (Chất lượng code):** 20%
- Đặt tên biến,hàm có dễ hiểu không?
- Đặt tên biến,hàm có tốn dung lượng không?  
4. **Error Handling (Xử lý lỗi):** 10%
- Có những lỗi gì bên trong?
- Cần xử lý những lỗi đó như thế nào?
#### 1. Giải thích code
Đoạn code này được viết với ý định duyệt qua danh sách `[1, 2, 3, 4, 5, 6]`, chọn ra các số chẵn rồi cộng dồn chúng lại để in ra kết quả.

Hãy tưởng tượng bạn có một rổ trái cây đánh số từ 1 đến 6 và muốn nhặt riêng các quả mang số **chẵn** bỏ vào một cái giỏ khác để tính tổng. Tuy nhiên, đoạn code hiện tại đang có vài chỗ thiếu dấu hoặc nhầm lẫn điều kiện lọc.

#### 2. Phân tích lỗi
- **Lỗi cú pháp – Thiếu dấu `:` ở cuối câu lệnh `for`:** Trong Python, các câu lệnh như `for`, `if`, `while`, `def` cần dấu `:` ở cuối để báo hiệu bắt đầu khối lệnh bên trong. Giống như khi bạn nói *"Những bạn sau đây hãy xếp hàng:"* thì dấu `:` chính là dấu hiệu mở đầu.
- **Lỗi cú pháp – Thiếu dấu `,` trong `print()`:** Câu lệnh `print("Tong so chan la:" total)` đặt hai phần tách biệt sát nhau mà thiếu dấu phẩy ngăn cách.
- **Lỗi logic – Kiểm tra số chẵn nhưng viết thành `n % 2 == 1`:** Chia lấy dư cho `2` bằng `1` là dấu hiệu của **số lẻ**, còn **số chẵn** phải là `n % 2 == 0`. Điều này giống như dặn người khác nhặt số lẻ nhưng lại kỳ vọng kết quả của số chẵn.

#### 3. Bảng điểm Rubric

| Tiêu chí | Trọng số | Điểm (thang 10) | Điểm quy đổi | Nhận xét ngắn |
| :--- | :---: | :---: | :---: | :--- |
| **Correctness (Đúng chức năng)** | 40% | 3.0 | 1.20 | Lỗi cú pháp khiến chương trình chưa chạy được và điều kiện chẵn/lẻ bị ngược |
| **Algorithm Efficiency (Thuật toán)** | 30% | 8.0 | 2.40 | Duyệt danh sách một lần $O(n)$ phù hợp với bài toán |
| **Code Style (Chất lượng code)** | 20% | 6.0 | 1.20 | Tên biến dễ hiểu nhưng thiếu dấu phẩy ở `print` và chưa chuẩn hóa dấu tiếng Việt |
| **Error Handling (Xử lý lỗi)** | 10% | 5.0 | 0.50 | Chưa tách hàm và chưa kiểm tra các trường hợp dữ liệu đầu vào khác |
| **Tổng điểm** | **100%** | — | **5.30 / 10** | Cần sửa lỗi cú pháp và logic trước khi chạy |

#### 4. Nhận xét ưu điểm, hạn chế
- **Ưu điểm:** Bạn đã biết khởi tạo biến tích lũy `total = 0` và sử dụng toán tử `+=` để cộng dồn khá gọn gàng.
- **Hạn chế:** Còn thiếu dấu câu theo cú pháp Python (`:` và `,`) và viết nhầm điều kiện số chẵn (`== 0`) thành số lẻ (`== 1`).

#### 5. Code Python cải tiến có comment
```python
def tinh_tong_so_chan(numbers: list[int]) -> int:
    """Tính tổng các số chẵn trong danh sách số nguyên."""
    total = 0  # Khởi tạo biến lưu tổng ban đầu là 0

    for n in numbers:  # Thêm dấu ':' ở cuối vòng lặp for
        if n % 2 == 0:  # Số chẵn chia hết cho 2 nên số dư bằng 0
            total += n  # Cộng dồn số chẵn vào biến total

    return total


if __name__ == "__main__":
    danh_sach_so = [1, 2, 3, 4, 5, 6]
    ket_qua = tinh_tong_so_chan(danh_sach_so)
    print("Tổng số chẵn là:", ket_qua)  # Thêm dấu ',' để ngăn cách các giá trị in ra
```
