# Thư mục nguồn nền — báo cáo tổ chức quốc tế & nghiên cứu khảo sát toàn cầu

> **Hiện vật của T1.2** (`plan.md` §3). File này chỉ chứa **nguồn nền xuyên quốc gia**. Văn bản pháp quy từng nước nằm ở `sources/legal/`; khoảng trống nguồn ghi ở `sources/gaps.md`.
>
> **Ngày rà soát**: 2026-07-26 — mọi đường dẫn dưới đây được truy cập trong ngày này.

---

## 0. Cách đọc file này

### 0.1. Cột trạng thái xác minh

| Ký hiệu | Nghĩa |
|---|---|
| ✅ | Đã mở trang gốc của tổ chức phát hành; tên, cơ quan, ngày, đường dẫn đều lấy từ đó |
| ◐ | Tên và đường dẫn khớp nhau qua nhiều kết quả độc lập, **nhưng chưa mở bản gốc**. Phải mở trước khi trích vào báo cáo |
| ⬜ | Mới biết là có tồn tại, chưa xác minh gì |

**Quy tắc**: không trích một dòng nào ở mức ◐ hoặc ⬜ vào `content/`. Nâng lên ✅ trước, hoặc bỏ.

### 0.2. Ranh giới quan trọng

File này ghi **nguồn**, không ghi **số liệu**. Các con số cụ thể (quy mô thị trường, số nền tảng, tỷ lệ nợ xấu) chỉ được rút ra khi mở bản gốc, và đi thẳng vào `data/*.md` ở P2 kèm số trang. Lý do: số đọc qua bản tóm tắt của bên thứ ba là đúng loại sai sót mà `target.md` §7.2 cấm.

### 0.3. Thứ bậc áp dụng

Xếp theo `target.md` §7.1. Trong file này chỉ có tầng 2 và tầng 3 (thống kê chính thức, tổ chức quốc tế, nghiên cứu bình duyệt). Tầng 1 (văn bản pháp quy gốc) thuộc `sources/legal/`. Tầng 5 (số liệu tự công bố của nền tảng) chưa thu thập, sẽ có ở P2 và luôn phải đánh dấu riêng.

---

## 1. Nguồn xương sống định lượng xuyên quốc gia

Đây là nhóm quan trọng nhất: không có nhóm này thì `target.md` §5 không đứng được.

### 1.1. Bộ chuẩn đối sánh của Cambridge (CCAF)

Hai báo cáo dưới đây là **nguồn định lượng xuyên quốc gia duy nhất có phương pháp nhất quán qua nhiều năm**. Chúng thu số liệu trực tiếp từ nền tảng qua khảo sát, nên thuộc tầng 3 chứ không phải tầng 2 — nhưng vì không có nguồn nào khác phủ được ngần ấy nước, chúng thực tế là xương sống của mọi so sánh quốc tế về P2P.

| # | Nguồn | TT |
|---|---|---|
| **G1** | Ziegler, T., Shneor, R., Wenzlaff, K., Wang, B. W., Kim, J., Odorovic, A., Ferri de Camargo Paes, F., Suresh, K., Zhang, B. Z., Johanson, D., Lopez, C., Mammadova, L., Adams, N., & Luo, D. (2020). *The Global Alternative Finance Market Benchmarking Report: Trends, Opportunities and Challenges for Lending, Equity and Non-Investment Alternative Finance Models*. Cambridge Centre for Alternative Finance, Cambridge Judge Business School. Tháng 4/2020. Dữ liệu năm 2018. PDF: `https://www.jbs.cam.ac.uk/wp-content/uploads/2020/08/2020-04-22-ccaf-global-alternative-finance-market-benchmarking-report.pdf` | ✅ |
| **G2** | Ziegler, T., Shneor, R., Wenzlaff, K., Suresh, K., Ferri de Camargo Paes, F., Mammadova, L., Wanga, C., Kekre, N., Mutinda, S., Wang, B. W., López Closs, C., Zhang, B., Forbes, H., Soki, E., Alam, N., & Knaup, C. (2021). *The 2nd Global Alternative Finance Market Benchmarking Report*. Cambridge Centre for Alternative Finance, Cambridge Judge Business School. Tháng 6/2021. Dữ liệu 2019–2020. PDF: `https://www.jbs.cam.ac.uk/wp-content/uploads/2021/06/ccaf-2021-06-report-2nd-global-alternative-finance-benchmarking-study-report.pdf` | ✅ |

| **G3-UK** | Zhang, B., Ziegler, T., Garvey, K., et al. (2018). *The 5th UK Alternative Finance Industry Report*. Cambridge Centre for Alternative Finance, Cambridge Judge Business School. Tháng 11/2018. **Dữ liệu 2014–2017, công bố bằng GBP.** PDF: `https://www.jbs.cam.ac.uk/fileadmin/user_upload/research/centres/alternative-finance/downloads/2018-5th-uk-alternative-finance-industry-report.pdf` | ✅ |

> **G3-UK thêm ngày 2026-07-26 tại T2.3** (mã cũ `UKD-1` trong `data/uk.md`). Đây là báo cáo **chuyên
> về một nước**, khác hai báo cáo toàn cầu ở trên, và là nguồn duy nhất dựng được chuỗi Anh 2014-2017
> **tách theo mô hình**. Ba cảnh báo phương pháp của CCAF áp nguyên; riêng `C-TYGIA` **không áp** vì số
> bằng bảng Anh cho thị trường Anh — không có phép quy đổi nào (lý do đầy đủ: `data/uk.md` §1.2a).
> Kiểm toàn vẹn tệp **PASS**, sha256 `43858d6f…6b1f68`, 56 trang. Độ lệch trang **ổn định −1** → neo
> được số trang in. Hai chỗ nguồn **tự mâu thuẫn**, phát hiện bằng đối chiếu số học: `data/uk.md` §4.

**Dùng cho**: `target.md` §5 toàn bộ; chương 3-7 phần quy mô thị trường; SQ3 (tỷ trọng vốn lẻ vs định chế — CCAF có tách chỉ số này).

**Ba cảnh báo phương pháp phải mang theo khi dùng:**

1. **Đây là số khảo sát tự nguyện, không phải số giám sát.** Mẫu đổi giữa các năm; nền tảng đã sụp thường không trả lời khảo sát nữa. Đây chính là **thiên lệch sống sót** mà `target.md` §7.5 cảnh báo — và nó nằm ngay trong nguồn định lượng chính. Phải nêu rõ ở chương 2 và ở mọi bảng dùng số CCAF.
2. **Phân loại của CCAF rộng hơn phạm vi báo cáo này.** "Alternative finance" của họ gồm cả gọi vốn cổ phần cộng đồng và các mô hình phi đầu tư — những thứ `target.md` §8 loại trừ. Phải lọc về đúng các dòng cho vay trước khi dùng.
3. **Mức độ tách hai thị trường** — ✅ **đã kiểm ngày 2026-07-26 (T2.0)**: CCAF tách theo mô hình (P2P consumer / business / property lending / balance sheet lending / invoice trading), **đầy đủ ở cấp khu vực nhưng đứt ở cấp quốc gia**. Phụ lục theo nước chỉ có tổng gộp mọi mô hình; cơ cấu theo mô hình của một nước chỉ có ở phiếu hồ sơ năm 2018 (35 nước, dạng văn xuôi, 1-3 mô hình dẫn đầu) và ở xếp hạng top 3-4 cho 2019-2020. Nguyên nhân: ngưỡng tối thiểu 10 quan sát theo từng nước và từng mô hình (G2 tr. 34). Hồ sơ đầy đủ + hệ quả cho các chương: **`data/source-audit-ccaf.md`**.

**Bốn cảnh báo bổ sung, phát hiện khi mở bản gốc (G2 tr. 32-34)** — chi tiết ở `data/source-audit-ccaf.md` §8:

4. **Mẫu co mạnh**: 1.227 đơn vị trả lời (2018) → 821 (2019) → 703 (2020). Biến động số liệu lẫn với biến động mẫu.
5. **Riêng Trung Quốc mất 320 đơn vị** khỏi mẫu do chính các lệnh siết — chuỗi số Trung Quốc của CCAF **không đo được quá trình xoá sổ**.
6. **Quy đổi USD theo tỷ giá bình quân năm**; G2 tự ghi nhận 2020 tỷ giá biến động mạnh ở châu Á, Nam Mỹ, châu Phi.
7. **Số bình quân có trọng số và đã loại giá trị ngoại lai** — không so trực tiếp với số bình quân của cơ quan quản lý.

**Kiểm toàn vẹn tệp** (`scripts/pdf_read_preflight.py`, 2026-07-26): cả hai **PASS**, không bị cắt cụt. G1 sha256 `49cec180…65de1`, 228 trang. G2 sha256 `dd2860b1…c37a3`, 197 trang.

⚠ **Neo trang**: ở G2, số trang in trùng số thứ tự trang trong tệp. Ở **G1 thì không** — độ lệch trôi từ +1 tới +13, và **phần phụ lục thì không neo trang được**, phải trích theo tên bảng. Xem `data/source-audit-ccaf.md` §1.

**Khoảng trống đã thấy ngay**: G2 dừng ở dữ liệu 2020. **Chưa tìm thấy bản thứ 3 phủ 2021–2025.** Nghĩa là năm năm cuối của phạm vi báo cáo (`target.md` §0.6 — hết 2025) chưa có nguồn định lượng xuyên quốc gia tương đương. Đây là rủi ro R1 hiện hình sớm hơn dự kiến → đã ghi vào `gaps.md` §1.

### 1.2. Cơ sở dữ liệu tín dụng fintech của BIS

| # | Nguồn | TT |
|---|---|---|
| **G3** | Cornelli, G., Frost, J., Gambacorta, L., Rau, P. R., Wardrop, R., & Ziegler, T. *Fintech and big tech credit: a new database*. BIS Working Papers No. 887, Bank for International Settlements, tháng 9/2020. PDF: `https://www.bis.org/publ/work887.pdf` | ◐ |

**Dùng cho**: kiểm chứng chéo số CCAF; tách **tín dụng fintech** khỏi **tín dụng của các tập đoàn công nghệ lớn** — một ranh giới `target.md` §8 cần vạch rõ. Phủ 79 nước.

**Lưu ý**: bộ này xây trên dữ liệu CCAF, nên **không phải nguồn độc lập** để kiểm chứng chéo về quy mô. Giá trị của nó nằm ở việc chuẩn hoá và ở phần phân tích các yếu tố quyết định tăng trưởng, không ở chỗ xác nhận lại con số.

### 1.3. Giám sát trung gian tài chính phi ngân hàng của FSB

| # | Nguồn | TT |
|---|---|---|
| **G4** | Financial Stability Board. *Global Monitoring Report on Nonbank Financial Intermediation 2025*. FSB, 16/12/2025. Phủ 29 khu vực pháp lý, dữ liệu năm 2024. PDF: `https://www.fsb.org/uploads/P161225.pdf` | ✅ |
| **G5** | Financial Stability Board. *Global Monitoring Report on Non-Bank Financial Intermediation 2024*. FSB, tháng 12/2024. PDF: `https://www.fsb.org/uploads/P161224.pdf` | ◐ |

**Dùng cho**: đây là **nguồn tầng 2 duy nhất** (số do cơ quan giám sát tập hợp) có chuỗi chạy tới 2024, tức phủ được đoạn cuối phạm vi mà CCAF bỏ trống.

**Hạn chế nặng, phải kiểm ngay ở P2**: các bản gần đây gộp cho vay fintech vào một mục nhỏ trong khối tài sản của các trung gian tài chính khác, chỉ một phần khu vực pháp lý báo cáo, và định nghĩa "cho vay fintech" của FSB là *cho vay qua nền tảng điện tử không do ngân hàng thương mại vận hành* — rộng hơn P2P đúng nghĩa. Nếu dùng, phải nêu rõ định nghĩa và số khu vực đã báo cáo, không trình bày như số phủ toàn cầu.

---

## 2. Nguồn khung điều tiết xuyên quốc gia

Nhóm này nuôi trực tiếp Khung B — sáu đòn bẩy L1-L6 (`target.md` §2.2) và Phụ lục C.

| # | Nguồn | Vai trò | TT |
|---|---|---|---|
| **R1** | Rowan, P., Miller, M., Schizas, E., Zhang, B. Z., Carvajal, A., Blandin, A., Garvey, K., Ziegler, T., Rau, R., Randall, D., Hu, A., Umer, Z., Cloud, K., Mammadova, L., Kim, J., & Yerolemou, N. (2019). *Regulating Alternative Finance: Results from a Global Regulator Survey*. CCAF, University of Cambridge Judge Business School, phối hợp với World Bank. Tháng 11/2019. Khảo sát **111 khu vực pháp lý**. PDF: `https://www.jbs.cam.ac.uk/wp-content/uploads/2020/08/2019-11-ccaf-regulating-alternative-finance-report.pdf` — bản World Bank: `https://documents1.worldbank.org/curated/en/266801571428246032/pdf/Regulating-Alternative-Finance-Results-from-a-Global-Regulatory-Survey.pdf` | **Nguồn nền tốt nhất cho Khung B.** Khảo sát chính cơ quan quản lý, không phải nền tảng. Cho biết bao nhiêu nước có chế độ chuyên biệt cho P2P, dùng công cụ gì | ✅ |
| **R2** | Committee on the Global Financial System & Financial Stability Board. *FinTech credit: Market structure, business models and financial stability implications*. CGFS–FSB, 22/5/2017. PDF: `https://www.bis.org/publ/cgfs_fsb1.pdf` | Bản phân loại mô hình kinh doanh có thẩm quyền nhất, ra **trước** đợt đổ vỡ Trung Quốc. Đối chiếu trực tiếp với Khung A (`target.md` §2.1) — kiểm xem khung tự dựng có bỏ sót trục nào không | ✅ |
| **R3** | Financial Stability Board. *Financial Stability Implications from FinTech: Supervisory and Regulatory Issues that Merit Authorities' Attention*. FSB, 27/6/2017. PDF: `https://www.fsb.org/uploads/R270617.pdf` | Đặt P2P vào bức tranh ổn định tài chính rộng hơn; nguồn cho lập luận "vì sao cơ quan quản lý phản ứng chậm" | ◐ |
| **R4** | Financial Stability Board. *FinTech and market structure in financial services: Market developments and potential financial stability implications*. FSB, 14/2/2019. PDF: `https://www.fsb.org/uploads/P140219.pdf` | Giai đoạn G5 (tái định hình) — nền tảng trở thành ngân hàng, hoặc bị ngân hàng/tập đoàn công nghệ hấp thụ | ◐ |
| **R5** | International Organization of Securities Commissions. *Crowdfunding 2015 Survey Responses Report*. IOSCOPD520, IOSCO, tháng 12/2015. 23 thành viên trả lời. PDF: `https://www.iosco.org/library/pubdocs/pdf/IOSCOPD520.pdf` | **Ảnh chụp trạng thái điều tiết trước đợt bùng nổ.** Giá trị nằm ở chỗ nó ghi lại việc phần lớn khu vực pháp lý *chưa có gì* vào đúng lúc thị trường sắp bùng — bằng chứng trực tiếp cho SQ4 (điều tiết sớm hay muộn) | ◐ |
| **R6** | International Organization of Securities Commissions. *IOSCO Research Report on Financial Technologies (Fintech)*. IOSCO, tháng 2/2017. PDF: `https://www.iosco.org/library/pubdocs/pdf/ioscopd554.pdf` | Góc nhìn cơ quan quản lý chứng khoán — quan trọng cho SQ1 vì Mỹ định danh P2P là chứng khoán | ◐ |
| **R7** | Garvey, K. *The Landscape of Peer to Peer / Marketplace Lending*. World Bank FinSAC Fintech Conference, 2019. PDF: `https://thedocs.worldbank.org/en/doc/382571560127611420-0130022019/original/FinSACFintech19KieranGarvey.pdf` | Tài liệu trình bày, không phải báo cáo bình duyệt → **chỉ dùng để định hướng, không trích số** | ◐ |

> **Ghi chú xác minh R5**: `iosco.org` chặn truy cập tự động (HTTP 403). Hai văn bản IOSCO phải mở thủ công bằng trình duyệt trước khi trích. Đã ghi vào `gaps.md` §3.

---

## 3. Nguồn về bao trùm tài chính và bối cảnh đang phát triển

Nhóm này nuôi chương 11 (Việt Nam) và các đối chiếu Indonesia / Ấn Độ.

| # | Nguồn | Vai trò | TT |
|---|---|---|---|
| **D1** | CGAP. *Crowdfunding and Financial Inclusion*. Working Paper, CGAP, tháng 3/2017. PDF: `https://www.cgap.org/sites/default/files/Working-Paper-Crowdfunding-and-Financial-Inclusion-Mar-2017.pdf` | Kiểm chứng lập luận "P2P mở rộng tiếp cận tín dụng" — CGAP tiếp cận vấn đề này thận trọng hơn hẳn tài liệu ngành | ◐ |
| **D2** | Asian Development Bank Institute. *Optimal Regulation of P2P Lending for Small and Medium-Sized Enterprises*. ADBI Working Paper No. 912. PDF: `https://www.adb.org/sites/default/files/publication/478611/adbi-wp912.pdf` | Cho vay doanh nghiệp nhỏ trong bối cảnh châu Á — trực tiếp phục vụ SQ7 và chương 8 | ◐ |
| **D3** | Asian Development Bank Institute. *Big Data-Based Peer-to-Peer Lending Fintech: Surveillance System through Utilization of Google Play Review*. ADBI Working Paper No. 943. PDF: `https://www.adb.org/sites/default/files/publication/497121/adbi-wp943.pdf` | Về Indonesia; cách tiếp cận giám sát nền tảng lậu qua dấu vết ứng dụng — liên quan nhóm biến tướng **B4** (`target.md` §4.1) | ◐ |
| **D4** | Asian Development Bank Institute. *Fintech Development and Regulatory Frameworks*. ADBI Working Paper No. 1014. PDF: `https://www.adb.org/sites/default/files/publication/532761/adbi-wp1014.pdf` | Đối chiếu khung điều tiết trong khu vực | ◐ |
| **D5** | Asian Development Bank. *P2P Lending and Monetary Policy Transmission*. ADB Economics Working Paper Series No. 749, tháng 11/2024. PDF: `https://www.adb.org/sites/default/files/publication/1007601/ewp-749-p2p-lending-monetary-policy-transmission.pdf` | Một trong số ít nguồn tổ chức quốc tế **có dữ liệu sau 2020**; có chuỗi số Trung Quốc 2014–2017 và mốc siết | ◐ |
| **D6** | OECD. *Financing SMEs and Entrepreneurs* (bộ Scoreboard, xuất bản hằng năm, gần 50 nước). Bản mới nhất: *Financing SMEs and Entrepreneurs 2026*, OECD Publishing. `https://www.oecd.org/en/publications/financing-smes-and-entrepreneurs-2026_075d8058-en.html` | Chuỗi số cho vay doanh nghiệp nhỏ theo nước, có mục tài chính thay thế. **Cẩn thận mốc phạm vi**: bản 2026 nằm sau mốc hết-2025, dùng phải gắn nhãn theo `target.md` §0.6 | ◐ |
| **D7** | OECD. *Alternative Financing Instruments for SMEs and Entrepreneurs*. OECD SME and Entrepreneurship Papers. PDF: `https://www.oecd.org/content/dam/oecd/en/publications/reports/2018/12/alternative-financing-instruments-for-smes-and-entrepreneurs_b9642127/dbdda9b6-en.pdf` | Khung phân loại công cụ tài chính thay thế; hữu ích để vạch ranh giới khái niệm ở chương 2 | ◐ |

---

## 4. Nghiên cứu bình duyệt — tuyến Trung Quốc

Chương 6 là chương dài nhất (`target.md` §6) nên tuyến này cần nền học thuật riêng. Ghi ở đây vì tất cả đều là phân tích cấp thị trường, không phải văn bản pháp quy — văn bản pháp quy Trung Quốc nằm ở `sources/legal/cn.md`.

| # | Nguồn | Vai trò | TT |
|---|---|---|---|
| **C1** | *The failure of Chinese peer-to-peer lending platforms: Finance and politics*. Journal of Corporate Finance. `https://www.sciencedirect.com/science/article/abs/pii/S0929119920302960` | Phân tích định lượng nguyên nhân đổ vỡ ở cấp nền tảng, tách yếu tố tài chính và yếu tố chính trị. **Nguồn tốt nhất tìm được cho câu hỏi "vì sao nền tảng này sụp mà nền tảng kia không"** | ◐ |
| **C2** | *Fintech market and regulation: Lessons from China's peer-to-peer lending platforms*. Journal of Corporate Finance. `https://www.sciencedirect.com/science/article/abs/pii/S0929119926000271` | Rút bài học điều tiết; **xuất bản 2026 → sau mốc phạm vi**, dùng được như phân tích nhưng dữ kiện phải kiểm mốc thời gian | ◐ |
| **C3** | *Too Much Technology and Too Little Regulation? The Spectacular Demise of P2P Lending in China*. Accounting, Economics, and Law. DOI: `10.1515/ael-2021-0056` | Tường thuật toàn bộ cung đường 2007 → 2019/20 dưới góc pháp lý. Hữu ích để dựng dòng thời gian T1.4 | ◐ |
| **C4** | *Regulatory Experimentation in China's Peer-to-Peer Lending Market*. Tsinghua China Law Review. PDF: `https://www.tsinghuachinalawreview.law.tsinghua.edu.cn/UploadFiles/2023-04-03/vrxvtgpzgldkvgge.pdf` | **Nguồn luật học Trung Quốc bản địa** — đúng tinh thần `target.md` §7.3 (ưu tiên nguồn gốc thay vì bản tường thuật tiếng Anh). Cần dùng để đối chiếu tên và số hiệu văn bản ở T1.3e | ◐ |
| **C5** | *The crowding-out effect of formal finance on the P2P lending market: An explanation for the failure of China's P2P lending industry*. Finance Research Letters. `https://www.sciencedirect.com/science/article/abs/pii/S1544612321002439` | Giả thuyết cạnh tranh cho SQ5 — mô hình chết vì bị tín dụng chính thức lấn át, không chỉ vì quản lý kém | ◐ |

**Ghi chú về C1-C5**: bốn trong năm nguồn nằm sau tường phí. Cần xác định đường tiếp cận trước khi tính chúng vào kế hoạch → `gaps.md` §4.

---

## 5. Nguồn báo chí tài chính (tầng 4)

Chưa lập danh mục bài cụ thể ở P1 — sẽ thu theo từng chương ở P2-P3. Ghi ở đây các đầu báo được `target.md` §7.1 chấp nhận, kèm ghi chú dùng vào đâu:

| Đầu báo | Dùng cho tuyến nào | Ghi chú |
|---|---|---|
| Caixin (財新) | Trung Quốc | Nguồn gốc tiếng Trung; đưa tin về các vụ đổ vỡ sớm và sâu hơn báo tiếng Anh |
| Financial Times | Anh, Mỹ | Theo sát Zopa, Funding Circle, RateSetter, Lendy |
| Reuters | Toàn tuyến | Dùng để xác định ngày sự kiện |
| Nikkei Asia | Nhật, Đông Nam Á | |

**Quy tắc dùng**: báo chí dùng để **xác định sự kiện và mốc thời gian**, không dùng để lấy số liệu thị trường. Số liệu phải quy về tầng 1-3.

---

## 6. Đánh giá độ phủ của thư mục nguồn nền

Kết luận sau khi rà soát ngày 2026-07-26:

| Chiều | Đánh giá |
|---|---|
| **Khung điều tiết xuyên quốc gia** | **Đủ tốt.** R1 (111 khu vực pháp lý) + R2 phủ được Khung A và Khung B. Đủ để bắt đầu T1.3 |
| **Định lượng đến 2020** | **Đủ.** G1 + G2 + G3 |
| **Định lượng 2021–2025** | **Thiếu nghiêm trọng.** Không có nguồn xuyên quốc gia nào tương đương CCAF cho đoạn này. G4/G5 chỉ vá được một phần và theo định nghĩa rộng hơn |
| **Tuyến Trung Quốc** | Nền học thuật đủ mạnh; vướng tường phí |
| **Tuyến Việt Nam** | ~~Trống hoàn toàn~~ → **sửa 2026-07-26**: G1 và G2 **có** Việt Nam trong phụ lục — chuỗi tổng khối lượng 2018-2020 và số nền tảng. Nhưng là **số gộp mọi mô hình**, không có cơ cấu (Việt Nam không có phiếu hồ sơ). Đánh giá "đủ để nói được điều gì đó có nguồn về quy mô, không đủ đỡ một chương định lượng" — `gaps.md` §2.1 |
| **Tách hai thị trường (§2.4)** | ✅ **Đã kiểm**: tách đầy đủ ở cấp khu vực, đứt ở cấp quốc gia. **R4 hiện hình ở dạng hẹp** — chương 8 phải neo vào bảng cấp khu vực. `data/source-audit-ccaf.md` |

**Hệ quả cho kế hoạch**: hai khoảng trống đầu tiên (định lượng 2021–2025, và Việt Nam) đủ nghiêm trọng để cần bàn tại **Cổng G2**, không phải muộn hơn. Đã ghi vào `sources/gaps.md`.

---

## 7. Nhật ký cập nhật file này

| Ngày | Thay đổi |
|---|---|
| 2026-07-26 | Lập file; 7 nguồn ở mức ✅, 17 nguồn ở mức ◐ |
| 2026-07-26 (T2.0) | Mở toàn văn G1 + G2. Đóng cảnh báo 3 của §1.1 (mức tách), thêm 4 cảnh báo phương pháp mới + kiểm toàn vẹn tệp + cảnh báo neo trang. Sửa hai dòng ở §6 (tuyến Việt Nam, tách hai thị trường) |
