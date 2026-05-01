<div align="center">

# 🌍 ZirContry

**Theo dõi quốc gia & khu vực của người chơi qua tra cứu IP — với PlaceholderAPI, cờ cảm xúc, bộ nhớ đệm SQLite và đầu ra màu sắc đẹp mắt.**

[![Version](https://img.shields.io/badge/version-2.0.0-5BCEFA?style=flat-square)](https://github.com/zirvn/ZirContry/releases)
[![MC Version](https://img.shields.io/badge/Minecraft-1.18--1.21.x%2B-57F287?style=flat-square)](https://papermc.io)
[![License](https://img.shields.io/badge/license-MIT-B5A3F5?style=flat-square)](LICENSE)
[![Folia](https://img.shields.io/badge/Folia-supported-FFD700?style=flat-square)](https://github.com/PaperMC/Folia)

</div>

---

## ✨ Tính năng

- **Tra cứu IP tự động** khi người chơi tham gia sử dụng [ip-api.com](https://ip-api.com) (miễn phí, không cần khóa) hoặc [ipinfo.io](https://ipinfo.io) (cao cấp, cần khóa API)
- **Bộ nhớ đệm SQLite** — mỗi IP được lưu trữ cục bộ; chỉ gọi API một lần cho mỗi IP
- **Cờ cảm xúc** 🇻🇳 🇺🇸 🇯🇵 bên cạnh tên quốc gia
- **Hỗ trợ PlaceholderAPI** với 9 placeholder
- **Tùy chọn riêng tư cho từng người chơi** — người chơi có thể ẩn vị trí của mình
- **Đầu ra chat mã màu đẹp mắt** sử dụng mã màu hex (`&#RRGGBB`)
- **Bảng xếp hạng quốc gia/khu vực hàng đầu** từ cơ sở dữ liệu
- **Tương thích Folia** — hoạt động trên các nhánh Paper đa luồng
- **Hỗ trợ Minecraft 1.18 → 1.21.x → các phiên bản tương lai** (Paper API)

---

## 📦 Cài đặt

1. Tải `ZirContry-2.0.0.jar` từ [Mục phát hành](https://github.com/zirvn/ZirContry/releases)
2. Đưa vào thư mục `plugins/` của máy chủ
3. Đảm bảo đã cài đặt [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)
4. Khởi động/lại máy chủ
5. Chỉnh sửa `plugins/ZirContry/config.yml` nếu cần
6. Chạy `/zircountry reload` để áp dụng thay đổi

> **Yêu cầu Java 17+.** Đã kiểm tra trên Paper, Purpur và Folia.

---

## 🖥️ Khả năng tương thích

| Phần mềm máy chủ | Hỗ trợ |
|-----------------|-----------|
| Paper 1.18+     | ✅        |
| Paper 1.19.x    | ✅        |
| Paper 1.20.x    | ✅        |
| Paper 1.21.x    | ✅        |
| Paper 1.21.1+   | ✅        |
| Purpur          | ✅        |
| Folia           | ✅        |
| Spigot 1.18+    | ✅        |

> ZirContry sử dụng Paper API ổn định và Java chuẩn — nó sẽ tiếp tục hoạt động trên các phiên bản tương lai mà không cần sửa đổi.

---

## 🔧 Lệnh

| Lệnh | Mô tả | Quyền |
|---------|-------------|---------|
| `/zircountry` | Kiểm tra vị trí của bạn | `zircountry.use` |
| `/zircountry <player>` | Kiểm tra vị trí người chơi khác | `zircountry.others` |
| `/zircountry hide` | Bật/tắt hiển thị vị trí của bạn | `zircountry.hide` |
| `/zircountry list` | Liệt kê tất cả người chơi trực tuyến kèm vị trí | `zircountry.list` |
| `/zircountry list country <kw>` | Lọc danh sách theo từ khóa quốc gia | `zircountry.list` |
| `/zircountry list region <kw>` | Lọc danh sách theo từ khóa khu vực | `zircountry.list` |
| `/zircountry top` | 10 quốc gia hàng đầu (DB mọi thời đại) | `zircountry.top` |
| `/zircountry top region` | 10 khu vực hàng đầu (DB mọi thời đại) | `zircountry.top` |
| `/zircountry info` | Thông tin plugin & thống kê DB | `zircountry.use` |
| `/zircountry reload` | Tải lại cấu hình | `zircountry.reload` |
| `/zircountry help` | Hiển thị menu trợ giúp | `zircountry.use` |

**Tên thay thế:** `/zcountry`, `/zc`

---

## 🔑 Quyền

| Quyền | Mô tả | Mặc định |
|------------|-------------|---------|
| `zircountry.use` | Sử dụng `/zircountry` cho chính mình | `true` |
| `zircountry.others` | Tra cứu người chơi khác | `op` |
| `zircountry.list` | Xem danh sách người chơi | `op` |
| `zircountry.top` | Xem quốc gia hàng đầu | `op` |
| `zircountry.hide` | Bật/tắt ẩn vị trí | `true` |
| `zircountry.reload` | Tải lại cấu hình | `op` |
| `zircountry.admin` | Tất cả quyền quản trị | `op` |

---

## 📝 PlaceholderAPI Placeholder

Tất cả placeholder đều có tiền tố `%zircountry_`:

| Placeholder | Ví dụ đầu ra | Mô tả |
|-------------|----------------|-------------|
| `%zircountry_country%` | `Vietnam` | Tên quốc gia |
| `%zircountry_region%` | `Thanh Hóa` | Vùng / Tiểu bang |
| `%zircountry_city%` | `Hà Trung` | Thành phố |
| `%zircountry_flag%` | `🇻🇳` | Cờ cảm xúc |
| `%zircountry_short%` | `Vietnam/Thanh Hóa` | Quốc gia/Khu vực |
| `%zircountry_full%` | `Hà Trung, Thanh Hóa, Vietnam` | Vị trí đầy đủ |
| `%zircountry_format%` | `🇻🇳 Vietnam` | Cờ + Quốc gia |
| `%zircountry_code%` | `VN` | Mã ISO 2 chữ cái |
| `%zircountry_hidden%` | `true` / `false` | Trạng thái tùy chọn riêng tư |

> Nếu người chơi đã ẩn vị trí của họ, tất cả placeholder (ngoại trừ `hidden`) trả về `[Hidden]` (có thể cấu hình).

**Ví dụ sử dụng (tiền tố tab, bảng điểm, v.v.):**
```
tablist-format: "%zircountry_flag% %player_name% &7| &b%zircountry_short%"
scoreboard-line: "&7Quốc gia: &b%zircountry_format%"
```


---

## ⚙️ Cấu hình

```yaml
# plugins/ZirContry/config.yml

# Nhà cung cấp tra cứu IP: ipinfo | ip-api
provider: "ip-api"

ipinfo:
  enabled: false
  api_key: ""         # Lấy tại https://ipinfo.io/account

ip-api:
  enabled: true       # Miễn phí, 45 yêu cầu/phút, không cần khóa

display:
  show_flags: true    # Hiển thị cờ cảm xúc 🇻🇳
  unknown_text: "Không rõ"
  send_title: true    # Hiển thị title khi /zircountry
  send_actionbar: true
  title_timing:
    fade_in: 10
    stay: 60
    fade_out: 10

messages:
  prefix: "&8[&b&lZirContry&8] &r"
  no_permission: "&c✗ Bạn không có quyền."
  player_only: "&c✗ Chỉ người chơi mới có thể dùng lệnh này."
  player_not_found: "&c✗ Không tìm thấy người chơi hoặc không trực tuyến."
  looking_up: "&7⟳ Đang tra cứu vị trí..."
  hidden: "&7[Ẩn]"
  location_hidden: "&e⚠ Người chơi này đã ẩn vị trí."
  hide_enabled: "&a✓ Vị trí của bạn hiện đã được ẩn."
  hide_disabled: "&e✓ Vị trí của bạn hiện đã hiển thị."
  reload_success: "&a✓ Đã tải lại cấu hình."

logging:
  verbose: false        # Ghi nhật ký cache trúng/trượt
  log_api_calls: false  # Ghi nhật ký mọi lần gọi API

database:
  file: "zircountry.db"       # Tệp SQLite (tương đối với thư mục plugin)
  cache_ttl_hours: 0          # 0 = lưu cache vĩnh viễn

---

## 🗄️ Database

ZirContry sử dụng SQLite — không cần thiết lập cơ sở dữ liệu bên ngoài. Dữ liệu được lưu trong `plugins/ZirContry/zircountry.db`.

**Schema:**
```sql
CREATE TABLE zir_country_data (
    ip         TEXT PRIMARY KEY,
    country    TEXT,
    region     TEXT,
    city       TEXT,
    fetched_at INTEGER DEFAULT 0
);
```

- Tất cả IP → dữ liệu vị trí được lưu cache khi tra cứu lần đầu

- Tồn tại sau khi khởi động lại máy chủ (không cần tìm nạp lại đối với IP đã biết)

- Cột `fetched_at` lưu trữ dấu thời gian Unix (ms) cho tính năng TTL trong tương lai

---

## 🌐 API Providers

### ip-api.com (default, free)
- Không cần khóa API
- Giới hạn tốc độ **45 yêu cầu/phút**
- Trả về: quốc gia, khu vực (bang/tỉnh), thành phố
- Endpoint: `http://ip-api.com/json/{ip}?fields=status,country,regionName,city`

### ipinfo.io (optional, pro)
- Yêu cầu khóa API từ [ipinfo.io/account](https://ipinfo.io/account)
- **50.000 yêu cầu/tháng** ở gói miễn phí; không giới hạn ở gói trả phí
- Độ chính xác cao hơn cho một số khu vực
- Kích hoạt trong cấu hình:
  ```yaml
  provider: "ipinfo"
  ipinfo:
    enabled: true
    api_key: "your_api_key_here"
  ```
  ---

## 🎨 Tham khảo màu sắc

ZirContry uses consistent hex colors throughout:

| Role | Hex | Preview |
|------|-----|---------|
| Accent (sky blue) | `#5BCEFA` | Thông tin & hiển thị quốc gia |
| Gold | `#FFD700` | Nhãn lệnh & số 1 hàng đầu |
| Mint green | `#57F287` | Khu vực & thành phố |
| Soft purple | `#B5A3F5` | Tiêu đề tra cứu người chơi |
| Red | `#ED4245` | Lỗi |
| Yellow | `#FEE75C` | Cảnh báo |

---

## ❓ FAQ

**H: Nó có hoạt động ngoại tuyến / trên máy chủ chế độ offline không?**
Có — nó tra cứu địa chỉ IP trực tiếp, không phải tài khoản Minecraft.

**H: Địa chỉ IP của người chơi tôi có được gửi đến bên thứ ba không?**
Chỉ địa chỉ IP (không phải tên người chơi hoặc UUID) được gửi đến nhà cung cấp tra cứu đã cấu hình. IP được lưu cache chỉ được lưu trữ cục bộ trong SQLite.

**H: Điều gì xảy ra nếu API bị lỗi?**
Tra cứu trả về LocationData.UNKNOWN (quốc gia/khu vực/thành phố = "Không rõ"). Dữ liệu đã lưu cache tiếp tục hoạt động bình thường.

**H: Tôi có thể thêm nhà cung cấp IP khác không?**
Có — hãy triển khai giao diện LocationProvider và đăng ký nó trong CountryManager.initProvider().

**H: Nó có hỗ trợ người chơi Bedrock (Geyser) không?**
Người chơi Bedrock kết nối qua Geyser có IP thực được truyền qua, vì vậy tra cứu hoạt động tương tự.

---

## 📜 Changelog

### v2.0.0
- Viết lại hoàn toàn với kiến trúc sạch
- Hỗ trợ màu hex (`&#RRGGBB`)
- Lưu trữ SQLite với bộ nhớ đệm được nạp sẵn
- Mở rộng PlaceholderAPI với 9 placeholder
- Hệ thống nhà cung cấp kép (ip-api / ipinfo)
- Hoàn thành tab cho tất cả lệnh con
- Bảng xếp hạng quốc gia/khu vực hàng đầu
- Hỗ trợ Folia
- Hỗ trợ cờ cảm xúc cho 70+ quốc gia

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

Made with ❤️ by **ZirVN** ·

</div>
