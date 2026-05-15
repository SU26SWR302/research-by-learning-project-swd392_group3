````md
# CrownDine - Hệ Thống Quản Lý Nhà Hàng Thông Minh

**CrownDine** là một giải pháp quản lý nhà hàng hiện đại và toàn diện, được thiết kế nhằm tối ưu hóa quy trình vận hành từ đặt bàn, gọi món đến quản lý bếp và thanh toán. Tích hợp AI cùng công nghệ thời gian thực, CrownDine mang đến trải nghiệm liền mạch cho cả khách hàng lẫn nhân viên.

---

# Tính Năng Nổi Bật

## Đặt Bàn Thông Minh

- Quy trình đặt bàn trực quan theo từng bước.
- Bản đồ bàn ăn tương tác cho phép khách hàng chọn vị trí mong muốn.
- Giao diện Calendar View chuyên nghiệp giúp nhân viên quản lý lịch đặt bàn dễ dàng.

## Menu Điện Tử & Gọi Món

- Menu điện tử sinh động với hình ảnh chất lượng cao và mô tả chi tiết.
- Hệ thống giỏ hàng linh hoạt và tùy chỉnh món ăn.
- Tìm kiếm và lọc món ăn mạnh mẽ theo danh mục.

## Hệ Thống Hiển Thị Nhà Bếp (KDS)

- Cập nhật trạng thái món ăn theo thời gian thực.
- Nhóm món theo từng “batch” theo thứ tự thời gian để tối ưu quy trình chế biến.
- Thông báo ngay lập tức cho nhân viên khi món ăn sẵn sàng phục vụ.

## Quản Lý Thu Ngân & Thanh Toán

- Quản lý hóa đơn nhanh chóng, hỗ trợ gộp và tách bàn.
- Tích hợp PayOS (QR Code, chuyển khoản ngân hàng).
- Báo cáo doanh thu định kỳ và xuất dữ liệu Excel.

## Chatbot AI Quản Trị

- Tích hợp Google Gemini AI để phân tích dữ liệu.
- Hỏi đáp về hiệu suất kinh doanh, tồn kho và dự đoán khách hàng.

## Bảo Mật & Phân Quyền

- Phân quyền chi tiết: Admin, Nhân viên, Bếp, Khách hàng.
- Xác thực bảo mật bằng JWT và Google OAuth2.

---

# Quy Trình Hoạt Động Hệ Thống

## 1. Hành Trình Đặt Bàn Của Khách Hàng

CrownDine cung cấp trải nghiệm đặt bàn liền mạch qua 4 bước:

### Bước 1: Chọn ngày & giờ

Khách hàng chọn ngày và khung giờ muốn đến. Hệ thống kiểm tra tình trạng bàn trống theo thời gian thực.

### Bước 2: Chọn bàn

Xem bản đồ nhà hàng tương tác với độ chi tiết cao. Khách hàng có thể chọn bàn yêu thích theo tầng, khu vực và số lượng chỗ ngồi.

### Bước 3: Đặt món trước

Duyệt menu điện tử và thêm món ăn vào đơn đặt bàn. Điều này giúp nhà bếp chuẩn bị trước để phục vụ nhanh hơn.

### Bước 4: Thanh toán

Xác nhận thông tin và thanh toán qua PayOS. Sau khi thanh toán thành công, hệ thống sẽ cấp mã QR hoặc xác nhận đặt bàn.

## 2. Vận Hành Nhà Bếp & Nhân Viên

- Đồng bộ thời gian thực: Khi khách hàng thanh toán hoặc nhân viên tạo đơn trực tiếp, Kitchen Display System (KDS) sẽ cập nhật ngay lập tức thông qua WebSocket.

- Phân nhóm đơn hàng: Nhà bếp nhận món ăn được nhóm theo thời gian chuẩn bị hoặc mức độ ưu tiên nhằm tối ưu quy trình nấu nướng.

- Vòng lặp thông báo: Khi bếp đánh dấu món là “Ready”, nhân viên sẽ nhận thông báo toast ngay trên giao diện frontend để phục vụ khách.

## 3. Quản Lý Bằng AI

Admin Chatbot (Gemini) không chỉ trả lời câu hỏi mà còn phân tích tình trạng đặt bàn hiện tại, món ăn phổ biến và khung giờ cao điểm để đưa ra các gợi ý hữu ích cho chủ nhà hàng.

---

# Công Nghệ Sử Dụng

## Backend (Hệ Sinh Thái Java)

- Framework: Spring Boot 3.5+
- Bảo mật: Spring Security, JWT, OAuth2
- Cơ sở dữ liệu: MySQL 8.0
- Migration: Flyway
- Realtime: Spring WebSocket (STOMP)
- Tích hợp AI: Spring AI (Google GenAI)
- Cloud: Cloudinary (Lưu trữ hình ảnh)
- Thanh toán: Tích hợp PayOS

## Frontend (Web Hiện Đại)

- Framework: React 19 (Vite)
- Ngôn ngữ: TypeScript
- Giao diện: Tailwind CSS 4, Radix UI, Lucide Icons
- Quản lý State: Zustand
- Lấy dữ liệu: React Query (TanStack)
- Form: React Hook Form + Zod
- Biểu đồ: Recharts
- Thông báo: Sonner, React Toastify

---

# Cài Đặt & Khởi Chạy

## Yêu Cầu

- JDK 21+
- Node.js 20+
- MySQL 8.x

## 1. Backend

```bash
cd backend

# Cấu hình application-dev.yml với thông tin DB, Cloudinary và PayOS
./mvnw spring-boot:run
````

## 2. Frontend

```bash
cd frontend

npm install
npm run dev
```

---

# Giấy Phép

Dự án này được phát hành theo giấy phép MIT License.

---

# Liên Hệ

* Author: Crowndine
* Email: [Crowdine@gmail.com](mailto:Crowdine@gmail.com)
* Website: Crowndine.com

---

Developed with ❤️ by the CrownDine Team.

```
```
