# Course & Task Management

<a id="fr-task-001"></a>
## FR-TASK-001 — Quản lý danh mục môn học

- **Mô tả:** Hệ thống phải cho phép sinh viên thêm, sửa, xóa và hiển thị danh sách các môn học trong học kỳ.
- **Tiêu chí chấp nhận:**
  - Mỗi môn học gồm: Tên môn, Mã môn học (Tùy chọn), Màu sắc nhận diện (Color tag).
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.3, FR-TASK-001; được duyệt.

<a id="fr-task-002"></a>
## FR-TASK-002 — Quản lý danh sách task học thuật

- **Mô tả:** Hệ thống phải cho phép sinh viên tạo, chỉnh sửa, xóa và theo dõi trạng thái các task học thuật.
- **Tiêu chí chấp nhận:**
  - Mỗi task bao gồm các trường bắt buộc: Tên task, Môn học liên kết, Phân loại (Assignment, Project, Quiz/Exam, Khác), Hạn chót (Deadline: ngày & giờ), Thời gian ước lượng (Estimated Effort tính bằng giờ), Hệ số mức độ quan trọng từ 1,0 đến 5,0 theo bước 0,1.
  - Hệ số mức độ quan trọng chỉ nhận giá trị trong khoảng 1,0–5,0 với bước tăng 0,1; giá trị cao hơn biểu thị task quan trọng hơn.
  - Deadline phải là thời gian trong tương lai tại thời điểm tạo task.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.3, FR-TASK-002; yêu cầu được duyệt. Trường mức độ quan trọng được đồng bộ theo UN-11 đã duyệt; thay thế các nhãn mức trong bản nguồn.

<a id="fr-task-003"></a>
## FR-TASK-003 — Cập nhật và lưu vết Remaining Effort

- **Mô tả:** Hệ thống phải duy trì trường dữ liệu "Thời gian còn lại cần thực hiện" (Remaining Effort) cho mỗi task, tự động khởi tạo bằng Estimated Effort và giảm dần khi sinh viên hoàn thành các phiên học.
- **Tiêu chí chấp nhận:**
  - Khi task mới tạo, Remaining Effort = Estimated Effort.
  - Remaining Effort không bao giờ mang giá trị âm.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.3, FR-TASK-003; được duyệt.

<a id="fr-task-004"></a>
## FR-TASK-004 — Phân loại trạng thái vòng đời của Task

- **Mô tả:** Hệ thống phải hỗ trợ quản lý trạng thái của task qua các giá trị: Pending (Chờ thực hiện), In Progress (Đang thực hiện), Completed (Đã hoàn thành), Overdue (Quá hạn).
- **Tiêu chí chấp nhận:**
  - Trạng thái Overdue được hệ thống tự động gán nếu thời điểm hiện tại vượt quá Deadline mà task chưa chuyển sang Completed.
- **Mức độ ưu tiên:** SHOULD.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.3, FR-TASK-004; được duyệt.
