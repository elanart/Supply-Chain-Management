# Domestic Logistics System

## Overview
Hệ thống logistics nội địa được thiết kế để tối ưu hóa các hoạt động logistics trong nước, tập trung vào quy trình đơn giản hóa từ đặt hàng inbound đến giao hàng outbound. Hệ thống sẽ kết nối giữa bên logistics, nhà cung cấp, dịch vụ vận chuyển và khách hàng.

- **Mục tiêu**: Cung cấp một nền tảng tập trung để quản lý và tối ưu hóa các hoạt động logistics nội địa.
- **Tính năng chính**:
  - Quản lý thông tin nhà cung cấp, đánh giá và xếp hạng các nhà cung cấp.
  - Quản lý các đơn hàng nhập kho và xuất kho, theo dõi trạng thái của đơn hàng.
  - Quản lý kho và theo dõi tồn kho theo thời gian thực.
  - Quản lý việc vận chuyển hàng và thông tin đơn vị vận chuyển.
  - Quản lý đơn giá của hàng hóa và các chi phí liên quan đến vận chuyển và lưu trữ hàng tồn kho.
  - Quản lý hóa đơn cho các nhà cung cấp và đại lý.
  - Phân tích và báo cáo: Cung cấp các báo cáo chi tiết về tình trạng tồn kho, bao gồm mức tồn kho hiện tại, hàng hóa sắp hết hạn và hàng hóa hết hạn. Ngoài ra cần cung cấp các báo cáo về hiệu suất của các nhà cung cấp dựa trên các chỉ số như chất lượng, giao hàng đúng hạn và giá cả.
- **Nice to have**:
  - Kênh hỗ trợ khách hàng: Cung cấp các kênh hỗ trợ khách hàng để giải quyết các vấn đề liên quan đến đơn hàng, giao hàng và các vấn đề khác.
- **Phạm vi**: Giới hạn trong các hoạt động logistics nội địa.

## Pain Points
1. **Quy trình phức tạp**: Khó khăn trong việc phối hợp giữa các nhà cung cấp, vận chuyển và quản lý kho.
2. **Thiếu khả năng theo dõi**: Khó theo dõi trạng thái đơn hàng và tồn kho theo thời gian thực.
3. **Sai sót thủ công**: Dễ xảy ra lỗi trong quy trình xử lý đơn hàng và lưu trữ dữ liệu.
4. **Tối ưu nguồn lực kém**: Chưa sử dụng hiệu quả các nguồn lực vận chuyển và lưu trữ.

## Acceptance Criteria
1. **Quản lý Nhà cung cấp**:
   - Thêm/Sửa/Xóa nhà cung cấp.
   - Lưu trữ và quản lý thông tin chi tiết về nhà cung cấp như tên, địa chỉ, số điện thoại, thông tin liên hệ, và điều kiện thanh toán.
   - Đánh giá và xếp hạng nhà cung cấp dựa trên các tiêu chí như chất lượng, giao hàng đúng hạn và giá cả.

2. **Quản lý Đơn hàng**:
   - Tạo đơn hàng nhập/xuất kho và gửi đến nhà cung cấp/đại lý để xác nhận và theo dõi trạng thái đơn hàng.
   - Cung cấp tính năng xác nhận hoặc hủy đơn hàng trong các trường hợp cần thiết.
   - Cập nhật trạng thái đơn hàng theo thời gian thực.

3. **Quản lý Kho**:
   - Theo dõi số lượng hàng tồn kho.
   - Kiểm tra và cập nhật số lượng hàng trong kho khi có đơn hàng nhập/xuất kho.
   - Cung cấp thông tin về hàng hóa sắp hết hạn hoặc đã hết hạn.

4. **Quản lý Giao hàng & đơn vị vận chuyển**:
   - Lên lịch và tổ chức giao hàng từ kho đến các địa điểm yêu cầu.
   - Theo dõi tình trạng và vị trí hàng hóa trong quá trình vận chuyển.
   - Quản lý thông tin và đánh giá hiệu suất đối tác vận chuyển.

5. **Quản lý Đơn giá & Thanh toán**:
   - Theo dõi và quản lý đơn giá của hàng hóa từ các nhà cung cấp và chi phí liên quan đến vận chuyển và kho bãi.
   - Quản lý thanh toán và hóa đơn, bao gồm các khoản phải trả và phải thu.

6. **Báo Cáo & Phân Tích**:
   - Báo cáo chi tiết về tình trạng tồn kho, bao gồm mức tồn kho hiện tại, hàng hóa sắp hết hạn và hàng hóa hết hạn.
   - Báo cáo hiệu suất nhà cung cấp dựa trên các chỉ số như chất lượng, giao hàng đúng hạn và giá cả.

## Requirements

### Functional Requirements
1. **Quản lý Nhà cung cấp**:
   - Thêm/Sửa/Xóa thông tin nhà cung cấp.
   - Theo dõi hiệu suất và xếp hạng nhà cung cấp.

2. **Quản lý Đơn hàng**:
   - Tạo, xác nhận, hủy và cập nhật đơn hàng nhập/xuất kho.
   - Theo dõi trạng thái đơn hàng theo thời gian thực.

3. **Quản lý Kho**:
   - Theo dõi và cập nhật tồn kho tự động.
   - Quản lý hàng hóa sắp hết hạn hoặc đã hết hạn.

4. **Quản lý Giao hàng**:
   - Lên lịch và theo dõi vận chuyển.
   - Quản lý thông tin và hiệu suất đối tác vận chuyển.

5. **Quản lý Thanh toán**:
   - Theo dõi đơn giá và chi phí vận hành.
   - Quản lý hóa đơn và thanh toán.

6. **Báo cáo & Phân tích**:
   - Tạo báo cáo chi tiết về tồn kho và hiệu suất nhà cung cấp.

### Non-Functional Requirements
1. **Hiệu năng**:
   - Hỗ trợ tối đa 1,000 đơn hàng đang hoạt động đồng thời.
   - Thời gian phản hồi dưới 2 giây cho các tác vụ thông thường.

2. **Bảo mật**:
   - Mã hóa dữ liệu nhạy cảm.
   - Tuân thủ các quy định bảo mật dữ liệu nội địa.

3. **Khả năng Mở rộng**:
   - Cho phép tích hợp thêm dịch vụ hoặc tăng số lượng người dùng trong tương lai.

4. **Khả dụng**:
   - Đảm bảo hệ thống hoạt động ổn định với thời gian uptime 99.5%.

## Timeline
1. **Phase 1: Thiết kế Boilerplate & xây dựng Flow và Core Data Model (Tuần 1)**:
   - Thiết lập kiến trúc dự án và cài đặt các công cụ phát triển cơ bản.
   - Định nghĩa luồng chảy các quy trình nghiệp vụ.
   - Xây dựng các model dữ liệu chính và quan hệ giữa chúng.

2. **Phase 2: Implement Code & Testing (Tuần 2 - 4)**:
   - Phát triển các tính năng theo Functional Requirements.
   - Tích hợp API cần thiết.
   - Kiểm tra chức năng, bảo mật và hiệu năng.
   - Sửa lỗi và tinh chỉnh hệ thống.

3. **Phase 3: Deploy và Maintain (Tuần 5  - 6)**:
   - Triển khai sản phẩm và theo dõi hiệu quả.
   - Xử lý vấn đề phát sinh và cải thiện tính năng.
