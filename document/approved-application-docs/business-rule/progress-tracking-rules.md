# Progress & Tracking Rules (Quy tắc Ghi nhận Tiến độ & Tái lập lịch)

<a id="br-progress-001"></a>
## BR-PROGRESS-001: Loại task đã hoàn thành

- **ID:** BR-PROGRESS-001
- **Quy tắc:** Các task học thuật đã được đánh dấu là "Completed" sẽ bị loại bỏ khỏi danh sách công việc cần lập lịch trong các lần chạy Plan hoặc Re-plan tiếp theo.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.3, BR-PROGRESS-001; được duyệt.

<a id="br-progress-002"></a>
## BR-PROGRESS-002: Effort còn lại sau session một phần

- **ID:** BR-PROGRESS-002
- **Quy tắc:** Khi một phiên học được ghi nhận là "Partially Completed", số giờ thực tế đã học sẽ được khấu trừ vào khối lượng công việc còn lại (Remaining Effort = Estimated Effort – Actual Hours Spent), và lượng thời gian còn lại sẽ được đưa vào hàng đợi tái phân bổ.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.3, BR-PROGRESS-002; được duyệt.

<a id="br-progress-003"></a>
## BR-PROGRESS-003: Đưa session bỏ lỡ vào Re-plan

- **ID:** BR-PROGRESS-003
- **Quy tắc:** Khi một phiên học bị ghi nhận là "Missed" hoặc thời gian của phiên học đã trôi qua mà không có ghi nhận hoàn thành, toàn bộ khối lượng công việc của phiên học đó được coi là chưa hoàn thành và phải được đưa vào danh sách cần tái lập lịch (Re-plan).

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.3, BR-PROGRESS-003; được duyệt.

<a id="br-progress-004"></a>
## BR-PROGRESS-004: Chỉ Re-plan từ hiện tại

- **ID:** BR-PROGRESS-004
- **Quy tắc:** Khi kích hoạt tính năng Re-plan, hệ thống chỉ được phép tính toán và sắp xếp lại các phiên học từ thời điểm hiện tại ($T_{current}$) trở về sau; không được làm xáo trộn các phiên học đã được đánh dấu "Completed" trong tuần.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.3, BR-PROGRESS-004; được duyệt.
