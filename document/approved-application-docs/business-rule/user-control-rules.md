# User Control Rules (Quy tắc Quyền hạn Người dùng)

<a id="br-user-001"></a>
## BR-USER-001: Quyền chỉnh sửa Study Session

- **ID:** BR-USER-001
- **Quy tắc:** Sinh viên có quyền tối cao trong việc thêm, sửa, di chuyển hoặc xóa bỏ bất kỳ Study Session nào do hệ thống tự động sinh ra.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.2, BR-USER-001; được duyệt.

<a id="br-user-002"></a>
## BR-USER-002: Bảo toàn deadline và tên task

- **ID:** BR-USER-002
- **Quy tắc:** Hệ thống AI tuyệt đối không được tự ý sửa đổi mốc Deadline hoặc Tên Task do sinh viên đã nhập vào.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.2, BR-USER-002; được duyệt.

<a id="br-user-003"></a>
## BR-USER-003: Xác nhận ghi đè giờ bận

- **ID:** BR-USER-003
- **Quy tắc:** AI không được tạo hoặc tự điều chỉnh phiên học trùng với khung giờ bận cố định. Khi sinh viên chủ động kéo thả phiên học vào khung giờ bận, hệ thống phải cảnh báo và chỉ ghi đè sau khi sinh viên xác nhận rõ ràng rằng họ chấp nhận đánh đổi lịch bận đó. Hệ thống phải ghi hành động ghi đè vào audit log, bao gồm người thực hiện, thời điểm, phiên học bị ảnh hưởng và khung giờ bận bị ghi đè.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.2, BR-USER-003; được duyệt.

<a id="br-user-004"></a>
## BR-USER-004: Giữ session khóa khi Re-plan

- **ID:** BR-USER-004
- **Quy tắc:** Sinh viên có quyền khóa (Lock / Pin) một phiên học cố định vào một khung giờ cụ thể; khi chạy Re-plan, hệ thống không được phép tự động di dời các phiên học đã bị khóa này.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.2, BR-USER-004; được duyệt.

<a id="br-user-005"></a>
## BR-USER-005: Sinh viên xác nhận kế hoạch

- **ID:** BR-USER-005
- **Quy tắc:** Mọi kế hoạch học tập do AI đề xuất chỉ được coi là chính thức áp dụng sau khi có hành động phê duyệt (Apply / Confirm) từ phía sinh viên.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 8.2, BR-USER-005; được duyệt.
