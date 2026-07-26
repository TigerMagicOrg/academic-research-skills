# Mục tiêu nghiên cứu: Mô hình P2P Lending trên thế giới — bài học thể chế cho Việt Nam

| Trường | Nội dung |
|---|---|
| **Trạng thái** | **v0.2** — đã chỉnh sau rà soát P1 |
| **Ngày lập** | 2026-07-26 |
| **Sửa lần cuối** | 2026-07-26 — bốn thay đổi, xem §12 |
| **Loại đầu ra** | Báo cáo chính sách / pháp lý |
| **Quy mô** | Sâu — ~50-80 trang, mục tiêu 100+ nguồn |
| **Ngôn ngữ** | Tiếng Việt (thuật ngữ gốc kèm trong ngoặc) |
| **Đích đến** | Việt Nam — có chương riêng |
| **Độc giả** | Tài liệu tham chiếu chung — không nhắm một cơ quan hay doanh nghiệp cụ thể |

---

## 0. Bảy quyết định đã chốt

1. **Lĩnh vực**: chính sách/pháp lý — trọng tâm phân tích là *trục điều tiết*, không dừng ở mô tả hiện tượng.
2. **Thể loại**: **tài liệu tham chiếu chung**, không nhắm một độc giả cụ thể. Đây là tài liệu *lập bản đồ*, không phải tài liệu *vận động*: nó trình bày không gian lựa chọn và đánh đổi, không chốt một khuyến nghị duy nhất. Xem chuẩn mực ở §7.4.
3. **Việt Nam**: là đích đến của toàn bộ bài học quốc tế, có chương riêng.
4. **"Châu Âu đang phát triển"** = Baltic + Đông Âu (Estonia, Latvia, Lithuania, Ba Lan).
5. **Độ sâu**: báo cáo lớn nhiều phần, mỗi khu vực một chương, Trung Quốc là chương dài nhất.
6. **Mốc kết thúc phạm vi**: **hết năm 2025**. Diễn biến năm 2026 chỉ đưa vào khi có nguồn chắc chắn, và phải được đánh dấu rõ là "sau mốc phạm vi" để người đọc biết phần đó chưa được rà soát đồng đều như phần chính.
7. **Tách cho vay tiêu dùng và cho vay doanh nghiệp nhỏ**: đây là **trục cắt ngang toàn báo cáo**, không phải một chương phụ. Xem §2.1 trục 5 và §6 chương 8.

---

## 1. Câu hỏi nghiên cứu

### 1.1. Câu hỏi tổng (RQ)

> **Điều kiện thể chế nào quyết định P2P lending trở thành một kênh tín dụng bổ sung bền vững, thay vì thành kênh huy động vốn trá hình quy mô lớn — và không gian lựa chọn thể chế của Việt Nam gồm những phương án nào, mỗi phương án đánh đổi cái gì lấy cái gì?**

Điểm mấu chốt của cách đặt câu hỏi này: nó coi *kết cục* của P2P ở mỗi nước là **biến phụ thuộc**, còn thiết kế thể chế là **biến độc lập**. Nếu chỉ kể lại lịch sử theo trình tự thời gian, báo cáo sẽ không trả lời được câu hỏi chính sách nào cả.

### 1.2. Câu hỏi thành phần (sub-RQ)

| # | Câu hỏi | Vì sao quan trọng |
|---|---|---|
| **SQ1** | P2P được định danh pháp lý là gì ở mỗi nước — trung gian thông tin, trung gian tín dụng, hay tổ chức phát hành chứng khoán — và định danh đó dẫn tới hệ quả gì? | Đây là biến giải thích mạnh nhất. Định danh sai một lần thì mọi quy định sau đó đều lệch. |
| **SQ2** | Cơ chế "bảo lãnh vốn" (dù ngầm hay công khai) xuất hiện ở đâu, và tại sao nó gần như luôn là điểm khởi đầu của đổ vỡ? | Là ranh giới giữa marketplace và shadow bank. Trọng tâm của toàn bộ phần "biến tướng". |
| **SQ3** | Nguồn vốn đến từ nhà đầu tư cá nhân hay định chế, và sự khác biệt đó tác động thế nào tới rủi ro ổn định xã hội? | Giải thích tại sao TQ thành khủng hoảng xã hội còn UK chỉ là ngành co lại. |
| **SQ4** | Điều tiết đến *sớm* hay *muộn* so với đỉnh tăng trưởng thì kết quả khác nhau ra sao? | Trục so sánh: Mỹ (2008, sớm nhất) — Anh (2014) — Trung Quốc/Indonesia (2015-2016, sau khi thị trường đã lớn). **Vị trí của Singapore và New Zealand trên trục này chưa có bằng chứng** — phải xác định ở P2 trước khi dùng, xem sửa v0.2 ở §2.3. |
| **SQ5** | Vì sao P2P bán lẻ suy tàn ngay cả ở những thị trường **không** có đổ vỡ (Anh, Mỹ)? | Câu hỏi khó chịu nhất và bị bỏ qua nhiều nhất: có thể mô hình này vốn không có lợi thế kinh tế bền vững, chứ không chỉ là chuyện quản lý kém. |
| **SQ6** | Sau đợt siết ở Trung Quốc, dòng vốn và nhân sự vận hành đã dịch chuyển sang đâu, và để lại hệ quả gì ở nước tiếp nhận? | Đây là kênh lây lan trực tiếp đến Việt Nam, Indonesia, Ấn Độ. Là mắt xích nối chương TQ với chương VN. |
| **SQ7** | Cho vay tiêu dùng và cho vay doanh nghiệp nhỏ khác nhau ra sao về logic kinh tế, cấu trúc rủi ro và hệ quả điều tiết? | Gộp hai loại này là sai lầm phân tích phổ biến nhất trong tài liệu về P2P. Cho vay doanh nghiệp là mảng duy nhất còn sống khoẻ ở châu Âu, và khung pháp lý EU chỉ điều chỉnh đúng mảng này. Xem §2.1 trục 5. |
| **SQ8** | Với ràng buộc thực tế của Việt Nam (dân trí tài chính, tín dụng đen, năng lực giám sát, hạ tầng dữ liệu tín dụng), những phương án thể chế nào là khả thi và mỗi phương án đánh đổi cái gì? | Câu hỏi đích. Trình bày dưới dạng bản đồ lựa chọn có đánh đổi, không chốt một khuyến nghị duy nhất (§7.4). |

---

## 2. Khung phân tích

Ba khung dưới đây là công cụ để đọc mọi case, và cũng là bộ khung bảng biểu xuyên suốt báo cáo.

### 2.1. Khung A — Phân loại mô hình (taxonomy)

Không có "một mô hình P2P". Cần phân loại theo bốn trục độc lập; hầu hết tranh cãi chính sách bắt nguồn từ việc gộp các loại rất khác nhau vào một tên gọi:

| Trục | Các giá trị | Ý nghĩa rủi ro |
|---|---|---|
| **Ai chịu rủi ro tín dụng** | Nhà đầu tư ↔ nền tảng ↔ bên bảo lãnh thứ ba ↔ tổ chức khởi tạo khoản vay (loan originator) | Trục quan trọng nhất. Nền tảng chịu rủi ro = ngân hàng không giấy phép. |
| **Bảng cân đối** | Marketplace thuần ↔ balance-sheet lending ↔ lai (đồng tài trợ) | Quyết định yêu cầu vốn nên áp hay không. |
| **Nguồn vốn** | Nhà đầu tư lẻ ↔ định chế ↔ hỗn hợp | Quyết định mức độ rủi ro chính trị - xã hội. |
| **Quan hệ với ngân hàng** | Độc lập ↔ ngân hàng đối tác khởi tạo khoản vay ↔ nền tảng tự trở thành ngân hàng | Con đường thoát của mô hình Mỹ và Anh. |
| **Loại người vay** | Cá nhân tiêu dùng ↔ hộ kinh doanh ↔ doanh nghiệp nhỏ ↔ bất động sản/dự án | **Trục cắt ngang toàn báo cáo.** Bốn loại này khác nhau về nguồn trả nợ, khả năng thẩm định, mức bảo vệ pháp lý người vay và mức độ tổn thương xã hội — nên phải chịu chế độ điều tiết khác nhau. Xem §2.4. |

Bốn "biến thể lai" cần gọi tên riêng vì chúng không phải P2P theo nghĩa gốc nhưng luôn bị xếp chung:
- **Mô hình ngân hàng đối tác** (Mỹ): ngân hàng cấp phép đứng tên khoản vay, nền tảng mua lại — thực chất là chênh lệch quy chế pháp lý, không phải "ngang hàng".
- **Marketplace của các tổ chức khởi tạo** (Baltic, điển hình Mintos): nhà đầu tư mua phần khoản vay do một công ty tài chính khác đã cấp; kèm "cam kết mua lại" (buyback). Rủi ro chuyển từ *người vay* sang *công ty tài chính trung gian* — nhà đầu tư thường không nhận ra sự dịch chuyển này.
- **Bảo lãnh gốc** (Trung Quốc): nền tảng cam kết hoàn vốn → sản phẩm được cảm nhận như tiền gửi.
- **Tín dụng nhúng** (embedded lending, sau 2020): hình hài hiện tại của phần lớn thị trường — P2P như một lớp cấp vốn phía sau, không còn giao diện "ngang hàng" nào.

### 2.2. Khung B — Sáu đòn bẩy điều tiết

Mọi nước đều chỉ có sáu công cụ; khác biệt nằm ở việc dùng công cụ nào, đến mức nào, và vào lúc nào. Đây sẽ là bảng so sánh xuyên quốc gia trung tâm của báo cáo:

| # | Đòn bẩy | Ví dụ hình thái |
|---|---|---|
| L1 | **Định danh & cấp phép** | Trung gian thông tin (TQ) / hoạt động đầu tư (Anh, Latvia) / chứng khoán (Mỹ) / luật chuyên biệt (Hàn Quốc) |
| L2 | **Yêu cầu vốn & tách bạch tiền khách hàng** | Vốn pháp định tối thiểu; bắt buộc ngân hàng giữ hộ tiền (custody) |
| L3 | **Giới hạn nhà đầu tư** | Trần % tài sản; trần tuyệt đối; kiểm tra hiểu biết; thời gian suy nghĩ |
| L4 | **Giới hạn người vay** | Trần dư nợ trên một nền tảng / toàn hệ thống; trần lãi suất; kiểm tra khả năng trả nợ |
| L5 | **Cấm nâng cấp tín dụng (credit enhancement)** | Cấm bảo lãnh, cấm quỹ dự phòng, cấm gộp quỹ |
| L6 | **Minh bạch & hạ tầng** | Công bố nợ xấu theo lứa vay, báo cáo lên trung tâm tín dụng, kế hoạch giải thể có trật tự (wind-down) |

### 2.3. Khung C — Vòng đời năm giai đoạn

Một mẫu hình lặp lại gần như y hệt ở mọi thị trường. Dùng khung này để định vị *hiện tại* Việt Nam đang ở đâu:

```
G1 Khoảng trống         → G2 Tăng trưởng bùng nổ  → G3 Biến chất
   (chưa có quy định)       (không kiểm soát)         (bảo lãnh, gộp quỹ, dự án giả)
                                                          ↓
G5 Tái định hình        ← G4 Đổ vỡ & can thiệp     ←──────┘
   (thành ngân hàng /       (siết, thanh lý)
    vốn định chế /
    tín dụng nhúng)
```

**Giả thuyết trung tâm cần kiểm chứng**: các nước can thiệp **sớm trong G2** kết thúc bằng một ngành nhỏ nhưng có trật tự; các nước can thiệp ở G3-G4 (Trung Quốc, Indonesia) trả giá bằng đổ vỡ xã hội. Việt Nam hiện được đặt giả định ở **cuối G2 / đầu G3** — cần kiểm chứng bằng dữ liệu.

> **Sửa v0.2 (2026-07-26) — rút giả thuyết can thiệp ở G1.** Bản v0.1 nêu Singapore và New Zealand can thiệp ở **G1**, tức trước khi thị trường hình thành. Rà soát P1 (`notes/timeline.md` §2.1) cho thấy **không khu vực pháp lý nào trong khảo sát làm được điều đó**: khoảng cách giữa nền tảng đầu tiên và văn bản điều tiết đầu tiên, ở mọi nước, tính bằng năm. Ngay cả Mỹ — can thiệp sớm nhất, 2008 — cũng là *hành động cưỡng chế sau khi đã bán 27 triệu USD giấy nợ chưa đăng ký*, không phải quy định phòng ngừa.
>
> Hệ quả cho SQ4: **không có phương án "điều tiết trước khi có thị trường"**. Mọi lựa chọn thực tế nằm trong khoảng G2-G4, và câu hỏi đúng là *sớm hay muộn trong G2*, không phải *G1 hay G3*. Đây là một thu hẹp phạm vi lựa chọn có ý nghĩa trực tiếp với chương 11: Việt Nam không thể học một mô hình chưa ai làm được.
>
> Vị trí của Singapore và New Zealand trên trục thời điểm **vẫn chưa có bằng chứng** — xem sửa ở §3 và `sources/gaps.md` §8.

### 2.4. Quy tắc tách hai thị trường

**Cho vay tiêu dùng và cho vay doanh nghiệp nhỏ là hai thị trường khác nhau đội chung một cái tên.** Gộp chúng lại là lỗi phân tích phổ biến nhất trong tài liệu về P2P, và là lỗi có hậu quả trực tiếp: nó dẫn tới đề xuất một chế độ điều tiết duy nhất cho hai thứ cần chế độ khác nhau.

| Chiều | Cho vay tiêu dùng | Cho vay doanh nghiệp nhỏ |
|---|---|---|
| Nguồn trả nợ | Thu nhập cá nhân — khó xác minh, dễ tổn thương trước cú sốc | Dòng tiền kinh doanh — có chứng từ, thẩm định được |
| Cơ sở thẩm định | Chấm điểm thống kê trên số lớn | Thẩm định từng hồ sơ, có tài sản bảo đảm |
| Kích thước khoản vay | Nhỏ, số lượng rất lớn | Lớn hơn nhiều, số lượng ít |
| Bảo vệ pháp lý người vay | Luật bảo vệ người tiêu dùng áp dụng đầy đủ | Giả định là bên có hiểu biết, mức bảo vệ thấp hơn |
| Hình thái lạm dụng đặc trưng | Bóc lột người vay: lãi cắt cổ, thu hồi nợ bạo lực | Rủi ro phía nhà đầu tư: thẩm định kém, dự án ảo |
| Tình trạng hiện nay | Gần như đã rút khỏi mô hình ngang hàng ở mọi thị trường trưởng thành | Mảng duy nhất còn hoạt động thực chất ở châu Âu |
| Vị trí trong khung EU | **Không thuộc phạm vi điều chỉnh** của quy chế gọi vốn cộng đồng toàn khối | Thuộc phạm vi điều chỉnh |

**Hệ quả bắt buộc đối với báo cáo:**

- Mọi bảng số liệu ở §5 phải tách hai loại. Nếu nguồn không tách được, phải ghi rõ là số gộp — không được lặng lẽ dùng như số của một loại.
- Mọi phát biểu về "P2P" trong phần kết luận phải nói rõ đang nói về loại nào.
- Chương 8 dành riêng cho việc đối chiếu hai thị trường này xuyên quốc gia.
- Riêng **cho vay bất động sản/dự án** tuy về hình thức thuộc nhóm doanh nghiệp nhưng có hồ sơ rủi ro riêng (tập trung, lệch kỳ hạn nặng) và là nguyên nhân trực tiếp của nhiều vụ đổ vỡ ở Anh và Hàn Quốc — được xử lý như một tiểu loại có tên riêng, không gộp vào cho vay doanh nghiệp nhỏ.

---

## 3. Phạm vi địa lý & phân tầng case

Không dàn đều. Ba tầng theo mức chi tiết:

### Tầng 1 — Nghiên cứu sâu (mỗi nước một chương)

| Nước | Vai trò trong lập luận | Nền tảng trọng điểm |
|---|---|---|
| **Trung Quốc** | Case đổ vỡ toàn diện, quy mô lớn nhất lịch sử. Chương dài nhất. | PPDai, Hongling Capital, Lufax, CreditEase/Yirendai, Ezubao (lừa đảo) |
| **Anh** | Nơi khai sinh; điều tiết sớm và tương đối tốt — nhưng bán lẻ vẫn tàn lụi. Case "quản đúng mà mô hình vẫn không sống" | Zopa, Funding Circle, RateSetter, Lendy (đổ vỡ) |
| **Mỹ** | Con đường "chứng khoán hoá + ngân hàng đối tác"; kết thúc bằng việc nền tảng trở thành ngân hàng | LendingClub, Prosper, SoFi, Upstart |
| **Việt Nam** | Đích đến | Tima, Fiin Credit, VayMuon, Lendbiz, Interloan |

### Tầng 2 — Nghiên cứu vừa (mỗi nước một mục lớn)

| Nước | Vì sao có mặt |
|---|---|
| **Hàn Quốc** | Nước đầu tiên trên thế giới ban hành **luật chuyên biệt** cho P2P. Mẫu lập pháp gần Việt Nam nhất về mặt truyền thống pháp lý. |
| **Indonesia** | Case cảnh báo gần nhất về mặt bối cảnh: dân số lớn, tài chính chưa bao trùm, nền tảng lậu tràn lan, hệ quả xã hội nặng. |
| **Latvia + Estonia** | Mô hình marketplace của tổ chức khởi tạo + cam kết mua lại; và quá trình chuyển đổi sang khung EU. |
| **Ấn Độ** | Điều tiết bằng ngân hàng trung ương với lệnh cấm nâng cấp tín dụng triệt để; đợt siết gần đây gần như xoá bỏ mô hình kinh doanh. |
| **Liên minh châu Âu (cấp khối)** | Quy chế gọi vốn cộng đồng toàn khối — và **lỗ hổng lớn**: nó chỉ điều chỉnh cho vay doanh nghiệp, không bao gồm cho vay tiêu dùng. Bài học trực tiếp cho VN về phạm vi điều chỉnh. |

### Tầng 3 — Đối chiếu ngắn (mỗi nước 1-2 trang)

Singapore · Nhật Bản · Úc & New Zealand · Ba Lan · Kenya (M-Shwari và tín dụng số phi P2P — dùng để đối chiếu ranh giới khái niệm).

**Vì sao Singapore có mặt** *(sửa v0.2)*: không phải vì "quản chặt". Cơ quan giám sát Singapore **đặt một cái giá cho việc nhận vốn của nhà đầu tư lẻ**: nền tảng được hưởng chế độ vốn thấp và miễn đặt cọc bảo đảm *chỉ khi* giới hạn nguồn vốn ở nhà đầu tư được công nhận và định chế, không giữ tiền khách hàng, và không đứng vai bên chính của khoản vay. Đây là **đòn bẩy L3 vận hành qua cấu trúc khuyến khích chứ không qua trần định lượng** — cách làm không lặp lại ở bất kỳ khu vực nào khác trong khảo sát, và là một phương án riêng cho bản đồ lựa chọn ở chương 11: *phân tầng nghĩa vụ theo loại nhà đầu tư, thay vì áp một chế độ duy nhất cho tất cả*.

**Vì sao Nhật Bản có mặt** *(sửa v0.2)*: không phải vì một quy định che giấu danh tính người vay. Thực hành ẩn danh hoá người vay là **hệ quả ngoài ý muốn** của việc đặt nghĩa vụ đăng ký kinh doanh cho vay lên *người ra quyết định cho vay*: để nhà đầu tư không rơi vào định nghĩa đó, ngành buộc phải khiến họ không biết mình đang cho ai vay. Cơ quan giám sát gỡ yêu cầu này ngày **18/3/2019**. Giá trị lập luận nằm ở chỗ: **một đòn bẩy L1 đặt sai tầng — áp lên người tham gia thay vì lên nền tảng — đã trực tiếp vô hiệu hoá đòn bẩy L6.** Bài học cho Việt Nam: khi định danh pháp lý, phải hỏi *định danh này áp lên ai*; nếu áp lên nhà đầu tư, thị trường sẽ tự tổ chức lại để né, và cách rẻ nhất để né gần như luôn là giảm thông tin họ có.

> Cả hai mô tả ở bản v0.1 ("quản chặt từ đầu, ngành nhỏ và ổn" / "giấu danh tính người vay → hệ quả") đọc sai cơ chế. Chi tiết và nguồn: `sources/legal/sg.md` §1.1, `sources/legal/jp.md` §1.2.
>
> ⚠ **Còn trống**: dữ liệu về *kết quả* của Singapore (quy mô ngành, số nền tảng, mốc can thiệp) vẫn bằng không. Không được viết "ngành nhỏ và ổn" cho tới khi có số — `sources/gaps.md` §8.2.

---

## 4. Ánh xạ bảy nội dung bạn yêu cầu vào khung phân tích

| Yêu cầu ban đầu | Được xử lý ở đâu | Ghi chú về cách xử lý |
|---|---|---|
| Lịch sử hình thành | Ch. 2 | Bám ba nguồn gốc riêng biệt: tài chính vi mô, cho vay tiêu dùng sau khủng hoảng 2008, và hiện tượng "chênh lệch pháp lý". Không kể như một dòng chảy duy nhất. |
| Quá trình phát triển | Ch. 2 + mở đầu mỗi chương quốc gia | Neo vào Khung C (vòng đời 5 giai đoạn) để so sánh được giữa các nước. |
| **Các biến tướng** | **Ch. 9 — chương độc lập** | Đây là chương giá trị nhất cho mục đích chính sách. Xây thành **bảng phân loại biến tướng** có dấu hiệu nhận biết sớm. Xem §4.1. |
| Bài học thất bại, rủi ro | Xuyên suốt + Ch. 10 tổng hợp | Mỗi thất bại phải quy về ít nhất một đòn bẩy L1-L6 bị thiếu hoặc đến muộn. Không dừng ở "vì lừa đảo". |
| Bài học thành công | Ch. 10 | **Cảnh báo phương pháp**: rất ít trường hợp thành công thật. Phải định nghĩa "thành công" trước — sống sót? hay có tác động phúc lợi? Xem §7.5. |
| Các mốc thời gian quan trọng | Phụ lục A — dòng thời gian đối chiếu | Dòng thời gian đa tuyến: mỗi nước một dòng, xếp song song để thấy quan hệ nhân quả lan truyền (đặc biệt: siết ở TQ 2018 → sóng dịch chuyển sang ĐNÁ 2019). |
| Mô hình & công ty điển hình | Rải trong các chương quốc gia + Phụ lục B | Mỗi công ty có một phiếu chuẩn hoá: mô hình theo Khung A, đỉnh quy mô, kết cục, nguyên nhân. |

### 4.1. Chương "Biến tướng" — phân loại đề xuất

Phần này là đóng góp chính sách cốt lõi: biến hiện tượng thành **bộ dấu hiệu cảnh báo sớm** dùng được cho cơ quan giám sát.

| Nhóm | Biến tướng | Dấu hiệu nhận biết sớm |
|---|---|---|
| **B1. Rủi ro cấu trúc** | Tự tài trợ (nền tảng huy động cho dự án của chính chủ sở hữu) | Người vay tập trung; quan hệ sở hữu chồng chéo |
| | Gộp quỹ, lệch kỳ hạn | Sản phẩm có kỳ hạn cố định mà tài sản cơ sở không khớp; rút vốn "bất kỳ lúc nào" |
| | Bảo lãnh gốc / quỹ dự phòng | Ngôn ngữ tiếp thị "an toàn", "đảm bảo", lợi suất cố định |
| **B2. Gian lận** | Dự án giả, người vay ma | Tỷ lệ nợ xấu công bố thấp bất thường và ổn định bất thường |
| | Mô hình Ponzi trực tiếp | Tăng trưởng huy động vượt xa tăng trưởng giải ngân |
| **B3. Bóc lột người vay** | Trừ lãi trước, phí ẩn → lãi thực ba chữ số | Chênh lệch giữa lãi suất công bố và lãi suất thực tế |
| | Cho vay sinh viên / cho vay "ép" | Nhóm khách hàng không có thu nhập |
| | Thu hồi nợ bạo lực, khai thác danh bạ điện thoại | Khiếu nại; quyền truy cập ứng dụng bất thường |
| **B4. Lách pháp lý** | Chọn nơi đăng ký để lách trần lãi suất | Cấu trúc pháp nhân đa tầng, xuyên biên giới |
| | Nền tảng lậu hoàn toàn (không đăng ký) | Chỉ tồn tại dưới dạng ứng dụng; không hiện diện pháp lý |
| | Dịch chuyển sau siết ở nước khác | Vốn/nhân sự/mã nguồn nước ngoài đến ồ ạt |

**Ghi chú**: B3 và B4 mới là hình thái *chủ đạo hiện nay ở Đông Nam Á*, chứ không phải B1-B2 kiểu Trung Quốc 2015-2018. Báo cáo phải phản ánh đúng trọng số này, nếu không khuyến nghị sẽ chống lại cuộc chiến của quá khứ.

---

## 5. Xương sống dữ liệu định lượng

Không có phần này, mọi kết luận chỉ là ý kiến. Với mỗi thị trường Tầng 1-2, cố gắng thu thập chuỗi số liệu theo năm:

| Chỉ số | Ghi chú thu thập |
|---|---|
| Số nền tảng đang hoạt động / đã đăng ký / đã rút lui | Chuỗi theo năm; là chỉ báo tốt nhất về vòng đời |
| Dư nợ và doanh số giải ngân | Phân biệt rõ hai khái niệm — thường bị nhầm lẫn hoặc cố tình gộp |
| Tỷ lệ nợ xấu / thu hồi | Ưu tiên số theo **lứa vay** (cohort), không lấy tỷ lệ trên tổng dư nợ đang tăng (chỉ số này che giấu rủi ro trong giai đoạn tăng trưởng) |
| Tỷ trọng vốn từ nhà đầu tư lẻ vs định chế | Chỉ báo trực tiếp của SQ3 |
| Số nhà đầu tư bị ảnh hưởng & giá trị chưa thu hồi khi đổ vỡ | Đại lượng đo tổn thất xã hội |
| Lãi suất bình quân người vay phải trả (đã gồm phí) | Để trả lời câu "có thay thế được tín dụng đen không" |

**Ba nguyên tắc bắt buộc:**

1. **Truy nguyên**: mỗi con số kèm nguồn và ngày. Số do nền tảng tự công bố đánh dấu riêng, không trộn với số của cơ quan quản lý.
2. **Tách hai thị trường** (§2.4): mỗi chỉ số tách cho vay tiêu dùng / doanh nghiệp nhỏ / bất động sản. Nguồn nào không tách được thì ghi rõ là số gộp.
3. **Mốc thời gian**: chuỗi số liệu chạy đến **hết 2025**. Dữ liệu 2026 chỉ đưa vào khi có nguồn chắc chắn và phải gắn nhãn "sau mốc phạm vi".

### 5.1. Hai đoạn dữ liệu, hai mức độ chắc chắn *(quyết định v0.2, 2026-07-26)*

Rà soát P1 phát hiện một đứt gãy không lường trước: **nguồn định lượng xuyên quốc gia duy nhất có phương pháp nhất quán dừng ở dữ liệu năm 2020** (`sources/sources.md` §1.1). Không có nguồn tương đương cho 2021-2025. Đây là rủi ro **R1** hiện hình ngay ở P1 thay vì cuối P2.

Đã cân nhắc ba phương án và **chọn phương án B**: chia xương sống định lượng làm hai đoạn, mỗi đoạn có mức độ chắc chắn và cách dùng riêng.

| | **Đoạn 1: 2013–2020** | **Đoạn 2: 2021–2025** |
|---|---|---|
| **Nguồn chính** | Bộ chuẩn đối sánh Cambridge (`sources.md` G1, G2), kiểm chéo bằng BIS (G3) | Số liệu cơ quan quản lý từng nước; giám sát của FSB (G4, G5) ở phạm vi hẹp |
| **Phương pháp** | Nhất quán, cùng định nghĩa, cùng cách thu thập | **Không nhất quán** — mỗi nước một định nghĩa, một cách đếm |
| **Được phép làm gì** | **So sánh chéo giữa các nước.** Bảng đa quốc gia, xếp hạng tương đối, tính tỷ trọng | **Chỉ mô tả theo từng nước.** Diễn biến nội bộ một thị trường theo thời gian |
| **Cấm** | — | **Không đặt số của hai nước cạnh nhau như thể so sánh được.** Không tính tổng khu vực. Không nói "nước A lớn hơn nước B" |
| **Nghĩa vụ ghi chú** | Nêu thiên lệch sống sót của nguồn khảo sát (§7.5) | Mỗi bảng phải ghi rõ nguồn, định nghĩa, và **câu cảnh báo không so sánh chéo** |

**Vì sao không chọn hai phương án kia:**

- **Phương án A** (dựng chuỗi 2021-2025 từ số liệu từng nước rồi vẫn so sánh chéo): tốn công nhất và **hỏng đúng mục đích của việc thu thập** — so sánh chéo giữa các định nghĩa khác nhau là so sánh giả.
- **Phương án C** (lùi mốc định lượng về hết 2020, giữ 2025 cho phần thể chế): gọn nhất, nhưng **cắt mất đúng đoạn Việt Nam ra văn bản (2025)** và đoạn hậu-quả của các đợt siết ở Ấn Độ (2024), Hàn Quốc (2020→). Đó là những đoạn có giá trị nhất với câu hỏi đích. Không chấp nhận được.

**Hệ quả cho các chương**: mọi phát biểu định lượng so sánh giữa các nước ở chương 10 (tổng hợp so sánh) phải **neo vào đoạn 1**. Nếu một luận điểm chỉ đứng được bằng dữ liệu đoạn 2, nó phải được trình bày như quan sát theo từng nước kèm giới hạn, không phải như phát hiện so sánh.

---

## 6. Cấu trúc đầu ra dự kiến

| Chương | Nội dung | Trang (ước) |
|---|---|---|
| 1 | Cách đọc tài liệu này + tổng quan các phát hiện chính | 4 |
| 2 | Nguồn gốc, định nghĩa, khung phân tích (A/B/C + quy tắc tách hai thị trường) | 7 |
| 3 | Anh — khai sinh, điều tiết, và sự tàn lụi của bán lẻ | 7 |
| 4 | Mỹ — con đường chứng khoán hoá và ngân hàng đối tác | 6 |
| 5 | Baltic & Đông Âu — marketplace tổ chức khởi tạo, cam kết mua lại, và khung EU | 6 |
| 6 | **Trung Quốc — bùng nổ, biến chất, xoá sổ** | **14** |
| 7 | Châu Á khác — Hàn Quốc, Indonesia, Ấn Độ, Singapore, Nhật | 9 |
| 8 | **Hai thị trường tách biệt: cho vay tiêu dùng vs cho vay doanh nghiệp nhỏ** | 6 |
| 9 | **Giải phẫu các biến tướng** (xuyên quốc gia) | 8 |
| 10 | Tổng hợp so sánh: cái gì quyết định kết cục | 6 |
| 11 | **Việt Nam — hiện trạng thể chế, khoảng trống, không gian lựa chọn** | 11 |
| PL A | Dòng thời gian đối chiếu đa quốc gia | 4 |
| PL B | Phiếu hồ sơ ~30 nền tảng điển hình | 6 |
| PL C | Bảng so sánh điều tiết theo sáu đòn bẩy L1-L6 | 3 |
| PL D | **Thuật ngữ đối chiếu** Việt – Anh – Trung – Hàn | 3 |
| PL E | **Mục lục tra cứu** (theo nền tảng, theo quốc gia, theo văn bản pháp quy) | 2 |

**Ghi chú về độ dài**: phần chính ~84 trang, phụ lục ~18 — tổng vượt ước tính 50-80 trang ban đầu, chủ yếu do thêm chương 8 và bộ phụ lục tra cứu. Nếu cần gọn lại, chỗ cắt hợp lý nhất là **Tầng 3** (§3), không phải chương Trung Quốc hay chương Việt Nam.

**Chương 11 (Việt Nam)** viết theo hướng **phân tích thể chế**, không phải phân tích số liệu — dữ liệu định lượng công khai về thị trường Việt Nam quá mỏng và phân tán để đỡ được một chương định lượng. Cụ thể:

- Mở đầu chương phải có **tuyên bố giới hạn dữ liệu** nêu rõ: đã tìm những nguồn nào, tìm được gì, không tìm được gì, và điều đó giới hạn kết luận đến đâu. Không lấp khoảng trống bằng ước đoán hay bằng số liệu do nền tảng tự công bố mà không đánh dấu.
- Trọng tâm chuyển sang: định danh pháp lý hiện hành của hoạt động, ánh xạ khoảng trống theo sáu đòn bẩy L1-L6, và đối chiếu với các nước có bối cảnh gần nhất (Indonesia, Hàn Quốc, Ấn Độ).
- Kết chương là **bản đồ không gian lựa chọn**: các phương án thể chế khả thi, điều kiện tiên quyết và đánh đổi của từng phương án, trình bày song song và cân bằng. Không xếp hạng, không chốt một phương án — đúng thể loại tài liệu tham chiếu (§7.4).

---

## 7. Chuẩn mực nguồn và bằng chứng

### 7.1. Thứ bậc nguồn (áp dụng chặt)

1. Văn bản pháp quy gốc và tài liệu của cơ quan quản lý (ngân hàng trung ương, cơ quan giám sát tài chính)
2. Số liệu thống kê chính thức và báo cáo giám sát
3. Nghiên cứu học thuật bình duyệt và báo cáo của tổ chức quốc tế (BIS, IMF, WB, CGAP)
4. Báo chí tài chính uy tín (Financial Times, Caixin, Nikkei Asia, Reuters)
5. Số liệu ngành / do nền tảng tự công bố — **luôn đánh dấu rõ là tự công bố**

### 7.2. Quy tắc bắt buộc

- Mọi số liệu và mọi khẳng định pháp lý đều phải có trích dẫn kèm ngày truy cập.
- **Số hiệu văn bản pháp luật phải được xác minh từ nguồn gốc**, không viết theo trí nhớ. Áp dụng cho cả văn bản Việt Nam.
- Khi các nguồn mâu thuẫn về số liệu (rất hay xảy ra với quy mô thị trường P2P Trung Quốc), **trình bày cả khoảng và nêu rõ nguồn nào nói gì**, không tự chọn một con số.
- Số liệu và sự kiện lấy đến **hết 2025**; phần 2026 nếu có phải gắn nhãn "sau mốc phạm vi".

### 7.3. Quy tắc ngôn ngữ

Nguồn tiếng Trung, tiếng Hàn, tiếng Indonesia được sử dụng tự do và **được khuyến khích** — với nhiều chủ đề (đặc biệt là Trung Quốc) đây mới là nguồn gốc, còn nguồn tiếng Anh chỉ là bản tường thuật lại.

| Thành phần | Quy tắc |
|---|---|
| **Nội dung trong thân bài** | Chuyển tải hoàn toàn sang **tiếng Việt**. Không chèn nguyên văn dài, không trích dẫn song ngữ trong thân bài. |
| **Trích dẫn nguồn** | Ghi ở dạng **tra cứu lại được**: tên gốc của văn bản/bài viết, số hiệu văn bản, cơ quan ban hành, ngày, đường dẫn. |
| **Thuật ngữ chuyên ngành** | Dùng tiếng Việt trong thân bài. Bản đối chiếu nguyên ngữ dồn về **Phụ lục D**, không rải trong thân bài. |

Lý do tách như vậy: thân bài đọc trôi chảy bằng một ngôn ngữ, còn khả năng truy nguyên vẫn được bảo toàn nguyên vẹn qua phần trích dẫn và phụ lục thuật ngữ.

### 7.4. Chuẩn mực của một tài liệu tham chiếu

Vì đây là tài liệu tham chiếu chung (§0.2) chứ không phải tài liệu vận động chính sách, bốn ràng buộc sau chi phối cách viết:

1. **Lập bản đồ, không kê đơn.** Ở mọi điểm có tranh luận chính sách thực sự, trình bày các phương án và đánh đổi song song, cân bằng. Nếu người viết có đánh giá riêng, đánh giá đó phải được **tách ra và gắn nhãn rõ** là đánh giá, không trộn vào phần trình bày sự kiện.
2. **Tách bạch ba tầng phát biểu.** Sự kiện có nguồn / suy luận từ sự kiện / đánh giá của người viết — phải phân biệt được bằng cách hành văn, không để người đọc phải đoán đang đọc tầng nào.
3. **Tự chứa và tra cứu được.** Mỗi chương đọc riêng được. Thuật ngữ giải thích ở lần xuất hiện đầu trong mỗi chương. Tham chiếu chéo bằng số mục. Có phụ lục thuật ngữ và mục lục tra cứu (PL D, PL E).
4. **Bền theo thời gian.** Phần nào phụ thuộc vào tình hình có thể thay đổi (đặc biệt là hiện trạng pháp lý Việt Nam) phải ghi rõ mốc thời gian hiệu lực của nhận định, để người đọc năm sau biết chỗ nào cần kiểm tra lại.

### 7.5. Hai bẫy phương pháp phải tránh

- **Thiên lệch sống sót**: nếu chỉ nghiên cứu các nền tảng còn tồn tại, sẽ kết luận sai về nguyên nhân thành công. Bắt buộc đưa các nền tảng đã sụp vào mẫu.
- **Định nghĩa "thành công"**: một nền tảng sống sót bằng cách từ bỏ mô hình P2P (trở thành ngân hàng, hoặc chuyển sang vốn định chế) **không phải là bằng chứng P2P thành công** — nó là bằng chứng ngược lại. Phải phân biệt rành mạch "doanh nghiệp thành công" với "mô hình thành công".

---

## 8. Ranh giới — những gì báo cáo KHÔNG làm

- Không dự báo thị trường, không định giá, không khuyến nghị đầu tư.
- Không đánh giá hay xếp hạng một nền tảng Việt Nam cụ thể nào đang hoạt động.
- Không mở rộng sang toàn bộ fintech tín dụng (mua trước trả sau, cho vay nhúng, tiền số) — chỉ nhắc khi cần vạch ranh giới khái niệm.
- Không bàn gọi vốn cổ phần cộng đồng (equity crowdfunding) trừ phần so sánh khung pháp lý EU.
- Không thu thập dữ liệu sơ cấp (phỏng vấn, khảo sát) trong phạm vi vòng này.

---

## 9. Kế hoạch thực hiện

| Giai đoạn | Việc | Sản phẩm |
|---|---|---|
| **P0** | Chốt `target.md` này | Mục tiêu đã duyệt |
| **P1** | Rà soát bối cảnh + dựng thư mục nguồn; xác minh toàn bộ văn bản pháp quy trọng yếu | Thư mục nguồn có chú giải; dòng thời gian sơ bộ |
| **P2** | Thu thập xương sống dữ liệu (§5) | Bảng dữ liệu theo nước/năm, có nguồn |
| **P3** | Viết các chương quốc gia (TQ trước — vì dài và khó nhất) | Bản thảo Ch. 3-7 |
| **P4** | Chương tách hai thị trường + biến tướng + tổng hợp so sánh | Bản thảo Ch. 8-10 |
| **P5** | Chương Việt Nam + bản đồ không gian lựa chọn | Bản thảo Ch. 11 |
| **P6** | Kiểm tra tính toàn vẹn: đối chiếu lại từng trích dẫn, rà mâu thuẫn nội bộ | Báo cáo kiểm tra |
| **P7** | Hoàn thiện; dựng bộ phụ lục tra cứu (PL A-E); viết chương 1 | Bản cuối |

Kiến nghị làm **P1 → P2 trước rồi dừng lại rà soát cùng nhau**: nếu xương sống dữ liệu mỏng hơn dự kiến ở một khu vực nào đó, phải điều chỉnh phạm vi ngay, chứ không phát hiện lúc đã viết xong.

---

## 10. Rủi ro còn lại của kế hoạch

Phạm vi đã chốt đủ để bắt đầu. Bốn rủi ro dưới đây không cần quyết ngay, nhưng cần theo dõi và xử lý đúng lúc phát sinh — ghi ở đây để không ai bất ngờ về sau.

| # | Rủi ro | Dấu hiệu phát hiện | Cách xử lý |
|---|---|---|---|
| R1 | **Xương sống dữ liệu mỏng hơn dự kiến** ở một hoặc nhiều khu vực, khiến phần so sánh định lượng không đứng được | ~~Cuối P2~~ → **đã xảy ra ở P1** | **Đã xử lý (v0.2)**: đứt gãy nằm ở trục *thời gian* chứ không ở một khu vực cụ thể — nguồn xuyên quốc gia dừng ở 2020. Áp dụng **§5.1 phương án B**: hai đoạn dữ liệu, đoạn 2021-2025 chỉ mô tả theo nước, không so sánh chéo. Rủi ro còn lại chuyển thành: *liệu đoạn 1 có đủ dày để đỡ chương 10 không* — kiểm ở cuối P2 |
| R2 | **Số liệu Trung Quốc mâu thuẫn nghiêm trọng giữa các nguồn** — quy mô đỉnh và tổn thất chưa thu hồi là hai đại lượng bị công bố rất khác nhau | P1-P2 | Áp dụng §7.2: trình bày khoảng, ghi rõ nguồn nào nói gì, không tự chọn một con số |
| R3 | **Chương Việt Nam thiếu nền định lượng đến mức ảnh hưởng độ tin cậy của kết luận** | P5 | Đã hạ kỳ vọng sang phân tích thể chế (§6). Nếu vẫn quá mỏng, thu hẹp phạm vi kết luận và nói rõ, thay vì nới suy luận |
| R4 | **Nguồn không tách được tiêu dùng / doanh nghiệp nhỏ**, làm hỏng quy tắc §2.4 | P2 | Ghi rõ là số gộp và không dùng số gộp để phát biểu về một loại riêng lẻ |

---

## 11. Trạng thái phê duyệt

| Hạng mục | Trạng thái |
|---|---|
| Lĩnh vực, thể loại, độc giả | ✅ Đã chốt (§0.1, §0.2) |
| Phạm vi địa lý & phân tầng case | ✅ Đã chốt (§0.3, §0.4, §3) |
| Độ sâu & cấu trúc đầu ra | ✅ Đã chốt (§0.5, §6) |
| Mốc thời gian kết thúc phạm vi | ✅ Đã chốt — hết 2025 (§0.6) |
| Tách cho vay tiêu dùng / doanh nghiệp nhỏ | ✅ Đã chốt — tách, làm trục cắt ngang (§0.7, §2.4) |
| Cách xử lý chương Việt Nam | ✅ Đã chốt — phân tích thể chế, có tuyên bố giới hạn dữ liệu (§6) |
| Quy tắc ngôn ngữ | ✅ Đã chốt (§7.3) |
| Cấu trúc xương sống định lượng | ✅ Đã chốt v0.2 — hai đoạn, phương án B (§5.1) |

**Bước tiếp theo**: P1 đã hoàn tất vòng một (`plan.md` §3). Khởi động **P2 — thu thập xương sống dữ liệu** theo cấu trúc hai đoạn ở §5.1. Dừng lại rà soát cùng nhau tại **Cổng G2** cuối P2 trước khi viết chương nào.

---

## 12. Nhật ký sửa đổi tài liệu này

Chỉ thêm, không sửa dòng cũ. Mỗi dòng ghi: sửa gì, vì sao, nguồn bằng chứng.

| Ngày | Mục | Thay đổi | Vì sao | Bằng chứng |
|---|---|---|---|---|
| 2026-07-26 | §2.3 (+ §1.2 SQ4) | **Rút giả thuyết can thiệp ở G1.** Trục SQ4 viết lại theo mốc thời gian đã xác minh; vị trí Singapore và New Zealand đánh dấu là chưa có bằng chứng | Không khu vực nào trong khảo sát điều tiết trước khi thị trường hình thành. Giả thuyết G1 không có bằng chứng nào | `notes/timeline.md` §2.1 · `sources/gaps.md` §8.3 |
| 2026-07-26 | §3 Tầng 3 — Singapore | Thay *"quản chặt từ đầu, ngành nhỏ và ổn"* bằng mô tả cơ chế thật: **định giá việc nhận vốn của nhà đầu tư lẻ**, L3 qua cấu trúc khuyến khích | Mô tả cũ đọc sai cơ chế. Cơ chế thật bổ sung một phương án mới cho bản đồ chương 11 | `sources/legal/sg.md` §1.1 |
| 2026-07-26 | §3 Tầng 3 — Nhật Bản | Thay *"giấu danh tính người vay → hệ quả"* bằng cơ chế thật: **hệ quả ngoài ý muốn của nghĩa vụ đăng ký áp lên nhà đầu tư**, gỡ bỏ 18/3/2019 | Mô tả cũ ngụ ý một quy định che giấu thông tin — không tồn tại. Cơ chế thật có giá trị lập luận cao hơn (L1 sai tầng vô hiệu hoá L6) | `sources/legal/jp.md` §1.2 |
| 2026-07-26 | §5 (thêm §5.1), §10 R1, §11 | **Chốt cấu trúc xương sống định lượng hai đoạn** (phương án B) | Nguồn xuyên quốc gia dừng ở dữ liệu 2020; năm năm cuối của phạm vi không có nguồn tương đương | `sources/sources.md` §1.1, §6 · `sources/gaps.md` §1 |

---

*Tài liệu này là bản thảo mục tiêu, không phải kết quả nghiên cứu. Mọi giả thuyết nêu ở §2.3 và §4.1 cần được kiểm chứng bằng dữ liệu ở các giai đoạn P1-P2.*
