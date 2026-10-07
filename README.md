Phân tích lỗi & Lập bảng Test Cases (trình bày trong README.md):
Đọc hiểu mã nguồn, xác định dòng lệnh sai logic và phân tích nguyên nhân kỹ thuật dẫn đến sự cố nghiệp vụ.
- const basePrice = bookingReservation.priceKey; -> Trong obj không có key priceKey dẫn đến undefined -> dẫn đến các giá trị sau bị sai 
Lập bảng 02 Test Cases đối chứng gồm các cột: Trường hợp kiểm thử, Dữ liệu đầu vào, Kết quả sai thực tế, Kết quả đúng mong đợi.

Trường hợp kiểm thử: Đề cho và chưa sửa
Dữ liệu đầu vào: 
const bookingReservation = {
  bookingId: "BK-2024-8891",
  guestName: "Trần Minh Quang",
  roomType: "Deluxe Ocean View",
  roomPrice: 1500000,
  checkInHour: 9
};
Kết quả sai thực tế:
Mã đặt phòng: BK-2024-8891
solution_ex1.js:22 Khách hàng: Trần Minh Quang
solution_ex1.js:23 Phụ thu nhận phòng sớm: NaN
solution_ex1.js:24 Tổng số tiền thanh toán: NaN
Kết quả đúng mong đợi:
Mã đặt phòng: BK-2024-8891
solution_ex1.js:22 Khách hàng: Trần Minh Quang
solution_ex1.js:23 Phụ thu nhận phòng sớm: 450000
solution_ex1.js:24 Tổng số tiền thanh toán: 1950000


Trường hợp kiểm thử: từ đề cho chuyển đổi giá khác
Dữ liệu đầu vào: 
const bookingReservation = {
  bookingId: "BK-2024-8891",
  guestName: "Trần Minh Quang",
  roomType: "Deluxe Ocean View",
  roomPrice: 1000000,
  checkInHour: 9
};
Kết quả sai thực tế:
Mã đặt phòng: BK-2024-8891
solution_ex1.js:22 Khách hàng: Trần Minh Quang
solution_ex1.js:23 Phụ thu nhận phòng sớm: NaN
solution_ex1.js:24 Tổng số tiền thanh toán: NaN
Kết quả đúng mong đợi:
Mã đặt phòng: BK-2024-8891
solution_ex1.js:22 Khách hàng: Trần Minh Quang
solution_ex1.js:23 Phụ thu nhận phòng sớm: 300000
solution_ex1.js:24 Tổng số tiền thanh toán: 1300000

