# Văn bản pháp quy — Nhật Bản

> **Hiện vật của T1.3j**. Ngày rà soát: 2026-07-26.
> Trọng tâm ghi ở `plan.md`: **đăng ký kép**; quy định che danh tính người vay và hệ quả.
> **Mức độ hoàn thành: trung bình.** Cơ chế đăng ký kép đã xác định được. **Vấn đề che danh tính người vay đã được giải quyết ở vòng rà soát thứ hai — xem §1.2.** Kết quả: mô tả trong `target.md` §3 cần được sửa lại.

---

## 0. Vai trò trong lập luận

Nhật Bản là case Tầng 3, và có mặt vì **một đặc điểm thể chế không lặp lại ở đâu khác**: quy định giám sát khiến nhà đầu tư **không được biết người vay là ai**. `target.md` §3 mô tả là *"giấu danh tính người vay → hệ quả"*.

Nếu xác nhận được, đây là một dữ kiện có sức nặng lý thuyết lớn hơn quy mô thị trường Nhật rất nhiều:

> Một chế độ điều tiết áp **minh bạch tối đa với cơ quan quản lý** (đăng ký kép, hai bộ nghĩa vụ) nhưng lại **cấm minh bạch với nhà đầu tư** về danh tính tài sản cơ sở. Nếu đó thực sự là hệ quả của quy định, thì Nhật Bản là bằng chứng cho một luận điểm quan trọng ở chương 10: **các đòn bẩy điều tiết có thể xung đột với nhau**, và một chế độ đầy đủ trên giấy vẫn có thể tạo ra một sản phẩm mà nhà đầu tư không thể thẩm định.

**Cảnh báo**: đoạn trên là *giả thuyết đã được viết vào `target.md` trước khi có dữ liệu*, không phải phát hiện. Rà soát vòng đầu chưa xác nhận được.

---

## 1. Khung pháp lý — đăng ký kép

| # | Văn bản | Cơ quan | Nghĩa vụ | TT |
|---|---|---|---|---|
| JP-1 | *Money Lending Business Act* (貸金業法) | Financial Services Agency (FSA) / cơ quan cấp tỉnh | Bên vận hành phải **đăng ký làm tổ chức cho vay tiền** | ◐ |
| JP-2 | *Financial Instruments and Exchange Act* (金融商品取引法 — FIEA) | FSA | Bên vận hành phải **đăng ký làm tổ chức kinh doanh công cụ tài chính**; phần vốn của nhà đầu tư thường được coi là **quyền lợi trong chương trình đầu tư tập thể** | ◐ |
| JP-3 | *Cabinet Office Ordinance Concerning Partial Revision of Regulation for Enforcement of the Money Lending Business Act* | FSA | Sửa đổi quy chế thi hành, công bố 1/4/2020 — **nội dung liên quan P2P chưa xác minh** | ⬜ |

**Đường dẫn:** FSA (tiếng Anh) — `https://www.fsa.go.jp/en/laws_regulations/index.html` · JP-3 — `https://www.fsa.go.jp/en/news/2020/20200401_lending.html`

**TT chung: ◐** — cơ chế đăng ký kép được nhiều nguồn tư vấn pháp lý độc lập mô tả thống nhất. **Chưa mở văn bản gốc nào.**

### 1.1. Cấu trúc thực tế của thị trường Nhật

Theo mô tả (◐, cần xác minh): cho vay qua sàn ở Nhật thường dùng cấu trúc **hợp danh ẩn danh** (匿名組合 — *tokumei kumiai*, "TK partnership"):

```
Nhà đầu tư → góp vốn vào hợp danh ẩn danh
                    ↓
    Bên vận hành (đăng ký kép: cho vay tiền + công cụ tài chính)
                    ↓
    Cho doanh nghiệp hoặc cá nhân vay
                    ↓
    Phân phối lợi tức ngược về nhà đầu tư
```

> **Đây không phải mô hình ngang hàng theo nghĩa gốc.** Nhà đầu tư không có quan hệ hợp đồng với người vay; họ là **thành viên góp vốn ẩn danh trong một hợp danh** mà bên vận hành mới là bên cho vay. Về mặt phân loại theo `target.md` §2.1, đây gần với **balance-sheet lending được cấp vốn bởi nhà đầu tư bên ngoài** hơn là marketplace thuần.
>
Giả thuyết đặt ra ở vòng rà soát thứ nhất — rằng việc che danh tính là **hệ quả cấu trúc** chứ không phải một quy định cấm — đã được vòng thứ hai xác nhận. Xem §1.2.

---

## 1.2. Vấn đề che danh tính người vay — đã giải quyết

**Đây là câu hỏi trọng tâm của T1.3j, và câu trả lời khác với mô tả trong `target.md` §3.**

| Trường | Nội dung |
|---|---|
| **Thực hành cũ** | 匿名化・複数化 — *ẩn danh hoá và đa số hoá* người vay. Nhà đầu tư không được biết tên và địa chỉ bên vay, và khoản vay được trình bày như cho nhiều bên vay |
| **Lý do tồn tại** | **Không phải để giấu thông tin.** Đó là biện pháp để **tránh việc nhà đầu tư bị coi là người ra quyết định cho vay** — vì nếu bị coi như vậy, từng nhà đầu tư sẽ phải **đăng ký kinh doanh cho vay tiền** theo *Money Lending Business Act*, điều bất khả thi trên thực tế |
| **Thời điểm gỡ bỏ** | **18/3/2019** — Cơ quan Dịch vụ Tài chính (FSA) trả lời qua **thủ tục xác nhận trước về áp dụng pháp luật** (法令適用事前確認手続, tương đương thư không-hành-động): nếu áp dụng một số biện pháp nhất định, nhà đầu tư **không** được coi là người ra quyết định cho vay — do đó **không còn cần ẩn danh hoá** |
| **Hệ quả** | Tên và địa chỉ bên vay về nguyên tắc được công bố; nhà đầu tư đánh giá được rủi ro bên vay trước khi quyết định |
| **Triển khai thực tế** | SBI Social Lending công bố bắt đầu công khai thông tin bên vay ngày **16/5/2019** |
| **TT** | ◐ — nhất quán qua nhiều nguồn tiếng Nhật độc lập gồm thông cáo doanh nghiệp và tài liệu của Ủy ban Pháp luật Tài chính. **Chưa mở văn bản trả lời gốc của FSA** |

**Nguồn:**
- 金融法委員会 (Ủy ban Pháp luật Tài chính), *貸付型クラウドファンディングにおける貸金業法の適用について* (Về việc áp dụng Luật kinh doanh cho vay tiền đối với gọi vốn cộng đồng dạng cho vay), 17/9/2019 — `https://www.flb.gr.jp/jdoc/publication56-j.pdf`
- 日本貸金業協会 · 第二種金融商品取引業協会, *貸付型ファンドに関するQ&A 【第二版】*, 1/11/2024 — `https://www.t2fifa.or.jp/wp-content/themes/base/assets/docs/info20230804.pdf`
- SBIホールディングス, thông cáo 16/5/2019 — `https://www.sbigroup.co.jp/news/2019/0516_11544.html` (**tự công bố — tầng 5**)

> ### Vì sao phát hiện này quan trọng hơn quy mô thị trường Nhật Bản
>
> `target.md` §3 mô tả Nhật là *"giấu danh tính người vay → hệ quả"*, ngụ ý một quy định che giấu thông tin. **Cơ chế thật khác hẳn, và thú vị hơn nhiều:**
>
> Việc che danh tính **không do ai muốn**. Nó là sản phẩm phụ của việc **định danh pháp lý ở tầng người tham gia**: luật cho vay tiền Nhật yêu cầu *người ra quyết định cho vay* phải đăng ký. Để nhà đầu tư không rơi vào định nghĩa đó, ngành buộc phải khiến nhà đầu tư *không biết mình đang cho ai vay* — tức **cố tình tạo ra sự mù thông tin để tránh một nghĩa vụ đăng ký**.
>
> Kết quả là một nghịch lý điều tiết hoàn hảo: **một quy định nhằm bảo vệ (đăng ký người cho vay) đã trực tiếp sinh ra một sản phẩm mà nhà đầu tư không thể thẩm định.** Đòn bẩy L1 đặt sai tầng đã vô hiệu hoá đòn bẩy L6.
>
> **Bài học chuyển giao cho Việt Nam, rất cụ thể**: khi định danh pháp lý, phải hỏi *định danh này áp lên ai* — lên nền tảng, hay lên người tham gia? Nếu áp lên nhà đầu tư, thị trường sẽ tự tổ chức lại để nhà đầu tư không rơi vào định nghĩa, và **cách rẻ nhất để làm điều đó gần như luôn là giảm thông tin họ có**. Đây là một dạng hệ quả ngoài ý muốn mà không khu vực nào khác trong khảo sát thể hiện rõ như vậy, và xứng đáng một mục riêng ở chương 10.
>
> **Việc phải làm**: sửa `target.md` §3 và ghi vào `plan.md` §5. Mô tả hiện tại đọc sai cơ chế.

---

## 2. Ánh xạ sáu đòn bẩy — Nhật Bản

| Đòn bẩy | Trạng thái | TT |
|---|---|---|
| **L1** | **Đăng ký kép** — hai chế độ song song. Nặng nhất trong khảo sát về số lượng giấy phép. Điểm mấu chốt: nghĩa vụ đăng ký cho vay tiền **có thể chạm tới cả nhà đầu tư**, và chính điều đó tạo ra vấn đề ở §1.2 | ◐ |
| **L2** | Chưa biết — nghĩa vụ đến từ hai luật, cần tách ra | ⬜ |
| **L3** | Chưa biết | ⬜ |
| **L4** | Nhật có trần lãi suất theo *Interest Rate Restriction Act* — **cần xác minh** có áp cho khoản vay qua sàn không | ⬜ |
| **L6** | **Trước 3/2019: bị vô hiệu hoá** bởi thực hành ẩn danh hoá. **Sau 3/2019: khôi phục** — công bố danh tính bên vay | ◐ |
| **L5** | Chưa biết | ⬜ |

---

## 3. Việc còn phải làm

| # | Việc | Ưu tiên |
|---|---|---|
| 1 | Mở văn bản trả lời gốc của FSA ngày 18/3/2019 — xác minh "một số biện pháp nhất định" là những biện pháp gì | **Cao nhất** |
| 2 | **Sửa `target.md` §3** cho khớp cơ chế thật, ghi vào `plan.md` §5 | **Cao nhất** |
| 3 | Đọc *貸付型ファンドに関するQ&A 第二版* (11/2024) — bản hướng dẫn ngành hiện hành | Cao |
| 4 | Xác minh nội dung JP-3 (sửa đổi quy chế thi hành 2020) liên quan gì tới P2P | Trung bình |
| 5 | Các vụ xử phạt của FSA đối với nền tảng cho vay qua sàn | Trung bình — dấu vết thực thi tốt nhất |
| 6 | Quy mô thị trường theo năm, đặc biệt trước/sau 3/2019 | Trung bình — đo tác động của việc gỡ ẩn danh |

---

## 4. Nhật ký cập nhật

| Ngày | Thay đổi |
|---|---|
| 2026-07-26 | Lập file; đăng ký kép ở mức ◐; nêu giả thuyết thay thế cho vấn đề che danh tính |
| 2026-07-26 (vòng 2) | **Giải quyết vấn đề che danh tính** — xác nhận là hệ quả cấu trúc của nghĩa vụ đăng ký, gỡ bỏ 18/3/2019. `target.md` §3 cần sửa |
