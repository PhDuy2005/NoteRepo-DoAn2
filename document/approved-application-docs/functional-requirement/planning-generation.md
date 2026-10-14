# Planning & Schedule Generation

<a id="fr-plan-001"></a>
## FR-PLAN-001 — Tự động sinh kế hoạch học tập tuần

- **Mô tả:** Hệ thống phải có khả năng tự động phân bổ danh sách các task tồn đọng vào các khoảng thời gian rảnh trong tuần để tạo thành một Kế hoạch học tập tuần (Weekly Study Plan) hoàn chỉnh.
- **Tiêu chí chấp nhận:**
  - Mỗi phân bổ là một Study Session có thời gian bắt đầu, kết thúc, ngày cụ thể và gắn với 01 Task xác định.
  - Toàn bộ các phân bổ phải tuân thủ nghiêm ngặt các Business Rules (BR-PLAN-001 đến BR-PLAN-008).
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.4, FR-PLAN-001; được duyệt.

<a id="fr-plan-002"></a>
## FR-PLAN-002 — Tự động chia nhỏ task lớn thành nhiều Study Session

- **Mô tả:** Hệ thống phải tự động phân rã các task có Estimated Effort lớn hơn thời lượng tối đa của một phiên học (hoặc lớn hơn dung lượng của slot rảnh) thành nhiều Study Sessions rải đều qua các ngày trước deadline.
- **Tiêu chí chấp nhận:**
  - Tổng thời lượng của các session được phân bổ cho một task không vượt quá Remaining Effort của task đó.
  - Các session của cùng một task không bị xếp dồn ép thiếu thực tế (ví dụ: không xếp liên tục 6 tiếng trong 1 buổi nếu sinh viên không cho phép).
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.4, FR-PLAN-002; được duyệt.

<a id="fr-plan-003"></a>
## FR-PLAN-003 — Kiểm thử xung đột và ràng buộc (Review & Validation)

- **Mô tả:** Hệ thống phải tự động rà soát kế hoạch vừa tạo trước khi trình bày cho sinh viên nhằm đảm bảo không có bất kỳ phiên học nào trùng lịch bận, không có phiên học nào vi phạm deadline và không vượt ngưỡng giờ học tối đa trong ngày.
- **Tiêu chí chấp nhận:**
  - Nếu phát hiện vi phạm, hệ thống phải kích hoạt vòng lặp điều chỉnh nội bộ giữa Review Agent và Planning Agent tối đa 3 lần để giải quyết vi phạm trước khi hiển thị.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.4, FR-PLAN-003; được duyệt.

<a id="fr-plan-004"></a>
## FR-PLAN-004 — Cảnh báo quá tải và nguy cơ trễ hạn

- **Mô tả:** Khi tổng Remaining Effort của các task cần hoàn thành trong tuần lớn hơn tổng số giờ rảnh khả dụng, hệ thống phải hiển thị cảnh báo quá tải rõ ràng, liệt kê các task có nguy cơ không kịp hoàn thành trước deadline.
- **Tiêu chí chấp nhận:**
  - Giao diện hiển thị chỉ báo quá tải màu đỏ/vàng kèm chênh lệch số giờ thiếu hụt.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.4, FR-PLAN-004; được duyệt.

<a id="fr-plan-005"></a>
## FR-PLAN-005 — Khóa cố định phiên học (Lock/Pin Session)

- **Mô tả:** Trong MVP, hệ thống phải cho phép sinh viên ghim cố định một phiên học trên lịch tuần để phiên học này không bị di chuyển trong các lần tái lập lịch sau.
- **Tiêu chí chấp nhận:**
  - Phiên học được đánh dấu biểu tượng "Đã khóa" (Pinned).
  - Thuật toán Re-plan giữ nguyên khung giờ của phiên học đã khóa.
- **Mức độ ưu tiên:** MUST.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 9.4, FR-PLAN-005; yêu cầu được duyệt. Mức COULD trong bản nguồn được thay bằng MUST cho MVP theo quyết định người dùng ngày 2026-10-14.
