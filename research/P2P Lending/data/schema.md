# Lược đồ bảng dữ liệu chuẩn

> **Hiện vật của T2.1** (`plan.md` §3). Định nghĩa cấu trúc mọi file `data/*.md` của giai đoạn P2.
> **Ngày lập**: 2026-07-26.
>
> File này định nghĩa **cách ghi**, không chứa dữ liệu. Dữ liệu nằm ở `data/{cn,uk,us,baltic,asia,vn}.md`.
> Kết quả kiểm nguồn dẫn tới thiết kế này: `data/source-audit-ccaf.md`.

---

## 1. Năm nguyên tắc chi phối thiết kế

| # | Nguyên tắc | Bắt nguồn từ |
|---|---|---|
| 1 | **Hai đoạn dữ liệu tách bạch.** Đoạn 1 (2013-2020) so sánh chéo được; đoạn 2 (2021-2025) chỉ mô tả theo từng nước | **D10** · `target.md` §5.1 |
| 2 | **Loại người vay là chiều bắt buộc**, không phải chiều tuỳ chọn. Không có ô nào được để trống chiều này — nếu nguồn không tách thì ghi giá trị `gộp` | **D7** · `target.md` §2.4, §5 nguyên tắc 2 |
| 3 | **Truy nguyên từng ô.** Mỗi con số mang nguồn, neo trong nguồn, ngày truy cập, tầng nguồn. Số do nền tảng tự công bố đánh dấu riêng | `target.md` §5 nguyên tắc 1, §7.1 |
| 4 | **Ô trống là dữ liệu.** "Đã tìm, không có" khác hẳn "chưa tìm". Hai trạng thái này phải phân biệt được, vì chương 11 dựa vào đúng sự phân biệt đó | `target.md` §6 (tuyên bố giới hạn dữ liệu) |
| 5 | **Không suy diễn trong bảng.** Bảng chỉ chứa số đọc được từ nguồn. Mọi phép tính, quy đổi, nội suy đi vào cột ghi chú hoặc ra ngoài bảng, có nhãn rõ | `target.md` §7.4 mục 2 |

**Nguyên tắc 4 nói rõ hơn**: một ô ghi `KHÔNG-CÓ` là một phát hiện nghiên cứu, ngang giá trị với một ô có số. Toàn bộ chương 11 và mục §5 của `data/coverage.md` được xây từ các ô này.

---

## 2. Đơn vị ghi: một dòng = một quan sát

Bảng ghi ở **dạng dài** (mỗi dòng một quan sát), không phải dạng rộng (mỗi dòng một năm, mỗi cột một chỉ tiêu).

**Vì sao**: kiểm nguồn ở `source-audit-ccaf.md` cho thấy mức tách **không đồng đều** — có nước có cơ cấu theo mô hình, có nước không; có năm có, có năm không. Ở dạng rộng, những chỗ khuyết đó thành ô trắng vô nghĩa, không phân biệt được "không tách được" với "chưa đi tìm". Ở dạng dài, mỗi ô khuyết là một dòng có trạng thái riêng.

---

## 3. Định nghĩa cột

Cột đánh dấu **B** là bắt buộc, **T** là tuỳ chọn.

| # | Cột | B/T | Nội dung |
|---|---|---|---|
| 1 | `ma` | B | Mã ô, đặt theo §7 |
| 2 | `khu_vuc` | B | Tên nước hoặc khu vực. Dùng đúng tên đã dùng ở `sources/legal/` |
| 3 | `cap` | B | `quốc gia` · `khu vực` · `toàn cầu` — xem §4.1 |
| 4 | `nam` | B | Năm dữ liệu, không phải năm xuất bản |
| 5 | `doan` | B | `1` · `2` · `ngoài` — xem §4.2. **Cột này quyết định số được phép dùng thế nào** |
| 6 | `chi_tieu` | B | Một trong sáu chỉ tiêu ở §5 |
| 7 | `loai_nguoi_vay` | B | `tiêu dùng` · `doanh nghiệp nhỏ` · `bất động sản` · `gộp` · `không áp dụng` — §4.3 |
| 8 | `mo_hinh` | B | `ngang hàng` · `bảng cân đối` · `gộp` · `không áp dụng` — §4.4 |
| 9 | `gia_tri` | B | Con số, hoặc một trong các mã trạng thái ở §6 |
| 10 | `don_vi` | B | `triệu USD` · `tỷ USD` · `nền tảng` · `%` · `người` … |
| 11 | `gia_tri_goc` | T | Giá trị theo nguyên tệ, nếu nguồn công bố bằng nội tệ |
| 12 | `nguyen_te` | T | Mã tiền tệ của cột 11 |
| 13 | `nguon` | B | Mã nguồn (`G1`, `G2`, `CN-3`…) hoặc trích dẫn đầy đủ nếu chưa có mã |
| 14 | `neo` | B | Vị trí trong nguồn: số trang in, tên bảng, hoặc tên mục. Xem §8 |
| 15 | `tang` | B | Tầng nguồn 1-5 theo `target.md` §7.1 |
| 16 | `tu_cong_bo` | B | `có` nếu số do nền tảng tự công bố, `không` nếu không |
| 17 | `ngay_truy_cap` | B | Ngày mở nguồn |
| 18 | `trang_thai` | B | `✅` đã mở bản gốc · `◐` nhiều nguồn khớp, chưa mở gốc · `⬜` mới biết là có |
| 19 | `canh_bao` | B | Mã cảnh báo phương pháp, xem §9. Nhiều mã ngăn bằng dấu phẩy |
| 20 | `ghi_chu` | T | Mọi thứ còn lại. Nơi duy nhất được phép ghi suy luận, và phải ghi rõ là suy luận |

**Không được để trống cột bắt buộc.** Nếu chưa biết thì ghi mã trạng thái ở §6, không để trắng — ô trắng không phân biệt được với sơ suất.

---

## 4. Từ điển giá trị

### 4.1. `cap`

| Giá trị | Nghĩa | Ghi chú |
|---|---|---|
| `quốc gia` | Một khu vực pháp lý | |
| `khu vực` | Nhóm nhiều nước theo cách gộp của chính nguồn | **Phải ghi rõ nguồn gộp thế nào** ở `ghi_chu` — "châu Âu" của CCAF trừ Anh ra |
| `toàn cầu` | Tổng thế giới | Thường trừ Trung Quốc — kiểm kỹ, các nguồn hay im lặng về chỗ này |

Cấp `khu vực` là **cấp chủ lực** của báo cáo cho các số có tách theo loại người vay, theo kết luận của `source-audit-ccaf.md` §0.

### 4.2. `doan` — cột quan trọng nhất của lược đồ

| Giá trị | Năm | Được phép dùng thế nào |
|---|---|---|
| `1` | 2013-2020 | **So sánh chéo giữa các nước.** Bảng đa quốc gia, xếp hạng tương đối, tính tỷ trọng |
| `2` | 2021-2025 | **Chỉ mô tả nội bộ một nước theo thời gian.** Cấm đặt cạnh số nước khác, cấm cộng tổng khu vực, cấm nói "nước A lớn hơn nước B" |
| `ngoài` | ≤2012 hoặc ≥2026 | Chỉ dùng làm bối cảnh. Dữ kiện từ 2026 trở đi phải mang nhãn **"sau mốc phạm vi"** ở `ghi_chu` |

Nguồn của quy tắc: **D10** · `target.md` §5.1. Đây là lý do cột này bắt buộc ở mọi dòng.

**Một dòng đoạn 1 và một dòng đoạn 2 không bao giờ được đứng chung trong một bảng của `content/`** — kể cả khi cùng nước, cùng chỉ tiêu. Nếu cần trình bày liên tục theo thời gian, phải cắt bảng và đặt câu cảnh báo ở §10 vào giữa.

### 4.3. `loai_nguoi_vay`

| Giá trị | Nghĩa |
|---|---|
| `tiêu dùng` | Người vay là cá nhân, mục đích tiêu dùng |
| `doanh nghiệp nhỏ` | Người vay là hộ kinh doanh hoặc doanh nghiệp |
| `bất động sản` | Cho vay dự án / bất động sản — **tiểu loại có tên riêng**, không gộp vào doanh nghiệp nhỏ (`target.md` §2.4 gạch cuối) |
| `gộp` | Nguồn không tách. **Số gộp không bao giờ được dùng để phát biểu về một loại riêng lẻ** |
| `không áp dụng` | Chỉ tiêu không có chiều người vay (ví dụ: số nền tảng toàn thị trường) |

**Cảnh báo ánh xạ**: dòng *P2P/Marketplace Business Lending* của CCAF là "cho vay doanh nghiệp", **không tách theo quy mô doanh nghiệp**. Khi ghi vào giá trị `doanh nghiệp nhỏ`, bắt buộc kèm mã cảnh báo `C-QUYMO` (§9).

### 4.4. `mo_hinh`

| Giá trị | Nghĩa |
|---|---|
| `ngang hàng` | Nhà đầu tư chịu rủi ro tín dụng; nền tảng là trung gian |
| `bảng cân đối` | Nền tảng tự giữ khoản vay trên bảng cân đối của mình |
| `gộp` | Nguồn không tách hai loại trên |
| `không áp dụng` | |

**Vì sao phải có cột này**: trục 2 của Khung A (`target.md` §2.1). Và vì một lỗi cụ thể đã thấy trong nguồn — ở nhiều nước dòng *Balance Sheet Consumer Lending* còn lớn hơn dòng ngang hàng (Indonesia 2018: 57%). Gộp nhầm hai dòng sẽ thổi phồng quy mô "P2P" đúng ở các nước báo cáo quan tâm nhất.

---

## 5. Bảy mã chỉ tiêu và định nghĩa chặt

Lấy từ sáu dòng của `target.md` §5 — tách thành bảy mã vì *dư nợ* và *doanh số giải ngân* phải là hai mã riêng, đúng như chính §5 cảnh báo. Định nghĩa dưới đây là bắt buộc — nguồn nào định nghĩa khác thì ghi vào `ghi_chu`, **không sửa số cho khớp**.

| Mã | Chỉ tiêu | Định nghĩa dùng trong báo cáo | Bẫy phải tránh |
|---|---|---|---|
| `NENTANG` | Số nền tảng | Số nền tảng **đang hoạt động** trong năm đó | Phải tách rõ *đang hoạt động* / *đã đăng ký* / *đã rút lui* — ba con số rất khác nhau. Ghi loại nào vào `ghi_chu`. Cũng phải ghi rõ có đếm nền tảng nước ngoài hay không |
| `GIAINGAN` | Doanh số giải ngân | **Tổng khối lượng cho vay phát sinh trong năm** | Không phải dư nợ. Đây là cặp khái niệm bị nhầm hoặc cố tình gộp nhiều nhất (`target.md` §5) |
| `DUNO` | Dư nợ | **Số dư còn lại tại một thời điểm** — thường cuối năm | Ghi rõ mốc thời điểm vào `ghi_chu` |
| `NOXAU` | Tỷ lệ nợ xấu / thu hồi | **Ưu tiên số theo lứa vay (cohort)** | Tỷ lệ trên tổng dư nợ đang tăng **che giấu rủi ro** trong giai đoạn tăng trưởng. Nếu buộc phải dùng, gắn mã `C-COHORT` |
| `VONLE` | Tỷ trọng vốn từ nhà đầu tư lẻ vs định chế | Tỷ trọng, đơn vị `%` | Chỉ báo trực tiếp của **SQ3**. Ghi rõ mẫu số là gì |
| `TONTHAT` | Số nhà đầu tư bị ảnh hưởng · giá trị chưa thu hồi | Hai đại lượng **tách rời**, mỗi cái một dòng | Đại lượng đo tổn thất xã hội. Với Trung Quốc hiện đang trống — `gaps.md` §10 |
| `LAISUAT` | Lãi suất bình quân người vay phải trả | **Đã gồm phí** | Để trả lời "có thay thế được tín dụng đen không". Lãi suất công bố không tính phí thì gắn `C-PHI` và ghi rõ |

Chỉ tiêu nằm ngoài bảy dòng trên: được thêm, nhưng phải thêm vào bảng này trước, không tự đặt mã trong file dữ liệu.

---

## 6. Mã trạng thái cho ô không có số

Điền vào cột `gia_tri`. Đây là cách nguyên tắc 4 được thực thi.

| Mã | Nghĩa | Bắt buộc kèm |
|---|---|---|
| `CHUA-TIM` | Chưa đi tìm | — |
| `KHONG-CO` | **Đã tìm, nguồn không công bố** | `ghi_chu` phải ghi **đã tìm ở đâu** — nếu không, mã này vô giá trị |
| `KHONG-TACH` | Nguồn có số nhưng không tách theo chiều đang cần | Dòng `gộp` tương ứng, nếu có |
| `BI-CHAN` | Nguồn tồn tại nhưng chặn truy cập tự động | Đường dẫn, để mở thủ công sau — nối với `gaps.md` §3 |
| `SAU-MOC` | Chỉ có số từ 2026 trở đi | Nhãn "sau mốc phạm vi" |
| `MAU-THUAN` | Các nguồn nói khác nhau | **Ghi tất cả các giá trị và nguồn tương ứng.** Không tự chọn một con số — `target.md` §7.2 |

`KHONG-CO` và `MAU-THUAN` là hai mã có giá trị nghiên cứu cao nhất. Chúng là đầu vào trực tiếp của `data/coverage.md` (T2.8) và của tuyên bố giới hạn dữ liệu ở chương 11.

---

## 7. Quy tắc đặt mã ô

```
<NƯỚC>-<NĂM>-<CHỈ TIÊU>-<LOẠI NGƯỜI VAY>
```

Mã nước hai chữ, chữ hoa. Loại người vay viết tắt: `TD` tiêu dùng · `DN` doanh nghiệp nhỏ · `BDS` bất động sản · `GOP` gộp · `NA` không áp dụng. Cấp khu vực dùng tiền tố khu vực: `EU`, `APAC`, `SSA`, `LAC`, `MENA`, `GLOBAL`.

Ví dụ: `VN-2020-GIAINGAN-GOP` · `KR-2019-NENTANG-NA` · `EU-2020-GIAINGAN-TD`

Mã phải **duy nhất trong toàn bộ `data/`**. Trùng mã nghĩa là hai nguồn nói về cùng một ô — khi đó gộp thành một dòng và dùng `MAU-THUAN`, không tạo hai dòng.

---

## 8. Quy tắc neo trong nguồn

| Loại nguồn | Neo bằng gì |
|---|---|
| PDF đã mở bản gốc | **Số trang in trên trang đó** — không phải số thứ tự trang trong tệp |
| PDF có chênh lệch hai hệ số trang | Số trang in, và ghi `C-TRANG` vào `canh_bao` |
| PDF không xác định được trang | **Tên bảng hoặc tên mục**, không đoán số trang |
| Trang web | Tên mục + ngày truy cập |
| Văn bản pháp quy | Số điều, khoản |

**Bối cảnh của quy tắc này**: khi kiểm G1 đã phát hiện độ lệch giữa số trang in và số thứ tự trang trong tệp trôi từ +1 tới +13, và ở phần cuối tài liệu thì không xác định được trang nào là trang nào (`source-audit-ccaf.md` §1). Kiểm toàn vẹn tệp đạt PASS vẫn không loại trừ được lỗi này. Neo sai trang là lỗi không tự lộ ra — người đọc lật tới nơi không thấy gì, và không có cách nào biết là do neo sai hay do số bịa.

---

## 9. Mã cảnh báo phương pháp

Điền vào cột `canh_bao`. Mã đi theo con số suốt đời con số đó — từ `data/` sang `content/` sang bảng in ra.

| Mã | Cảnh báo |
|---|---|
| `C-KHAOSAT` | Số khảo sát tự nguyện, không phải số giám sát |
| `C-SONGSOT` | Thiên lệch sống sót: nền tảng đã sụp thường không còn trả lời khảo sát (`target.md` §7.5) |
| `C-MAU` | Mẫu biến động mạnh giữa các năm — biến động số liệu lẫn với biến động mẫu |
| `C-TUCONGBO` | Số do nền tảng tự công bố (tầng 5) |
| `C-TYGIA` | Quy đổi ngoại tệ có thể làm sai lệch biến động theo năm |
| `C-GOP` | Số gộp nhiều mô hình hoặc nhiều loại người vay |
| `C-QUYMO` | Nguồn không tách theo quy mô doanh nghiệp |
| `C-COHORT` | Tỷ lệ nợ xấu tính trên tổng dư nợ, không theo lứa vay |
| `C-PHI` | Lãi suất chưa gồm phí |
| `C-DINHNGHIA` | Nguồn dùng định nghĩa rộng hơn hoặc hẹp hơn định nghĩa ở §5 |
| `C-TRANG` | Nguồn có chênh lệch hệ số trang, neo trang cần thận trọng |
| `C-GIANTIEP` | Trích gián tiếp qua nguồn thứ ba, chưa mở bản gốc |

**Bốn mã dùng mặc định cho mọi số CCAF**: `C-KHAOSAT`, `C-SONGSOT`, `C-MAU`, `C-TYGIA`. Lý do đầy đủ ở `source-audit-ccaf.md` §8.

---

## 10. Mẫu bảng dùng trong `data/*.md`

Mỗi file dữ liệu một nước gồm bốn phần theo thứ tự: bảng đoạn 1 → bảng đoạn 2 → ô trống → nhật ký.

### 10.1. Bảng đoạn 1 (2013-2020)

```markdown
## Đoạn 1 — 2013-2020 (so sánh chéo được)

| ma | nam | chi_tieu | loai_nguoi_vay | mo_hinh | gia_tri | don_vi | nguon | neo | tang | tu_cong_bo | ngay_truy_cap | trang_thai | canh_bao | ghi_chu |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
```

### 10.2. Bảng đoạn 2 (2021-2025) — bắt buộc mang câu cảnh báo

Mọi bảng đoạn 2, ở mọi file, ở cả `data/` lẫn `content/`, phải mở đầu bằng đúng khối này:

```markdown
## Đoạn 2 — 2021-2025 (chỉ mô tả theo từng nước)

> ⚠ **Không so sánh chéo giữa các nước.** Số trong bảng này lấy từ cơ quan quản lý từng
> nước, mỗi nước một định nghĩa và một cách đếm. Chỉ dùng để mô tả diễn biến nội bộ của
> chính thị trường này theo thời gian. Không đặt cạnh số của nước khác, không cộng tổng
> khu vực, không phát biểu nước nào lớn hơn nước nào. Căn cứ: quyết định **D10**,
> `target.md` §5.1.
>
> **Định nghĩa nguồn dùng ở bảng này**: <ghi rõ cơ quan nào, định nghĩa gì, đếm thế nào>

| ma | nam | chi_tieu | ... |
|---|---|---|---|
```

Dòng "Định nghĩa nguồn" **không được bỏ trống**. Nó chính là thứ làm cho bảng đoạn 2 dùng được — thiếu nó thì bảng chỉ là một dãy số không diễn giải được.

### 10.3. Mục ô trống

Liệt kê mọi dòng mang mã ở §6, kèm nơi đã tìm. Đây là phần chảy thẳng vào `data/coverage.md`.

### 10.4. Nhật ký

Ngày · đã thêm gì · nguồn nào mới mở.

---

## 11. Danh sách thu thập bắt buộc

Ba nhóm dưới đây **phải có kết quả** — kể cả kết quả là `KHONG-CO` — trước khi đóng P2 và trình Cổng G2.

### 11.1. Ba câu hỏi "sau khi siết" — quyết định câu trả lời cho SQ5

Nguồn yêu cầu: `gaps.md` §11, §14.2. `target.md` §1.2 gọi SQ5 là câu hỏi *"khó chịu nhất và bị bỏ qua nhiều nhất"*.

| # | Nước | Câu hỏi | Ô dữ liệu tối thiểu | Vì sao quyết định |
|---|---|---|---|---|
| 1 | **Hàn Quốc** | Sau luật chuyên biệt 8/2020, ngành phát triển hay co lại? | `NENTANG` và `GIAINGAN` các năm 2020-2025 | Nếu co lại → kết luận là *"luật chuyên biệt làm việc co lại có trật tự, không cứu được mô hình"*, **rất khác** với "Việt Nam nên làm luật như Hàn Quốc". Định hình chương 11 |
| 2 | **Ấn Độ** | Sau đợt siết 8/2024, ngành còn lại gì? | `NENTANG` và `GIAINGAN` các năm 2024-2025 | Ấn Độ có đủ sáu đòn bẩy ở mức chặt nhất khảo sát. Nếu ngành vẫn không sống được thì kết luận **không thể** là "cần quản chặt hơn" |
| 3 | **Singapore** | "Nhỏ bao nhiêu, ổn theo nghĩa nào" | `NENTANG`, `GIAINGAN`, và **mốc can thiệp** | `gaps.md` §8.2. Cấm viết "ngành nhỏ và ổn" cho tới khi có số |

**Cả ba đều nằm ngoài tầm với của nguồn xuyên quốc gia** — `source-audit-ccaf.md` §6 đã kiểm và xác nhận. Phải lấy từ cơ quan quản lý từng nước, tức rơi vào **đoạn 2** và chịu lệnh cấm so sánh chéo. Hệ quả: câu trả lời cho SQ5 sẽ có dạng *ba mô tả nội bộ đặt song song*, không phải một so sánh định lượng. Cần nói rõ điều này khi viết.

Với Singapore đã có phần khởi đầu ở đoạn 1 (`source-audit-ccaf.md` §7.2) — nhưng mốc can thiệp vẫn trống, nên câu hỏi chưa đóng.

### 11.2. Hai đại lượng tổn thất xã hội Trung Quốc

`gaps.md` §10, rủi ro **R2**. Hai ô: `CN-<năm>-TONTHAT-*` cho *số nhà đầu tư bị ảnh hưởng* và cho *giá trị chưa thu hồi*. Nếu kết quả là `KHONG-CO`, phải ghi đầy đủ đã tìm ở đâu — vì khi đó **SQ3 chỉ trả lời được định tính**, và đó là một quyết định phải trình Cổng G2.

### 11.3. Việt Nam — ghi cả những gì không tìm thấy

`gaps.md` §2, rủi ro **R3**. `data/vn.md` phải ghi đầy đủ dấu vết tìm kiếm, không chỉ kết quả. Đây là nguyên liệu trực tiếp của tuyên bố giới hạn dữ liệu mở đầu chương 11 (`target.md` §6).

Ba nhóm số đã tìm được ở T2.0 (`source-audit-ccaf.md` §7.1) phải chuyển vào `data/vn.md` **kèm nguyên vẹn bốn giới hạn** đi cùng — đặc biệt là: đó là số **gộp mọi mô hình**, không phải số P2P, và có đếm cả nền tảng nước ngoài.

---

## 12. Kiểm trước khi đóng một file dữ liệu

| # | Kiểm |
|---|---|
| 1 | Mọi dòng có đủ 17 cột bắt buộc, không ô nào để trắng |
| 2 | Mọi dòng có `doan` đúng; không có bảng nào trộn lẫn hai đoạn |
| 3 | Mọi bảng đoạn 2 mang đủ khối cảnh báo **và** dòng định nghĩa nguồn |
| 4 | Mọi dòng `loai_nguoi_vay = gộp` có mã `C-GOP` |
| 5 | Mọi dòng tầng 5 có `tu_cong_bo = có` và mã `C-TUCONGBO` |
| 6 | Mọi dòng `KHONG-CO` có ghi rõ đã tìm ở đâu |
| 7 | Mọi dòng `MAU-THUAN` liệt kê đủ các giá trị và nguồn, không tự chọn một |
| 8 | Mọi neo trang PDF là số trang in, không phải số thứ tự trang trong tệp |
| 9 | Không mã ô nào trùng với file dữ liệu khác |
| 10 | Không dòng nào ở trạng thái `◐` hoặc `⬜` bị trích sang `content/` |

---

## 13. Nhật ký cập nhật

| Ngày | Thay đổi |
|---|---|
| 2026-07-26 | Lập lược đồ. Thiết kế dạng dài thay vì dạng rộng sau kết quả kiểm nguồn T2.0; thêm mã trạng thái ô trống, mã cảnh báo phương pháp, quy tắc neo trang; đưa ba câu hỏi "sau khi siết" vào danh sách thu thập bắt buộc |
