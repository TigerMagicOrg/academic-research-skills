# Dữ liệu định lượng — Anh

> **Hiện vật của T2.3** (`plan.md` §3). Ghi theo `data/schema.md`.
> **Ngày thu thập**: 2026-07-26.
>
> `khu_vuc` = **Anh** · `cap` = **quốc gia** cho mọi dòng trong file này, khai ở tiêu đề bảng thay vì
> lặp ở từng dòng (mẫu `schema.md` §10.1); cột `doan` do chính bảng khai báo.
> **Đơn vị giữ nguyên theo nguồn**: UKD-1 công bố bằng bảng Anh, G1 và G2 công bố bằng USD đã quy đổi.
> Không tự quy đổi — mọi dòng USD mang `C-TYGIA`, dòng GBP thì không (xem §1.2).

---

## 0. Bốn phát hiện của lần thu thập này — đọc trước khi dùng bất kỳ con số nào

### 0.1. Anh là ảnh phản chiếu của Trung Quốc về mặt chất lượng nguồn

`data/cn.md` §0 kết luận Trung Quốc **không có một chuỗi số nào do cơ quan quản lý công bố cho giai
đoạn đỉnh**, và mọi dòng đều tầng 5. Anh ngược lại ở đoạn 1: ba nguồn CCAF đều **đã mở bản gốc, kiểm
sha256, kiểm toàn vẹn tệp PASS**, và **có tách theo loại người vay đầy đủ ở cấp quốc gia** — thứ mà
`data/source-audit-ccaf.md` kết luận là đứt ở hầu hết các nước khác.

Hệ quả trực tiếp: **đây là file dữ liệu đầu tiên có dòng đạt `✅`**, nên là file đầu tiên có dòng đủ
điều kiện trích sang `content/` theo `schema.md` §12 kiểm 10.

Nhưng sự đối xứng chỉ đúng ở đoạn 1. Ở đoạn 2 (2021-2025) Anh **tệ ngang Trung Quốc**, vì lý do khác:
xem §0.4.

### 0.2. Hai thị trường tách nhau rõ rệt — và tách theo hai hướng ngược nhau

Đây là phát hiện có giá trị nhất của lần thu thập này, và nó đi thẳng vào **chương 8** (`target.md`
§2.4, SQ7). Cho vay tiêu dùng và cho vay doanh nghiệp ở Anh **không cùng một quỹ đạo**:

| Doanh số giải ngân | 2019 | 2020 | Đổi |
|---|---|---|---|
| P2P cho vay **doanh nghiệp** | $2.538m | $3.262m | **+29%** |
| P2P cho vay **tiêu dùng** | $2.161m | $255m | **−88%** |

Cùng một nước, cùng một năm, cùng một khung điều tiết, cùng một cú sốc COVID — hai kết cục ngược
chiều. Không thể giải thích bằng biến số vĩ mô chung, nên nó là bằng chứng mạnh cho luận điểm trung
tâm của `target.md` §2.4: *hai thị trường khác nhau đội chung một cái tên*.

### 0.3. Nguyên nhân của cú sập tiêu dùng đã được nguồn nêu đích danh — và nó trả lời SQ5

G2 (tr. 75) **tự giải thích** cú giảm: phần lớn là do **Zopa — nền tảng ngang hàng đầu tiên trên thế
giới — lấy được giấy phép ngân hàng đầy đủ năm 2020 và trở thành ngân hàng số**, nên khối lượng của
Zopa không còn được xếp vào cho vay ngang hàng nữa.

Đây đúng là tình huống mà `target.md` §7.5 định nghĩa sẵn: *một nền tảng sống sót bằng cách từ bỏ mô
hình P2P **không phải** bằng chứng P2P thành công — nó là bằng chứng ngược lại.* Ở đây ta có một
trường hợp đo được bằng số: mô hình bán lẻ ngang hàng ở nước khai sinh ra nó thu hẹp **88% trong một
năm**, không phải vì đổ vỡ, không phải vì bị cấm, mà vì người dẫn đầu **tự nguyện bước ra**.

> ⚠ **Chưa được viết thành kết luận cho SQ5 ở giai đoạn này.** Mới có một năm và một nền tảng. Phần
> còn lại của cú giảm (ngoài Zopa) chưa tách được — G2 không cho biết Zopa chiếm bao nhiêu trong
> $1.906m sụt giảm. Ghi thành việc 3 ở §6.

### 0.4. Đoạn 2 bị chặn ở nguồn gốc, và khoảng trống đó đang được lấp bằng số rác

`fca.org.uk` trả về **HTTP 403** với truy cập tự động ngày 2026-07-26 — đúng rào cản đã ghi ở
`plan.md` T1.3a và `gaps.md` §3. Theo `schema.md` §6 đây là `BI-CHAN` (nguồn tồn tại, chặn truy cập),
**không phải** `CHUA-TIM`.

Điều đáng ghi hơn: chỗ trống đó **không trống trên mạng**. Tra cứu công khai trả về một loạt con số
"quy mô thị trường P2P Anh" từ các hãng nghiên cứu thương mại, và chúng **không đo cùng một thứ**:

| Con số gặp phải | Thực chất đo gì |
|---|---|
| £283 triệu (2022) | **Doanh thu của các nền tảng**, không phải khối lượng cho vay |
| £376,6 triệu (2023) | Cũng là doanh thu ngành, nguồn khác |
| 3,2 tỷ USD (2022) | Khối lượng cho vay — khác đại lượng, khác đơn vị tiền |

Ba con số này bị trình bày lẫn lộn dưới cùng một nhãn "market size", chênh nhau **một bậc độ lớn**, và
không nguồn nào công bố phương pháp. **Không dòng nào trong số đó được đưa vào bảng.** Chúng thuộc
dưới tầng 5 của `target.md` §7.1 — không phải số nền tảng tự công bố, mà là số của bên thứ ba bán báo
cáo, không có phương pháp kiểm được.

> Đây là một quan sát về phương pháp đáng mang sang các nước khác: **khi nguồn chính thức bị chặn,
> khoảng trống không im lặng — nó được lấp bằng số của các hãng bán báo cáo.** Rủi ro không phải là
> thiếu số, mà là nhặt nhầm số. Đối chiếu với `data/cn.md` §5 mục 1, nơi khoảng trống thật sự im lặng
> (không ai công bố gì cho 2020) — hai hình thái khoảng trống khác nhau, cần xử lý khác nhau.

---

## 1. Nguồn dùng trong file này

### 1.1. Danh mục

| Mã | Nguồn | Tầng | TT |
|---|---|---|---|
| `G1` | CCAF, *The Global Alternative Finance Market Benchmarking Report* (4/2020, dữ liệu 2018). Đã có mã ở `sources.md` §1.1 | 3 | ✅ |
| `G2` | CCAF, *The 2nd Global Alternative Finance Market Benchmarking Report* (6/2021, dữ liệu 2019-2020). Đã có mã ở `sources.md` §1.1 | 3 | ✅ |
| `UKD-1` | **Nguồn mới — nay đã đăng ký ở `sources.md` §1.1 với mã chính thức `G3-UK`.** Zhang, B., Ziegler, T., Garvey, K., et al. *The 5th UK Alternative Finance Industry Report*. Cambridge Centre for Alternative Finance, Cambridge Judge Business School, 11/2018. Dữ liệu 2014-2017, công bố bằng GBP. PDF: `https://www.jbs.cam.ac.uk/fileadmin/user_upload/research/centres/alternative-finance/downloads/2018-5th-uk-alternative-finance-industry-report.pdf` | 3 | ✅ |
| `UKD-2` | `fca.org.uk` — Cơ quan Quản lý Ứng xử Tài chính Anh. Trang dữ liệu nền tảng cho vay ngang hàng. **HTTP 403 với truy cập tự động** ngày 2026-07-26; phải mở thủ công | 1-2 | ⬜ **chưa mở được** |

**Kiểm toàn vẹn tệp** (`scripts/pdf_read_preflight.py`, 2026-07-26) — cả ba PDF **PASS**, không cắt cụt:

| Nguồn | sha256 | Số trang |
|---|---|---|
| G1 | `49cec180…65de1` | 228 |
| G2 | `dd2860b1…c37a3` | 197 |
| UKD-1 | `43858d6f…6b1f68` | 56 |

G1 và G2 khớp **đúng từng ký tự** với sha256 đã ghi ở `sources.md` §1.1 từ phiên trước → xác nhận là
cùng một tệp, không phải bản khác cùng tên.

### 1.2. Hai quy ước riêng của file này

**(a) Mã cảnh báo CCAF — không áp máy móc cả bốn.** `sources.md` §1.1 quy định bốn mã mặc định cho mọi
số CCAF: `C-KHAOSAT`, `C-SONGSOT`, `C-MAU`, `C-TYGIA`. Ba mã đầu áp cho **mọi** dòng CCAF trong file
này. Riêng `C-TYGIA` **chỉ áp cho dòng USD** (G1, G2): nó cảnh báo sai lệch do quy đổi ngoại tệ, mà
dòng UKD-1 là **số bảng Anh của một thị trường Anh — không có phép quy đổi nào xảy ra**. Gắn
`C-TYGIA` vào đó là cảnh báo một rủi ro không tồn tại, làm loãng giá trị của chính mã cảnh báo.

**(b) Neo nguồn G1 không dùng số trang.** Phiếu hồ sơ quốc gia *United Kingdom* của G1 nằm trong phần
phụ lục và **không có số trang in đọc được trên trang đó**. `plan.md` §2 ghi "tr. 221" — con số đó
**không dùng làm neo**, đúng theo `schema.md` §8 (*"PDF không xác định được trang → tên bảng hoặc tên
mục, không đoán số trang"*) và đúng cảnh báo T2.0 số 3. Đo lại độ lệch trang của G1 trong lần này:
**dao động từ −2 tới −14**, xác nhận `C-TRANG`. G2 và UKD-1 ngược lại có độ lệch **ổn định −1**, nên
neo số trang in được và không cần `C-TRANG`.

---

## 2. Đoạn 1 — 2013-2020 (so sánh chéo được)

`khu_vuc` = Anh · `cap` = quốc gia · `doan` = **1**

| ma | nam | chi_tieu | loai_nguoi_vay | mo_hinh | gia_tri | don_vi | nguon | neo | tang | tu_cong_bo | ngay_truy_cap | trang_thai | canh_bao | ghi_chu |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| UK-2014-GIAINGAN-TD | 2014 | GIAINGAN | tiêu dùng | ngang hàng | 547 | triệu GBP | UKD-1 | biểu đồ *Total UK Alternative Finance Market Volume by Key Model, 2014-2017*, tr. 12 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | *P2P Consumer Lending* |
| UK-2015-GIAINGAN-TD | 2015 | GIAINGAN | tiêu dùng | ngang hàng | 909 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2016-GIAINGAN-TD | 2016 | GIAINGAN | tiêu dùng | ngang hàng | 1169 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2017-GIAINGAN-TD | 2017 | GIAINGAN | tiêu dùng | ngang hàng | 1403 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | Nguồn nêu tăng 20% so 2016 — **khớp phép chia 1403/1169 = 20,0%** |
| UK-2018-GIAINGAN-TD | 2018 | GIAINGAN | tiêu dùng | ngang hàng | 1800 | triệu USD | G1 | phiếu hồ sơ quốc gia *United Kingdom*, phần phụ lục hồ sơ nước | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-TRANG | Nguồn ghi **17%** tổng khối lượng ($10.368m) và làm tròn thành "$1,8 tỷ". Ghi đúng số nguồn nêu, không tự nhân lại |
| UK-2019-GIAINGAN-TD | 2019 | GIAINGAN | tiêu dùng | ngang hàng | 2161 | triệu USD | G2 | Bảng 2.2 *UK Volume by Model Type 2019-2020*, tr. 75 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA | |
| UK-2020-GIAINGAN-TD | 2020 | GIAINGAN | tiêu dùng | ngang hàng | 255 | triệu USD | G2 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA | **−88% trong một năm.** Nguồn tự nêu nguyên nhân chính: Zopa chuyển thành ngân hàng số — xem §0.3 |
| UK-2014-GIAINGAN-DN | 2014 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 749 | triệu GBP | UKD-1 | biểu đồ *…by Key Model, 2014-2017*, tr. 12 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | *P2P Business Lending*. `C-QUYMO` bắt buộc theo `schema.md` §4.3 — nguồn không tách theo quy mô doanh nghiệp |
| UK-2015-GIAINGAN-DN | 2015 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 881 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | |
| UK-2016-GIAINGAN-DN | 2016 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 1232 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | |
| UK-2017-GIAINGAN-DN | 2017 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 2039 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | Nguồn nêu tăng 66% — **khớp 2039/1232 = 65,5%**. Mô hình lớn nhất thị trường Anh năm 2017 |
| UK-2018-GIAINGAN-DN | 2018 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 2500 | triệu USD | G1 | phiếu hồ sơ quốc gia *United Kingdom* | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-TRANG, C-QUYMO | Nguồn ghi **24,5%** tổng khối lượng, làm tròn "$2,5 tỷ" |
| UK-2019-GIAINGAN-DN | 2019 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 2538 | triệu USD | G2 | Bảng 2.2, tr. 75 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-QUYMO | |
| UK-2020-GIAINGAN-DN | 2020 | GIAINGAN | doanh nghiệp nhỏ | ngang hàng | 3262 | triệu USD | G2 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-QUYMO | **+29% trong khi tiêu dùng −88%** — xem §0.2. G2 tr. 76 ghi nước đứng thứ hai là Ý ($808m), tức Anh gấp **4 lần** nước kế tiếp |
| UK-2014-GIAINGAN-BDS | 2014 | GIAINGAN | bất động sản | ngang hàng | `KHONG-CO` | — | UKD-1 | biểu đồ *…by Key Model, 2014-2017*, tr. 12 | 3 | không | 2026-07-26 | ✅ | — | Biểu đồ có cột 2014 cho các mô hình khác nhưng **để trống ô này** (ký hiệu "-"), tức mô hình chưa được tách riêng năm 2014, không phải bằng 0 |
| UK-2015-GIAINGAN-BDS | 2015 | GIAINGAN | bất động sản | ngang hàng | 609 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | *P2P Property Lending*. Tiểu loại có tên riêng theo `target.md` §2.4, **không gộp vào doanh nghiệp nhỏ** |
| UK-2016-GIAINGAN-BDS | 2016 | GIAINGAN | bất động sản | ngang hàng | 1147 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2017-GIAINGAN-BDS | 2017 | GIAINGAN | bất động sản | ngang hàng | 1218 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | Nguồn nêu tăng 6% — **khớp 1218/1147 = 6,2%**. Tăng trưởng chậm hẳn lại |
| UK-2018-GIAINGAN-BDS | 2018 | GIAINGAN | bất động sản | ngang hàng | 2100 | triệu USD | G1 | phiếu hồ sơ quốc gia *United Kingdom* | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-TRANG | Nguồn ghi **19,8%** tổng khối lượng, làm tròn "$2,1 tỷ" |
| UK-2019-GIAINGAN-BDS | 2019 | GIAINGAN | bất động sản | ngang hàng | 1899 | triệu USD | G2 | Bảng 2.2, tr. 75 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA | |
| UK-2020-GIAINGAN-BDS | 2020 | GIAINGAN | bất động sản | ngang hàng | 1312 | triệu USD | G2 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA | Giảm 31%. Là mảng gắn với vụ đổ vỡ Lendy — xem §5 mục 4 |
| UK-2014-GIAINGAN-GOP | 2014 | GIAINGAN | gộp | gộp | 1740 | triệu GBP | UKD-1 | biểu đồ *Total UK Alternative Finance Market Volume*, tr. 11 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | ⚠ **Tổng mọi mô hình tài chính thay thế, KHÔNG phải số P2P** — gồm cả gọi vốn cổ phần, quyên góp, thưởng. Cảnh báo 1 của T2.0. Không dùng như số P2P ở bất kỳ đâu |
| UK-2015-GIAINGAN-GOP | 2015 | GIAINGAN | gộp | gộp | 3200 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | như trên |
| UK-2016-GIAINGAN-GOP | 2016 | GIAINGAN | gộp | gộp | 4580 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | như trên |
| UK-2017-GIAINGAN-GOP | 2017 | GIAINGAN | gộp | gộp | 6190 | triệu GBP | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | Nguồn nêu tăng 35,15% |
| UK-2018-GIAINGAN-GOP | 2018 | GIAINGAN | gộp | gộp | 10368 | triệu USD | G1 | phiếu hồ sơ quốc gia *United Kingdom* | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-TRANG, C-GOP, C-DINHNGHIA | Nguồn ghi Anh chiếm **57%** tổng khối lượng châu Âu 2018, xếp **thứ 3 thế giới**. Vẫn là số gộp mọi mô hình |
| UK-2019-GIAINGAN-GOP | 2019 | GIAINGAN | gộp | gộp | 11016 | triệu USD | G2 | Bảng 2.2, tr. 75 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-GOP, C-DINHNGHIA | |
| UK-2020-GIAINGAN-GOP | 2020 | GIAINGAN | gộp | gộp | 12643 | triệu USD | G2 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-TYGIA, C-GOP, C-DINHNGHIA | ⚠ **Tổng tăng trong khi P2P tiêu dùng sập.** Phần tăng đến từ quyên góp ($5.769m, mô hình lớn nhất 2020 do COVID) — minh hoạ rõ nhất vì sao cấm dùng số gộp để phát biểu về P2P |
| UK-2015-VONLE-TD | 2015 | VONLE | tiêu dùng | ngang hàng | 32 | % | UKD-1 | biểu đồ *Proportion of Funding from Institutional Investors, 2015-2017*, tr. 18 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | **Tỷ trọng vốn định chế**; phần còn lại là vốn lẻ. Mẫu số = tổng khối lượng của chính mô hình đó |
| UK-2016-VONLE-TD | 2016 | VONLE | tiêu dùng | ngang hàng | 32 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2017-VONLE-TD | 2017 | VONLE | tiêu dùng | ngang hàng | 39 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | Nguồn ghi tương ứng **£554 triệu** vốn định chế |
| UK-2015-VONLE-DN | 2015 | VONLE | doanh nghiệp nhỏ | ngang hàng | 26 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | |
| UK-2016-VONLE-DN | 2016 | VONLE | doanh nghiệp nhỏ | ngang hàng | 28 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | |
| UK-2017-VONLE-DN | 2017 | VONLE | doanh nghiệp nhỏ | ngang hàng | 40 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-QUYMO | Nguồn ghi tương ứng **£815 triệu** vốn định chế |
| UK-2015-VONLE-BDS | 2015 | VONLE | bất động sản | ngang hàng | 25 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2016-VONLE-BDS | 2016 | VONLE | bất động sản | ngang hàng | 25 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | |
| UK-2017-VONLE-BDS | 2017 | VONLE | bất động sản | ngang hàng | 34 | % | UKD-1 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU | Số tiền tương ứng nguồn nêu **không nhất quán** — xem §4.2 |
| UK-2019-VONLE-GOP | 2019 | VONLE | gộp | gộp | 43 | % | G2 | mục *Institutionalisation*, tr. 84 | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | **Cấp quốc gia, gộp mọi mô hình** — không nối tiếp được với ba chuỗi theo mô hình ở trên |
| UK-2020-VONLE-GOP | 2020 | VONLE | gộp | gộp | 66 | % | G2 | như trên | 3 | không | 2026-07-26 | ✅ | C-KHAOSAT, C-SONGSOT, C-MAU, C-GOP, C-DINHNGHIA | Tăng 23 điểm trong một năm. Một phần là hệ quả số học của việc mảng tiêu dùng (vốn lẻ cao) sập, chứ không chỉ là vốn định chế vào thêm |
| UK-2020-NENTANG-NA-HOATDONG | 2020 | NENTANG | không áp dụng | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | Cơ quan quản lý Anh có danh sách nền tảng được cấp phép theo điều 36H, nhưng `fca.org.uk` trả **HTTP 403** với truy cập tự động. Phải mở thủ công — xem §5 mục 1 |
| UK-2017-NOXAU-GOP | 2017 | NOXAU | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | Chưa tra trong ba nguồn CCAF theo từ khoá nợ xấu / quá hạn / theo lứa vay. Việc 4 ở §6 |
| UK-2017-LAISUAT-GOP | 2017 | LAISUAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | Chi phí phía **người vay** đã gồm phí. Chưa tra |
| UK-2017-LOITUC-GOP | 2017 | LOITUC | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | Lợi suất phía **người cho vay** — mã mới thêm ở T2.2a. Anh là nước dự đoán có chỉ tiêu này (lợi suất chào mời là số nền tảng quảng cáo). Chưa tra |
| UK-2019-TONTHAT-GOP-TIEN | 2019 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | **Giá trị chưa thu hồi** vụ Lendy (đổ vỡ 2019, mảng bất động sản). `target.md` §3 nêu đích danh Lendy nhưng chưa có số. Việc 5 ở §6 |
| UK-2019-TONTHAT-GOP-NGUOI | 2019 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | **Số nhà đầu tư bị ảnh hưởng** vụ Lendy. Đại lượng đối xứng với ô còn mở của Trung Quốc (`cn.md` §5 mục 2) |

---

## 3. Đoạn 2 — 2021-2025 (chỉ mô tả theo từng nước)

> ⚠ **Không so sánh chéo giữa các nước.** Số trong bảng này lấy từ cơ quan quản lý từng
> nước, mỗi nước một định nghĩa và một cách đếm. Chỉ dùng để mô tả diễn biến nội bộ của
> chính thị trường này theo thời gian. Không đặt cạnh số của nước khác, không cộng tổng
> khu vực, không phát biểu nước nào lớn hơn nước nào. Căn cứ: quyết định **D10**,
> `target.md` §5.1.
>
> **Định nghĩa nguồn dùng ở bảng này**: **chưa xác lập được.** Nguồn dự kiến là Cơ quan Quản lý Ứng xử
> Tài chính Anh (FCA) — cơ quan cấp phép hoạt động cho vay ngang hàng theo điều 36H — nhưng chưa mở
> được (§0.4). Vì `schema.md` §10.2 quy định dòng định nghĩa nguồn **không được bỏ trống**, bảng này
> **chưa có dòng số nào**, chỉ có các ô trạng thái. Khi mở được FCA, phải điền định nghĩa (đếm cái gì,
> nền tảng được cấp phép hay đang hoạt động, dư nợ hay giải ngân) **trước khi** ghi con số đầu tiên.

`khu_vuc` = Anh · `cap` = quốc gia · `doan` = **2**

| ma | nam | chi_tieu | loai_nguoi_vay | mo_hinh | gia_tri | don_vi | nguon | neo | tang | tu_cong_bo | ngay_truy_cap | trang_thai | canh_bao | ghi_chu |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| UK-2021-GIAINGAN-GOP | 2021 | GIAINGAN | gộp | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | `fca.org.uk` HTTP 403. **Không lấp bằng số hãng nghiên cứu thương mại** — §0.4 |
| UK-2022-GIAINGAN-GOP | 2022 | GIAINGAN | gộp | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | như trên |
| UK-2023-GIAINGAN-GOP | 2023 | GIAINGAN | gộp | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | như trên |
| UK-2024-GIAINGAN-GOP | 2024 | GIAINGAN | gộp | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | như trên |
| UK-2025-GIAINGAN-GOP | 2025 | GIAINGAN | gộp | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | **Mốc cuối phạm vi báo cáo** (`target.md` §0.6) — ô này phải có kết quả trước Cổng G2 |
| UK-2022-NENTANG-NA-HOATDONG | 2022 | NENTANG | không áp dụng | gộp | `BI-CHAN` | — | UKD-2 | — | 1 | không | 2026-07-26 | ⬜ | — | Số nền tảng còn được cấp phép sau khi mảng bán lẻ thu hẹp. Là chỉ báo vòng đời tốt nhất theo `schema.md` §5 |

---

## 4. Hai chỗ nguồn tự mâu thuẫn — phát hiện bằng đối chiếu số học

Không nguồn nào trong ba nguồn CCAF mâu thuẫn với nguồn kia. Nhưng **UKD-1 mâu thuẫn với chính nó** ở
hai chỗ, và cả hai chỉ lộ ra khi làm phép tính kiểm tra. Ghi lại vì `target.md` §7.2 buộc trình bày,
và vì chúng là bằng chứng cụ thể cho mức tin cậy của nguồn.

### 4.1. Chứng khoán nợ 2017: £72 triệu hay £79 triệu?

| Vị trí trong UKD-1 | Phát biểu |
|---|---|
| Tóm tắt điều hành, tr. 7 | *"Debt-based Securities stagnated to £79 million, a drop of £5 million compared to 2016"* → 2017 = £79m |
| Thân bài, tr. 12 | *"dropped by 9% to £72 million in 2017 from £79 million in 2016"* → 2017 = £72m, 2016 = £79m |

Hai chỗ **lệch nhau một năm**: tóm tắt gán £79m cho 2017, thân bài gán £79m cho 2016. Biểu đồ cùng
trang 12 đứng về phía thân bài (£72m / £79m). Không ảnh hưởng dòng nào trong bảng §2 — chứng khoán nợ
nằm ngoài phạm vi ba mô hình P2P — nhưng nó **hạ mức tin cậy của phần tóm tắt điều hành**: mọi con số
trong file này đều lấy từ thân bài và biểu đồ, không lấy từ tóm tắt.

### 4.2. Vốn định chế: £411 triệu và £163 triệu bị đảo chỗ

UKD-1 tr. 18 viết: *Equity-based Crowdfunding có mức định chế hoá cao nhất, còn P2P Property Lending
thấp hơn, "representing £411 million and £163 million, respectively"* — tức theo thứ tự: cổ phần
£411m, bất động sản £163m.

Phép nhân nói ngược lại:

| Mô hình | Khối lượng 2017 | Tỷ trọng định chế | Tích |
|---|---|---|---|
| Gọi vốn cổ phần | £333m | 49% | **£163m** |
| P2P bất động sản | £1.218m | 34% | **£414m** ≈ £411m |

Hai con số bị đặt nhầm thứ tự trong câu. **Tỷ lệ phần trăm mới là phần đáng tin** — chúng nhất quán
giữa văn xuôi và biểu đồ, và tự chúng khớp phép nhân. Vì vậy các dòng `VONLE` ở §2 ghi **phần trăm**,
không ghi số tiền; số tiền chỉ nêu ở `ghi_chu` cho hai dòng mà văn xuôi nêu rõ ràng không lẫn (£554m
tiêu dùng, £815m doanh nghiệp — cả hai đều tự khớp phép nhân).

> `schema.md` nguyên tắc 5 cấm suy diễn **trong bảng**. Phép nhân ở đây không đi vào ô nào — nó chỉ
> dùng để **quyết định tin phần nào của nguồn**, và kết quả của việc quyết định đó được ghi ra đây.

---

## 5. Ô trống — đã tìm ở đâu

### 1. Số nền tảng — `BI-CHAN`, không phải `CHUA-TIM`

Nguồn đúng tồn tại và biết đích danh: FCA giữ sổ đăng ký các nền tảng được cấp phép hoạt động cho vay
ngang hàng theo điều 36H (`sources/legal/uk.md`). Rào cản là **kỹ thuật, không phải thiếu nguồn** —
`fca.org.uk` trả HTTP 403 với truy cập tự động, đúng như đã ghi ở `plan.md` T1.3a và `gaps.md` §3.

**Cạm bẫy đã tránh**: G2 Bảng 1.3 (tr. 40) có dòng "UK 60 / 19 / 79" cho 2019 và "53 / 14 / 67" cho
2020, trông rất giống số nền tảng. **Không phải.** Tên bảng là *Domestic vs Foreign Number of
Observations from Respondents* — đó là **số đơn vị trả lời khảo sát**, tức cỡ mẫu, không phải số nền
tảng đang hoạt động trên thị trường. Ghi nó vào ô `NENTANG` sẽ là đúng loại sai lầm mà bài học 1 của
T2.2 cảnh báo (*kiểm nguồn này đo cái gì trước khi thu, không phải sau*).

### 2. Nợ xấu — `CHUA-TIM`, chưa tra

Chưa tra trong ba nguồn CCAF theo từ khoá nợ xấu / quá hạn / theo lứa vay. Ghi trung thực là **chưa
tìm**, không phải "không có" — `schema.md` nguyên tắc 4 phân biệt hai trạng thái này, và ghi nhầm
`KHONG-CO` sẽ đóng sai một hướng tìm còn mở. Việc 4 ở §6.

Ghi chú định hướng: Anh là nước **có khả năng có số theo lứa vay nhất** trong toàn khảo sát, vì đòn
bẩy L6 (`target.md` §2.2) được siết bằng PS19/14 với nghĩa vụ công bố. Nếu Anh cũng không có, đó là
một phát hiện mạnh cho `target.md` §5 (*ưu tiên số theo lứa vay*).

### 3. Lãi suất người vay và lợi suất người cho vay — `CHUA-TIM`

Cả `LAISUAT` lẫn `LOITUC` đều chưa tra. Đây là cặp chỉ tiêu mà T2.2a vừa tách làm hai mã riêng
(`schema.md` §5.1), và Anh là nước được dự đoán sẽ có `LOITUC` vì lợi suất chào mời nhà đầu tư là con
số các nền tảng quảng cáo công khai.

⚠ Khi tìm được, phải kiểm **đo phía nào** trước khi ghi vào ô — đúng bài học 3 của T2.2.

### 4. Tổn thất vụ Lendy — `CHUA-TIM`, và là mắt xích còn thiếu của chương 3

`target.md` §3 Tầng 1 nêu đích danh Lendy là case đổ vỡ của Anh, nhưng **chưa có một con số nào**: cả
giá trị chưa thu hồi lẫn số nhà đầu tư bị ảnh hưởng.

Ô này có giá trị đòn bẩy cao bất thường: nó là **đại lượng đối xứng trực tiếp** với ô còn mở của Trung
Quốc (`cn.md` §5 mục 2 — số nhà đầu tư bị ảnh hưởng). Nếu Anh có số người còn Trung Quốc không, thì
câu hỏi cho Cổng G2 về SQ3 đổi hình: không còn là *"có đo được tổn thất bằng người không"* mà là *"vì
sao nước này đo được còn nước kia thì không"* — một câu hỏi về năng lực thể chế, tức đúng loại câu hỏi
báo cáo này đặt ra.

### 5. Năm 2013 — ngoài tầm ba nguồn hiện có

Đoạn 1 bắt đầu từ 2013 (`schema.md` §4.2) nhưng UKD-1 chỉ lùi tới 2014. Số 2013 nằm ở các báo cáo UK
đời trước của CCAF (báo cáo thứ 2 hoặc thứ 3). Chưa đi tìm. Ảnh hưởng nhỏ: 2013 là năm trước khi có
quy định (FCA nhận quyền quản từ 1/4/2014), nên thiếu nó không làm hỏng trục SQ4.

---

## 6. Việc phát sinh từ lần thu thập này

| # | Việc | Đi đâu |
|---|---|---|
| 1 | ~~Đăng ký `UKD-1` vào `sources.md` §1.1~~ ✅ **Xong 2026-07-26** — mã chính thức **`G3-UK`**, kèm sha256 và kết quả kiểm toàn vẹn. Còn lại: đổi `UKD-1` → `G3-UK` trong bảng §2 của file này ở lần sửa sau, để không lẫn với đợt kiểm vừa chạy | ✅ `sources.md` §1.1 |
| 2 | **Mở `fca.org.uk` thủ công** — đóng 7 ô `BI-CHAN` (1 ở đoạn 1, 6 ở đoạn 2). Đây là việc chặn **toàn bộ đoạn 2 của Anh**, tức chặn một nửa chương 3 | Trước Cổng G2 |
| 3 | Tách phần sụt giảm tiêu dùng 2019→2020 do Zopa ra khỏi phần còn lại. G2 nêu Zopa là nguyên nhân chính nhưng không cho tỷ lệ. Không có số này thì **không viết được kết luận SQ5** từ case Anh | Trước P3 |
| 4 | Tra `NOXAU`, `LAISUAT`, `LOITUC` trong ba nguồn CCAF đã có — chúng đang là `CHUA-TIM` chứ không phải `KHONG-CO`, nên chưa được coi là đã đóng | T2.3 vòng hai |
| 5 | Tìm số tổn thất vụ Lendy (§5 mục 4) — nguồn dự kiến là thông báo của cơ quan quản lý hoặc hồ sơ thanh lý | Trước P3 |
| 6 | Ghi vào `gaps.md`: rào cản FCA nay **có hệ quả định lượng đo được** (7 ô), không còn chỉ là rào cản với văn bản pháp quy như §3 hiện ghi | Cập nhật `gaps.md` |
| 7 | Cân nhắc tìm báo cáo UK đời trước của CCAF cho năm 2013 (§5 mục 5) — ưu tiên thấp | Tuỳ chọn |

---

## 7. Kiểm trước khi đóng file (`schema.md` §12)

| # | Kiểm | Kết quả |
|---|---|---|
| 1 | Đủ 17 cột bắt buộc, không ô trắng | ✅ 14 cột trong bảng theo mẫu §10.1; 3 cột (`khu_vuc`, `cap`, `doan`) là hằng số của cả bảng, khai ngay trên mỗi bảng |
| 2 | `doan` đúng, không bảng nào trộn hai đoạn | ✅ |
| 3 | Bảng đoạn 2 có đủ khối cảnh báo **và** dòng định nghĩa nguồn | ✅ — dòng định nghĩa ghi rõ **chưa xác lập được**, kèm điều kiện phải điền trước khi ghi con số đầu tiên |
| 4 | Mọi dòng `gộp` **có số** mang `C-GOP` (dòng mã trạng thái được miễn — §12.1) | ✅ |
| 5 | Mọi dòng tầng 5 có `tu_cong_bo = có` và `C-TUCONGBO` | ✅ không áp dụng — file này không có dòng tầng 5 nào |
| 6 | Mọi dòng `KHONG-CO` ghi rõ đã tìm ở đâu | ✅ — 1/1 dòng (`UK-2014-GIAINGAN-BDS`) |
| 7 | Mọi dòng `MAU-THUAN` liệt kê đủ giá trị và nguồn | ✅ không áp dụng — không dòng nào `MAU-THUAN`; hai chỗ nguồn tự mâu thuẫn xử lý ở §4 vì không rơi vào ô nào của bảng |
| 8 | Neo trang PDF là số trang in | ✅ — G2 và UKD-1 neo số trang in (độ lệch ổn định −1, đã đo). G1 **không neo trang**, neo theo tên mục + `C-TRANG` (§1.2b) |
| 9 | Không mã ô trùng với file dữ liệu khác | ✅ — `data/` có `cn.md` (tiền tố `CN`, `CNSZ`) và file này (tiền tố `UK`) |
| 10 | Không dòng `◐`/`⬜` bị trích sang `content/` | ✅ — `content/` chưa có nội dung. **39 dòng đạt `✅`** và đủ điều kiện trích; 12 dòng `⬜` (`BI-CHAN`/`CHUA-TIM`) thì không |
| 11 | Dòng `NENTANG`/`TONTHAT` có đoạn biến thể (§7.1) | ✅ — 2 dòng `NENTANG` mang `-HOATDONG`, 2 dòng `TONTHAT` mang `-TIEN`/`-NGUOI` |
| 12 | Dòng `LOITUC` mang `C-LECHPHIA`; ô `LAISUAT` không bị coi là đã lấp | ✅ không áp dụng — dòng `LOITUC` duy nhất đang là `CHUA-TIM`, chưa có số để cảnh báo |

> **Khác biệt lớn nhất so với `cn.md`**: ở đó **không dòng nào** đạt `✅` nên không dòng nào được trích
> sang `content/`. Ở đây **39/51 dòng đạt `✅`**. Chương 3 (Anh) vì vậy có thể viết phần định lượng
> ngay sau Cổng G2, còn chương 6 (Trung Quốc) thì không — dù chương 6 mới là chương dài nhất.

> **Cả 12 kiểm chạy bằng máy**, không đọc mắt: một trình kiểm nhỏ đọc bảng, tách cột và tự tính lại
> kiểm 1/4/5/9/11/12 cùng quy tắc `C-QUYMO` của §4.3, kể cả kiểm trùng mã **chéo sang `cn.md`**. Lần
> chạy đầu bắt được số dòng ghi tay ở §7 và §8 sai (ghi 45, thực tế 51) — đã sửa theo kết quả máy.

---

## 8. Nhật ký

| Ngày | Đã thêm | Nguồn mới mở |
|---|---|---|
| 2026-07-26 | Lập file. **51 dòng**: 45 dòng đoạn 1, 6 dòng đoạn 2. Trong đó **38 ô có giá trị số**, tất cả ở đoạn 1; 1 ô `KHONG-CO`, 5 ô `CHUA-TIM`, 7 ô `BI-CHAN`. Dựng đủ **chuỗi ba mô hình P2P tách theo loại người vay cho 2014-2020** — mức tách tốt nhất của cả khảo sát. Đối chiếu số học sáu tốc độ tăng trưởng khớp nguồn, và bắt được **hai chỗ UKD-1 tự mâu thuẫn** (§4) | `UKD-1` (báo cáo UK thứ 5 của CCAF, mới; sha256 `43858d6f…`, preflight PASS, 56 trang). `UKD-2` (FCA) **HTTP 403, chưa mở được** |
