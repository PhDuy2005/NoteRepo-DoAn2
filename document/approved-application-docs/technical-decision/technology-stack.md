# Công nghệ sử dụng

## Mục lục

- [Công nghệ sử dụng](#công-nghệ-sử-dụng)
  - [Mục lục](#mục-lục)
  - [Tổng quan](#tổng-quan)
  - [Danh sách công nghệ](#danh-sách-công-nghệ)
  - [Các quyết định còn bỏ ngỏ](#các-quyết-định-còn-bỏ-ngỏ)

## Tổng quan

Tài liệu này ghi nhận các công nghệ được chọn cho hệ thống theo chỉ đạo trực tiếp của người dùng.

**Nguồn và trạng thái:** Chỉ đạo trực tiếp của người dùng trong phiên làm việc ngày 2026-10-12, được ghi nhận.

## Danh sách công nghệ

| ID | Nhóm | Công nghệ | Vai trò dự kiến | Trạng thái / nguồn |
| --- | --- | --- | --- | --- |
| TECH-01 | Backend | Java 21, Spring Boot 4, Gradle | Xây dựng và build API cùng các dịch vụ phía máy chủ | Được ghi nhận; chỉ đạo trực tiếp của người dùng |
| TECH-02 | Frontend | Vue với TypeScript | Xây dựng giao diện và logic phía máy khách | Được ghi nhận; chỉ đạo trực tiếp của người dùng |
| TECH-03 | Cơ sở dữ liệu | MySQL | Lưu trữ dữ liệu ứng dụng | Được ghi nhận; chỉ đạo trực tiếp của người dùng |
| TECH-04 | Framework agent | Spring AI | Tích hợp năng lực agent/AI trong ứng dụng Spring | Được ghi nhận; chỉ đạo trực tiếp của người dùng |
| TECH-05 | Nhà cung cấp LLM / gateway | OpenAI thông qua 9router | Cung cấp quyền truy cập mô hình ngôn ngữ lớn qua 9router | Được ghi nhận; chỉ đạo trực tiếp của người dùng |

## Các quyết định còn bỏ ngỏ

Các nội dung sau chưa được chốt trong chỉ đạo hiện tại:

- Phiên bản cụ thể của Vue, TypeScript và MySQL.
- Phiên bản Spring AI, mô hình OpenAI cụ thể, API tương thích được sử dụng qua 9router và cấu hình xác thực/kết nối.
- Công cụ quản lý dependency và quy trình build cho frontend.
- Thư viện frontend bổ trợ, chiến lược quản lý trạng thái và thư viện UI.
- Cấu hình kết nối, migration, backup và môi trường triển khai MySQL.
- Nền tảng triển khai, CI/CD và các công cụ quan sát hệ thống.

