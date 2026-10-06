# Schedule & Availability Management

<a id="fr-schedule-001"></a>
## FR-SCHEDULE-001 — Khai báo khung giờ bận cố định

- **Mô tả:** Hệ thống phải cho phép sinh viên tạo, sửa, xóa các khoảng thời gian bận cố định trong tuần (lịch học trên trường, ca làm việc, việc cá nhân).
- **Tiêu chí chấp nhận:**
  - Mỗi khung giờ bận gồm: Tên hoạt động, Thứ trong tuần, Giờ bắt đầu, Giờ kết thúc.
  - Hệ thống kiểm tra ràng buộc: Giờ kết thúc phải lớn hơn Giờ bắt đầu.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.2, FR-SCHEDULE-001; được duyệt.

<a id="fr-schedule-002"></a>
## FR-SCHEDULE-002 — Tự động tính toán quỹ thời gian rảnh (Available Slots)

- **Mô tả:** Hệ thống phải tự động tính toán các khoảng thời gian trống khả dụng (Available Slots) trong tuần bằng cách lấy toàn bộ thời gian trong ngày trừ đi các khung giờ bận cố định và khung giờ ngủ/nghỉ ngơi mặc định.
- **Tiêu chí chấp nhận:**
  - Hiển thị trực quan tổng số giờ rảnh khả dụng trong tuần trên giao diện.
  - Các slot rảnh không được giao thoa với bất kỳ khung giờ bận cố định nào.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.2, FR-SCHEDULE-002; được duyệt.

<a id="fr-schedule-003"></a>
## FR-SCHEDULE-003 — Thiết lập ngoại lệ theo ngày (Ad-hoc Availability)

- **Mô tả:** Hệ thống nên cho phép sinh viên đánh dấu nhanh một ngày cụ thể hoặc một buổi cụ thể là "Hoàn toàn bận" (Unavailable) đột xuất mà không làm ảnh hưởng đến mẫu lịch lặp lại hàng tuần.
- **Tiêu chí chấp nhận:**
  - Sinh viên có thể chọn một ngày trong tuần hiện tại và chuyển trạng thái thành "Nghỉ/Bận đột xuất".
- **Mức độ ưu tiên:** SHOULD.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.2, FR-SCHEDULE-003; được duyệt.
