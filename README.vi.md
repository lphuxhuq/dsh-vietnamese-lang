# dsh-vietnamese-lang

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![DeepSeek Harness](https://img.shields.io/badge/DSH-plugin-brightgreen)](https://github.com/deepseek-ai/deepseek-harness)

Gói ngôn ngữ Tiếng Việt cho giao diện Web [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) (`dsh`).

[English](README.md) | Tiếng Việt

## Tính năng

- **Bao phủ toàn diện giao diện DSH**: Dịch thuật đầy đủ và chuẩn xác 50 không gian tên (namespace) cốt lõi của Harness (Trò chuyện, Quỹ đạo hoạt động, Quản lý Workspace, Cài đặt hệ thống, Chọn mô hình, Phê duyệt công cụ, Cây thư mục tệp, Terminal, Bàn giao sản phẩm, So sánh khác biệt Diff, Xem trước tài liệu, v.v.).
- **Tích hợp nguyên bản**: Đăng ký trực tiếp vào `LocaleRuntime` chính thức của DSH, xuất hiện trong danh mục chọn ngôn ngữ tại `Cài đặt > Cài đặt chung > Ngôn ngữ`.
- **Cơ chế Fallback thông minh**: Các khóa chưa có bản dịch từ plugin bên thứ ba sẽ tự động hiển thị bằng tiếng Anh (hoặc ngôn ngữ gốc).
- **Không can thiệp mã nguồn lõi**: Hoạt động độc lập dưới dạng plugin Cordis client chuẩn thông qua ModuleLoader.

## Cài đặt

Cài đặt bằng dòng lệnh `dsh`:

```sh
dsh plugin --profile web add dsh-vietnamese-lang
```

Hoặc cài trực tiếp từ repository GitHub:

```sh
dsh plugin --profile web add https://github.com/lphuxhuq/dsh-vietnamese-lang
```

Sau khi cài đặt xong, tải lại giao diện Web của DeepSeek Harness, mở **Cài đặt (Settings) > Cài đặt chung (General) > Ngôn ngữ (Language)** và chọn **Tiếng Việt**.

## Cấu trúc thư mục

```
dsh-vietnamese-lang/
├── cordis.patch.yml   # Khai báo plugin cho loader của DSH
├── index.mjs          # Entry phía Host (no-op)
├── lib/
│   └── client.js      # Bundle client chứa 50 bộ từ điển tiếng Việt
├── package.json       # Manifest chứa dsh.bundle & dsh.client
└── README.md
```

## Giấy phép

[MIT](LICENSE)
