# Kiểm nguồn CCAF — mức tách hai thị trường (rủi ro R4)

> **Hiện vật của T2.0** (`plan.md` §3). Việc bắt buộc làm trước khi điền bất kỳ ô dữ liệu nào — `gaps.md` §12, §14.2.
> **Ngày kiểm**: 2026-07-26. **Đối tượng**: G1 và G2 (`sources.md` §1.1), mở bản gốc toàn văn.
>
> Câu hỏi kiểm: *`target.md` §2.4 bắt mọi chỉ số phải tách cho vay tiêu dùng / doanh nghiệp nhỏ / bất động sản. Nguồn xương sống định lượng có tách được như vậy không, và có nhất quán qua mọi khu vực không?*

---

## 0. Kết luận

**Tách được — nhưng không ở mức mà `target.md` §5 giả định, và mức tách suy giảm đúng theo chiều thời gian mà báo cáo cần nhất.**

| Cấp | Có tách theo mô hình không | Phạm vi năm |
|---|---|---|
| Toàn cầu / theo khu vực | ✅ **Có, đầy đủ** — bảng mô hình × năm | 2013-2020 |
| Một nước cụ thể, chuỗi theo năm | ❌ **Không.** Phụ lục chỉ có **tổng gộp mọi mô hình** | 2018, 2019, 2020 |
| Một nước cụ thể, ảnh chụp cơ cấu | ◐ **Có, nhưng chỉ một năm 2018** — 35 nước, dạng văn xuôi, chỉ 1-3 mô hình dẫn đầu | Chỉ 2018 |
| Một nước cụ thể, 2019-2020 | ◐ **Chỉ nếu nước đó lọt top 3-4 của mô hình đó** | 2019, 2020 |

**Rủi ro R4 hiện hình, ở dạng hẹp hơn dự kiến.** Không phải "nguồn không tách được" — mà là **tách ở cấp khu vực thì đầy đủ, xuống cấp quốc gia thì đứt**. Chương 8 vẫn viết được, nhưng phải đổi nền: neo vào bảng mô hình **cấp khu vực**, không neo vào chuỗi số **cấp quốc gia**.

**Một cái bẫy phải chặn ngay**: con số tổng của một nước trong Phụ lục 1 của G2 là **tổng mọi mô hình tài chính thay thế**, gồm cả gọi vốn cổ phần và quyên góp — những thứ `target.md` §8 loại trừ. Đây **không phải** số P2P của nước đó và tuyệt đối không được dùng như vậy.

---

## 1. Cách kiểm

| Bước | Chi tiết |
|---|---|
| Tải bản gốc | Từ đúng đường dẫn ghi ở `sources.md` §1.1, ngày 2026-07-26 |
| Kiểm toàn vẹn tệp | Chạy `scripts/pdf_read_preflight.py` — **cả hai PASS**, ba tín hiệu đếm trang khớp nhau, không bị cắt cụt |
| Đọc | Trích toàn văn theo trang, đọc phần phương pháp, các bảng mô hình, phụ lục và toàn bộ 35 phiếu hồ sơ quốc gia |

| Tệp | Số trang | sha256 |
|---|---|---|
| G1 | 228 | `49cec1803d836b7b9dbfa8e0678a90250372c7bbfef2457d61e93b9a04565de1` |
| G2 | 197 | `dd2860b15696c3ebe7e1dbca8c375465dc0cbfc172dabd1383b564f5763c37a3` |

**Cảnh báo về neo trang — áp dụng cho mọi trích dẫn G1 sau này.** Ở **G2**, số trang in trùng số thứ tự trang PDF (đã kiểm 6 điểm). Ở **G1 thì không**: độ lệch trôi dần từ **+1** (đầu tài liệu) tới **+13** (cuối tài liệu). Quy đổi bằng phép cộng là sai. Mọi số trang G1 trong hồ sơ này lấy **số in trên chính trang đó**, hoặc suy từ trang lân cận rồi **đối chiếu lại với mục lục** — cách này đã kiểm được cho khối phiếu hồ sơ quốc gia (mục lục ghi Hàn Quốc tr. 211, Latvia tr. 216, Ấn Độ tr. 204; cả ba khớp với suy luận từ trang lân cận).

**Riêng phần cuối G1 thì không neo trang được.** Ở khối endnote + phụ lục, thứ tự văn bản trích ra bị trộn: các dòng của bảng phụ lục hiện ra lẫn vào những trang mang tiêu đề chạy và số in của phần endnote (233-239). Không xác định được dòng nào thuộc trang in nào. **Quy tắc: mọi trích dẫn từ phụ lục G1 ghi theo tên bảng, không ghi số trang.**

Preflight PASS chỉ chứng minh tệp không bị cắt cụt — **nó không chứng minh số trang in khớp số trang PDF**. Hai phát hiện trên là ví dụ trực tiếp: tệp toàn vẹn, nhưng neo trang vẫn có thể sai.

---

## 2. Mức tách theo từng cấp

### 2.1. Cấp khu vực — đầy đủ

Đây là nơi tách tốt nhất, và là nơi chương 8 phải neo vào.

| Bảng | Nội dung | Nguồn |
|---|---|---|
| Bảng 2.1 | Châu Âu (trừ Anh) — **mọi mô hình × 2015-2020**, sáu năm liền | G2 tr. 74 |
| Bảng 2.2 | Anh — mọi mô hình × 2019-2020 | G2 tr. 75 |
| Bảng 3.1 | Châu Á-TBD (trừ Trung Quốc) — mọi mô hình × 2018-2020, kèm tốc độ tăng | G2 tr. 100 |

Ba dòng cho vay ngang hàng luôn tách rời nhau trong các bảng này: **tiêu dùng / doanh nghiệp / bất động sản**. Ví dụ Bảng 2.1: cho vay tiêu dùng ngang hàng 2.901 triệu USD (2020) tách khỏi cho vay doanh nghiệp ngang hàng 1.844 triệu và cho vay bất động sản ngang hàng 500 triệu.

### 2.2. Cấp quốc gia, chuỗi theo năm — **không có tách**

| Phụ lục | Nội dung | Nguồn |
|---|---|---|
| Phụ lục 1 | Tổng khối lượng mỗi nước, 2019 và 2020 — **gộp mọi mô hình** | G2 tr. 191-192 |
| Phụ lục 2 | Số nền tảng mỗi nước, tách trong nước / nước ngoài, 2019 và 2020 | G2 tr. 193-196 |
| Phụ lục (G1) | Tổng khối lượng mỗi nước 2018 — gộp mọi mô hình; và số nền tảng 2018 | G1, phụ lục — *không neo trang được*, xem §1 |

Không nước nào có chuỗi *mô hình × năm*. Đây chính là ô trống làm R4 hiện hình.

### 2.3. Cấp quốc gia, ảnh chụp một năm — có, chỉ 2018

**Chương 8 của G1 — "Phiếu hồ sơ quốc gia"** (tr. 198-232 bản in): 35 nước, mỗi nước một trang.

Đã đọc **toàn bộ 35 phiếu**. Kết quả: **cả 35 phiếu đều nêu cơ cấu theo mô hình** — nhưng ở dạng **văn xuôi**, chỉ **1-3 mô hình dẫn đầu**, kèm tỷ trọng % và giá trị USD, và **chỉ cho năm 2018**. Chuỗi số 2015-2018 in kèm là **tổng gộp**, không tách.

Vài ví dụ đọc được nguyên văn:

| Nước | Cơ cấu 2018 như phiếu ghi | Trang in |
|---|---|---|
| Latvia | Cho vay tiêu dùng ngang hàng **90,5%** (230,3 triệu USD) | G1 tr. 216 |
| Ba Lan | Cho vay tiêu dùng ngang hàng **84,4%** (281,4 triệu USD) | G1 tr. 218 |
| Anh | Doanh nghiệp **24,5%** (2,5 tỷ) · bất động sản **19,8%** (2,1 tỷ) · tiêu dùng **17%** (1,8 tỷ) | G1 tr. 221 |
| Hàn Quốc | Bất động sản ngang hàng **54,1%** (407,2 triệu) · tiêu dùng ngang hàng **15,1%** (114 triệu) | G1 tr. 211 |
| Ấn Độ | Cho vay doanh nghiệp trên bảng cân đối **48,5%** (265,5 triệu) · tiêu dùng ngang hàng **38%** (207,8 triệu) | G1 tr. 204 |

**Giới hạn phải mang theo**: đây là *tỷ trọng của 1-3 mô hình dẫn đầu*, không phải bảng phân rã đầy đủ. Phần dư không được liệt kê. Không thể cộng ngược ra giá trị của một mô hình không lọt top.

**Việt Nam không nằm trong 35 nước có phiếu hồ sơ.**

### 2.4. Cấp quốc gia, 2019-2020 — chỉ xếp hạng đầu bảng

| Hình | Nội dung | Nguồn |
|---|---|---|
| Hình 2.7 | **Top bốn** nước châu Âu theo từng mô hình nợ, 2019-2020 | G2 tr. 76 |
| Hình 3.2 | **Top ba** nước châu Á-TBD theo từng mô hình nợ, 2019-2020 | G2 tr. 102 |

Ngay cả độ sâu xếp hạng cũng **không nhất quán giữa hai khu vực** — châu Âu lấy bốn, châu Á lấy ba. Một nước không lọt top thì không có số theo mô hình cho hai năm đó, dù vẫn có số tổng ở Phụ lục 1.

---

## 3. Nguyên nhân gốc — quy tắc ngưỡng quan sát

Phần phương pháp của G2 (tr. 34) giải thích vì sao ô *quốc gia × mô hình* bị bịt:

> Trong phần lớn trường hợp, dữ liệu chỉ được báo cáo khi có **tối thiểu 10 quan sát theo từng nước và từng mô hình**. Ở các trường hợp khác, nhóm nghiên cứu **cân nhắc riêng** tuỳ theo nước và mô hình cụ thể, khi ngưỡng đó ít phù hợp (ví dụ với các nước tương đối nhỏ).

Hai hệ quả:

1. **Không phải nguồn không thu được số.** G2 tr. 33 ghi rõ nền tảng khai báo *theo mô hình và theo từng nước*. Dữ liệu thô **có** chiều quốc gia × mô hình; bản công bố **không** phơi ra, trừ các thị trường đủ lớn.
2. **Ngoại lệ mang tính tuỳ nghi.** Câu "cân nhắc riêng" nghĩa là chính quy tắc bịt ô cũng không áp dụng đồng đều. Không suy ra được một nước vắng mặt là do thiếu quan sát hay do quyết định biên tập.

**Hệ quả thao tác**: không có cách nào lấp ô trống này bằng cách đọc kỹ hơn. Muốn có chuỗi *quốc gia × mô hình × năm* thì phải lấy từ **cơ quan quản lý từng nước** — tức rơi vào đoạn 2 của D10, nơi **cấm so sánh chéo** (`target.md` §5.1).

---

## 4. Ánh xạ từ vựng CCAF sang quy tắc `target.md` §2.4

Bộ mô hình của CCAF không trùng khít với trục phân loại của báo cáo. Bảng ánh xạ dưới đây là bắt buộc khi rút số.

| `target.md` §2.4 | Dòng CCAF dùng được | Cảnh báo |
|---|---|---|
| Cho vay tiêu dùng | *P2P/Marketplace Consumer Lending* | ✅ Khớp trực tiếp |
| Cho vay doanh nghiệp nhỏ | *P2P/Marketplace Business Lending* | ⚠ CCAF không tách theo **quy mô** doanh nghiệp. Đây là "cho vay doanh nghiệp", không phải "doanh nghiệp nhỏ" |
| Bất động sản / dự án | *P2P/Marketplace Property Lending* | ✅ Khớp; giữ tách riêng đúng như §2.4 yêu cầu |
| — | *Balance Sheet …Lending* | ❌ **Không phải ngang hàng.** Nền tảng tự giữ rủi ro trên bảng cân đối. Thuộc trục 2 Khung A, phải để riêng |
| — | *Invoice Trading*, *Real Estate Crowdfunding*, *Equity/Donation/Reward* | ❌ Ngoài phạm vi `target.md` §8 |

**Tên gọi đổi giữa hai bản**: G1 dùng *P2P Consumer Lending*, G2 đổi thành *P2P/Marketplace Consumer Lending*. Cùng một dòng. Khi ghép số 2018 (G1) với 2019-2020 (G2) phải biết điều này, nếu không sẽ tưởng là hai chỉ tiêu khác nhau.

**Điểm cần cẩn trọng nhất**: gộp nhầm *Balance Sheet Consumer Lending* vào cho vay tiêu dùng ngang hàng. Ở nhiều nước dòng này còn lớn hơn dòng ngang hàng — Indonesia 2018: 57% trên bảng cân đối. Gộp nhầm sẽ thổi phồng quy mô "P2P" đúng ở những nước mà `target.md` quan tâm nhất.

---

## 5. Hệ quả cho quy tắc §2.4 và cho các chương

| Nơi chịu ảnh hưởng | Làm được gì | Không làm được gì |
|---|---|---|
| **Chương 8** (hai thị trường) | So sánh cơ cấu **theo khu vực**, 2015-2020; và ảnh chụp cơ cấu **35 nước năm 2018** | Không dựng được chuỗi tiêu dùng-vs-doanh nghiệp **theo năm cho một nước** từ nguồn xuyên quốc gia |
| **Chương 10** (tổng hợp so sánh) | Neo vào bảng khu vực — vẫn đủ đỡ luận điểm "doanh nghiệp là mảng còn sống ở châu Âu" | Không xếp hạng các nước theo từng loại cho vay ngoài top 3-4 |
| **Các chương quốc gia** | Nêu cơ cấu năm 2018 cho mọi nước có phiếu hồ sơ; nêu tổng khối lượng theo năm | Với nước **không** có phiếu — **gồm Việt Nam, Estonia, Trung Quốc** — không có cơ cấu nào từ nguồn này |
| **`target.md` §5 nguyên tắc 2** | Giữ nguyên tinh thần | Câu *"mỗi chỉ số tách theo ba loại"* **không thực hiện được ở cấp quốc gia**. Phải hạ xuống: tách ở cấp khu vực, còn cấp quốc gia thì ghi rõ là số gộp |

Dòng cuối là một **lệch giữa `target.md` và thực tế nguồn**. Theo `plan.md` §8 quy tắc 6, không tự sửa `target.md` — mang tới **Cổng G2**, đã ghi vào `gaps.md` §14.3.

---

## 6. Ba câu hỏi "sau khi siết" — CCAF đóng góp được tới đâu

Kiểm luôn trong lần mở này (`gaps.md` §11, §14.2).

| Câu hỏi | CCAF trả lời được không | Ghi chú |
|---|---|---|
| **Hàn Quốc** sau luật 8/2020 | ❌ Gần như không | G2 dừng ở dữ liệu 2020; luật hiệu lực **tháng 8/2020** nên chỉ phủ ~4 tháng sau mốc. Phải lấy từ cơ quan quản lý Hàn Quốc |
| **Ấn Độ** sau đợt siết 8/2024 | ❌ Không | Ngoài hẳn phạm vi năm của cả hai bản. Phải lấy từ ngân hàng trung ương Ấn Độ |
| **Singapore** — "nhỏ bao nhiêu" | ◐ **Một phần — và đây là số đầu tiên tìm được** | Xem §7 |

G2 tr. 115 có ghi nhận **định tính** đáng lưu cho SQ5: về luật Hàn Quốc, báo cáo dẫn lo ngại của giới hành nghề rằng luật mới *có thể dựng rào cản gia nhập và đẩy các đơn vị đang hoạt động ra khỏi thị trường*. Đây là **giả thuyết được ghi nhận, không phải kết quả đo được** — dùng làm giả thuyết cần kiểm ở P2, không dùng làm bằng chứng.

---

## 7. Phát hiện phụ — ba ô mà sổ khoảng trống đang ghi là "bằng không"

Ba phát hiện dưới đây **không phải mục tiêu của lần kiểm này**, nhưng làm sai lệch hiện trạng ghi ở `gaps.md` nên phải ghi lại ngay.

### 7.1. Việt Nam — có chuỗi ba năm, không phải "một con số duy nhất"

`gaps.md` §2 ghi số liệu thị trường Việt Nam là *"một con số duy nhất: khoảng 40 công ty (2019), từ tường thuật báo chí"*. **Không còn đúng.**

| Chỉ tiêu | 2018 | 2019 | 2020 | Nguồn |
|---|---|---|---|---|
| Tổng khối lượng tài chính thay thế | 17.463.460 USD | 46.158.438 USD | 110.419.316 USD | G1 phụ lục khối lượng · G2 tr. 191 |
| Số nền tảng hoạt động tại VN | 14 | 15 | 13 | G1 phụ lục số nền tảng · G2 tr. 193 |
| — trong đó thành lập trong nước | 5 | 4 | 3 | như trên |
| — trong đó đặt trụ sở nước ngoài | 9 | 11 | 10 | như trên |

**Bốn giới hạn phải đi kèm, không được tách rời khỏi các con số này:**

1. **Là tổng gộp mọi mô hình**, không phải số P2P. Việt Nam không có phiếu hồ sơ nên **không biết cơ cấu theo mô hình**.
2. **Là số khảo sát tự nguyện**, không phải số giám sát.
3. **Đếm cả nền tảng nước ngoài** hoạt động tại Việt Nam — nên "13 nền tảng" không phải "13 công ty Việt Nam". Số trong nước là 3-5.
4. **Vênh với con số báo chí**: 14-15 nền tảng (CCAF) so với "khoảng 40 công ty" (báo chí 2019). Hai cách đếm khác nhau, **không được chọn một con số** — theo `target.md` §7.2 phải trình bày cả hai kèm nguồn và cách đếm.

Dù vậy, đây là **chuỗi ba năm từ nguồn tầng 3 có phương pháp công bố** — hơn hẳn hiện trạng ghi trong sổ khoảng trống. Không đảo được quyết định **D8** (chương 11 theo hướng phân tích thể chế) vì bốn giới hạn trên vẫn quá nặng, nhưng đủ để chương 11 nói được điều gì đó có nguồn thay vì hoàn toàn im lặng về quy mô.

### 7.2. Singapore — ô "dữ liệu kết quả bằng không" không còn đúng hẳn

`gaps.md` §8.2 ghi *"không một con số nào về quy mô ngành, số nền tảng"*.

| Chỉ tiêu | 2014 | 2015 | 2016 | 2017 | 2018 | 2019 | 2020 |
|---|---|---|---|---|---|---|---|
| Tổng khối lượng (triệu USD) | 22 | 40 | 164 | 191 | 500 | 497 | 963 |
| Số nền tảng | | | | | | 24 (12 trong nước) | 22 (11 trong nước) |

Nguồn: chuỗi 2014-2018 từ phiếu hồ sơ G1 tr. 210; 2019-2020 từ G2 tr. 191 và tr. 193. Số 2018 ở phụ lục G1 ghi chi tiết hơn — 499.653.248 USD.

Cơ cấu năm 2018 (G1 tr. 210): bất động sản ngang hàng **22,4%** · doanh nghiệp ngang hàng **21,2%** · quyên góp có phần thưởng **20,6%**. Đáng chú ý: **cho vay tiêu dùng ngang hàng không lọt top ba** — phù hợp với cơ chế đã mô tả ở **D12** (Singapore định giá việc nhận vốn nhà đầu tư lẻ), nhưng là *dấu hiệu*, chưa đủ làm bằng chứng.

Quy mô **tăng gấp gần 44 lần** giữa 2014 và 2020, gần gấp đôi riêng trong 2020 — ngược chiều với mô tả cũ *"ngành nhỏ và ổn"* đã bị **D12** loại bỏ. Vẫn **chưa** trả lời được câu hỏi ở §6 (mốc can thiệp nằm ở đâu, "ổn" nghĩa là gì), nên mục 8 giữ mức 🟡.

### 7.3. Hàn Quốc — có chuỗi tổng bắc qua đúng mốc luật

| 2015 | 2016 | 2017 | 2018 | 2019 | 2020 |
|---|---|---|---|---|---|
| 41 tr. | 376 tr. | 1.130 tr. | 753 tr. | 1.604 tr. | 1.304 tr. USD |

Nguồn: G1 tr. 211 (2015-2018) · G2 tr. 191 (2019-2020).

**Không được đọc thẳng chuỗi này thành "hiệu lực của luật".** Ba lý do: (a) luật hiệu lực 8/2020 nên 2020 chỉ chứa ~4 tháng; (b) chính G1 tr. 211 ghi mức giảm 2018 *một phần do một số nền tảng lớn không tham gia khảo sát năm đó* — tức chuỗi này lẫn biến động mẫu với biến động thị trường; (c) là số gộp mọi mô hình.

**Cả ba phát hiện ở §7 là số liệu, không phải nguồn.** Chúng phải được chuyển vào `data/vn.md` và `data/asia.md` ở T2.6/T2.7 kèm nguyên vẹn phần giới hạn, chứ không được trích thẳng từ file này vào `content/`.

---

## 8. Cảnh báo phương pháp bổ sung — phát hiện trong lần đọc này

`sources.md` §1.1 đã ghi ba cảnh báo. Lần mở bản gốc này thêm bốn cảnh báo nữa, đều lấy từ phần phương pháp G2 tr. 32-34.

| # | Cảnh báo | Vì sao quan trọng với báo cáo này |
|---|---|---|
| 4 | **Mẫu co mạnh và không đều**: 1.227 đơn vị trả lời (2018) → 821 (2019) → 703 (2020) | Biến động số liệu giữa các năm **lẫn** biến động mẫu với biến động thị trường. Mọi phát biểu "thị trường giảm X%" phải kiểm xem có phải hiệu ứng mẫu không |
| 5 | **Riêng Trung Quốc mất 320 đơn vị** khỏi mẫu 2018, do chính các lệnh siết buộc đóng cửa | Đúng biến số mà chương 6 muốn đo lại là nguyên nhân làm mẫu biến mất. Chuỗi số Trung Quốc của CCAF **không đo được quá trình xoá sổ** — phải lấy nguồn khác |
| 6 | **Quy đổi USD theo tỷ giá bình quân năm**; G2 tự ghi nhận 2020 tỷ giá biến động mạnh ở châu Á, Nam Mỹ, châu Phi | Một phần mức "giảm" 2020 của các thị trường mới nổi là hiệu ứng tỷ giá. Không diễn giải thành co hẹp thị trường mà không kiểm |
| 7 | **Số bình quân có trọng số và đã loại giá trị ngoại lai** | Các chỉ tiêu bình quân (quy mô khoản vay, lãi suất) không phải bình quân thô. Không so trực tiếp với số bình quân của cơ quan quản lý |

Cảnh báo 4 và 5 làm **nặng thêm** cảnh báo thiên lệch sống sót đã ghi ở `sources.md` §1.1 mục 1: không chỉ nền tảng đã sụp thôi trả lời khảo sát, mà **quy mô rút lui khỏi mẫu lớn tới mức tự nó là một biến**.

---

## 9. Việc còn lại sinh ra từ lần kiểm này

| # | Việc | Đi đâu |
|---|---|---|
| 1 | Chuyển ba nhóm số ở §7 vào `data/vn.md`, `data/asia.md` kèm nguyên phần giới hạn | T2.6, T2.7 |
| 2 | Rút bảng mô hình cấp khu vực (Bảng 2.1, 2.2, 3.1) vào các file dữ liệu tương ứng | T2.3, T2.5, T2.6 |
| 3 | Rút cơ cấu 2018 từ 35 phiếu hồ sơ cho các nước thuộc phạm vi báo cáo | T2.2-T2.7 |
| 4 | Quyết định hạ yêu cầu tách của `target.md` §5 nguyên tắc 2 xuống cấp khu vực | **Cổng G2** — `gaps.md` §14.3 |
| 5 | Chuỗi *quốc gia × mô hình × năm* phải lấy từ cơ quan quản lý từng nước, và khi đó rơi vào đoạn 2 của **D10** — cấm so sánh chéo | Ràng buộc thường trực của P2 |

---

## 10. Nhật ký cập nhật

| Ngày | Thay đổi |
|---|---|
| 2026-07-26 | Lập file. Mở bản gốc G1 + G2, kiểm toàn vẹn PASS, đọc toàn bộ 35 phiếu hồ sơ quốc gia. Kết luận R4; phát hiện phụ về Việt Nam, Singapore, Hàn Quốc; bốn cảnh báo phương pháp mới |
