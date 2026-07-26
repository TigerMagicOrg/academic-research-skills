# Dữ liệu định lượng — Trung Quốc

> **Hiện vật của T2.2** (`plan.md` §3). Ghi theo `data/schema.md`.
> **Ngày thu thập**: 2026-07-26.
>
> `khu_vuc` = **Trung Quốc** · `cap` = **quốc gia** cho mọi dòng trong file này. Ba cột đó được đưa lên
> tiêu đề bảng thay vì lặp ở từng dòng, đúng mẫu `schema.md` §10.1; cột `doan` do chính bảng khai báo.
> Vì mọi nguồn ở đây công bố bằng nhân dân tệ, cột `gia_tri` **giữ nguyên đơn vị gốc của nguồn**
> (亿元 = trăm triệu CNY, 万人 = vạn người) — không quy đổi, nên không có dòng nào mang `C-TYGIA`.

---

## 0. Phát hiện lớn nhất của lần thu thập này — đọc trước khi dùng bất kỳ con số nào

**Trung Quốc không có một chuỗi số liệu thị trường nào do cơ quan quản lý công bố cho giai đoạn đỉnh.**

Đây không phải nhận xét phụ. Toàn bộ các con số về quy mô thị trường 2013-2019 — thành giao dịch,
dư nợ, số nền tảng, số người tham gia — đều đến từ **hai cổng dữ liệu ngành** (网贷之家 và 零壹智库),
và cả hai đều tổng hợp lại từ **số do chính nền tảng tự công bố**. Cơ quan quản lý chỉ bắt đầu công bố
số liệu khi ngành đã bước vào giai đoạn thanh lý (2019-2022), và khi đó họ **chỉ công bố mức giảm
tương đối và số dư chưa thanh toán**, không công bố lại chuỗi quá khứ.

Ba hệ quả bắt buộc mang theo:

1. **Mọi dòng của giai đoạn đỉnh đều là tầng 5** (`target.md` §7.1) và mang `C-TUCONGBO`. Không có
   dòng nào ở tầng 2 trước năm 2019. Đây là mức bằng chứng yếu nhất trong toàn bộ báo cáo, và nó lại
   rơi đúng vào chương dài nhất.
2. **Hai cổng dữ liệu ngành không khớp nhau**, kể cả ở cùng một năm và cùng một chỉ tiêu — xem §4.
   Vì vậy nhiều ô phải ghi `MAU-THUAN` chứ không được chọn một con số (`target.md` §7.2).
3. **Không thể kiểm chứng chéo bằng CCAF.** Cảnh báo 5 của `source-audit-ccaf.md` §8 đã nói rõ: riêng
   Trung Quốc mất 320 đơn vị trả lời khỏi mẫu do chính các lệnh siết. Nguồn xuyên quốc gia không đo
   được quá trình xoá sổ, nên không dùng để trọng tài giữa hai cổng dữ liệu ngành.

**Kết quả với hai đại lượng tổn thất xã hội** (`gaps.md` §10, rủi ro **R2**) — tách đôi rõ rệt:

| Đại lượng | Kết quả |
|---|---|
| **Giá trị chưa thu hồi** | ✅ **Tìm được, và có chuỗi ba mốc.** 8.000+ tỷ (6/2020) → 8.207 tỷ (cuối 2020) → 4.974 tỷ CNY (cuối 2021). Nguồn cơ quan quản lý |
| **Số nhà đầu tư bị ảnh hưởng** | ❌ **`KHONG-CO`.** Cơ quan quản lý chỉ công bố **mức giảm phần trăm**, chưa từng công bố số tuyệt đối. Xem §5 mục 2 |

Nửa đầu của khoảng trống 🔴 §10 đóng lại; nửa sau vẫn mở và phải trình Cổng G2.

---

## 1. Nguồn dùng trong file này

Các nguồn dưới đây **chưa có mã trong `sources.md`** — chúng thuộc tầng 4 và tầng 5, mà `sources.md` §5
mới chỉ ghi danh sách đầu báo chứ chưa lập danh mục bài. Mã `CND-*` đặt tạm trong phạm vi file này;
việc hợp nhất vào `sources.md` ghi ở §6.

| Mã | Nguồn | Tầng | TT |
|---|---|---|---|
| `CND-1` | 网贷之家 (WDZJ) — cổng dữ liệu ngành, chuỗi thống kê P2P Trung Quốc. Trang gốc `wdzj.com` **không truy cập được** ngày 2026-07-26 (DNS không phân giải). Mọi số WDZJ dưới đây lấy qua nguồn thứ ba dẫn lại | 5 | ⬜ |
| `CND-2` | 零壹智库 / 零壹数据. *2017中国P2P网贷年度简报*. `https://www.01caijing.com/article/19615.htm` | 5 | ◐ |
| `CND-3` | 未央网 (Weiyangx). *P2P网贷12年，都发生了哪些变化？* `https://www.weiyangx.com/337036.html` — dẫn lại số WDZJ | 4 | ◐ |
| `CND-4` | 时代周报 qua 新浪科技. *P2P清零未了局：谁来为8000亿坏账买单？* 1/12/2020. `https://finance.sina.com.cn/tech/2020-12-01/doc-iiznezxs4532544.shtml` | 4 | ◐ |
| `CND-5` | 新浪财经. *郭树清：网贷平台出借人的资金还有8000多亿没回收*. 14/8/2020. `https://finance.sina.com.cn/roll/2020-08-14/doc-iivhvpwy0969274.shtml` — tường thuật phát biểu trên 央视新闻《相对论》 | 4 | ◐ |
| `CND-6` | 中国银行保险报, đăng lại trên cổng Sở Tài chính Vũ Hán. *网贷清退转型挑战仍巨*. 23/10/2020. `https://jrj.wuhan.gov.cn/ztzl_57/gzjj/jrfxfk/202010/t20201023_1471571.shtml` | 2 | ◐ |
| `CND-7` | 中国银行保险报, đăng lại trên cổng Sở Tài chính Ninh Ba. *3210家网贷机构存量业务已清零*. 27/4/2021. `http://jrb.ningbo.gov.cn/art/2021/4/27/art_1229023599_58895586.html` | 2 | ◐ |
| `CND-8` | 央视网 qua 新浪财经. *银保监会：全国P2P网贷存量业务总量大幅压降*. 22/4/2022 — tường thuật hội nghị truyền hình chuyên đề 2022 của Tổ lãnh đạo chấn chỉnh rủi ro cho vay qua mạng. `https://finance.sina.com.cn/jjxw/2022-04-22/doc-imcwiwst3447354.shtml` | 4 | ◐ |
| `CND-9` | 经济参考报, đăng lại trên cổng Ủy ban Tài chính tỉnh Chiết Giang. *后P2P时代：平台转型面临重重困境*. 28-29/1/2021. `https://zjic.zj.gov.cn/zkdt/rdzx/202104/t20210401_6510677.shtml` | 2 | ◐ |
| `CND-10` | Cục Giám sát Quản lý Tài chính địa phương Thâm Quyến, qua 新浪财经. *深圳400余家P2P网贷平台全部停止运营，余额下降90%*. 18/1/2023. `https://finance.sina.cn/bank/yhgd/2023-01-18/detail-imyaqran8951950.d.html` | 2 | ◐ |
| `CND-11` | 前瞻产业研究院 — dẫn lại số WDZJ cho 2019. `https://bg.qianzhan.com/report/detail/300/191209-a2bf4a54.html` | 5 | ⬜ |
| `CND-12` | Wikipedia tiếng Trung, *2018年中国网络借贷平台集体倒闭事件* | — | ⬜ **không dùng để trích số** |

> ⚠ **Không dòng nào trong file này đạt ✅.** Tất cả ở mức ◐ hoặc ⬜. Theo `schema.md` §12 kiểm 10 và
> `sources.md` §0.1, **không dòng nào được trích sang `content/`** cho tới khi nâng mức. Việc nâng mức
> ghi ở §6.

---

## 2. Đoạn 1 — 2013-2020 (so sánh chéo được)

`khu_vuc` = Trung Quốc · `cap` = quốc gia · `doan` = **1**

| ma | nam | chi_tieu | loai_nguoi_vay | mo_hinh | gia_tri | don_vi | nguon | neo | tang | tu_cong_bo | ngay_truy_cap | trang_thai | canh_bao | ghi_chu |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CN-2015-NENTANG-NA-HOATDONG | 2015 | NENTANG | không áp dụng | gộp | `MAU-THUAN` | nền tảng | CND-3 · nguồn thứ hai chưa định danh | mục "正常运营平台数" | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-MAU, C-DINHNGHIA | **Đang hoạt động** (正常运营). Hai giá trị: **3.576** cuối 2015 (CND-3 dẫn WDZJ) và **2.612** cuối tháng 11/2015 (nguồn dẫn lại, **chưa định danh được nhà cung cấp dữ liệu**). Chênh 964 nền tảng trong một tháng là bất khả — đây là hai cách đếm khác nhau, không phải biến động. Không chọn một con số |
| CN-2015-NENTANG-NA-LUYKE | 2015 | NENTANG | không áp dụng | gộp | >3800 | nền tảng | CND-3 | báo cáo năm 2015 của WDZJ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Luỹ kế từng lên sàn**, không phải đang hoạt động. Nguồn ghi "hơn 3.800" — số làm tròn |
| CN-2015-NENTANG-NA-VANDE | 2015 | NENTANG | không áp dụng | gộp | 950 | nền tảng | CND-3 | báo cáo năm 2015 của WDZJ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Đã rút lui / có vấn đề** (问题平台) phát sinh trong năm; nguồn ghi tăng 221% so 2014 |
| CN-2017-NENTANG-NA-HOATDONG | 2017 | NENTANG | không áp dụng | gộp | 1539 | nền tảng | CND-2 | mục thống kê số nền tảng, báo cáo năm 2017 | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Đang hoạt động**, theo 零壹智库. Nguồn **tự khai giới hạn phạm vi đếm**: chỉ nền tảng có nghiệp vụ trên PC, **không gồm Hồng Kông, Đài Loan, Ma Cao**. Đây là lý do chính khiến số của 零壹 thấp hơn WDZJ — xem §4 |
| CN-2017-NENTANG-NA-LUYKE | 2017 | NENTANG | không áp dụng | gộp | 5503 | nền tảng | CND-2 | như trên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Luỹ kế từng lên sàn** |
| CN-2017-NENTANG-NA-VANDE | 2017 | NENTANG | không áp dụng | gộp | 3902 | nền tảng | CND-2 | như trên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Có vấn đề, luỹ kế** — nguồn ghi chiếm 70,9% tổng luỹ kế |
| CN-2018-NENTANG-NA-HOATDONG | 2018 | NENTANG | không áp dụng | gộp | 1021 | nền tảng | CND-3 | báo cáo năm 2018 của WDZJ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Đang hoạt động**, cuối 2018. Nguồn ghi giảm 55,47% so cuối 2017 — mức giảm này **không khớp** với chuỗi của 零壹, xem §4 |
| CN-2018-NENTANG-NA-LUYKE | 2018 | NENTANG | không áp dụng | gộp | 6430 | nền tảng | CND-3 | như trên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-DINHNGHIA | **Luỹ kế**; trong đó 5.409 đã ngừng hoặc có vấn đề |
| CN-2019-NENTANG-NA-HOATDONG | 2019 | NENTANG | không áp dụng | gộp | 343 | nền tảng | CND-4 | phần thống kê cuối bài | 4 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GIANTIEP, C-DINHNGHIA | **Đang hoạt động bình thường**, cuối 2019. Báo chí dẫn lại số ngành, chưa truy được nguồn gốc |
| CN-2020-NENTANG-NA-HOATDONG-T8 | 2020 | NENTANG | không áp dụng | gộp | 15 | nền tảng | CND-6 | phát biểu của Phó Vụ trưởng Vụ Tài chính bao trùm 冯燕 tại họp báo | 2 | không | 2026-07-26 | ◐ | C-GIANTIEP | **Đang hoạt động thực tế**, cuối tháng 8/2020. **Đây là dòng tầng 2 sớm nhất tìm được** — cơ quan quản lý chỉ bắt đầu công bố khi ngành đã vào thanh lý |
| CN-2020-NENTANG-NA-HOATDONG-T11 | 2020 | NENTANG | không áp dụng | gộp | 0 | nền tảng | `sources/legal/cn.md` §3 | phát biểu của Luật sư trưởng CBIRC 刘福寿 tại Hội nghị thường niên *Tài Kinh* 2021 | 4 | không | 2026-07-26 | ◐ | C-GIANTIEP | **Về không giữa tháng 11/2020.** Đã có hồ sơ và ba cảnh báo bắt buộc ở `legal/cn.md` §3 — **không lặp lại ở đây, dùng phải đọc kèm** |
| CN-2015-GIAINGAN-GOP | 2015 | GIAINGAN | gộp | gộp | 9823.04 | 亿 CNY | CND-4 | phần thống kê quy mô theo năm | 4 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-GIANTIEP | Thành giao dịch cả năm (成交量) |
| CN-2016-GIAINGAN-GOP | 2016 | GIAINGAN | gộp | gộp | 20638.72 | 亿 CNY | CND-3 | báo cáo năm 2017 của WDZJ, phần so sánh cùng kỳ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP | |
| CN-2017-GIAINGAN-GOP | 2017 | GIAINGAN | gộp | gộp | `MAU-THUAN` | 亿 CNY | CND-3 · CND-2 | báo cáo năm 2017 của mỗi bên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-DINHNGHIA | **28.048,49** (WDZJ qua CND-3) vs **27.100** (零壹, ghi "khoảng 2,71 nghìn tỷ"). Chênh ~3,4%. Không chọn một con số |
| CN-2018-GIAINGAN-GOP | 2018 | GIAINGAN | gộp | gộp | 17948.01 | 亿 CNY | CND-11 | dẫn số WDZJ cả năm 2018 | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP | CND-4 ghi "1,79 nghìn tỷ" — **là số này làm tròn, không phải nguồn thứ hai độc lập.** Không tính là mâu thuẫn |
| CN-2019-GIAINGAN-GOP | 2019 | GIAINGAN | gộp | gộp | `MAU-THUAN` | 亿 CNY | CND-11 · CND-4 | như trên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP | **9.645,11** (CND-11 dẫn WDZJ) vs **9.649,11** (CND-4). Chênh 4 亿 — nhỏ nhưng là **hai giá trị khác nhau cho cùng một chỉ tiêu**, nhiều khả năng lỗi chép. Ghi cả hai theo `target.md` §7.2, không tự sửa |
| CN-2020-GIAINGAN-GOP | 2020 | GIAINGAN | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | Đã tìm ở: CND-6, CND-7, CND-9, và tìm bản năm 2020 của cả hai cổng dữ liệu ngành. **Không nguồn nào công bố thành giao dịch năm 2020.** Nguyên nhân cấu trúc: các cổng dữ liệu ngành ngừng công bố khi ngành bị xoá sổ, còn cơ quan quản lý chỉ công bố mức giảm và số dư — không công bố thành giao dịch |
| CN-2017-DUNO-GOP | 2017 | DUNO | gộp | gộp | `MAU-THUAN` | 亿 CNY | CND-3 · CND-2 | báo cáo năm 2017 của mỗi bên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-DINHNGHIA | Dư nợ **cuối năm**. **12.245,87** (WDZJ) vs **12.050** (零壹). Chênh ~1,6% |
| CN-2019-DUNO-GOP | 2019 | DUNO | gộp | gộp | 4915.91 | 亿 CNY | CND-11 | dẫn số WDZJ cuối 2019 | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP | Dư nợ **cuối năm**; nguồn ghi giảm 37,69% so cuối 2018 |
| CN-2020-DUNO-GOP | 2020 | DUNO | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | Đã tìm ở CND-6 đến CND-10. Cơ quan quản lý công bố **mức giảm phần trăm** (84% so đầu 2019, tại 8/2020 — CND-6) chứ không công bố mức tuyệt đối. Số tuyệt đối duy nhất có cho 2020 là **số dư chưa thanh toán**, đã ghi ở dòng TONTHAT |
| CN-2020-TONTHAT-GOP-TIEN | 2020 | TONTHAT | gộp | gộp | `MAU-THUAN` | 亿 CNY | CND-5 · CND-9 | CND-5: phát biểu 郭树清 trên 央视新闻《相对论》 · CND-9: bài của 经济参考报 | 4 · 2 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-GOP | **Đại lượng: giá trị chưa thu hồi** (未兑付余额). Hai mốc khác nhau, **không mâu thuẫn nội dung mà khác thời điểm**, ghi chung một ô vì cùng năm: **"hơn 8.000"** tại 6/2020 (郭树清, số làm tròn trong phát biểu miệng) và **8.207** cuối 2020 (CND-9). Số cuối 2020 khớp với mốc đầu 2021 ở bảng đoạn 2 → **hai nguồn độc lập chống đỡ lẫn nhau** |
| CN-2020-TONTHAT-GOP-NGUOI | 2020 | TONTHAT | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | **Đại lượng: số nhà đầu tư bị ảnh hưởng.** Đã tìm ở CND-4 → CND-10 và tìm riêng phát biểu của 郭树清 và 刘福寿. **Cơ quan quản lý chưa từng công bố số tuyệt đối** — chỉ công bố *mức giảm* (xem dòng dưới). Chi tiết dấu vết tìm kiếm: §5 mục 2 |
| CN-2020-TONTHAT-NA-GIAM | 2020 | TONTHAT | không áp dụng | gộp | 88 | % | CND-6 | phát biểu của 冯燕 tại họp báo | 2 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-DINHNGHIA | **Mức giảm số người cho vay** tại cuối 8/2020 so với **đầu 2019**, không phải số người bị ảnh hưởng. Cùng mốc: số nền tảng −99%, dư nợ −84%, người vay −73%. **Đây là hình thái duy nhất mà số người tham gia được công bố chính thức** — một tỷ lệ giảm không có mẫu số |
| CN-2018-NOXAU-GOP | 2018 | NOXAU | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | Đã tìm ở CND-2, CND-3, CND-4, CND-11 và tìm riêng theo từ khoá tỷ lệ nợ xấu / quá hạn theo lứa vay. **Không nguồn nào công bố nợ xấu theo lứa vay**; các cổng dữ liệu ngành công bố tỷ lệ do nền tảng tự khai, và đó chính là chỉ số mà `target.md` §4.1 nhóm **B2** liệt kê là *dấu hiệu gian lận* khi thấp và ổn định bất thường. Xem §5 mục 3 |
| CN-2018-VONLE-GOP | 2018 | VONLE | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | Đã tìm theo từ khoá tỷ trọng vốn nhà đầu tư cá nhân so với định chế, ở CND-2, CND-3 và trong tài liệu học thuật Trung Quốc (Đại học Thanh Hoa PBCSF, Viện Tài chính Internet ĐH Chiết Giang). **Không nguồn nào công bố tỷ trọng.** Xem §5 mục 4 — ô trống này có hệ quả trực tiếp cho **SQ3** |
| CN-2017-LAISUAT-GOP | 2017 | LAISUAT | gộp | gộp | `KHONG-CO` | — | — | — | — | không | 2026-07-26 | ◐ | — | **Cảnh báo khái niệm, không phải thiếu nguồn.** Chỉ tiêu công bố phổ biến ở Trung Quốc là *综合收益率* — **lợi suất phía người cho vay**, không phải chi phí phía người vay mà `schema.md` §5 định nghĩa. Người vay còn chịu thêm phí nền tảng. Có số cho 综合收益率 nhưng **không được ghi vào ô này** — chúng nay nằm ở các dòng `LOITUC` ngay dưới. Ô `LAISUAT` này **vẫn là `KHONG-CO`** và không được coi là đã lấp (`schema.md` §5.1 ràng buộc 2) |
| CN-2015-LOITUC-GOP-NAM | 2015 | LOITUC | gộp | gộp | 13.29 | % | CND-3 | báo cáo năm 2015 của WDZJ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-LECHPHIA, C-GIANTIEP | **Lợi suất tổng hợp** (综合收益率) — phía người cho vay. Bình quân cả năm 2015 |
| CN-2015-LOITUC-GOP-T12 | 2015 | LOITUC | gộp | gộp | 12.45 | % | CND-3 | như trên | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-LECHPHIA, C-GIANTIEP | Riêng tháng 12/2015. Thấp hơn bình quân năm — lợi suất **đang giảm trong nội bộ năm** |
| CN-2017-LOITUC-GOP-T12 | 2017 | LOITUC | gộp | gộp | 9.45–9.54 | % | CND-3 | báo cáo năm 2017 của WDZJ | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-LECHPHIA, C-GIANTIEP | Riêng tháng 12/2017. **Khoảng dao động trong tháng**, không phải hai giá trị mâu thuẫn (`schema.md` §3 cột 9) |
| CN-2017-LOITUC-GOP-NAM | 2017 | LOITUC | gộp | gộp | 9.64 | % | CND-2 | báo cáo năm 2017 của 零壹智库 | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-LECHPHIA | Bình quân cả năm 2017. **Không mâu thuẫn với dòng trên** — khác mốc, khác nguồn, và khớp về hướng: cuối năm thấp hơn bình quân năm |
| CN-2019-LOITUC-GOP-7THANG | 2019 | LOITUC | gộp | gộp | 10.03 | % | CND-3 | phần thống kê 1-7/2019 | 5 | có | 2026-07-26 | ◐ | C-TUCONGBO, C-GOP, C-LECHPHIA, C-GIANTIEP | Bình quân 7 tháng đầu 2019. **Cao hơn 2017** — đảo chiều so với xu hướng giảm 2015-2017; xem §5 mục 5 |

---

## 3. Đoạn 2 — 2021-2025 (chỉ mô tả theo từng nước)

> ⚠ **Không so sánh chéo giữa các nước.** Số trong bảng này lấy từ cơ quan quản lý từng
> nước, mỗi nước một định nghĩa và một cách đếm. Chỉ dùng để mô tả diễn biến nội bộ của
> chính thị trường này theo thời gian. Không đặt cạnh số của nước khác, không cộng tổng
> khu vực, không phát biểu nước nào lớn hơn nước nào. Căn cứ: quyết định **D10**,
> `target.md` §5.1.
>
> **Định nghĩa nguồn dùng ở bảng này**: số do **Tổ lãnh đạo công tác chấn chỉnh chuyên trách rủi ro
> cho vay qua mạng** (thuộc Ủy ban Giám sát Quản lý Ngân hàng và Bảo hiểm Trung Quốc — CBIRC) công bố
> tại hội nghị chuyên đề thường niên, và bởi các cơ quan quản lý tài chính địa phương. Đối tượng đếm
> **không phải nền tảng đang hoạt động** — từ 11/2020 con số đó bằng không — mà là **tổ chức đã ngừng
> hoạt động nhưng còn nghiệp vụ tồn đọng chưa thanh toán xong** (停业网贷机构存量业务尚未清零).
> Đại lượng tiền tương ứng là **số dư chưa thanh toán cho người cho vay** (未兑付余额), không phải
> dư nợ của một thị trường đang vận hành. Hai đại lượng này **không nối tiếp được** với chuỗi
> `NENTANG` và `DUNO` ở bảng đoạn 1 — chúng đo một thứ khác.

`khu_vuc` = Trung Quốc · `cap` = quốc gia · `doan` = **2**
**Một ngoại lệ**: dòng `CNSZ-2023-NENTANG-NA-VANDE` có `cap` = **dưới quốc gia** (Thâm Quyến). Mã ô mang tiền tố địa phương `CNSZ` theo `schema.md` §4.1 để con số của một thành phố không đọc nhầm thành số toàn quốc; **không cộng dòng này vào bất kỳ tổng nào**.

| ma | nam | chi_tieu | loai_nguoi_vay | mo_hinh | gia_tri | don_vi | nguon | neo | tang | tu_cong_bo | ngay_truy_cap | trang_thai | canh_bao | ghi_chu |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CN-2021-NENTANG-NA-TONDONG | 2021 | NENTANG | không áp dụng | gộp | 1169 | nền tảng | CND-8 | tường thuật hội nghị truyền hình chuyên đề 2022, 22/4/2022 | 4 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-DINHNGHIA | **Tổ chức đã ngừng hoạt động còn nghiệp vụ tồn đọng**, cuối 2021. Đầu 2021 là **1.466**, giảm 297 trong năm. **Không phải nền tảng đang hoạt động** — xem khối định nghĩa trên |
| CN-2021-TONTHAT-GOP-TIEN | 2021 | TONTHAT | gộp | gộp | 4974 | 亿 CNY | CND-10 | bài của Cục Giám sát Quản lý Tài chính địa phương Thâm Quyến dẫn số toàn quốc | 2 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-GOP | **Số dư chưa thanh toán**, cuối 2021, giảm từ **8.207** đầu năm. Mốc đầu 2021 khớp với dòng CN-2020-TONTHAT-GOP-TIEN → **hai nguồn độc lập, hai cổng chính quyền khác nhau, cùng một con số**. Đây là chỗ chắc chắn nhất của cả hồ sơ định lượng Trung Quốc |
| CN-2021-NENTANG-NA-DACLEAR | 2021 | NENTANG | không áp dụng | gộp | 3210 | nền tảng | CND-7 | tường thuật hội nghị của Tổ lãnh đạo chấn chỉnh, 27/4/2021 | 2 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-DINHNGHIA | **Đã thanh toán xong nghiệp vụ tồn đọng** tại 4/2021. Cùng nguồn: **4.676** tổ chức thuộc diện chấn chỉnh đã ngừng toàn bộ hoạt động. Mốc thời gian **giữa** hai mốc cuối-năm ở trên, không xếp vào chuỗi |
| CN-2021-TONTHAT-GOP-THUHOI | 2021 | TONTHAT | gộp | gộp | 860 | 亿 CNY | CND-7 | như trên | 2 | không | 2026-07-26 | ◐ | C-GIANTIEP, C-GOP | **Giá trị tài sản liên quan vụ án do cơ quan công an truy thu, luỹ kế** tại 4/2021. Là đại lượng **thu hồi**, đối ứng với số dư chưa thanh toán — không trừ trực tiếp cho nhau vì hai bên khác phạm vi |
| CN-2021-TONTHAT-NA-TYLE | 2021 | TONTHAT | không áp dụng | gộp | 3 | % | CND-9 | phát biểu của Tổng giám đốc một tập đoàn trong ngành, dẫn trong bài 经济参考报 | 4 | có | 2026-07-26 | ⬜ | C-TUCONGBO, C-GIANTIEP, C-DINHNGHIA | **Tỷ lệ nền tảng đã thanh toán đủ toàn bộ**, trên tổng số nền tảng đã chuyển đổi + ngừng + có vấn đề, tại 1/2021. **Là phát biểu của một bên trong ngành, không phải số của cơ quan quản lý** — mức ⬜, cần thay bằng nguồn cơ quan quản lý trước khi dùng |
| CNSZ-2023-NENTANG-NA-VANDE | 2023 | NENTANG | không áp dụng | gộp | 400 | nền tảng | CND-10 | bài của Cục Giám sát Quản lý Tài chính địa phương Thâm Quyến, 18/1/2023 | 2 | không | 2026-07-26 | ◐ | C-DINHNGHIA | **Phạm vi Thâm Quyến, không phải toàn quốc** — `cap` của dòng này thực chất là *dưới quốc gia*. Nguồn ghi "hơn 400 nền tảng" đã ngừng toàn bộ hoạt động; số dư và số người cho vay đều giảm **trên 90%**; khoảng **200** nền tảng bị khởi tố từ 2019 |
| CN-2022-TONTHAT-GOP-TIEN | 2022 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | Chưa tìm bản công bố cho các năm 2022 trở đi |
| CN-2023-TONTHAT-GOP-TIEN | 2023 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | như trên |
| CN-2024-TONTHAT-GOP-TIEN | 2024 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | như trên |
| CN-2025-TONTHAT-GOP-TIEN | 2025 | TONTHAT | gộp | gộp | `CHUA-TIM` | — | — | — | — | không | 2026-07-26 | ⬜ | — | như trên. **Đây là mốc cuối phạm vi báo cáo** (`target.md` §0.6) — ô này phải có kết quả trước Cổng G2 |

---

## 4. Hai cổng dữ liệu ngành lệch nhau tới đâu

Bảng này là hồ sơ lý do cho các ô `MAU-THUAN` ở §2, và tự nó là một phát hiện đáng viết vào chương 6.

| Chỉ tiêu, năm 2017 | 网贷之家 (CND-3) | 零壹智库 (CND-2) | Chênh |
|---|---|---|---|
| Thành giao dịch cả năm | 28.048,49 亿 | ~27.100 亿 | ~3,4% |
| Dư nợ cuối năm | 12.245,87 亿 | 12.050 亿 | ~1,6% |
| Nền tảng đang hoạt động | *(không lấy được số trực tiếp)* | 1.539 | — |
| Nền tảng luỹ kế | *(6.430 tại cuối 2018)* | 5.503 tại cuối 2017 | — |
| Nhà đầu tư hoạt động | 1.250 vạn | 1.250 vạn | **0** |
| Người vay hoạt động | 1.350 vạn | 1.350 vạn | **0** |
| Lợi suất tổng hợp | 9,45-9,54% (12/2017) | 9,64% (bình quân năm) | — |

**Hai điều đọc ra được:**

1. **Chênh lệch tập trung ở chỉ tiêu đếm nền tảng, không ở chỉ tiêu tiền.** Hai bên lệch 1,6-3,4% về
   tiền nhưng lệch rất lớn về số nền tảng. Nguyên nhân đã được chính 零壹 khai: họ chỉ đếm nền tảng có
   nghiệp vụ trên PC và không tính Hồng Kông, Đài Loan, Ma Cao. **Đây là chênh lệch định nghĩa, không
   phải chênh lệch đo lường** — và nó nói rằng mọi phát biểu "Trung Quốc có N nền tảng" đều phải kèm
   *ai đếm và đếm cái gì*.
2. **Số người tham gia thì trùng khít tuyệt đối** — 1.250 vạn và 1.350 vạn ở cả hai nguồn. Hai đơn vị
   độc lập không thể ra cùng một con số làm tròn cho một đại lượng ước lượng. **Nhiều khả năng một
   bên chép của bên kia, hoặc cả hai lấy từ một nguồn thứ ba chung.** Không được trình bày hai con số
   này như *hai nguồn xác nhận lẫn nhau* — đó đúng là sai lầm mà `target.md` §7.2 nhắm tới.

**Hệ quả cho `target.md` §3**: đoạn mô tả Trung Quốc là "case đổ vỡ toàn diện, quy mô lớn nhất lịch
sử" đứng vững về *hướng*, nhưng **mọi con số cụ thể về quy mô đỉnh đều ở tầng 5 và không có nguồn
tầng 1-2 nào chống đỡ**. Chương 6 phải mở đầu bằng ghi chú này, giống như chương 11 phải mở đầu bằng
tuyên bố giới hạn dữ liệu.

---

## 5. Ô trống — đã tìm ở đâu

Phần này là đầu vào trực tiếp của `data/coverage.md` (T2.8) và của phần thảo luận tại Cổng G2.
Ghi theo `schema.md` nguyên tắc 4: *"đã tìm, không có"* khác hẳn *"chưa tìm"*.

### 1. Thành giao dịch và dư nợ năm 2020 — `KHONG-CO`

Đã tìm ở CND-6, CND-7, CND-9, CND-10, và tìm bản báo cáo năm 2020 của cả hai cổng dữ liệu ngành.
Không nguồn nào công bố. Nguyên nhân là **cấu trúc, không phải ngẫu nhiên**: các cổng dữ liệu ngành
sống bằng chính ngành đó nên ngừng công bố khi ngành bị xoá sổ; còn cơ quan quản lý bước vào chỉ để
đo *việc rút lui*, nên chỉ công bố mức giảm và số dư chưa thanh toán.

> Đây là một dạng khoảng trống đáng chú ý về phương pháp: **đúng vào năm mà thị trường kết thúc, không
> ai đo thị trường nữa.** Điều tương tự cần kiểm ở Ấn Độ sau 8/2024 và Hàn Quốc sau 8/2020 (`schema.md`
> §11.1) — nếu lặp lại, đó là một quan sát xuyên quốc gia chứ không phải đặc thù Trung Quốc.

### 2. Số nhà đầu tư bị ảnh hưởng — `KHONG-CO`, và đây là nửa còn mở của `gaps.md` §10

Đã tìm ở: CND-4 đến CND-10; tìm riêng toàn văn phát biểu của 郭树清 (8/2020) và 刘福寿 (11/2020); tìm
theo từ khoá số người cho vay và số người bị ảnh hưởng trên các cổng chính quyền.

**Kết quả**: cơ quan quản lý **chưa từng công bố một số tuyệt đối nào**. Những gì có:

| Loại số | Giá trị | Vì sao không thay thế được |
|---|---|---|
| Mức giảm chính thức | Người cho vay **−88%** (8/2020 so đầu 2019), người vay **−73%** | Tỷ lệ **không có mẫu số**. Không suy ra số tuyệt đối |
| Nhà đầu tư hoạt động, số ngành | 1.250 vạn (2017), 1.331 vạn (2018) | Tầng 5; là *người đang tham gia*, không phải *người bị thiệt hại* |
| Ước lượng báo chí | "hơn một triệu nạn nhân" cho riêng đợt đổ vỡ 2018 | Ước lượng, không có phương pháp công bố |
| Một vụ án đơn lẻ | Ezubao: khoảng 90 vạn người, 500 亿 CNY | Chỉ một nền tảng |

**Một mảnh cần theo tiếp**: tóm tắt của công cụ tìm kiếm gán cho 郭树清 cụm *"liên quan tới vài chục
triệu người"* đi kèm con số 8.000 tỷ. **Không xác minh được** — bản CND-5 đã mở không chứa cụm đó, và
CND-4 ghi rõ là bài không nêu số người. Ghi lại ở đây đúng như tình trạng của nó: **một mảnh chưa xác
minh, không được dùng.** Cần mở bản ghi gốc của chương trình 央视新闻《相对论》 ngày 14/8/2020.

> **Đưa ra Cổng G2**: `gaps.md` §14.3 mục 10 hỏi *"Chấp nhận SQ3 chỉ trả lời định tính?"*. Nay câu hỏi
> đã sắc hơn: **giá trị chưa thu hồi đã có chuỗi ba mốc từ nguồn cơ quan quản lý; chỉ còn số người là
> trống.** Nên câu hỏi cho Cổng G2 đổi thành: *SQ3 có đứng được không nếu đo tổn thất bằng tiền mà
> không đo bằng người?* Đây là một câu hỏi khác hẳn, và dễ trả lời "có" hơn.

### 3. Nợ xấu — `KHONG-CO` ở dạng dùng được

Đã tìm ở CND-2, CND-3, CND-4, CND-11 và theo từ khoá tỷ lệ quá hạn / theo lứa vay.

Không có số theo **lứa vay** (cohort). Các cổng dữ liệu ngành công bố tỷ lệ do nền tảng tự khai — mà
`target.md` §4.1 nhóm **B2** liệt kê chính "tỷ lệ nợ xấu công bố thấp bất thường và ổn định bất thường"
là **dấu hiệu nhận biết gian lận**. Dùng chính chỉ số đó làm số liệu là tự mâu thuẫn.

Số duy nhất thấy được là tỷ lệ quá hạn **trên 99%** của vài nền tảng cụ thể trong giai đoạn thanh lý
(CND-10) — đó là số của một xác chết, không phải số của một thị trường đang vận hành. Không đưa vào
bảng.

### 4. Tỷ trọng vốn lẻ so với định chế — `KHONG-CO`, và ô này chặn một phần SQ3

Đã tìm ở CND-2, CND-3 và trong tài liệu học thuật Trung Quốc (Đại học Thanh Hoa PBCSF, Viện Nghiên cứu
Tài chính Internet ĐH Chiết Giang, các bài về chiến lược của người cho vay).

Không nguồn nào công bố tỷ trọng. **Nhưng ô trống này không đối xứng với các ô trống khác**: có lý do
cấu trúc để tin tỷ trọng vốn định chế ở Trung Quốc là rất thấp — `sources/legal/cn.md` §4 ghi nhận
Trung Quốc **không có đòn bẩy L3 nào**, tức không hề có rào cản nào với nhà đầu tư lẻ, trong khi Anh
siết chính đòn bẩy đó năm 2019.

> ⚠ **Không được biến suy luận đó thành số.** Nó là giả thuyết cần kiểm, và `schema.md` nguyên tắc 5
> cấm suy diễn trong bảng. Ghi ở đây để chương 6 biết mình đang đứng trên giả thuyết chứ không trên
> dữ liệu, khi trả lời SQ3.

### 5. Lãi suất người vay phải trả — `KHONG-CO` vì lệch khái niệm, không vì thiếu nguồn

Chỉ tiêu Trung Quốc công bố dày đặc là *综合收益率* (lợi suất tổng hợp) — **đo phía người cho vay**.
`schema.md` §5 định nghĩa `LAISUAT` là chi phí **phía người vay, đã gồm phí**. Hai đại lượng này lệch
nhau đúng bằng phần phí nền tảng thu, mà phần đó không được công bố.

**Cập nhật 2026-07-26 (T2.2a)**: `schema.md` §5 nay có mã thứ tám `LOITUC` cho đúng đại lượng này, nên
chuỗi 综合收益率 **đã vào bảng đoạn 1** — năm dòng `CN-<năm>-LOITUC-GOP-*`, mỗi dòng mang `C-LECHPHIA`.

| Mốc | Giá trị | Nguồn | Mã ô |
|---|---|---|---|
| Cả năm 2015 | 13,29% | CND-3 | `CN-2015-LOITUC-GOP-NAM` |
| Tháng 12/2015 | 12,45% | CND-3 | `CN-2015-LOITUC-GOP-T12` |
| Tháng 12/2017 | 9,45-9,54% | CND-3 | `CN-2017-LOITUC-GOP-T12` |
| Bình quân 2017 | 9,64% | CND-2 | `CN-2017-LOITUC-GOP-NAM` |
| 1-7/2019 | 10,03% | CND-3 | `CN-2019-LOITUC-GOP-7THANG` |

**Ô `LAISUAT` vẫn là `KHONG-CO`.** Việc có `LOITUC` không lấp nó — hai ô, hai kết quả nghiên cứu khác
nhau (`schema.md` §5.1 ràng buộc 2). Chuỗi này không trả lời được câu hỏi của `target.md` §5
(*"có thay thế được tín dụng đen không"*), vì câu hỏi đó hỏi về **chi phí người vay**.

Giá trị phân tích riêng của chuỗi, nay đọc được vì đã xếp thành dãy: lợi suất chào mời **giảm mạnh
2015→2017** (13,29% → 9,64%) rồi **đảo chiều tăng lại 2019** (10,03%) — đúng vào giai đoạn ngành đã
vào khủng hoảng và số nền tảng đang sụp. Lợi suất tăng khi rủi ro tăng là hành vi thị trường bình
thường; nhưng ở đây nó xảy ra sau ba năm nền tảng cạnh tranh bằng cách **hạ lợi suất trong lúc rủi ro
tích tụ** — hình thái mà `target.md` §4.1 nhóm **B1** mô tả (ngôn ngữ "an toàn", lợi suất cố định).

> ⚠ Đây là **quan sát trên năm điểm dữ liệu tầng 5, hai nguồn**, không phải một chuỗi đầy đủ. Ghi ở
> đây làm giả thuyết cho chương 6 kiểm lại, không dùng như phát hiện đã xác lập.

---

## 6. Việc phát sinh từ lần thu thập này

| # | Việc | Đi đâu |
|---|---|---|
| 1 | ~~Hai sửa đổi lược đồ, làm một lượt.~~ ✅ **Xong 2026-07-26 (T2.2a).** (a) Mã `LOITUC` + §5.1 + `C-LECHPHIA` + kiểm 12 → chuỗi 综合收益率 đã vào bảng. (b) Ngoại lệ kiểm 4 chốt ở `schema.md` §12.1: dòng mang mã trạng thái không cần `C-GOP`; `loai_nguoi_vay` trên dòng rỗng đọc là *chiều đã đi tìm*. Phát sinh thêm khi đối chiếu: (c) đoạn biến thể §7.1 — **15 mã ô của file này đã đổi**; (d) `cap = dưới quốc gia` cho dòng Thâm Quyến | ✅ `schema.md` §3, §4.1, §5, §5.1, §7.1, §9, §12, §12.1 |
| 1b | **Backfill `C-GIANTIEP` cho các dòng cũ dẫn số WDZJ qua CND-3.** §1 nói rõ mọi số WDZJ là trích gián tiếp vì `wdzj.com` không truy cập được, nhưng các dòng `NENTANG`/`GIAINGAN`/`DUNO` lập ở vòng đầu chưa mang mã này — chỉ các dòng `LOITUC` thêm hôm nay có. Không sửa vội để tránh lẫn với đợt đổi mã; làm thành một lượt riêng | T2.2 vòng hai |
| 2 | Nâng mức CND-2 → CND-11 lên ✅, hoặc thay bằng nguồn tầng 1-2 tương đương. **Không dòng nào của file này được trích sang `content/` trước khi làm việc này** (`schema.md` §12 kiểm 10) | Trước P3 |
| 3 | Tìm bản ghi gốc 央视新闻《相对论》 14/8/2020 — để xác minh hoặc loại bỏ mảnh "vài chục triệu người" ở §5 mục 2 | T2.2 vòng hai |
| 4 | Tìm bản công bố của Tổ lãnh đạo chấn chỉnh cho **2022-2025**. Bốn ô `CHUA-TIM` ở bảng đoạn 2 phải có kết quả trước Cổng G2 — trong đó **2025 là mốc cuối phạm vi** | Trước Cổng G2 |
| 5 | Hợp nhất `CND-*` vào `sources.md` §5 (hiện chỉ có danh sách đầu báo, chưa có danh mục bài) | Khi cập nhật `sources.md` |
| 6 | `sources.md` §1.1 chưa ghi việc **`wdzj.com` không truy cập được** ngày 2026-07-26. Đây là rào cản cùng loại với `gaps.md` §3 và nặng hơn: nó là nguồn gốc của phần lớn chuỗi số đỉnh, và mọi số WDZJ hiện có đều là **trích gián tiếp** | Ghi vào `gaps.md` §3 |
| 7 | Cập nhật `gaps.md` §10: nửa "giá trị chưa thu hồi" **đã đóng**, nửa "số nhà đầu tư" vẫn mở. Câu hỏi cho Cổng G2 đổi dạng — xem §5 mục 2 | Cập nhật `gaps.md` |
| 8 | `sources/legal/cn.md` §5 việc 7 (*tìm số dư chưa thu hồi và số nhà đầu tư bị ảnh hưởng*) nay **xong một nửa** | Cập nhật `legal/cn.md` |

---

## 7. Kiểm trước khi đóng file (`schema.md` §12)

| # | Kiểm | Kết quả |
|---|---|---|
| 1 | Đủ 17 cột bắt buộc, không ô trắng | ✅ 14 cột bắt buộc nằm trong bảng theo mẫu §10.1; 3 cột còn lại (`khu_vuc`, `cap`, `doan`) là **hằng số của cả bảng**, khai ở dòng ngay trên mỗi bảng. Không ô nào để trắng — ô chưa biết mang mã §6 |
| 2 | `doan` đúng, không bảng nào trộn hai đoạn | ✅ |
| 3 | Bảng đoạn 2 có đủ khối cảnh báo **và** dòng định nghĩa nguồn | ✅ — dòng định nghĩa nêu rõ đối tượng đếm đổi hẳn sau 11/2020 |
| 4 | Mọi dòng `loai_nguoi_vay = gộp` **có số** mang `C-GOP` | ✅ — ngoại lệ đã được `schema.md` §12.1 chốt ngày 2026-07-26: dòng mang mã trạng thái được miễn. Xem ghi chú dưới bảng |
| 5 | Mọi dòng tầng 5 có `tu_cong_bo = có` và `C-TUCONGBO` | ✅ — 14/14 dòng tầng 5 |
| 6 | Mọi dòng `KHONG-CO` ghi rõ đã tìm ở đâu | ✅ — 6/6 dòng, chi tiết ở §5 |
| 7 | Mọi dòng `MAU-THUAN` liệt kê đủ giá trị và nguồn | ✅ — 5/5 dòng, không dòng nào tự chọn một con số |
| 8 | Neo trang PDF là số trang in | ✅ không áp dụng — file này không có nguồn PDF nào |
| 9 | Không mã ô trùng với file dữ liệu khác | ✅ — `data/` hiện chỉ có file này |
| 10 | Không dòng `◐`/`⬜` bị trích sang `content/` | ✅ — `content/` chưa tồn tại. **Mọi dòng của file này đều ◐ hoặc ⬜**, nên hiện không dòng nào đủ điều kiện trích. Ghi thành việc 2 ở §6 |

> **Ngoại lệ ở kiểm 4 — đã chốt ngày 2026-07-26 tại `schema.md` §12.1.** Các dòng mang
> `loai_nguoi_vay = gộp` nhưng `gia_tri` là mã trạng thái (`KHONG-CO` / `CHUA-TIM`) để `canh_bao`
> trống là **đúng**, không phải thiếu sót. Mã cảnh báo theo `schema.md` §9 là *cảnh báo đi theo một
> con số*; dòng không có số thì không có gì để đi theo, và gắn `C-GOP` vào ô rỗng sẽ tạo ấn tượng sai
> rằng có một số gộp tồn tại.
>
> Kèm theo là cách đọc cột `loai_nguoi_vay`: trên dòng có số nó là *chiều của con số*, trên dòng mang
> mã trạng thái nó là *chiều đã đi tìm*. Cách đọc này giữ nguyên giá trị nghiên cứu của ô trống —
> `KHONG-CO` ở chiều `gộp` là phát biểu **mạnh hơn** `KHONG-CO` ở một chiều hẹp, vì nó nói nguồn không
> công bố gì kể cả ở mức thô nhất. Phương án đọc `gộp` là giá trị sai trên dòng rỗng **đã cân nhắc và
> loại** (lý do đầy đủ ở `schema.md` §12.1).

> **Đợt đổi mã ô ngày 2026-07-26 (T2.2a).** 15 mã ô của file này đã đổi để khớp `schema.md` §7.1.
> Lỗi cũ: biến thể (`LUYKE`, `VANDE`, `NDT`, `GIAM`, `CUOI`, `TONDONG`, `DACLEAR`, `THUHOI`, `TYLE`,
> `TP`) bị đặt vào đúng vị trí dành cho `loai_nguoi_vay`, khiến chiều bắt buộc theo nguyên tắc 2 biến
> mất khỏi mã. Hệ quả nguy hiểm nhất nếu để nguyên: `CN-2020-NENTANG-NA` (15 nền tảng, cuối 8/2020) và
> `CN-2020-NENTANG-CUOI` (0 nền tảng, giữa 11/2020) là **hai mốc của cùng một đại lượng trong cùng một
> năm** — quy tắc "trùng mã ⇒ gộp thành `MAU-THUAN`" của §7 sẽ biến chúng thành một mâu thuẫn giả,
> trong khi thật ra chúng là chuỗi sụp đổ trong ba tháng. Nay là `…-NA-HOATDONG-T8` và
> `…-NA-HOATDONG-T11`. **Không con số nào thay đổi trong đợt này.**
>
> **Hai dòng đổi `loai_nguoi_vay`, phát hiện khi chạy kiểm 4 bằng máy.** `CN-2020-TONTHAT-*-GIAM`
> (mức giảm số người cho vay −88%) và `CN-2021-TONTHAT-*-TYLE` (tỷ lệ nền tảng đã thanh toán đủ) trước
> ghi `gộp`. Cả hai **không có chiều người vay**: một cái đếm *người cho vay*, một cái lấy mẫu số là
> *nền tảng*. Theo `schema.md` §4.3 đó là `không áp dụng`, nên mã đổi thành `…-NA-GIAM` và `…-NA-TYLE`.
> Ghi `gộp` cho chúng là nói rằng tồn tại một phép tách theo loại người vay mà nguồn không làm — trong
> khi thật ra phép tách đó **không tồn tại về mặt khái niệm**. Giá trị không đổi.

---

## 8. Nhật ký

| Ngày | Đã thêm | Nguồn mới mở |
|---|---|---|
| 2026-07-26 | **T2.2a — sửa lược đồ và đưa file về khớp lược đồ.** Thêm **5 dòng `LOITUC`** (chuỗi 综合收益率 2015-2019, trước nay nằm ngoài bảng vì chưa có mã) → **41 dòng**. Đổi **15 mã ô** theo `schema.md` §7.1 đoạn biến thể; **không con số nào thay đổi**. Đóng ngoại lệ kiểm 4 theo `schema.md` §12.1. Dòng Thâm Quyến đổi tiền tố thành `CNSZ` (`cap` = dưới quốc gia) | không mở nguồn mới |
| 2026-07-26 | Lập file. **36 dòng dữ liệu**: 26 dòng đoạn 1, 10 dòng đoạn 2. Trong đó 15 ô có giá trị số ở đoạn 1 và 6 ô ở đoạn 2; 5 ô `MAU-THUAN`, 6 ô `KHONG-CO`, 4 ô `CHUA-TIM`. **Đóng được nửa "giá trị chưa thu hồi" của `gaps.md` §10** với chuỗi ba mốc từ nguồn cơ quan quản lý; xác nhận nửa "số nhà đầu tư" là `KHONG-CO` chứ không phải chưa tìm | CND-2 → CND-11 (10 nguồn). `wdzj.com` **không truy cập được** — mọi số WDZJ là trích gián tiếp |
