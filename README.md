# jmeter
# Báo cáo Thực hành Kiểm thử Hiệu năng với Apache JMeter

**Người kiểm thử:** Nguyễn Xuân Thanh  

## 1. Mục tiêu thực hành
- Sử dụng Apache JMeter để kiểm thử hiệu năng (Performance/Load Testing) cho hệ thống API.
- Đánh giá khả năng chịu tải của API `GET https://reqres.in/api/users?page=2` khi có nhiều người dùng truy cập đồng thời.

## 2. Kịch bản kiểm thử (Test Plan)
- **Công cụ sử dụng:** Apache JMeter 5.6.3
- **Cấu hình Thread Group (Giả lập người dùng):**
  - **Number of Threads (Users):** 10 (Giả lập 10 người dùng truy cập cùng lúc).
  - **Ramp-up period:** 2 giây.
  - **Loop Count:** 1 lần.

## 3. Kết quả kiểm thử

### 3.1. Chi tiết từng Request (View Results Tree)
- Cả 10 lượt gọi API đều được server xử lý thành công (trả về mã 200 OK và đúng định dạng JSON).
*<img width="1018" height="569" alt="Screenshot 2026-10-07 103731" src="https://github.com/user-attachments/assets/ed433629-cfd6-4242-8b13-69800859f6ba" />
*

### 3.2. Bảng thống kê tổng quan (Summary Report)
- **Tổng số lượng Request (Samples):** 10
- **Thời gian phản hồi trung bình (Average):** 202 ms
- **Tỷ lệ lỗi (Error %):** 0.00%
- **Kết luận:** Hệ thống hoạt động rất ổn định, không có request nào bị rớt (fail) dưới mức tải này.
*<img width="1011" height="568" alt="Screenshot 2026-10-07 103751" src="https://github.com/user-attachments/assets/4532012b-13d4-4e01-ab26-1d22e9ffd7d9" />
*
