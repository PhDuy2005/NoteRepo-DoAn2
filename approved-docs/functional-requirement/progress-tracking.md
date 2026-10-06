# Progress Tracking

<a id="fr-progress-001"></a>
## FR-PROGRESS-001 — Ghi nhận hoàn thành phiên học (Check-in / Complete)

- **Mô tả:** Hệ thống phải cung cấp thao tác 1-chạm (1-click) để sinh viên đánh dấu một Study Session là đã hoàn thành (Completed).
- **Tiêu chí chấp nhận:**
  - Trạng thái session chuyển sang Completed trên lịch giao diện.
  - Remaining Effort của task tương ứng tự động giảm trừ bằng đúng thời lượng session.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.6, FR-PROGRESS-001; được duyệt.

<a id="fr-progress-002"></a>
## FR-PROGRESS-002 — Ghi nhận tiến độ dở dang hoặc bỏ lỡ phiên học

- **Mô tả:** Hệ thống phải cho phép sinh viên ghi nhận khi phiên học không hoàn thành trọn vẹn: nhập số giờ thực tế đã học (Partially Completed) hoặc đánh dấu bỏ lỡ (Missed).
- **Tiêu chí chấp nhận:**
  - Khi chọn Missed, Remaining Effort của task giữ nguyên, session được đánh dấu màu xám/đỏ.
  - Khi chọn Partially Completed, sinh viên có thể nhập số phút thực tế đã học.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.6, FR-PROGRESS-002; được duyệt.

<a id="fr-progress-003"></a>
## FR-PROGRESS-003 — Tổng kết tiến độ tuần (Weekly Progress Summary)

- **Mô tả:** Hệ thống nên hiển thị bảng tóm tắt ngắn về mức độ tuân thủ kế hoạch trong tuần: Số giờ đã học thực tế / Số giờ đã lên kế hoạch, Tỷ lệ phiên học hoàn thành (%).
- **Tiêu chí chấp nhận:**
  - Hiển thị trực quan ở góc màn hình lịch tuần.
- **Mức độ ưu tiên:** SHOULD.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.6, FR-PROGRESS-003; được duyệt.
