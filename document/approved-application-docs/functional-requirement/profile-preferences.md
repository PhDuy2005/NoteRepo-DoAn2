# Profile & Preference Management

<a id="fr-profile-001"></a>
## FR-PROFILE-001 — Quản lý thông tin học tập cá nhân

- **Mô tả:** Hệ thống phải cho phép sinh viên tạo mới, xem và cập nhật thông tin hồ sơ cơ bản (Họ tên, chuyên ngành, ghi chú cá nhân).
- **Tiêu chí chấp nhận:**
  - Dữ liệu hồ sơ được lưu trữ bền vững và hiển thị đúng khi sinh viên truy cập lại.
  - Cho phép cập nhật thông tin bất cứ lúc nào.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.1, FR-PROFILE-001; được duyệt.

<a id="fr-profile-002"></a>
## FR-PROFILE-002 — Cấu hình sở thích và tham số lập lịch

- **Mô tả:** Hệ thống phải cho phép sinh viên cấu hình các tham số lập lịch cá nhân: Thời lượng phiên học mong muốn (Target Session Duration: 30–120 phút), Số giờ học tối đa trong ngày (Max Hours/Day: 1–12 giờ), Khung giờ học ưa thích trong ngày (Buổi sáng / Buổi chiều / Buổi tối).
- **Tiêu chí chấp nhận:**
  - Hệ thống chặn nhập các giá trị vô lý (ví dụ: số giờ học/ngày > 16 giờ hoặc thời lượng session < 15 phút).
  - Các tham số này được truyền trực tiếp làm ràng buộc cho Planning Agent khi sinh lịch.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.1, FR-PROFILE-002; được duyệt.
