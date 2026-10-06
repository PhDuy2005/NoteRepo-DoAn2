# Re-planning

<a id="fr-replan-001"></a>
## FR-REPLAN-001 — Tái lập kế hoạch động khi có biến động

- **Mô tả:** Hệ thống phải cho phép sinh viên kích hoạt chức năng "Tái lập kế hoạch" (Re-plan) để sắp xếp lại các task chưa hoàn thành từ thời điểm hiện tại đến hết tuần.
- **Tiêu chí chấp nhận:**
  - Giữ nguyên 100% các phiên học đã hoàn thành trong quá khứ.
  - Chỉ phân bổ lại các phiên học chưa thực hiện vào các khung giờ rảnh còn lại của tuần.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.7, FR-REPLAN-001; được duyệt.

<a id="fr-replan-002"></a>
## FR-REPLAN-002 — Tự động kích hoạt đề xuất Re-plan khi có sai lệch

- **Mô tả:** Hệ thống nên hiển thị thông báo gợi ý tái lập lịch khi phát hiện có từ 02 phiên học bị Missed hoặc khi sinh viên thêm mới một lịch bận đột xuất trong tuần.
- **Tiêu chí chấp nhận:**
  - Xuất hiện thanh thông báo (Banner) gợi ý kèm nút bấm "Re-plan ngay".
- **Mức độ ưu tiên:** SHOULD.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.7, FR-REPLAN-002; được duyệt.
