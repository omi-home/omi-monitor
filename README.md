# omi-monitor

OMI Monitor: web app (Next.js) chạy local làm màn hình giám sát cho OMI — theo dõi realtime các run/agent, quản lý execution profile và cài đặt OMI.

- Spec: [ChangeRequest-0011 omi-home/omi-plugins#280](https://github.com/omi-home/omi-plugins/issues/280), quyết định kiến trúc: ADR-0004 trong `omi-home/omi-plugins`.
- Web app chỉ là giao diện: đọc dữ liệu qua `omi watch --output jsonl`, ghi qua `omi` CLI; không mở `state.sqlite` trực tiếp.
- Phân phối: bản build Next.js standalone `.tar.gz` + sha256 trên GitHub Release, plugin khởi chạy bằng `omi web`.
