# Use Case Specifications

## UC-01: Manage Student Profile

- **ID:** UC-01
- **Name:** Manage Student Profile
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên tạo mới, xem và cập nhật thông tin hồ sơ học tập cá nhân cùng các thông số sở thích học tập.
- **Preconditions:** Sinh viên đã mở ứng dụng.
- **Trigger:** Sinh viên chọn màn hình quản lý hồ sơ hoặc lần đầu khởi tạo hệ thống.
- **Main Flow:**
  1. Sinh viên mở giao diện quản lý hồ sơ cá nhân.
  2. Hệ thống hiển thị các thông tin hiện tại: Tên sinh viên, MSSV (tùy chọn), danh sách sở thích học tập (thời lượng phiên học mặc định, số giờ học tối đa/ngày, thời điểm học ưa thích: sáng/chiều/tối).
  3. Sinh viên chỉnh sửa các giá trị sở thích.
  4. Sinh viên chọn "Lưu hồ sơ".
  5. Hệ thống xác thực tính hợp lệ của dữ liệu (ví dụ: thời lượng phiên học phải > 0) và lưu lại.
  6. Hệ thống thông báo cập nhật hồ sơ thành công.
- **Alternative Flow:**
  - **4a. Dữ liệu nhập không hợp lệ:** Hệ thống hiển thị thông báo lỗi cụ thể (ví dụ: số giờ học tối đa trong ngày không được vượt quá 16 giờ) và yêu cầu nhập lại.
- **Postconditions:** Thông tin hồ sơ và sở thích học tập mới được lưu lại để phục vụ cho các thuật toán lập lịch.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-01; được duyệt.

## UC-02: Manage Availability

- **ID:** UC-02
- **Name:** Manage Availability
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên khai báo, chỉnh sửa và xóa các khoảng thời gian bận cố định (lịch học trên trường, lịch làm việc, lịch cá nhân) để xác định các slot thời gian rảnh trong tuần.
- **Preconditions:** Sinh viên đã có hồ sơ học tập trong hệ thống.
- **Trigger:** Sinh viên truy cập màn hình quản lý lịch bận / availability.
- **Main Flow:**
  1. Sinh viên xem lưới thời gian (time-grid) theo tuần của mình.
  2. Sinh viên chọn tạo một khung thời gian bận (Fixed Time Block).
  3. Sinh viên nhập: Tên hoạt động (ví dụ: Học môn Mạng máy tính, Đi làm ca sáng), Ngày trong tuần, Giờ bắt đầu, Giờ kết thúc, Tính lặp lại theo tuần (Có/Không).
  4. Sinh viên nhấn "Lưu khung giờ".
  5. Hệ thống kiểm tra tính hợp lệ về thời gian (Giờ kết thúc > Giờ bắt đầu).
  6. Hệ thống cập nhật lưới thời gian và tự động suy diễn các khoảng thời gian rảnh (Available Slots).
- **Alternative Flow:**
  - **5a. Trùng lặp khung giờ cố định:** Hệ thống hiển thị cảnh báo trùng với một khung giờ cố định đã có và yêu cầu người dùng xác nhận ghi đè hoặc chỉnh sửa lại.
- **Postconditions:** Lịch rảnh tuần của sinh viên được cập nhật chính xác làm đầu vào cho quá trình lập lịch.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-02; được duyệt.

## UC-03: Manage Courses

- **ID:** UC-03
- **Name:** Manage Courses
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên quản lý danh mục các môn học đang theo học trong học kỳ.
- **Preconditions:** Sinh viên đã truy cập ứng dụng.
- **Trigger:** Sinh viên chọn chức năng quản lý môn học.
- **Main Flow:**
  1. Hệ thống hiển thị danh sách các môn học hiện có kèm mã môn và màu đại diện (nếu có).
  2. Sinh viên chọn "Thêm môn học mới".
  3. Sinh viên nhập: Tên môn học, Mã môn (ví dụ: IT001 - Tùy chọn) và Tên giảng viên (Tùy chọn).
  4. Sinh viên nhấn "Lưu".
  5. Hệ thống lưu môn học và cập nhật danh sách hiển thị.
- **Alternative Flow:**
  - Sinh viên chọn Sửa hoặc Xóa: Hệ thống cho phép cập nhật thông tin môn học. Nếu môn học đã có task liên kết, hệ thống yêu cầu xác nhận trước khi xóa.
- **Postconditions:** Môn học mới được ghi nhận để liên kết với các bài tập và đồ án học thuật.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-03; được duyệt. Trường ưu tiên môn học trong bản nguồn được bỏ theo UN-11 đã duyệt; mức độ quan trọng được gán cho từng task.

## UC-04: Manage Academic Tasks

- **ID:** UC-04
- **Name:** Manage Academic Tasks
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên tạo mới, chỉnh sửa, xem chi tiết và hủy bỏ các task học thuật (bài tập, đồ án, ôn thi).
- **Preconditions:** Đã có ít nhất một môn học được tạo trong hệ thống.
- **Trigger:** Sinh viên chọn chức năng quản lý bài tập/task.
- **Main Flow:**
  1. Sinh viên mở danh sách task học thuật.
  2. Sinh viên chọn "Tạo task mới".
  3. Sinh viên nhập thông tin: Tên task, Môn học liên kết, Phân loại task (Assignment / Project / Exam Prep / Other), Hạn chót nộp bài (Deadline: Ngày & Giờ), Thời gian ước lượng cần hoàn thành (Estimated Effort - tính bằng giờ), Hệ số mức độ quan trọng từ 1,0 đến 5,0 theo bước 0,1.
  4. Sinh viên chọn "Lưu task".
  5. Hệ thống kiểm tra dữ liệu: Deadline phải lớn hơn thời điểm hiện tại, Estimated Effort phải > 0.
  6. Hệ thống lưu task với trạng thái ban đầu là "Pending".
- **Alternative Flow:**
  - **5a. Deadline trong quá khứ hoặc Effort <= 0:** Hệ thống thông báo lỗi trường dữ liệu không hợp lệ.
- **Postconditions:** Task được thêm vào hàng đợi công việc chờ lập lịch.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-04; được duyệt. Nhãn ưu tiên trong bản nguồn được thay bằng hệ số mức độ quan trọng theo UN-11 đã duyệt.

## UC-05: Generate Weekly Study Plan

- **ID:** UC-05
- **Name:** Generate Weekly Study Plan
- **Actor:** Sinh viên
- **Description:** Hệ thống tự động kích hoạt tiến trình Multi-Agent để phân tích công việc, đối chiếu thời gian rảnh và sinh ra kế hoạch học tập theo tuần.
- **Preconditions:** Sinh viên đã cấu hình availability và có ít nhất một task học thuật chưa hoàn thành.
- **Trigger:** Sinh viên bấm nút "Tạo kế hoạch tuần" (Generate Weekly Plan).
- **Main Flow:**
  1. Sinh viên chọn tuần cần lập lịch (mặc định là tuần hiện tại hoặc tuần kế tiếp).
  2. Hệ thống thu thập dữ liệu: Profile/Preferences, Danh sách Available Slots trong tuần, Danh sách Task chưa hoàn thành kèm Deadline và Remaining Effort.
  3. Hệ thống kích hoạt quy trình Multi-Agent (Profile Agent đánh giá workload, Planning Agent xếp lịch, Review Agent kiểm thử ràng buộc).
  4. Hệ thống sinh ra bản dự thảo kế hoạch học tập (Draft Study Plan) bao gồm danh sách các Study Sessions phân bổ vào các ngày.
  5. Hệ thống hiển thị bản kế hoạch trên giao diện lịch tuần kèm bản tóm tắt phân bổ công việc.
- **Alternative Flow:**
  - **4a. Phát hiện quá tải nghiêm trọng (Overload):** Tổng effort vượt quá tổng thời gian rảnh. Hệ thống vẫn sinh lịch tối đa theo năng lực và hiển thị cảnh báo đỏ kèm danh sách các task bị tràn/nguy cơ trễ deadline.
  - **4b. Không có task nào cần làm:** Hệ thống thông báo không có task nào đủ điều kiện lập lịch trong tuần này.
- **Postconditions:** Kế hoạch học tập tuần dạng Draft được tạo ra và hiển thị cho sinh viên xem xét.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-05; được duyệt.

## UC-06: Review Generated Plan

- **ID:** UC-06
- **Name:** Review Generated Plan
- **Actor:** Sinh viên
- **Description:** Sinh viên xem xét tính hợp lý của kế hoạch học tập do hệ thống đề xuất, đọc các cảnh báo xung đột và các giải thích logic.
- **Preconditions:** Một kế hoạch học tập tuần dạng Draft vừa được sinh ra (từ UC-05).
- **Trigger:** Kế hoạch học tập tuần hiển thị trên màn hình.
- **Main Flow:**
  1. Sinh viên duyệt qua các Study Session được phân bổ từ Thứ 2 đến Chủ Nhật.
  2. Sinh viên xem các chỉ số thống kê tuần: Tổng số giờ học được xếp, số task được giải quyết, các cảnh báo nếu có.
  3. Sinh viên xem giải thích ngắn gọn tại sao một task lại được xếp vào khung giờ đó (UC-10).
  4. Sinh viên nhấn "Xác nhận áp dụng kế hoạch" (Apply Plan).
  5. Hệ thống chuyển trạng thái kế hoạch từ "Draft" sang "Active".
- **Alternative Flow:**
  - **4a. Sinh viên thấy kế hoạch chưa tối ưu:** Sinh viên chọn "Chỉnh sửa thủ công" (chuyển sang UC-07) hoặc "Yêu cầu sinh lại" kèm điều chỉnh thông số.
- **Postconditions:** Kế hoạch học tập tuần chính thức có hiệu lực.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-06; được duyệt.

## UC-07: Modify Study Plan

- **ID:** UC-07
- **Name:** Modify Study Plan
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên trực tiếp điều chỉnh các phiên học trong kế hoạch tuần (thay đổi thời gian, đổi task, xóa phiên học, thêm phiên học mới).
- **Preconditions:** Kế hoạch tuần đã tồn tại (ở trạng thái Draft hoặc Active).
- **Trigger:** Sinh viên thực hiện thao tác kéo thả hoặc chọn một Study Session trên lịch tuần.
- **Main Flow:**
  1. Sinh viên chọn một Study Session cụ thể trên lịch.
  2. Sinh viên thực hiện một trong các thao tác:
     - Thay đổi khung giờ bắt đầu / kết thúc.
     - Đổi sang ngày khác trong tuần.
     - Gán phiên học đó cho một task khác.
     - Xóa bỏ phiên học.
  3. Hệ thống kiểm tra xem thay đổi có vi phạm các khung giờ bận cố định (Availability) hay không.
  4. Hệ thống cập nhật phiên học và hiển thị lịch mới.
- **Alternative Flow:**
  - **3a. Thay đổi làm phiên học trùng vào khung giờ bận cố định:** Hệ thống hiển thị cảnh báo xung đột và cho sinh viên chọn đổi sang khung giờ khác hoặc xác nhận ghi đè nếu chấp nhận đánh đổi lịch bận. Khi sinh viên xác nhận ghi đè, hệ thống ghi nhận hành động vào audit log.
- **Postconditions:** Kế hoạch học tập được cập nhật theo ý chí chủ quan của sinh viên.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-07; được duyệt.

## UC-08: Record Progress

- **ID:** UC-08
- **Name:** Record Progress
- **Actor:** Sinh viên
- **Description:** Cho phép sinh viên cập nhật kết quả thực tế sau mỗi phiên học (hoàn thành, bỏ lỡ, hoặc làm được một phần).
- **Preconditions:** Kế hoạch tuần đang ở trạng thái Active và phiên học đã tới hoặc qua thời gian bắt đầu.
- **Trigger:** Sinh viên chọn một Study Session trong ngày trên giao diện.
- **Main Flow:**
  1. Sinh viên mở phiên học cần cập nhật.
  2. Sinh viên chọn một trong các trạng thái:
     - **Completed:** Đã hoàn thành phiên học đúng kế hoạch.
     - **Partially Completed:** Đã học một phần (sinh viên nhập số giờ thực tế đã học và ước lượng số giờ còn lại của task).
     - **Missed / Skipped:** Đã bỏ qua hoặc không thể học phiên này (có thể nhập lý do tùy chọn).
  3. Sinh viên nhấn "Lưu tiến độ".
  4. Hệ thống cập nhật trạng thái phiên học và điều chỉnh Remaining Effort của Academic Task tương ứng.
- **Alternative Flow:**
  - **4a. Phiên học bị Missed hoặc dở dang:** Hệ thống thông báo tiến độ bị chậm và hiển thị nút gợi ý "Tái lập kế hoạch" (Re-plan).
- **Postconditions:** Tiến độ thực tế được ghi nhận vào hệ thống; dữ liệu task được cập nhật số giờ còn lại.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-08; được duyệt.

## UC-09: Re-plan Study Schedule

- **ID:** UC-09
- **Name:** Re-plan Study Schedule
- **Actor:** Sinh viên
- **Description:** Hệ thống tính toán lại và phân bổ lại các phiên học chưa hoàn thành vào các khung giờ rảnh còn lại trong tuần khi có sự cố trễ hạn hoặc thay đổi lịch rảnh.
- **Preconditions:** Kế hoạch tuần đang Active, có phiên học bị bỏ lỡ hoặc sinh viên vừa thay đổi khung giờ bận trong tuần.
- **Trigger:** Sinh viên nhấn nút "Tái lập lịch tuần" (Re-plan Schedule).
- **Main Flow:**
  1. Hệ thống xác định thời điểm hiện tại và giữ nguyên các phiên học đã hoàn thành (Completed) trong quá khứ.
  2. Hệ thống thu thập các task chưa hoàn thành và khối lượng công việc còn lại (Remaining Effort).
  3. Hệ thống cập nhật danh sách các slot rảnh từ thời điểm hiện tại đến hết tuần.
  4. Hệ thống kích hoạt Multi-Agent để phân bổ lại các phiên học vào các slot rảnh còn lại.
  5. Hệ thống hiển thị bản kế hoạch điều chỉnh (Updated Plan) kèm thông báo những phiên học nào đã được chuyển dời.
  6. Sinh viên xem xét và xác nhận áp dụng kế hoạch mới.
- **Alternative Flow:**
  - **4a. Quỹ thời gian còn lại trong tuần không đủ bù đắp:** Hệ thống ưu tiên xếp các task có deadline gần nhất trong tuần; các task có deadline xa hơn được cảnh báo dời sang tuần sau hoặc hiển thị cảnh báo không đủ thời gian.
- **Postconditions:** Kế hoạch cho các ngày còn lại trong tuần được đồng bộ và cập nhật mới.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-09; được duyệt.

## UC-10: Explain Planning Decision

- **ID:** UC-10
- **Name:** Explain Planning Decision
- **Actor:** Sinh viên
- **Description:** Hệ thống cung cấp lời giải thích ngắn gọn, súc tích về căn cứ và lý do một task được xếp vào một khung giờ cụ thể hoặc lý do một task được ưu tiên hơn task khác.
- **Preconditions:** Kế hoạch học tập tuần đã được sinh ra.
- **Trigger:** Sinh viên nhấn vào biểu tượng "Tại sao?" (Why this slot?) tại một phiên học hoặc xem bản tóm tắt tuần.
- **Main Flow:**
  1. Sinh viên bấm vào một Study Session trên lịch tuần.
  2. Hệ thống hiển thị popup giải thích ngắn gọn gồm:
     - Căn cứ deadline (ví dụ: "Task A có deadline vào Thứ 5 nên được ưu tiên làm trước Thứ 5").
     - Căn cứ mức độ ưu tiên và khối lượng (ví dụ: "Đồ án có khối lượng 6 giờ được chia làm 3 phiên học rải đều").
     - Căn cứ sở thích cá nhân (ví dụ: "Được xếp vào buổi tối từ 19:30 theo khung giờ học ưa thích đã cài đặt").
  3. Sinh viên đọc hiểu và đóng cửa sổ popup.
- **Alternative Flow:** Không có flow ngoại lệ.
- **Postconditions:** Người dùng hiểu được tính logic của hệ thống, tăng mức độ tin tưởng vào kế hoạch.

**Nguồn và trạng thái:** `docs/requirements_analysis_v0.1.md`, mục 7, UC-10; được duyệt.
