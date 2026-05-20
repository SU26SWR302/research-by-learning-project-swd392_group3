# CrownDine - Hệ Thống Quản Lý Nhà Hàng Thông Minh

**CrownDine** là hệ thống quản lý nhà hàng hiện đại giúp tối ưu quy trình đặt bàn, gọi món, vận hành bếp và thanh toán. Hệ thống tích hợp AI và công nghệ realtime nhằm mang lại trải nghiệm mượt mà cho cả khách hàng và nhân viên.

---

# Tính Năng Chính

## Đặt Bàn Thông Minh

- Quy trình đặt bàn theo từng bước đơn giản.
- Bản đồ bàn ăn tương tác cho phép khách hàng tự chọn vị trí.
- Calendar View hỗ trợ nhân viên quản lý lịch đặt bàn hiệu quả.

## Menu Điện Tử & Gọi Món

- Menu điện tử với hình ảnh và mô tả chi tiết.
- Giỏ hàng linh hoạt, hỗ trợ tùy chỉnh món ăn.
- Tìm kiếm và lọc món theo danh mục.

## Kitchen Display System (KDS)

- Đồng bộ trạng thái món ăn theo thời gian thực.
- Nhóm món theo batch để tối ưu quy trình chế biến.
- Thông báo ngay khi món sẵn sàng phục vụ.

## Thanh Toán & Thu Ngân

- Hỗ trợ gộp bàn, tách hóa đơn.
- Tích hợp PayOS (QR Code, chuyển khoản).
- Báo cáo doanh thu và xuất dữ liệu Excel.

## AI Chatbot Quản Trị

- Tích hợp Google Gemini AI.
- Hỗ trợ phân tích doanh thu, món ăn phổ biến và dự đoán lượng khách.

## Bảo Mật & Phân Quyền

- Phân quyền: Admin, Staff, Kitchen, Customer.
- Xác thực bằng JWT và Google OAuth2.

---

# Quy Trình Hoạt Động

## Quy Trình Đặt Bàn

1. Chọn ngày và thời gian.
2. Chọn bàn trên bản đồ tương tác.
3. Đặt món trước từ menu điện tử.
4. Thanh toán qua PayOS và nhận xác nhận đặt bàn.

## Vận Hành Nhà Hàng

- Hệ thống đồng bộ dữ liệu realtime bằng WebSocket.
- Bếp nhận đơn theo mức độ ưu tiên.
- Nhân viên nhận thông báo khi món hoàn thành.

## Quản Lý Bằng AI

Chatbot AI hỗ trợ phân tích dữ liệu vận hành, khung giờ cao điểm và xu hướng khách hàng để hỗ trợ ra quyết định.

---

# Công Nghệ Sử Dụng

## Backend

- Spring Boot 3.5+
- Spring Security, JWT, OAuth2
- MySQL 8
- Flyway
- Spring WebSocket (STOMP)
- Spring AI (Google GenAI)
- Cloudinary
- PayOS

## Frontend

- React 19 + Vite
- TypeScript
- Tailwind CSS 4
- Radix UI, Lucide Icons
- Zustand
- React Query
- React Hook Form + Zod
- Recharts

---

# Giấy Phép

Dự án được phát hành theo giấy phép MIT License.

---
# Liên Hệ

- Author: Crowndine
- Email: Crowdine@gmail.com
- Website: Crowndine.com
- Jira: [Crowndine Jira Workspace](https://vuxducgiang.atlassian.net/?continue=https%3A%2F%2Fvuxducgiang.atlassian.net%2Fwelcome%2Fsoftware%3FprojectId%3D10000&atlOrigin=eyJpIjoiY2E3M2MzNjViZGVmNDBiNGIzYjZlZDZhMmE5NmU1YjQiLCJwIjoiamlyYS1zb2Z0d2FyZSJ9)
```
