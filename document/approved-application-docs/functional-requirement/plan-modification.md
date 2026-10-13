# Study Plan Interaction & Modification

<a id="fr-modify-001"></a>
## FR-MODIFY-001 — Chỉnh sửa trực tiếp phiên học trên lịch

- **Mô tả:** Hệ thống phải cho phép sinh viên kéo thả hoặc mở hộp thoại chỉnh sửa để thay đổi ngày, giờ bắt đầu, giờ kết thúc của bất kỳ Study Session nào trong kế hoạch.
- **Tiêu chí chấp nhận:**
  - Cập nhật thời gian session ngay lập tức trên giao diện người dùng.
  - Hiển thị cảnh báo nếu vị trí mới trùng với lịch bận cố định.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.5, FR-MODIFY-001; được duyệt.

<a id="fr-modify-002"></a>
## FR-MODIFY-002 — Xóa hoặc thêm mới phiên học thủ công

- **Mô tả:** Hệ thống phải cho phép sinh viên tự do xóa một phiên học do hệ thống gợi ý hoặc tạo thêm một phiên học thủ công cho một task bất kỳ.
- **Tiêu chí chấp nhận:**
  - Xóa session: Khối lượng thời gian tương ứng được hoàn trả lại vào Remaining Effort của task.
  - Thêm session: Thời lượng session được khấu trừ vào Remaining Effort của task.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.5, FR-MODIFY-002; được duyệt.
