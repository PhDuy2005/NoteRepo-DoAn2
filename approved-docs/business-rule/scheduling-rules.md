# Scheduling Rules (Quy tắc Lập lịch)

<a id="br-plan-001"></a>
## BR-PLAN-001: Không chồng lấn khung bận

- **ID:** BR-PLAN-001
- **Quy tắc:** Một phiên học (Study Session) tuyệt đối không được chồng lấn (overlap) với bất kỳ khung thời gian nào được đánh dấu là bận cố định (Unavailable / Fixed Time Slot) của sinh viên.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-001; được duyệt.

<a id="br-plan-002"></a>
## BR-PLAN-002: Giới hạn giờ học mỗi ngày

- **ID:** BR-PLAN-002
- **Quy tắc:** Tổng thời lượng của các phiên học được xếp trong một ngày không được vượt quá số giờ học tối đa mỗi ngày (Max Daily Study Hours) do sinh viên thiết lập trong Profile.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-002; được duyệt.

<a id="br-plan-003"></a>
## BR-PLAN-003: Giới hạn thời lượng session

- **ID:** BR-PLAN-003
- **Quy tắc:** Thời lượng của một phiên học đơn lẻ không được nhỏ hơn thời lượng tối thiểu (Min Session Duration: mặc định 30 phút) và không được lớn hơn thời lượng tối đa (Max Session Duration: mặc định 180 phút) để đảm bảo khả năng tập trung.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-003; được duyệt.

<a id="br-plan-004"></a>
## BR-PLAN-004: Session trước deadline

- **ID:** BR-PLAN-004
- **Quy tắc:** Mọi phiên học phục vụ cho một Academic Task phải kết thúc trước mốc thời gian Deadline của task đó. Hệ thống không được xếp phiên học của một task sau thời điểm deadline của nó.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-004; được duyệt.

<a id="br-plan-005"></a>
## BR-PLAN-005: Chia task lớn

- **ID:** BR-PLAN-005
- **Quy tắc:** Khi phân bổ một task lớn có thời gian ước lượng (Estimated Effort) vượt quá thời lượng phiên học tối đa, hệ thống phải tự động chia task đó thành nhiều phiên học riêng biệt trên lịch.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-005; được duyệt.

<a id="br-plan-006"></a>
## BR-PLAN-006: Thứ tự ưu tiên khi thiếu thời gian

- **ID:** BR-PLAN-006
- **Quy tắc:** Khi quỹ thời gian rảnh trong tuần không đủ để phân bổ toàn bộ các task tồn đọng, hệ thống phải ưu tiên xếp lịch theo thứ tự: Task có mức độ khẩn cấp cao hơn (Deadline gần hơn) $\rightarrow$ Task có mức ưu tiên cao hơn (Priority level) $\rightarrow$ Task có trọng số môn học cao hơn.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-006; được duyệt.

<a id="br-plan-007"></a>
## BR-PLAN-007: Khoảng nghỉ giữa session

- **ID:** BR-PLAN-007
- **Quy tắc:** Giữa hai phiên học liên tiếp trong cùng một ngày phải có khoảng nghỉ tối thiểu (Buffer time: mặc định ít nhất 15 phút) trừ khi sinh viên chủ động chỉnh sửa thủ công.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-007; được duyệt.

<a id="br-plan-008"></a>
## BR-PLAN-008: Bảo vệ session trong quá khứ

- **ID:** BR-PLAN-008
- **Quy tắc:** Các phiên học trong quá khứ (trước thời điểm hiện tại) không bao giờ được phép chỉnh sửa tự động hoặc di dời khi chạy thuật toán lập lịch lại.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.1, BR-PLAN-008; được duyệt.
