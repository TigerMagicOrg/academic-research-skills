# Kế hoạch & Trạng thái — Nghiên cứu P2P Lending

> **File này là bảng điều khiển tiến độ.** Phạm vi và mục tiêu nằm ở `target.md` — file đó là nguồn chân lý duy nhất về *làm cái gì*; file này chỉ theo dõi *đã làm tới đâu*. Không chép lại nội dung phạm vi vào đây, để hai file không trôi khỏi nhau.

---

## ⚡ QUY TRÌNH VÀO VIỆC (đọc trước tiên khi mở phiên mới)

Thực hiện đúng sáu bước sau, theo thứ tự:

1. **Đọc `target.md`** — nắm phạm vi, khung phân tích, các quyết định đã chốt.
2. **Đọc §1 và §2 của file này** — biết đang ở đâu và việc kế tiếp là gì.
3. **⚠ ĐỐI CHIẾU LEDGER VỚI THỰC TẾ.** Với mọi hạng mục đánh dấu ✅ ở §3, kiểm tra hiện vật tương ứng ở §4 có thật sự tồn tại trên đĩa và có nội dung hay không.
   *Lý do*: nếu phiên trước bị ngắt giữa chừng, ledger có thể ghi xong việc chưa xong. **Ledger không phải bằng chứng — hiện vật mới là bằng chứng.**
4. **Nếu phát hiện lệch**: sửa lại trạng thái ở §3 cho khớp thực tế **trước**, ghi một dòng vào §6, rồi mới làm tiếp. Không làm tiếp trên nền một ledger sai.
5. **Làm việc kế tiếp** ghi ở §2.
6. **Trước khi kết thúc phiên**: cập nhật §1, §2, §3 và ghi một dòng vào §6. Đây là bước bắt buộc, không phải tuỳ chọn.

**Quy tắc vàng**: không đánh ✅ cho hạng mục nào mà hiện vật chưa tồn tại ở đúng đường dẫn ghi tại §4.

---

## 1. Trạng thái hiện tại

| Trường | Giá trị |
|---|---|
| **Cập nhật lần cuối** | 2026-07-26 |
| **Giai đoạn hiện tại** | **P2 — Xương sống dữ liệu định lượng** 🔄 đã khởi động (T2.0, T2.1 xong) |
| **Giai đoạn kế tiếp** | Tiếp tục P2 từ **T2.2** — thu thập theo từng nước |
| **Tiến độ tổng thể** | 2/8 giai đoạn · 2/9 việc của P2 · 0/11 chương bản thảo |
| **Đang bị chặn** | Không. Hai việc bắt buộc trước khi thu thập đã xong; **R4 đã kiểm** và hiện hình ở dạng hẹp. Còn **4 khoảng trống 🔴** cho Cổng G2 — `sources/gaps.md` §14.3 |
| **Chốt kiểm soát gần nhất phía trước** | **Cổng G2** — rà soát cùng người dùng sau khi xong P2, trước khi viết bất kỳ chương nào |

> **Ghi chú về mức hoàn thành P1.** Toàn bộ 5 hạng mục T1.1-T1.5 đã có hiện vật. Nhưng **xác minh chưa xong**: trong 11 khu vực pháp lý, chỉ 2 văn bản đạt mức ✅ (mở bản gốc) — Biện pháp quản lý tạm thời của Trung Quốc và Master Direction của Ấn Độ. Phần còn lại ở mức ◐ (nhiều nguồn độc lập khớp nhau, chưa mở bản gốc). Nguyên nhân chính là **rào cản truy cập kỹ thuật**, không phải thiếu nguồn — xem `sources/gaps.md` §3.
>
> **Hệ quả**: có thể sang P2, nhưng **không thể sang P3 (viết chương)** trước khi nâng các văn bản trọng yếu lên ✅. Quy tắc `target.md` §7.2 không cho phép viết một khẳng định pháp lý từ nguồn thứ cấp.

---

## 2. Việc tiếp theo

> **T2.2 — Thu thập dữ liệu Trung Quốc** → `data/cn.md`.
>
> Điền theo đúng `data/schema.md`: dạng dài, mỗi dòng một quan sát, 17 cột bắt buộc. Ưu tiên hai ô của `gaps.md` §10 — *số nhà đầu tư bị ảnh hưởng* và *giá trị chưa thu hồi*; nếu không có thì ghi `KHONG-CO` kèm đầy đủ dấu vết đã tìm ở đâu, vì đó là đầu vào của một quyết định tại Cổng G2.
>
> Lưu ý riêng cho Trung Quốc: CCAF **mất 320 đơn vị trả lời** khỏi mẫu do chính các lệnh siết, nên chuỗi số của họ không đo được quá trình xoá sổ (`source-audit-ccaf.md` §8 cảnh báo 5). Phải tìm nguồn khác cho đoạn thanh lý.

**Hai việc bắt buộc trước khi thu thập — ✅ đã xong ngày 2026-07-26:**

- ✅ **Kiểm nguồn có tách được hai thị trường không** (T2.0). Kết quả: tách đầy đủ ở **cấp khu vực**, đứt ở **cấp quốc gia**. R4 hiện hình ở dạng hẹp hơn dự kiến. Hồ sơ: `data/source-audit-ccaf.md`.
- ✅ **Ba câu hỏi "sau khi siết" đã vào danh sách thu thập bắt buộc** (`data/schema.md` §11.1). Kiểm thêm được: cả ba **ngoài tầm nguồn xuyên quốc gia**, phải lấy từ cơ quan quản lý từng nước → rơi vào đoạn 2 → cấm so sánh chéo.

**Ba hệ quả từ T2.0 phải mang theo suốt P2:**

1. **Số tổng của một nước trong phụ lục CCAF là tổng gộp mọi mô hình**, gồm cả gọi vốn cổ phần và quyên góp — **không phải số P2P**. Không dùng như số P2P ở bất kỳ đâu.
2. **Không gộp *Balance Sheet Lending* vào cho vay ngang hàng.** Ở nhiều nước dòng này còn lớn hơn (Indonesia 2018: 57%).
3. **Neo trang G1 phải cẩn thận** — lệch hai hệ số trang, và phần phụ lục thì trích theo tên bảng, không theo số trang.

**Còn lại cho Cổng G2** (không chặn P2): khoảng trống 🔴 #2, #5, #10, #11; quyết định mới về việc hạ yêu cầu tách của `target.md` §5 nguyên tắc 2; hai lệch phạm vi ở `gaps.md` §6 và §13.

**Ràng buộc cần nhớ** (trích từ `target.md`, không thay thế bản gốc):

- Số hiệu văn bản pháp luật **phải xác minh từ nguồn gốc**, tuyệt đối không viết theo trí nhớ — kể cả văn bản Việt Nam.
- Mọi ghi chép về dữ liệu phải tách **cho vay tiêu dùng / doanh nghiệp nhỏ / bất động sản** (`target.md` §2.4). ⚠ T2.0 cho thấy yêu cầu này **không thực hiện được ở cấp quốc gia**; trong khi chờ Cổng G2 quyết, giữ nguyên chiều tách trong lược đồ và ghi giá trị `gộp` kèm mã `C-GOP` ở những ô nguồn không tách.
- Phạm vi thời gian đến **hết 2025**; dữ kiện 2026 phải gắn nhãn "sau mốc phạm vi".
- Nội dung viết bằng tiếng Việt; nguồn ghi ở dạng tra cứu lại được (`target.md` §7.3).

---

## 3. Bảng công việc

**Ký hiệu trạng thái**: ⬜ chưa bắt đầu · 🔄 đang làm · ✅ xong · ⏸ tạm dừng · ⚠ bị chặn · ❌ đã bỏ

### P0 — Xác định phạm vi ✅

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T0.1 | Thống nhất mục tiêu, phạm vi, khung phân tích | ✅ | `target.md` |
| T0.2 | Chốt 7 quyết định nền (`target.md` §0) | ✅ | `target.md` §0 |
| T0.3 | Lập file kế hoạch & theo dõi | ✅ | `plan.md` |

### P1 — Rà soát bối cảnh & xác minh nguồn ✅ (vòng một)

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T1.1 | Dựng cấu trúc thư mục làm việc | ✅ | các thư mục ở §4 |
| T1.2 | Thư mục nguồn nền: báo cáo của tổ chức quốc tế và nghiên cứu khảo sát toàn cầu | ✅ | `sources/sources.md` — 24 nguồn (7 ✅, 17 ◐) |
| T1.3 | **Xác minh văn bản pháp quy** — 11 khu vực pháp lý, xem bảng con bên dưới | ✅ | `sources/legal/*.md` — 11 file |
| T1.4 | Dòng thời gian sơ bộ đa tuyến (mỗi nước một dòng, xếp song song) | ✅ | `notes/timeline.md` — 9 tuyến, 2008-2025 |
| T1.5 | Ghi nhận các khoảng trống nguồn phát hiện được | ✅ | `sources/gaps.md` — 5 🔴, 6 🟡, 6 🟢 |

**T1.3 chi tiết** — mỗi mục cần: tên gốc văn bản, số hiệu, cơ quan ban hành, ngày hiệu lực, đường dẫn, tóm tắt tiếng Việt các điều khoản cốt lõi, ánh xạ vào sáu đòn bẩy L1-L6.

**Cột "Mức"**: mức xác minh cao nhất đạt được trong khu vực đó (`sources/sources.md` §0.1). ✅ = đã mở bản gốc · ◐ = nhiều nguồn độc lập khớp nhau.

| ID | Khu vực pháp lý | TT | Mức | Kết quả vòng một |
|---|---|---|---|---|
| T1.3a | Anh | ✅ | ◐ | 4 văn bản (SI 2013/1881 + điều 36H, PS14/4, PS19/14). **FCA và legislation.gov.uk chặn truy cập tự động** — phải mở thủ công |
| T1.3b | Mỹ | ✅ | ◐ | 5 văn bản/phán quyết. Lỗ hổng đã định danh: quy tắc "bên cho vay thật" của OCC |
| T1.3c | Liên minh châu Âu | ✅ | ◐ cao | **Nhiệm vụ trọng tâm đã trả lời: cho vay tiêu dùng NẰM NGOÀI phạm vi ECSPR.** Cần mở Điều 1 để nâng lên ✅ |
| T1.3d | Latvia + Estonia | ✅ | ◐ | Estonia: luật 2015 + ECSPR. Latvia: tìm được *Kolektīvās finansēšanas pakalpojumu likums* ở vòng 2. Câu hỏi cam kết mua lại **chuyển sang EU** |
| T1.3e | **Trung Quốc** | ✅ | **✅** | 7 văn bản, chuỗi 2015→2020 đầy đủ. Biện pháp quản lý tạm thời 2016 đã mở bản gốc |
| T1.3f | Hàn Quốc | ✅ | ◐ | Luật chuyên biệt 2019/2020. **Có sẵn bản dịch chính thức tầng 1** — nâng lên ✅ dễ |
| T1.3g | Indonesia | ✅ | ◐ | Chuỗi 3 văn bản OJK; vòng 2 xác định **POJK 40/2024 là văn bản chủ**. Nội dung chi tiết còn trống |
| T1.3h | Ấn Độ | ✅ | **✅** | Master Direction 2017 + sửa đổi 2024, đã mở bản gốc. **Hồ sơ đầy đủ nhất về đòn bẩy** |
| T1.3i | Singapore | ✅ | ◐ | Vòng 2 làm rõ cơ chế: **L3 vận hành qua cấu trúc khuyến khích**. Dữ liệu kết quả vẫn bằng không |
| T1.3j | Nhật Bản | ✅ | ◐ | Vòng 2 **giải quyết vấn đề che danh tính** — là hệ quả cấu trúc, gỡ bỏ 18/3/2019. `target.md` §3 cần sửa |
| T1.3k | **Việt Nam** | ✅ | ◐ | 4 văn bản, mọi số hiệu đã xác minh. **Phát hiện: bối cảnh đổi căn bản trong 2025** (Nghị định 94 + 2 quyết định NHNN) |

### P2 — Xương sống dữ liệu định lượng 🔄

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T2.0 | **Kiểm nguồn có tách được hai thị trường không** (rủi ro **R4**) — việc bắt buộc trước khi điền ô dữ liệu nào, `gaps.md` §12 | ✅ | `data/source-audit-ccaf.md` |
| T2.1 | Thiết kế bảng dữ liệu chuẩn (cột theo `target.md` §5, bắt buộc có cột phân loại người vay) | ✅ | `data/schema.md` |
| T2.2 | Thu thập — Trung Quốc | ⬜ | `data/cn.md` |
| T2.3 | Thu thập — Anh | ⬜ | `data/uk.md` |
| T2.4 | Thu thập — Mỹ | ⬜ | `data/us.md` |
| T2.5 | Thu thập — Baltic & Đông Âu | ⬜ | `data/baltic.md` |
| T2.6 | Thu thập — Hàn Quốc, Indonesia, Ấn Độ, Singapore, Nhật | ⬜ | `data/asia.md` |
| T2.7 | Thu thập — Việt Nam (dự kiến rất mỏng; ghi rõ đã tìm gì, không thấy gì) | ⬜ | `data/vn.md` |
| T2.8 | **Báo cáo độ phủ dữ liệu**: khu vực nào đủ, khu vực nào không, ảnh hưởng tới kết luận ra sao | ⬜ | `data/coverage.md` |

> ### 🚩 CỔNG G2 — DỪNG LẠI RÀ SOÁT CÙNG NGƯỜI DÙNG
> Sau T2.8, **dừng và trình bày báo cáo độ phủ dữ liệu**. Không tự động chuyển sang P3.
> Nếu xương sống dữ liệu mỏng hơn dự kiến, đây là thời điểm điều chỉnh phạm vi — không phải sau khi đã viết xong các chương.

### P3 — Các chương quốc gia ⬜

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T3.0 | Ch. 2 — Nguồn gốc, định nghĩa, khung phân tích. **Viết lại từ `target.md` §2 thành văn bản báo cáo**, làm trước để neo các chương quốc gia | ⬜ | `content/ch02-khung-phan-tich.md` |
| T3.1 | Ch. 6 — Trung Quốc (làm trước: dài nhất, khó nhất) | ⬜ | `content/ch06-trung-quoc.md` |
| T3.2 | Ch. 3 — Anh | ⬜ | `content/ch03-anh.md` |
| T3.3 | Ch. 4 — Mỹ | ⬜ | `content/ch04-my.md` |
| T3.4 | Ch. 5 — Baltic & Đông Âu | ⬜ | `content/ch05-baltic-dong-au.md` |
| T3.5 | Ch. 7 — Châu Á khác | ⬜ | `content/ch07-chau-a-khac.md` |

### P4 — Các chương xuyên quốc gia ⬜

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T4.1 | Ch. 8 — Tách hai thị trường: tiêu dùng vs doanh nghiệp nhỏ | ⬜ | `content/ch08-hai-thi-truong.md` |
| T4.2 | Ch. 9 — Giải phẫu các biến tướng | ⬜ | `content/ch09-bien-tuong.md` |
| T4.3 | Ch. 10 — Tổng hợp so sánh | ⬜ | `content/ch10-tong-hop.md` |

### P5 — Chương Việt Nam ⬜

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T5.1 | Ch. 11 — Việt Nam, **mở đầu bằng tuyên bố giới hạn dữ liệu** | ⬜ | `content/ch11-viet-nam.md` |
| T5.2 | Bản đồ không gian lựa chọn thể chế (trình bày cân bằng, không xếp hạng) | ⬜ | trong `ch11` |

### P6 — Kiểm tra tính toàn vẹn ⬜

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T6.1 | Đối chiếu lại từng trích dẫn với nguồn gốc | ⬜ | `checks/citations.md` |
| T6.2 | Rà mâu thuẫn nội bộ giữa các chương (đặc biệt số liệu bị nhắc ở nhiều chỗ) | ⬜ | `checks/consistency.md` |
| T6.3 | Kiểm tra tuân thủ quy tắc tách hai thị trường (`target.md` §2.4) | ⬜ | `checks/market-split.md` |
| T6.4 | Kiểm tra chuẩn mực tài liệu tham chiếu — ba tầng phát biểu có tách bạch không (`target.md` §7.4) | ⬜ | `checks/reference-standard.md` |

### P7 — Hoàn thiện ⬜

| ID | Việc | TT | Hiện vật |
|---|---|---|---|
| T7.1 | PL A — Dòng thời gian đối chiếu | ⬜ | `content/pl-a-dong-thoi-gian.md` |
| T7.2 | PL B — Phiếu hồ sơ ~30 nền tảng | ⬜ | `content/pl-b-ho-so-nen-tang.md` |
| T7.3 | PL C — Bảng so sánh sáu đòn bẩy L1-L6 | ⬜ | `content/pl-c-don-bay.md` |
| T7.4 | PL D — Thuật ngữ đối chiếu Việt–Anh–Trung–Hàn | ⬜ | `content/pl-d-thuat-ngu.md` |
| T7.5 | PL E — Mục lục tra cứu | ⬜ | `content/pl-e-tra-cuu.md` |
| T7.6 | Ch. 1 — Cách đọc + tổng quan phát hiện chính (**viết sau cùng**) | ⬜ | `content/ch01-tong-quan.md` |
| T7.7 | Ghép bản cuối | ⬜ | `content/bao-cao-p2p-lending.md` |

---

## 4. Hiện vật & cấu trúc thư mục

### 4.1. Quy tắc phân vùng

**Toàn bộ đầu ra của nghiên cứu — mọi chương, mọi phụ lục, bản ghép cuối — nằm trong thư mục `content/`.** Không viết nội dung báo cáo ra ngoài thư mục này.

| Vùng | Chứa gì | Vai trò |
|---|---|---|
| **`content/`** | Các chương, phụ lục, bản ghép cuối | **Đầu ra** — thứ người đọc nhận được |
| `sources/`, `data/`, `notes/` | Nguồn, dữ liệu thô, ghi chú, dòng thời gian | Nguyên liệu — làm ra đầu ra, không phải đầu ra |
| `checks/` | Kết quả kiểm tra toàn vẹn | Quy trình chất lượng |
| `target.md`, `plan.md` | Phạm vi và trạng thái | Điều hành dự án |

Lý do tách: `content/` phải luôn ở trạng thái xuất bản được — mở ra là thấy đúng báo cáo, không lẫn ghi chú làm việc dở dang. Muốn giao nộp hay xuất bản thì bàn giao đúng một thư mục.

### 4.2. Cấu trúc mục tiêu

Dựng dần theo tiến độ, chưa cần có ngay từ đầu:

```
research/P2P Lending/
├── target.md                  ✅ phạm vi & mục tiêu (nguồn chân lý)
├── plan.md                    ✅ file này — kế hoạch & trạng thái
│
├── content/                   ⬜ ★ ĐẦU RA — toàn bộ nội dung báo cáo
│   ├── ch01-tong-quan.md              ⬜
│   ├── ch02-khung-phan-tich.md        ⬜
│   ├── ch03-anh.md                    ⬜
│   ├── ch04-my.md                     ⬜
│   ├── ch05-baltic-dong-au.md         ⬜
│   ├── ch06-trung-quoc.md             ⬜
│   ├── ch07-chau-a-khac.md            ⬜
│   ├── ch08-hai-thi-truong.md         ⬜
│   ├── ch09-bien-tuong.md             ⬜
│   ├── ch10-tong-hop.md               ⬜
│   ├── ch11-viet-nam.md               ⬜
│   ├── pl-a-dong-thoi-gian.md         ⬜
│   ├── pl-b-ho-so-nen-tang.md         ⬜
│   ├── pl-c-don-bay.md                ⬜
│   ├── pl-d-thuat-ngu.md              ⬜
│   ├── pl-e-tra-cuu.md                ⬜
│   └── bao-cao-p2p-lending.md         ⬜ bản ghép cuối
│
├── sources/                   ✅ nguyên liệu
│   ├── sources.md             ✅ thư mục nguồn có chú giải — 24 nguồn
│   ├── gaps.md                ✅ khoảng trống nguồn đã phát hiện
│   └── legal/                 ✅ văn bản pháp quy, mỗi khu vực một file
│       └── {cn,uk,us,eu,baltic,kr,id,in,sg,jp,vn}.md   ✅ 11 file
├── data/                      🔄 nguyên liệu (P2)
│   ├── schema.md              ✅ định nghĩa cột của bảng dữ liệu
│   ├── source-audit-ccaf.md   ✅ kiểm mức tách hai thị trường (R4)
│   ├── coverage.md            ⬜ báo cáo độ phủ (đầu vào của Cổng G2)
│   └── {cn,uk,us,baltic,asia,vn}.md   ⬜
├── notes/                     ✅ nguyên liệu
│   └── timeline.md            ✅ dòng thời gian đa tuyến, 9 tuyến 2008-2025
└── checks/                    ⬜ kết quả kiểm tra toàn vẹn (P6)
```

> **Lưu ý về chương 2**: chương "Nguồn gốc, định nghĩa, khung phân tích" lấy nội dung từ `target.md` §2 nhưng phải được **viết lại thành văn bản báo cáo** trong `content/ch02-khung-phan-tich.md`. Không dùng `target.md` làm chương 2 — hai file phục vụ hai mục đích khác nhau.

---

## 5. Nhật ký quyết định

Ghi lại để không bàn lại chuyện đã chốt. **Chỉ thêm dòng mới, không sửa dòng cũ** — nếu một quyết định bị đảo, thêm dòng mới ghi rõ nó thay thế dòng nào.

| ID | Ngày | Quyết định | Nơi ghi đầy đủ |
|---|---|---|---|
| D1 | 2026-07-26 | Lĩnh vực: chính sách/pháp lý | `target.md` §0.1 |
| D2 | 2026-07-26 | Thể loại: tài liệu tham chiếu chung — lập bản đồ, không kê đơn | `target.md` §0.2, §7.4 |
| D3 | 2026-07-26 | Việt Nam có chương riêng, là đích đến của bài học quốc tế | `target.md` §0.3 |
| D4 | 2026-07-26 | "Châu Âu đang phát triển" = Baltic + Đông Âu | `target.md` §0.4 |
| D5 | 2026-07-26 | Báo cáo sâu, nhiều phần; Trung Quốc là chương dài nhất | `target.md` §0.5 |
| D6 | 2026-07-26 | Mốc kết thúc phạm vi: hết 2025 | `target.md` §0.6 |
| D7 | 2026-07-26 | Tách cho vay tiêu dùng / doanh nghiệp nhỏ thành trục cắt ngang | `target.md` §0.7, §2.4 |
| D8 | 2026-07-26 | Chương Việt Nam theo hướng phân tích thể chế, kèm tuyên bố giới hạn dữ liệu | `target.md` §6 |
| D9 | 2026-07-26 | Ngôn ngữ: nội dung tiếng Việt, nguồn ghi dạng tra cứu được, thuật ngữ gốc dồn về PL D | `target.md` §7.3 |
| D10 | 2026-07-26 | **Xương sống định lượng chia hai đoạn** (phương án B): 2013-2020 so sánh chéo được; 2021-2025 chỉ mô tả theo từng nước, cấm so sánh chéo | `target.md` §5.1 |
| D11 | 2026-07-26 | **Rút giả thuyết can thiệp ở G1.** Không nước nào điều tiết trước khi thị trường hình thành; trục SQ4 viết lại theo mốc đã xác minh | `target.md` §2.3, §1.2 · thay phần G1 của D-gốc trong §2.3 v0.1 |
| D12 | 2026-07-26 | **Sửa mô tả Singapore**: không phải "quản chặt từ đầu" mà là **định giá việc nhận vốn của nhà đầu tư lẻ** — L3 qua cấu trúc khuyến khích | `target.md` §3 Tầng 3 |
| D13 | 2026-07-26 | **Sửa mô tả Nhật Bản**: che danh tính không phải quy định che giấu mà là **hệ quả ngoài ý muốn của nghĩa vụ đăng ký áp lên nhà đầu tư**; gỡ bỏ 18/3/2019 | `target.md` §3 Tầng 3 |

---

## 6. Nhật ký phiên làm việc

Mỗi phiên ghi **một dòng**, thêm vào cuối bảng. Ngắn gọn, nêu đúng ba thứ: đã làm gì, đã đổi trạng thái nào, để lại việc gì.

| Ngày | Đã làm | Trạng thái thay đổi | Để lại |
|---|---|---|---|
| 2026-07-26 | Thảo luận và chốt phạm vi qua 5 vòng hỏi đáp; lập `target.md`; lập `plan.md` | P0 → ✅ | Khởi động P1 từ T1.1 |
| 2026-07-26 | Chạy trọn P1: dựng thư mục; lập thư mục nguồn nền (24 nguồn); xác minh văn bản pháp quy 11 khu vực (2 vòng); dựng dòng thời gian đa tuyến; lập sổ khoảng trống | T1.1-T1.5 → ✅ · P1 → ✅ vòng một | Rà soát cùng người dùng trước P2 |
| 2026-07-26 | Rà soát kết quả P1; chốt phương án B cho đứt gãy dữ liệu; sửa 3 chỗ trong `target.md` (Nhật Bản, Singapore, giả thuyết G1) → `target.md` lên v0.2 | D10-D13 ghi vào §5 · R1 → ✅ đã xử lý | Khởi động P2 từ T2.1; hai việc bắt buộc làm trước khi điền dữ liệu (§2) |
| 2026-07-26 | Vào P2: mở toàn văn G1+G2, kiểm toàn vẹn tệp, đọc phương pháp + bảng mô hình + phụ lục + toàn bộ 35 phiếu hồ sơ quốc gia → kết luận R4; thiết kế lược đồ dữ liệu dạng dài; cập nhật `gaps.md` (§2, §8.2, §11, §12, §14) và `sources.md` (§1.1, §6) | T2.0 mới lập → ✅ · T2.1 → ✅ · P2 → 🔄 · R4 → ⚠ hiện hình dạng hẹp | Thu thập từ T2.2 (Trung Quốc). Ba hệ quả của T2.0 phải mang theo (§2) |

---

## 7. Rủi ro đang theo dõi

Đồng bộ với `target.md` §10. Cập nhật cột trạng thái khi có diễn biến.

| ID | Rủi ro | Phát hiện ở | TT |
|---|---|---|---|
| R1 | Xương sống dữ liệu mỏng hơn dự kiến ở một hoặc nhiều khu vực | ~~Cuối P2~~ → P1 | ✅ **Đã xử lý** — quyết định **D10**, phương án B: hai đoạn dữ liệu (`target.md` §5.1). Rủi ro còn lại chuyển dạng: *đoạn 1 (2013-2020) có đủ dày đỡ chương 10 không* — kiểm cuối P2 |
| R2 | Số liệu Trung Quốc mâu thuẫn nghiêm trọng giữa các nguồn | P1-P2 | ⚠ **Đã hiện hình, ở dạng nặng hơn dự kiến**: không chỉ là các nguồn mâu thuẫn, mà **hai đại lượng đo tổn thất xã hội có thể không nguồn nào công bố**. `gaps.md` §10 |
| R3 | Chương Việt Nam thiếu nền định lượng tới mức ảnh hưởng độ tin cậy | P5 | ⚠ **Đã xác nhận ở P1**, sớm hơn bốn giai đoạn. **Nhẹ đi một phần ở T2.0**: tìm được chuỗi tổng khối lượng 2018-2020 và số nền tảng, nhưng là **số gộp mọi mô hình** và đếm cả nền tảng nước ngoài. D8 vẫn đứng. `gaps.md` §2.1 |
| R4 | Nguồn không tách được tiêu dùng / doanh nghiệp nhỏ | P2 | ⚠ **Đã kiểm ở T2.0 — hiện hình ở dạng hẹp hơn dự kiến.** Không phải "không tách được": tách **đầy đủ ở cấp khu vực**, **đứt ở cấp quốc gia** (ngưỡng 10 quan sát/nước/mô hình). Chương 8 đổi nền sang bảng cấp khu vực. Quyết định còn lại — có hạ yêu cầu của `target.md` §5 nguyên tắc 2 không — đưa ra Cổng G2. `data/source-audit-ccaf.md` |

> **Cả bốn rủi ro đều đã chạm tới ở P1**, sớm hơn dự kiến của kế hoạch. Không rủi ro nào chặn hoàn toàn, nhưng không rủi ro nào còn là giả định.

---

## 8. Quy tắc bảo trì file này

1. **Cập nhật ngay khi đổi trạng thái**, không dồn đến cuối phiên rồi cập nhật một lượt theo trí nhớ.
2. **Không đánh ✅ nếu hiện vật chưa tồn tại** ở đúng đường dẫn ghi tại §4.
3. **Không chép nội dung phạm vi từ `target.md` sang đây.** Chỉ tham chiếu bằng số mục. Hai file trôi khỏi nhau là hỏng cả hai.
4. **Nhật ký quyết định (§5) và nhật ký phiên (§6) chỉ thêm, không sửa.**
5. Khi phát hiện việc mới phát sinh, **thêm ID mới vào đúng giai đoạn** thay vì nhét vào ghi chú của việc khác.
6. Khi tới một cổng kiểm soát (hiện có Cổng G2), **dừng thật** — không tự vượt cổng dù thấy đủ dữ kiện để đi tiếp.
7. **Mọi nội dung báo cáo ghi vào `content/`** (§4.1). Ghi chú, dữ liệu thô, nguồn không được để lẫn vào đó — `content/` phải luôn ở trạng thái xuất bản được.
