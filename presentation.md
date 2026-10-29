---
marp: true
theme: default
paginate: true
size: 16:9
style: |
  section {
    background-color: #F3EBE1; /* Màu nền Be ấm */
    color: #262E5B; /* Màu chữ Xanh Navy đậm */
    font-family: 'Segoe UI', Arial, sans-serif;
    padding-top: 45px;
    padding-bottom: 35px;
    padding-left: 55px;
    padding-right: 85px;
    position: relative;
    font-size: 21px;
    line-height: 1.45;
  }
  section::after {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 32px;
    height: 100%;
    background-color: #262E5B;
    border-top-left-radius: 16px;
    border-bottom-left-radius: 16px;
  }
  h1, h2, h3, h4 {
    color: #262E5B;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    margin-top: 0;
  }
  h1 {
    font-size: 2.5em;
    margin-top: 0;
    margin-bottom: 0.2em;
    line-height: 1.15;
  }
  h2 {
    font-size: 1.7em;
    border-bottom: 3px solid #262E5B;
    padding-bottom: 8px;
    margin-top: 0;
    margin-bottom: 20px;
    line-height: 1.25;
  }
  h3 {
    font-size: 1.15em;
    color: #3B4684;
    margin-top: 10px;
    margin-bottom: 6px;
  }
  p, li {
    color: #262E5B;
  }
  li {
    margin-bottom: 7px;
  }
  strong {
    color: #1A2042;
    font-weight: 700;
  }
  .badge {
    display: inline-block;
    border: 2px solid #262E5B;
    border-radius: 20px;
    padding: 6px 18px;
    font-weight: bold;
    font-size: 0.9em;
    margin: 15px 0;
  }
  .pill {
    display: inline-block;
    border: 2px solid #262E5B;
    border-radius: 50px;
    padding: 8px 28px;
    font-size: 1.05em;
    font-weight: 600;
    margin: 15px 0;
  }
  .box {
    background-color: #E6DDD0;
    border-left: 6px solid #262E5B;
    padding: 14px 20px;
    border-radius: 6px;
    margin: 12px 0;
  }
  .img-guide {
    background-color: #ffffff;
    border: 2px dashed #262E5B;
    padding: 12px 16px;
    border-radius: 8px;
    font-size: 0.85em;
    color: #3B4684;
    margin-top: 12px;
  }
  .grid-2 {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 30px;
    align-items: center;
  }
  ul, ol {
    margin-left: 1.2em;
    font-size: 0.9em;
  }
  img {
    border-radius: 6px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    max-width: 100%;
  }
  footer {
    color: #555F8C;
    font-size: 0.75em;
  }
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 12px 0;
    font-size: 0.88em;
  }
  th {
    background-color: #262E5B;
    color: #F3EBE1;
    padding: 8px 12px;
    text-align: left;
  }
  td {
    border-bottom: 1px solid #C5B9A8;
    padding: 8px 12px;
    background-color: #FAF6F0;
  }
---




<!-- _class: lead -->
# TRỰC QUAN HÓA<br>DỮ LIỆU
<div class="badge">Kể chuyện Trực quan & Nguyên lý Thiết kế</div>

**Tháng 10, 2026**  
Thuyết trình bởi: **Nhóm 20**

**Thành viên:** Trần Thị Mai Anh (P1) • Vũ Đức Quý (P2) • Nguyễn Hữu Quyết (P3) • Nguyễn Lê Tùng Dương (P4)  
*Dựa trên tác phẩm: Hands-On Data Visualization (Jack Dougherty & Ilya Ilyankou)*

---




## NỘI DUNG TRÌNH BÀY

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 30px;">
  <div style="border: 2px solid #262E5B; border-radius: 16px; padding: 15px 20px;">
    <h3 style="margin: 0; font-size: 1.2em;">01. NỀN TẢNG DỮ LIỆU</h3>
    <p style="margin: 5px 0 0; font-size: 0.85em; color: #555F8C;">Thu thập, làm sạch & so sánh có ý nghĩa (Ch. 3, 4, 5)<br><strong>Người thuyết trình: Người 1</strong></p>
  </div>
  <div style="border: 2px solid #262E5B; border-radius: 16px; padding: 15px 20px;">
    <h3 style="margin: 0; font-size: 1.2em;">03. TRỰC QUAN KHÔNG GIAN</h3>
    <p style="margin: 5px 0 0; font-size: 0.85em; color: #555F8C;">Bản đồ Choropleth, thang màu & chuẩn hóa (Ch. 7)<br><strong>Người thuyết trình: Người 3</strong></p>
  </div>
  <div style="border: 2px solid #262E5B; border-radius: 16px; padding: 15px 20px;">
    <h3 style="margin: 0; font-size: 1.2em;">02. THIẾT KẾ BIỂU ĐỒ</h3>
    <p style="margin: 5px 0 0; font-size: 0.85em; color: #555F8C;">Cấu trúc đồ thị, Zero-baseline & phối màu (Ch. 6)<br><strong>Người thuyết trình: Người 2</strong></p>
  </div>
  <div style="border: 2px solid #262E5B; border-radius: 16px; padding: 15px 20px;">
    <h3 style="margin: 0; font-size: 1.2em;">04. ĐẠO ĐỨC & KỂ CHUYỆN</h3>
    <p style="margin: 5px 0 0; font-size: 0.85em; color: #555F8C;">Nhận diện lừa dối, Cartogram & Tell-Show-Why (Ch. 14, 15)<br><strong>Người thuyết trình: Người 4</strong></p>
  </div>
</div>

---




<!-- _class: lead -->
# NỀN TẢNG DỮ LIỆU
# THU THẬP, LÀM SẠCH & CHUẨN HÓA

<div class="pill">Từ Dữ Liệu Thô Đến Phép So Sánh Công Bằng (Chương 3, 4, 5)</div>

**Phần 1 — Bài Thuyết Trình Trực Quan Hóa Dữ Liệu**
Dựa trên tác phẩm *Hands-On Data Visualization* (Jack Dougherty & Ilya Ilyankou)

<!-- 
[Ghi chú thuyết trình]:
Chào mọi người. Trước khi chúng ta có thể vẽ nên những biểu đồ đẹp mắt hay những bản đồ tương tác ấn tượng, mọi dự án trực quan hóa thành công đều bắt đầu từ phần chìm của tảng băng trôi: Nền tảng dữ liệu. Phần trình bày đầu tiên này sẽ đi qua 3 bước sống còn: Tìm kiếm và phản biện dữ liệu (Chương 3), Làm sạch dữ liệu bẩn (Chương 4), và Tạo ra các phép so sánh có ý nghĩa (Chương 5).
-->

---




## NỘI DUNG TRÌNH BÀY (OUR CONTENTS)

**01. Chương 3: Tìm kiếm & Đặt câu hỏi với Dữ liệu**
- Triết lý dữ liệu & 5 câu hỏi định hướng săn tìm dữ liệu
- Ranh giới Dữ liệu Công khai (Public) vs. Riêng tư (Private)
- Kỹ thuật bảo vệ quyền riêng tư: Làm mờ (Masking) & Tổng hợp (Aggregating)
- Quản trị nguồn gốc & Nhận diện các dấu hiệu "Dữ liệu xấu" (Bad Data)

**02. Chương 4: Kỹ thuật Làm sạch Dữ liệu Bẩn**
- Thực trạng dữ liệu thô & Các lỗi định dạng kinh điển
- Chuẩn hóa chuỗi, Tái cấu trúc bảng (Transpose, Split, Combine)
- Gom cụm (Clustering) để xử lý sự bất nhất trong tên gọi

**03. Chương 5: Tạo Phép So Sánh Có Ý Nghĩa**
- Độ chính xác trong ngôn từ: Mean vs. Median, $\%$ Change vs. Điểm $\%$, Tương quan vs. Nhân quả
- Chuẩn hóa dữ liệu (Normalization) & Phòng tránh 3 bẫy thiên vị chọn mẫu (Sampling Biases)

---




<!-- _class: lead -->
# 01. TÌM KIẾM & PHẢN BIỆN DỮ LIỆU
### CHƯƠNG 3: FIND AND QUESTION YOUR DATA

<div class="pill">"Dữ liệu không tự nhiên sinh ra từ hư không, và những con số không bao giờ hoàn toàn trung lập."</div>

---




## TRIẾT LÝ CỐT LÕI: DỮ LIỆU KHÔNG TRUNG LẬP

Trước khi bắt tay vào vẽ biểu đồ, ta luôn phải đối mặt với 2 câu hỏi lớn: **"Tìm dữ liệu đáng tin cậy ở đâu?"** và **"Dữ liệu này thực sự đại diện cho điều gì?"**

- **Sự ngộ nhận về "Tính khách quan của dữ liệu" (Data Objectivity):**
  - Dữ liệu luôn được con người thu thập và công bố vì những mục đích cụ thể (tường minh hoặc ngầm định).
  - Nó chịu sự chi phối bởi bối cảnh xã hội, lịch sử và cấu trúc quyền lực đương thời.
- **Góc nhìn từ *Data Feminism* (Catherine D'Ignazio & Lauren Klein, 2020):**
  - Khi làm việc với bất kỳ bộ dữ liệu nào, hãy dừng lại và hỏi:
    1. *Câu chuyện của ai đang được kể lại?* (Whose stories are told?)
    2. *Góc nhìn của ai đang bị bỏ qua hoặc im lặng?* (Whose perspectives remain unspoken?)

<div class="img-guide">
🖼️ <b>Gợi ý hình minh họa:</b> Thiết kế một sơ đồ cân bằng hoặc hình vẽ tảng băng trôi: Phần nổi là "Con số & Bảng biểu (Numbers & Tables)", phần chìm bên dưới là "Bối cảnh xã hội, Mục đích thu thập, Cấu trúc quyền lực & Những góc nhìn bị bỏ sót".
</div>

<!-- 
[Ghi chú thuyết trình]:
Nhiều người nghĩ rằng "con số không biết nói dối". Nhưng thực tế, con số do con người thu thập. Ai là người quyết định thu thập cái gì và bỏ qua cái gì? Nếu nhảy vào vẽ biểu đồ ngay mà không đặt câu hỏi về nguồn gốc dữ liệu, chúng ta rất dễ tạo ra những đồ thị vô nghĩa hoặc gây hiểu lầm nghiêm trọng.
-->

---




## 5 CÂU HỎI ĐỊNH HƯỚNG TÌM KIẾM DỮ LIỆU (PHẦN 1)

Thay vì chỉ gõ từ khóa ngẫu nhiên lên Google, các nhà báo dữ liệu và chuyên gia thư viện sử dụng 5 câu hỏi định hướng:

### 1. Câu hỏi chính xác bạn muốn trả lời bằng dữ liệu là gì?
- **Nguyên tắc:** Hãy viết rõ ràng thành một câu hỏi có dấu chấm hỏi ở cuối để định hình tư duy và tránh việc não bộ tự động nhảy cóc sang kết luận.
- **Ví dụ thực tế 1 — Đại dịch thuốc giảm đau Opioid tại Mỹ (*Washington Post*, 2019):**
  - *Câu hỏi cốt lõi:* Có bao nhiêu viên thuốc giảm đau kê đơn đã được gửi tới từng quận của Mỹ (tính theo đầu người), và công ty nào chịu trách nhiệm?
  - *Phát hiện từ dữ liệu DEA:* Hơn $100\text{ tỷ}$ viên thuốc được phân phối (2006–2014); một số quận nông thôn vùng Appalachia nhận trên $150\text{ viên/người/năm}$; chỉ 6 tập đoàn chiếm hơn $75\%$ tổng lượng phân phối.
- **Ví dụ thực tế 2 — Sẵn sàng điều chỉnh câu hỏi khi nghiên cứu:**
  - Từ câu hỏi ngây thơ ban đầu (*"Điểm thi trường công ở Connecticut thập niên 1960 là bao nhiêu?"* $\rightarrow$ thời đó chưa có thi chuẩn hóa) đổi thành câu hỏi sâu sắc hơn: *"Khi nào người mua nhà bắt đầu biết đến điểm thi và nó ảnh hưởng thế nào đến giá bất động sản?"*

---




## 5 CÂU HỎI ĐỊNH HƯỚNG TÌM KIẾM DỮ LIỆU (PHẦN 2)

### 2. Tổ chức nào có khả năng đã thu thập hoặc công bố dữ liệu này?
- **Cơ quan chính phủ:** Cấp độ nào (địa phương, bang, quốc gia, quốc tế)? Nhánh nào (hành pháp, lập pháp, tư pháp)?
- **Phi chính phủ:** Viện nghiên cứu học thuật, tổ chức báo chí, phi lợi nhuận (NGO), hay tập đoàn tư nhân?

### 3. Dữ liệu có sẵn ở cấp độ phân giải (Level of Aggregation) nào?
- **Dữ liệu cá nhân (Disaggregated/Individual)** cho phép phân tích chi tiết, trong khi **Dữ liệu tổng hợp (Aggregated)** giúp nhìn thấy bức tranh toàn cảnh và bảo vệ quyền riêng tư.
- **Ví dụ từ Điều tra Dân số Mỹ (US Census):**
  - Luật liên bang bảo mật hồ sơ cá nhân trong **72 năm**, sau đó mới công khai (ví dụ: hiện có thể xem bản viết tay từng hộ gia đình năm 1940).
  - Với dữ liệu hiện tại, Census tổng hợp theo **Hệ thống phân cấp địa lý**:
    $$\text{Tiểu bang (State)} \rightarrow \text{Quận (County)} \rightarrow \text{Thị trấn} \rightarrow \text{Census Tract (2.500–8.000 dân)} \rightarrow \text{Block Group} \rightarrow \text{Census Block}$$

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 5 PDF / Trang 74 Sách):</b> Ghép song song <b>Figure 3.1</b> (Bản chụp sổ điều tra dân số viết tay năm 1940 của gia đình tác giả Jack Dougherty) và <b>Figure 3.2</b> (Bản đồ phân cấp các lớp ranh giới địa lý Census tại Hartford, Connecticut).
</div>

---




## 5 CÂU HỎI ĐỊNH HƯỚNG TÌM KIẾM DỮ LIỆU (PHẦN 3)

### 4. Các ấn phẩm trước đây đã từng dùng dữ liệu tương tự chưa?
- Lần theo dấu vết từ **chú thích chân trang (footnotes)** của các bài báo, sách học thuật hoặc bảng biểu cũ để tìm ra kho lưu trữ gốc và cập nhật dữ liệu mới nhất nhằm so sánh sự thay đổi theo thời gian.

### 5. Điều gì xảy ra nếu CHƯA AI từng thu thập dữ liệu bạn cần?
- Sự vắng mặt của dữ liệu thường không phải do vô tình, mà phản ánh **bất bình đẳng quyền lực**.
- **Case Study: Ngôi sao quần vợt Serena Williams & Tử vong thai sản (2017):**
  - Sau biến chứng nguy hiểm tính mạng khi sinh con, Williams lên tiếng rằng phụ nữ da đen có nguy cơ tử vong khi mang thai/sinh nở **cao gấp hơn $3\text{ lần}$** phụ nữ da trắng.
  - Khi các nhà báo điều tra sâu hơn, họ phát hiện hệ thống y tế Mỹ **không hề có hệ thống quốc gia nào theo dõi biến chứng thai sản**, dù có hệ thống theo dõi rất kỹ bệnh tim hay thay khớp háng.
  - *Bài học:* Các cấu trúc quyền lực thường chỉ đếm những gì họ coi trọng. Nếu dữ liệu chưa tồn tại, việc chỉ ra khoảng trống đó hoặc tự thu thập chính là đóng góp lớn lao.

<div class="img-guide">
🖼️ <b>Gợi ý hình minh họa:</b> Hình ảnh biểu tượng "Khoảng trống dữ liệu" (Missing Dataset) hoặc infographic so sánh tỷ lệ tử vong thai sản ($3\times$) đặt cạnh dấu chấm hỏi lớn về hệ thống thu thập dữ liệu y tế.
</div>

---




## DỮ LIỆU CÔNG KHAI (PUBLIC) VS. RIÊNG TƯ (PRIVATE)

Khi tìm kiếm dữ liệu, người làm trực quan hóa phải nắm rõ các cuộc tranh luận pháp lý và đạo đức:

| Khía cạnh | Dữ liệu Khu vực Tư nhân (Big Tech) | Dữ liệu Khu vực Công (Chính phủ) |
| :--- | :--- | :--- |
| **Thực trạng thu thập** | **Chủ nghĩa tư bản giám sát** (*Surveillance Capitalism* - Shoshana Zuboff): Google (lịch sử tìm kiếm/cookie), Amazon (Alexa ghi âm), Facebook (theo dõi hành vi mua sắm ngoài nền tảng). | Chính phủ thu thập dữ liệu công dân; công chúng dùng **Đạo luật Tự do Thông tin (FOIA)** / *Sunshine Laws* để yêu cầu minh bạch hóa. |
| **Dữ liệu bị cấm công khai cá nhân** | Phụ thuộc vào chính sách riêng và các đạo luật mới nổi (như CCPA của California). | - **HIPAA:** Bảo mật hồ sơ bệnh án của bệnh nhân.<br>- **FERPA:** Bảo mật kết quả học tập của học sinh/sinh viên.<br>$\rightarrow$ *Bắt buộc phải ẩn danh và tổng hợp (Aggregate).* |
| **Dữ liệu cá nhân được công khai vì lợi ích chung** | Dữ liệu di chuyển tổng hợp (như Apple chia sẻ dữ liệu di chuyển iPhone trong đại dịch Covid-19). | 1. Khoản đóng góp tài chính cho ứng viên chính trị (FEC).<br>2. Hồ sơ sở hữu và giá trị bất động sản địa phương.<br>3. Mức lương lãnh đạo các tổ chức miễn thuế (Mẫu IRS 990).<br>4. Hồ sơ sử dụng vũ lực của cảnh sát (*The Force Report*). |

---




## ĐẠO ĐỨC DỮ LIỆU: LÀM MỜ (MASKING) & TỔNG HỢP (AGGREGATING)

<div class="box">
<b>Câu hỏi đạo đức cốt lõi:</b> Ngay cả khi dữ liệu cá nhân là <i>hợp pháp và công khai</i>, việc tái xuất bản nó lên biểu đồ/bản đồ có gây hại cho cá nhân (nạn nhân) nhiều hơn là mang lại lợi ích cho cộng đồng không?
</div>

**Ví dụ thực tế: Bản đồ cuộc gọi cảnh sát 911 về tội phạm bạo lực**
Một số sở cảnh sát công bố dữ liệu mở kèm địa chỉ chính xác của nạn nhân. Nếu đưa thẳng lên bản đồ, bạn có thể gây tổn thương tâm lý hoặc nguy hiểm vật lý cho họ. Có 2 giải pháp xử lý:

1. **Giải pháp 1: Làm mờ thông tin nhạy cảm (Masking)** — Ẩn các ký tự cuối của địa chỉ:
   - *Dữ liệu gốc (Nguy hiểm):* `Jan 1 | 1234 Main St | Aggravated Assault`
   - *Dữ liệu đã làm mờ (An toàn hơn):* `Jan 1 | 1XXX Main St | Aggravated Assault`
2. **Giải pháp 2: Tổng hợp theo nhóm lớn (Aggregating)** — Gom nhóm theo khu phố hoặc vùng điều tra dân số (vừa bảo vệ danh tính, vừa làm rõ xu hướng tổng thể):
   - `East Side | Aggravated Assault | Frequency: 13`
   - `West Side | Aggravated Assault | Frequency: 21`

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 10-11 PDF / Trang 79-80 Sách):</b> Vẽ sơ đồ mũi tên chuyển đổi từ 1 bảng dữ liệu địa chỉ chi tiết (`1234 Main St`) tách thành 2 nhánh: Nhánh 1 là bảng Masked (`1XXX Main St`) và Nhánh 2 là bảng Aggregated theo Neighborhood (`East Side: 13, West Side: 21`).
</div>

---




## QUẢN TRỊ NGUỒN DỮ LIỆU (SOURCE YOUR DATA)

Để đảm bảo **tính minh bạch, độ tin cậy và khả năng tái lập (replicability)** cho dự án, hãy rèn luyện thói quen 3 bước ngay khi tải dữ liệu về:

1. **Bước 1: Đặt tên file có ý nghĩa (Meaningful Filenames)**
   - ❌ *Tên file tệ (Cần tránh):* `data.csv`, `file.ods`, `download.xlsx`
   - ✅ *Tên file chuẩn (Nguồn + Từ khóa + Ngày tháng `YYYY-MM-DD`, chữ thường, không khoảng trắng):*
     - `town-demographics-2019-12-02.csv`
     - `eurostat-1999-2019-co2-emissions.xlsx`
2. **Bước 2: Tạo tab `notes` riêng biệt bên trong bảng tính**
   - Ghi rõ tổ chức phát hành, đường link gốc, định nghĩa các nhãn viết tắt, người tải và ngày cập nhật.
3. **Bước 3: Tạo bản sao lưu độc lập (Tab `backup`)**
   - Nhân bản dữ liệu gốc sang một tab tên là `backup` và **tuyệt đối không chạm vào nó** trước khi bắt đầu chỉnh sửa hay làm sạch trên tab `data`.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 14 PDF / Trang 83 Sách):</b> Chèn <b>Figure 3.3</b> chụp giao diện bảng tính có 3 tab rõ ràng ở đáy: <code>data</code> | <code>notes</code> | <code>backup</code> cùng nội dung ghi chú nguồn kiểm tra nhà hàng tại New York.
</div>

---




## NHẬN DIỆN "DỮ LIỆU XẤU" (RECOGNIZE BAD DATA) — PHẦN 1

Dựa trên cẩm nang nổi tiếng *The Quartz Guide to Bad Data*, hãy kiểm tra ngay 5 dấu hiệu cảnh báo sau khi mở file dữ liệu:

- **1. Giá trị khuyết thiếu (Missing Values) bị nhập sai:**
  - Ô trống (`blank`/`null`) có ý nghĩa hoàn toàn khác với số `0`.
  - **Cảnh báo:** Nhiều người nhập `0` hoặc `-1` hoặc `-999` để đại diện cho "không có dữ liệu", làm sai lệch hoàn toàn các hàm tính toán như `SUM` hay `AVERAGE`.
- **2. Mất số 0 ở đầu (Missing Leading Zeros):**
  - Xảy ra khi bảng tính tự động ép kiểu văn bản (Text) sang kiểu số (Number).
  - *Ví dụ:* Mã bưu chính (Zip code) của Hartford là `06106` bị biến thành `6106`. Mã FIPS của Quận Los Angeles là `037` bị cắt thành `37` (làm hệ thống hiểu nhầm thành mã bang Bắc Carolina!).
- **3. Chạm ngưỡng giới hạn dòng/cột của phần mềm cũ:**
  - Nếu dữ liệu dừng đột ngột ở đúng dòng thứ **$65.536$** (giới hạn Excel `.xls` cũ) hoặc cột **$255$** $\rightarrow$ Dữ liệu đã bị cắt cụt! *(Thực tế: Cơ quan Y tế Công cộng Anh từng làm mất hàng ngàn kết quả xét nghiệm Covid-19 vì lỗi giới hạn dòng này).*
- **4. Lỗi định dạng ngày tháng bất nhất:**
  - Nhầm lẫn giữa chuẩn Mỹ `MM/DD/YYYY` (`11/3/2020` là ngày 3/11) và chuẩn quốc tế `DD/MM/YYYY` (ngày 11/3).
  - Xuất hiện ngày mặc định hệ thống (`1/1/1900`, `1904`, `1970`) hoặc số thứ tự nội bộ của Excel (ví dụ: ngày 1/3/2020 bị hiển thị thành con số `43891`).

---




## NHẬN DIỆN "DỮ LIỆU XẤU" — CÁI BẪY GEOCODING SAI LỆCH

Khi chuyển đổi địa chỉ hoặc địa chỉ IP thành tọa độ địa lý (Kinh độ/Vĩ độ), các công cụ tự động có thể tạo ra những "ảo giác dữ liệu" hài hước nhưng nguy hiểm:

- **Trường hợp 1: Huyền thoại tại tiểu bang Kansas (Alberto Cairo)**
  - Một bản đồ từng chỉ ra cư dân vùng đồng quê Bắc Kansas xem nội dung người lớn trực tuyến nhiều nhất nước Mỹ.
  - **Sự thật:** Hàng triệu địa chỉ IP ẩn danh (dùng VPN) không xác định được vị trí cụ thể đã bị phần mềm Geocoding tự động gán vào **tâm địa lý chính xác của lục địa Mỹ** — tình cờ nằm tại một trang trại ở Bắc Kansas!
- **Trường hợp 2: Sự bùng nổ dân số tại "Đảo Null" (Imaginary Null Island)**
  - Trên quy mô toàn cầu, các dữ liệu bị lỗi tọa độ hoặc khuyết thiếu vị trí thường bị gán mặc định về tọa độ $(0, 0)$ (giao điểm giữa đường Xích đạo và Kinh tuyến gốc).
  - Vị trí này thực chất chỉ là một phao thời tiết giữa Đại Tây Dương (ngoài khơi Tây Phi), được giới dữ liệu gọi vui là **"Null Island"**.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 16 PDF / Trang 85 Sách):</b> Chèn <b>Figure 3.4</b> hiển thị 2 bản đồ cạnh nhau: Bên trái là chấm đỏ tại <i>Geographic Center of Contiguous US</i> (Kansas), bên phải là chấm đỏ tại <i>Imaginary Null Island</i> ở tọa độ $(0,0)$.
</div>

---




## PHẢN BIỆN SÂU DỮ LIỆU (QUESTION YOUR DATA)

Máy tính không thể làm thay bước này — bạn phải đọc kỹ **Metadata** để chất vấn 3 tầng ý nghĩa ẩn sau các con số:

1. **Nhãn cột (Column Headers) thực sự có nghĩa là gì?**
   - Cột `Elevation` (Độ cao) tính bằng mét hay feet?
   - Cột `Income` (Thu nhập) tính theo cá nhân, gia đình hay hộ gia đình? Là số trung bình (`Mean`) hay trung vị (`Median`)?
2. **Dữ liệu được thu thập như thế nào & Sai số (Margin of Error) ra sao?**
   - Khảo sát Cộng đồng Mỹ (ACS) lấy mẫu nhỏ ở cấp khu vực (khoảng $4.000\text{ dân}$) có thể cho kết quả thu nhập trung bình là $\$50.000$ nhưng **sai số lên tới $\pm \$25.000$** (tức giá trị thực nằm từ $\$25.000$ đến $\$75.000$ $\rightarrow$ gần như vô nghĩa nếu không chú thích!).
3. **Dữ liệu mang tính "Kiến tạo Xã hội" (Socially Constructed) đến mức nào?**
   - Các danh mục phân loại thay đổi theo quyền lực chính trị và thời gian.
   - *Ví dụ:* Trong 100 năm Điều tra Dân số Mỹ, danh mục chủng tộc liên tục bị định nghĩa lại: Tách `Native White` và `Foreign-born White` (1930) $\rightarrow$ chuyển `Mexican` qua lại giữa `Other races` và `White` $\rightarrow$ đổi `Negro` thành `Black` (1980) $\rightarrow$ cho phép chọn đa chủng tộc (2000).

---




<!-- _class: lead -->
# 02. KỸ THUẬT LÀM SẠCH DỮ LIỆU BẨN
### CHƯƠNG 4: CLEAN UP MESSY DATA

<div class="pill">"Đừng ngạc nhiên nếu bạn dành nhiều thời gian để dọn dẹp dữ liệu hơn là phân tích và vẽ biểu đồ."</div>

---




## THỰC TRẠNG PHŨ PHÀNG CỦA DỮ LIỆU THÔ (RAW DATA)

Hiếm khi nào dữ liệu tải về có thể đưa vào vẽ biểu đồ ngay lập tức. Một bảng dữ liệu thực tế thường chứa đầy "rác" cấu trúc:

| Year | City | Amount | Các lỗi "kinh điển" xuất hiện trong bảng bên |
| :--- | :--- | :--- | :--- |
| `1990` | `New York City` | `$1,123,456.00` | - **Cột Year:** Lẫn lộn năm đơn lẻ (`1990`), khoảng năm (`1995-96`) và thập kỷ (`2000s`). |
| `1995-96` | *(Trống)* | `2.2 mil` | - **Cột City:** Ô bị bỏ trống, viết tắt tùy tiện (`NYC`), dùng dấu gạch dưới (`New_York`). |
| `2000s` | `NYC` | `No data` | - **Cột Amount:** Trộn lẫn ký hiệu tiền tệ (`$`), chữ viết tắt (`mil`), chữ báo khuyết (`No data`) và dấu cộng (`5000000+`) khiến máy tính hiểu nhầm toàn bộ cột số thành văn bản (Text)! |
| `2020` | `New_York` | `5000000+` | |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 20 PDF / Trang 89 Sách):</b> Chèn <b>Figure 4.1</b> (Bản phác thảo viết tay bảng dữ liệu lộn xộn với các dòng <code>1990 | New York City | $1,123,456.00</code>...).
</div>

---




## KỸ THUẬT 1: XỬ LÝ TRÙNG LẶP, KHOẢNG TRẮNG & KÝ TỰ THỪA

Để máy tính hiểu đúng dữ liệu, ta phải chuẩn hóa từng ô về định dạng nguyên thủy:

1. **Loại bỏ bản ghi trùng lặp (Duplicates) & Khoảng trắng thừa (Whitespaces):**
   - Các khoảng trắng vô hình ở đầu hoặc cuối chuỗi (Trailing spaces, ví dụ `"Brazil "` thay vì `"Brazil"`) khiến máy tính coi đây là 2 quốc gia khác nhau khi gom nhóm hoặc nối bảng.
2. **Tách bỏ đơn vị đo lường và ký hiệu khỏi cột số:**
   - Phải xóa bỏ `$`, `,`, `kg`, `%` hoặc các hậu tố chữ (`282,805a` $\rightarrow$ `282805`) để chuyển chuỗi văn bản (thường căn trái) về định dạng số thực thụ (thường căn phải).
3. **Cẩn trọng khi Tìm và Thay thế hàng loạt (Find & Replace):**
   - **Bài toán thực tế:** Dữ liệu dân số 169 thị trấn ở Connecticut luôn thừa chữ `"town"` ở cuối (`Hartford town`, `New Haven town`, `Newtown town`).
   - **Bẫy kỹ thuật:** Nếu tìm chữ `"town"` và thay bằng khoảng trống, tên thị trấn **`Newtown`** sẽ bị biến dạng thành **`New`**!
   - **Giải pháp chuẩn:** Phải tìm kiếm chính xác chuỗi **`" town"` (có một dấu cách ở đằng trước)** để vừa bảo toàn từ `Newtown`, vừa không để lại khoảng trắng thừa ở cuối câu.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 24 PDF / Trang 93 Sách):</b> Chèn <b>Figure 4.3</b> có mũi tên đỏ ghi chú <i>"Make sure it begins with a space character"</i> trước chữ <code> town</code>.
</div>

---




## KỸ THUẬT 2: TÁI CẤU TRÚC BẢNG (TRANSPOSE, SPLIT & COMBINE)

Dữ liệu sạch về nội dung nhưng sai về **hình dáng cấu trúc** cũng không thể vẽ được biểu đồ:

### 1. Xoay trục Dữ liệu — Hàng thành Cột (Transpose)
- **Mâu thuẫn góc nhìn (Stephen Few):**
  - Khi trình bày **Bảng (Table)** cho người đọc, thời gian thường xếp **nằm ngang** theo tiêu đề cột từ trái sang phải (`2000 | 2010 | 2020`).
  - Khi vẽ **Biểu đồ đường (Line Chart)**, phần mềm lại yêu cầu thời gian phải chạy **thẳng đứng** theo cột đầu tiên từ trên xuống dưới.
- $\rightarrow$ Kỹ thuật **Transpose** giúp đảo ngược ma trận Hàng $\leftrightarrow$ Cột chỉ trong một bước mà không cần gõ lại.

### 2. Tách cột (Split) và Gộp cột (Combine / Concatenate)
- **Tách cột (Splitting):** Khi nhiều thực thể bị nhét chung vào 1 ô, cần tách theo dấu phân cách (dấu phẩy, khoảng trắng, hoặc ký tự tùy chỉnh như hai dấu gạch ngang `--`):
  - `300 Summit St, Hartford CT--06106` $\rightarrow$ Tách thành 4 cột: `Street` | `City` | `State` | `Zip`.
- **Gộp cột (Concatenating):** Ngược lại, khi cần đưa dữ liệu vào công cụ bản đồ (Geocoding), ta nối các cột rời rạc lại thành một địa chỉ hoàn chỉnh kèm dấu phẩy phân cách.

---




## KỸ THUẬT 3: GOM CỤM CHUẨN HÓA TÊN GỌI BẤT NHẤT (CLUSTERING)

Khi gộp dữ liệu từ nhiều nguồn hoặc từ phiếu khảo sát tự điền, cùng một thực thể có thể bị viết theo hàng chục cách khác nhau.

- **Ví dụ thực tế từ Dữ liệu Viện trợ Nước ngoài của Mỹ (Greenbook Dataset):**
  - Chỉ riêng 2 quốc gia là **Triều Tiên (North Korea)** và **Hàn Quốc (South Korea)** nhưng trong cột `Country` xuất hiện tới **26 cách viết khác nhau**:
    - `Korea, N` | `Korea-North` | `Korea North` | `North Korea` | `N Korea` | `Korea, No`...
    - `SouthKorea` | `south Korea` | `So Korea` | `Korea, South`...
  - Đồng thời cột `Funding Agency` cũng bị viết sai chính tả: `Dept of Agriculture`, `Department of Argic`, `Department - Agriculture`.
- **Giải pháp Gom cụm thông minh (Clustering Algorithms):**
  - Thay vì dò bằng mắt thường qua hàng vạn dòng, sử dụng thuật toán gom cụm dựa trên **độ tương đồng chuỗi ký tự**:
    1. *Key Collision (Fingerprinting):* Chuẩn hóa chữ hoa/thường, bỏ dấu câu, sắp xếp lại từ khóa để phát hiện nhanh các biến thể giống nhau (tốc độ cao, phù hợp dữ liệu lớn).
    2. *Nearest Neighbor (Láng giềng gần nhất):* Tính khoảng cách chỉnh sửa giữa các chuỗi để bắt các lỗi chính tả phức tạp (độ chính xác tinh vi hơn).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 33 & 39 PDF / Trang 102 & 108 Sách):</b> Ghép <b>Figure 4.11</b> (Bảng dữ liệu thô có hàng loạt kiểu viết Korea) và <b>Figure 4.18</b> (Giao diện gom cụm 7 biến thể của South Korea về 1 tên chuẩn duy nhất).
</div>

---




<!-- _class: lead -->
# 03. TẠO PHÉP SO SÁNH CÓ Ý NGHĨA
### CHƯƠNG 5: MAKE MEANINGFUL COMPARISONS

<div class="pill">"Trọng tâm của tư duy định lượng nằm ở một câu hỏi duy nhất: So sánh với cái gì? (Compared to what?)" — Edward Tufte</div>

---




## SỰ CHÍNH XÁC TRONG NGÔN TỪ (1): MEAN VS. MEDIAN

Trong giao tiếp hàng ngày, người ta hay gọi chung là "trung bình" (average), nhưng trong phân tích dữ liệu, việc chọn sai đại lượng sẽ bóp méo hoàn toàn câu chuyện:

- **Trung bình cộng (Mean):** Tổng tất cả giá trị chia cho số lượng phần tử. **Rất nhạy cảm và dễ bị kéo lệch bởi các giá trị ngoại lai (Outliers).**
- **Trung vị (Median / Phân vị thứ 50):** Giá trị nằm ở chính giữa dãy số đã sắp xếp. **Kháng nhiễu tuyệt đối trước các giá trị cực đoan ở hai đầu.**

| Dãy số khảo sát | Giá trị các phần tử | Trung bình cộng (Mean) | Trung vị (Median) |
| :--- | :--- | :---: | :---: |
| **Dãy chuẩn (Đồng đều)** | $1, \; 2, \; \mathbf{3}, \; 4, \; 5$ | **$3$** | **$3$** |
| **Khi xuất hiện Outlier ($100$)** | $1, \; 2, \; \mathbf{3}, \; 4, \; 100$ | **$22$** *(Tăng vọt ảo!)* | **$3$** *(Giữ nguyên)* |

<div class="box">
💡 <b>Câu chuyện kinh điển:</b> <i>"Khi một tỷ phú bước vào phòng, xét theo số Trung bình (Mean) thì tất cả mọi người trong phòng bỗng chốc trở thành triệu phú. Nhưng xét theo Trung vị (Median), không ai giàu lên cả."</i> $\rightarrow$ Luôn ưu tiên dùng <b>Median</b> khi so sánh thu nhập, giá nhà, tài sản!
</div>

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 43 PDF / Trang 112 Sách):</b> Chèn <b>Figure 5.1</b> chụp bảng tính đối chiếu dãy <code>1, 2, 3, 4, 100</code> cho kết quả <code>Mean = 22</code> và <code>Median = 3</code>.
</div>

---




## SỰ CHÍNH XÁC TRONG NGÔN TỪ (2): $\%$ CHANGE VS. ĐIỂM $\%$

Sự nhầm lẫn giữa **Thay đổi phần trăm (Percent Change)** và **Điểm phần trăm (Percentage Point Difference)** là công cụ thao túng số liệu phổ biến nhất trong chính trị và truyền thông:

- **1. Thay đổi phần trăm (Percent Change / Relative Change):** Đo mức độ biến thiên tương đối so với gốc ban đầu:
  $$\text{Percent Change} = \frac{\text{Giá trị Mới} - \text{Giá trị Cũ}}{|\text{Giá trị Cũ}|} \times 100\%$$
- **2. Chênh lệch điểm phần trăm (Percentage Point Difference):** Phép trừ trực tiếp giữa hai con số bản thân chúng đã là phần trăm:
  $$\text{Percentage Point Difference} = \text{Phần trăm Mới} - \text{Phần trăm Cũ}$$

### Ví dụ thực tế: Mánh khóe tăng thuế bán hàng (Sales Tax)
Giả sử một chính trị gia đề xuất tăng thuế tiêu dùng từ **$5\%$ lên $6\%$** và tuyên bố trước cử tri: *"Mức thuế chỉ tăng có $1\%$ thôi!"* $\rightarrow$ **Tuyên bố này hoàn toàn SAI!**
- ✅ **Cách nói đúng 1:** Mức thuế tăng thêm **$1\text{ điểm phần trăm}$** ($6\% - 5\% = 1\text{ percentage point}$).
- ✅ **Cách nói đúng 2:** Gánh nặng thuế của người dân tăng tới **$20\%$** vì:
  $$\frac{6 - 5}{5} = \frac{1}{5} = 0.20 = 20\%$$

---




## SỰ CHÍNH XÁC TRONG NGÔN TỪ (3): TƯƠNG QUAN $\neq$ NHÂN QUẢ

Hãy cực kỳ thận trọng với các động từ ám chỉ quan hệ nhân quả trong bài thuyết trình như: *"dẫn đến" (leads to)*, *"thúc đẩy" (promotes)*, *"gây ra" (sparks/causes)*.

- **Tương quan (Correlation):** Hai biến số cùng biến thiên hoặc có liên hệ phụ thuộc lẫn nhau trên biểu đồ (ví dụ: Tuổi thọ trung bình càng cao thì Tỷ lệ sinh càng thấp).
- **Nhân quả (Causation):** Sự thay đổi của biến độc lập trực tiếp tạo ra sự thay đổi ở biến phụ thuộc.
- **3 bước bắt buộc nếu muốn khẳng định Quan hệ Nhân quả:**
  1. Chứng minh có sự **tương quan (correlation)** rõ rệt về mặt thống kê giữa hai biến.
  2. Xây dựng được một **lý thuyết giải thích thuyết phục** về cơ chế tác động từ biến nguyên nhân sang biến kết quả.
  3. **Xác định và cô lập mọi biến gây nhiễu (Confounding variables)** — những yếu tố ẩn bên ngoài có thể đang đồng thời chi phối cả hai biến số bạn đang xét.

<div class="img-guide">
🖼️ <b>Gợi ý hình minh họa:</b> Vẽ sơ đồ tam giác: Biến A $\leftrightarrow$ Biến B (Nét đứt: Tương quan quan sát thấy), và ở đỉnh trên là "Biến gây nhiễu ẩn (Confounding Variable C)" chiếu hai mũi tên nét liền tác động xuống cả A và B.
</div>

---




## CHUẨN HÓA DỮ LIỆU (NORMALIZE YOUR DATA)

So sánh các **số đếm thô (raw counts)** giữa các đơn vị có quy mô khác nhau là sai lầm sơ đẳng. **Chuẩn hóa (Normalization)** là quy đổi dữ liệu về một thước đo tham chiếu chung (tỷ lệ/rates).

### Case Study: Đâu là tiểu bang an toàn nhất nước Mỹ về giao thông năm 2018? (Alberto Cairo & IIHS)

| Lần thử nghiệm | Câu hỏi đặt ra & Công thức chuẩn hóa | Top 3 Bang "An toàn nhất" | Tại sao phép so sánh này vẫn chưa hoàn hảo? |
| :--- | :--- | :--- | :--- |
| **Lần 1: Dùng số đếm thô** | Bang nào có tổng số người chết vì tai nạn thấp nhất? (Số thô) | 1. Washington D.C. ($31$)<br>2. Rhode Island ($59$)<br>3. Vermont ($68$) | **Bất công:** Đây đều là những nơi cực kỳ ít dân so với California hay Texas! |
| **Lần 2: Chuẩn hóa theo Dân số** | Bang nào có tỷ lệ tử vong trên $100.000\text{ dân}$ thấp nhất?<br>$\frac{\text{Số ca tử vong}}{\text{Dân số}} \times 100.000$ | 1. Washington D.C. ($4,4$)<br>2. New York ($4,8$)<br>3. Massachusetts ($5,2$) | **Chưa chuẩn:** Đây là hành lang đô thị Đông Bắc, người dân đi tàu điện ngầm/tàu hỏa chứ ít lái xe hơi! |
| **Lần 3: Chuẩn hóa theo Quãng đường lái xe (VMT)** | Bang nào có tỷ lệ tử vong trên $100\text{ triệu dặm}$ xe chạy thấp nhất?<br>$\frac{\text{Số ca tử vong}}{\text{Triệu dặm VMT}} \times 100$ | 1. Massachusetts ($0,54$)<br>2. Minnesota ($0,63$)<br>3. New Jersey ($0,73$) | *Washington D.C. văng khỏi Top 5!* Phép so sánh này phản ánh sát thực tế rủi ro khi tham gia giao thông hơn hẳn. |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 46-47 PDF / Trang 115-116 Sách):</b> Trình bày sự thay đổi thứ hạng qua 3 bảng <b>Table 5.1, Table 5.2 và Table 5.3</b> để khán giả thấy rõ D.C. và New York thay đổi vị trí thế nào khi đổi mẫu số chuẩn hóa.
</div>

---




## CÁC PHƯƠNG PHÁP CHUẨN HÓA KHÁC & KHI NÀO KHÔNG CẦN CHUẨN HÓA?

Ngoài tỷ lệ theo đầu người (*per capita*), khi phân tích dữ liệu chuyên sâu cần lưu ý:

- **1. Điều chỉnh theo lạm phát và sức mua (Dữ liệu chuỗi thời gian):**
  - Không thể so sánh trực tiếp thu nhập $\$10.000$ năm 1970 với $\$10.000$ năm 2020.
  - Phải quy đổi từ **Dữ liệu danh nghĩa (Nominal data)** sang **Dữ liệu thực (Real data / Constant dollars)** để phản ánh đúng sức mua.
- **2. Điều chỉnh theo mùa vụ (Seasonal Adjustment):**
  - Loại bỏ biến động chu kỳ tự nhiên (ví dụ: doanh thu du lịch luôn tăng vào mùa hè, mua sắm tăng vào dịp lễ cuối năm) để thấy xu hướng thực chất.
- **3. Chỉ số hóa (Indexing) & Điểm chuẩn hóa ($z\text{-score}$):**
  - Đưa các biến có đơn vị đo khác nhau về cùng một mốc gốc (Base 100) hoặc độ lệch chuẩn.

<div class="box">
⚠️ <b>Khi nào KHÔNG CẦN chuẩn hóa dữ liệu?</b><br>
Khi biến số đó bản chất đã là một <b>đại lượng đo lường trên thang quy chiếu chung (Measured variables)</b>. Ví dụ: <b>Độ tuổi trung vị (Median Age)</b> (con người đều sống trong khoảng $0\text{–}120\text{ tuổi}$) hoặc <b>Thu nhập hộ gia đình trung vị (Median Income)</b> (xét trong cùng một năm và cùng một đơn vị tiền tệ) có thể đem ra so sánh trực tiếp giữa các thành phố.
</div>

---




## CẢNH GIÁC VỚI 3 BẪY THIÊN VỊ CHỌN MẪU (SAMPLING BIASES)

Ngay cả khi không cố tình "chọn quả anh đào" (*cherry-picking*), dữ liệu của bạn vẫn có thể bị bóp méo nghiêm trọng từ khâu lấy mẫu:

### 1. Thiên vị chọn mẫu (Selection Bias)
- Mẫu được chọn khác biệt có hệ thống so với tổng thể chung (*"Những gì bạn thấy phụ thuộc vào nơi bạn nhìn"* — Bergstrom & West).
- **Ví dụ:** Nếu bạn đứng trước cửa phòng tập Gym sau giờ tập bóng rổ để đo chiều cao ngẫu nhiên người đi ra, bạn sẽ kết luận sai lầm rằng chiều cao trung bình của dân số cao vượt trội!

### 2. Thiên vị không phản hồi (Non-response Bias)
- Những người từ chối trả lời khảo sát có đặc điểm khác biệt hoàn toàn với người trả lời.
- **Ví dụ thực tế:** Trong khảo sát thu nhập của US Census năm 2020 (đại dịch Covid-19), nhóm hộ gia đình thu nhập thấp có tỷ lệ không phản hồi cao bất thường $\rightarrow$ chỉ còn người giàu trả lời, làm mức thu nhập trung vị báo cáo bị **đội lên cao giả tạo**.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 49 PDF / Trang 118 Sách):</b> Chèn <b>Figure 5.2</b> minh họa <i>Selection bias</i> (Khung màu xanh khoanh vùng <code>Gym</code> chứa toàn các thanh cao vượt trội so với <code>General population</code> xung quanh).
</div>

---




## BẪY THIÊN VỊ TỰ LỰA CHỌN (SELF-SELECTION BIAS) & CÁCH KHẮC PHỤC

### 3. Thiên vị tự lựa chọn (Self-selection Bias)
- Thường xảy ra khi đánh giá hiệu quả của một chương trình (phòng khám giảm cân, dịch vụ xã hội, trường học tự chọn) nơi người tham gia **tự nguyện đăng ký**.
- ❌ **Cách so sánh SAI:** So sánh trực tiếp nhóm không tham gia (**Nhóm A**) với nhóm tự nguyện đăng ký giảm cân (**Nhóm B**).
  - *Lý do:* Nhóm B ngay từ đầu đã có **động lực (motivation) và ý thức ăn kiêng/tập luyện cao hơn hẳn** Nhóm A!
- ✅ **Giải pháp thiết kế chuẩn (Chia ngẫu nhiên):**
  - Lấy toàn bộ những người đã tình nguyện đăng ký (**Nhóm B** — có cùng mức độ quyết tâm), sau đó **chia ngẫu nhiên (Randomly split)** thành **Nhóm C** (áp dụng phác đồ 1) và **Nhóm D** (áp dụng phác đồ 2) để so sánh công bằng!

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 50 PDF / Trang 119 Sách):</b> Chèn <b>Figure 5.3</b> minh họa sơ đồ: Không so sánh <code>(A) non-participants</code> với <code>(B) participants</code>, mà cho nhóm <code>(B)</code> đi qua cánh cửa tách ngẫu nhiên (<code>random</code>) thành hai nhóm <code>(C)</code> và <code>(D)</code>.
</div>

---




<!-- _class: lead -->
# TỔNG KẾT PHẦN 1
### HÀNH TRANG TRƯỚC KHI VẼ BIỂU ĐỒ

1. **Tìm kiếm & Phản biện (Ch. 3):** Đặt câu hỏi sắc bén, tôn trọng quyền riêng tư (Masking/Aggregating), ghi chú nguồn gốc (`data` - `notes` - `backup`) và kiểm tra kỹ "Dữ liệu xấu" cùng Metadata.
2. **Làm sạch & Chuẩn hóa Cấu trúc (Ch. 4):** Dọn sạch khoảng trắng, tách/gộp cột, xoay trục (Transpose) và gom cụm (Cluster) các tên gọi bất nhất.
3. **So sánh Công bằng (Ch. 5):** Dùng từ chuẩn xác (ưu tiên *Median*, phân biệt *Điểm phần trăm*), chuẩn hóa số thô sang tỷ lệ hợp lý và loại bỏ bẫy thiên vị chọn mẫu.

<div class="pill">Tiếp theo: Phần 2 — Trực quan hóa Biểu đồ Thực chiến (Chart Your Data - Chương 6)</div>
---



<!-- _class: lead -->
# TRỰC QUAN HÓA BIỂU ĐỒ THỰC CHIẾN
# CHART YOUR DATA

<div class="pill">Nguyên Lý Thiết Kế Thị Giác & Lựa Chọn Biểu Đồ Kể Chuyện (Chương 6)</div>

**Phần 2 — Bài Thuyết Trình Trực Quan Hóa Dữ Liệu**
Dựa trên tác phẩm *Hands-On Data Visualization* (Jack Dougherty & Ilya Ilyankou)

<!-- 
[Ghi chú thuyết trình]:
Sau khi đã có một bộ dữ liệu sạch và được chuẩn hóa công bằng ở Phần 1, bước tiếp theo là biến những con số khô khan thành hình ảnh trực quan. Một độ dốc của đường kẻ hay một cụm điểm phân tán có thể truyền tải thông điệp tới mắt người đọc nhanh hơn bất kỳ bảng số liệu nào. Phần 2 sẽ đi sâu vào giải phẫu đồ thị, các nguyên tắc thiết kế cốt lõi và cách chọn đúng loại biểu đồ cho từng câu chuyện dữ liệu.
-->

---



## NỘI DUNG TRÌNH BÀY (OUR CONTENTS)

**01. Tư duy Thiết kế & Giải phẫu Cấu trúc Đồ thị**
- Khi nào nên (và không nên) vẽ biểu đồ?
- Giải phẫu các thành phần chuẩn của một biểu đồ (Anatomy of a Chart)

**02. Hai Nguyên Tắc Bất Di Bất Dịch & Thẩm Mỹ Thị Giác**
- Nguyên tắc Gốc $0$ (Zero-baseline) cho Biểu đồ Cột/Thanh vs. Ngoại lệ ở Biểu đồ Đường
- Nguyên tắc Tổng $100\%$ và quy tắc Kim đồng hồ cho Biểu đồ Tròn
- Loại bỏ "Rác đồ họa" (Chart Junk), tối ưu nhãn, bố cục và nguyên tắc phối màu

**03. Các Nhóm Biểu Đồ Thực Chiến & Câu Chuyện Dữ Liệu**
- Nhóm so sánh danh mục: Cột ghép (Grouped), Cột tách cụm (Split), Cột chồng (Stacked)
- Nhóm phân bố & Chuỗi thời gian: Histogram, Line Chart, Stacked Area, Annotated & Filtered Line
- Nhóm biểu đồ nâng cao: Range Chart (Bất bình đẳng), Scatter Plot & Bubble Chart (Tương quan đa biến)

---



<!-- _class: lead -->
# 01. TƯ DUY THIẾT KẾ & GIẢI PHẪU ĐỒ THỊ
### DECONSTRUCT A CHART & DESIGN PRINCIPLES

<div class="pill">"Chỉ vì dữ liệu có thể biến thành biểu đồ, không có nghĩa là nó nên được vẽ thành biểu đồ."</div>

---



## TƯ DUY CỐT LÕI TRƯỚC KHI VẼ BIỂU ĐỒ

Trước khi chọn loại biểu đồ, hãy dừng lại và trả lời 3 câu hỏi nền tảng:

1. **Quy luật hình ảnh có thực sự quan trọng với câu chuyện của bạn không?**
   - Nếu chỉ cần tra cứu vài con số cụ thể, một **bảng dữ liệu (Table)** hoặc **một câu văn ngắn** đôi khi hiệu quả hơn biểu đồ. Chỉ vẽ biểu đồ khi cần làm nổi bật xu hướng (trends), hình thái phân bố (patterns) hoặc khoảng cách chênh lệch.
2. **Hai yếu tố quyết định việc chọn loại biểu đồ:**
   - **Định dạng dữ liệu hiện có (Data Format):** Dữ liệu liên tục theo thời gian, dữ liệu phân loại danh mục, hay dữ liệu đa biến?
   - **Câu chuyện bạn muốn nhấn mạnh (Data Story):** Bạn muốn so sánh các nhóm, xem tỷ trọng trong tổng thể, hay tìm mối tương quan?
3. **Sự giằng co giữa "Tuân thủ quy tắc" và "Phá vỡ quy tắc" (Lisa Charlotte Rost):**
   - Các quy tắc giúp biểu đồ trung thực và dễ hiểu, nhưng áp dụng máy móc có thể kìm hãm sự sáng tạo.
   - Đôi khi các quy tắc tự mâu thuẫn nhau: *Làm sao vừa tạo ra một biểu đồ đơn giản, dễ hiểu ngay lập tức, lại vừa phản ánh được hết sự phức tạp của dữ liệu?* $\rightarrow$ Hãy tự hỏi: **"Bạn muốn biểu đồ của mình được đánh giá dựa trên giá trị nào?"**

---



## GIẢI PHẪU CẤU TRÚC MỘT BIỂU ĐỒ CHUẨN (ANATOMY OF A CHART)

Một biểu đồ chuyên nghiệp và đáng tin cậy được cấu thành từ 8 bộ phận cốt lõi:

1. **Tiêu đề chính (Title) & Tiêu đề phụ (Subtitle):**
   - *Tiêu đề kể chuyện (Story Title):* Ngắn gọn, nêu bật thông điệp chính (VD: *"Đại dịch tấn công người Da đen và gốc La-tinh nặng nề nhất"*).
   - *Tiêu đề kỹ thuật (Technical Title):* Mô tả biến số, không gian, thời gian (VD: *"Số ca tử vong do Covid-19 theo chủng tộc tại New York, Mùa xuân 2020"*).
   - **Chiến lược kết hợp (Hybrid):** Dùng *Tiêu đề kể chuyện* làm **Title** (chữ to, đậm) và *Tiêu đề kỹ thuật* làm **Subtitle** (chữ nhỏ, màu nhạt hơn ở ngay dưới).
2. **Trục hoành ($x\text{-axis}$) & Trục tung ($y\text{-axis}$):** Xác định thang đo và đơn vị tính.
3. **Chuỗi dữ liệu (Data series) & Điểm dữ liệu (Data points):** Biểu diễn các quan sát.
4. **Nhãn trực tiếp (Labels) & Chú thích (Annotations):** Giải thích bối cảnh ngay trên đồ thị (VD: chỉ mũi tên vào đỉnh thất nghiệp năm 2020 và ghi *"Tác động của Covid-19"*).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 58 PDF / Trang 127 Sách):</b> Chèn <b>Figure 6.1: Common chart components</b> (Sơ đồ giải phẫu đầy đủ vị trí của Title, Subtitle, y-axis, x-axis, data series, data point, Tooltip, Annotation, Legend, Notes/Source/Credits).
</div>

---



## GIẢI PHẪU ĐỒ THỊ: CHÚ GIẢI, NGUỒN, SAI SỐ & TOOLTIP

4 thành phần còn lại quyết định độ minh bạch và trải nghiệm người đọc:

5. **Bảng chú giải (Legend):** Giải thích ý nghĩa của màu sắc và ký hiệu hình học. *(Mẹo: Nếu có thể gắn nhãn trực tiếp vào đường/cột thì nên ẩn Legend đi để biểu đồ thoáng hơn).*
6. **Ghi chú, Nguồn & Tác giả (Notes / Source / Credits):**
   - Đặt ở chân biểu đồ để说明 dữ liệu lấy từ đâu, xử lý thế nào và ai là người thiết kế $\rightarrow$ Xây dựng **uy tín (credibility)** và **trách nhiệm giải trình (accountability)**.
7. **Thanh sai số (Error Bars / Uncertainty):**
   - Nếu dữ liệu lấy từ khảo sát mẫu có biên độ sai số (như dữ liệu thu nhập ACS), hãy vẽ **Error Bars** hoặc ghi chú rõ (VD: *"Biên độ sai số vượt quá $\pm 10\%$ tại khu vực X và Y"*).
8. **Hộp thông tin tương tác (Tooltips):**
   - Rất hữu ích trên web để hiển thị số liệu chi tiết khi di chuột (hover) mà không làm rối mắt.
   - **Lưu ý quan trọng:** Vì Tooltip biến mất khi in ra giấy và khó bấm trên màn hình điện thoại nhỏ, **tuyệt đối không giấu thông tin cốt lõi trong Tooltip** (chỉ dùng cho thông tin phụ trợ *nice-to-have*).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 54 PDF / Trang 123 Sách):</b> Cắt hình đầu tiên trong Bảng 6.1 (<b>Error bars in bar or column chart</b>: <code>Boulder County - Median Income: 78,642 ± 1,583</code>) để minh họa cách biểu diễn thanh sai số chữ $I$ trên đỉnh cột và Tooltip.
</div>

---



<!-- _class: lead -->
# 02. NGUYÊN TẮC BẤT DI BẤT DỊCH & THẨM MỸ ĐỒ THỊ
### UNBREAKABLE RULES & CHART AESTHETICS

<div class="pill">Hai quy tắc không bao giờ được bẻ cong và nghệ thuật tối giản hóa thị giác</div>

---



## QUY TẮC BẤT DI BẤT DỊCH 1: TRỤC BIỂU ĐỒ CỘT/THANH PHẢI BẮT ĐẦU TỪ $0$

- **Tại sao Biểu đồ Cột (Column) và Thanh (Bar) bắt buộc có Gốc $0$ (Zero-baseline)?**
  - Biểu đồ cột và thanh mã hóa giá trị thông qua **chiều dài (length)** và **chiều cao (height)** của khối hình chữ nhật.
  - Mắt người sẽ tự động so sánh tỷ lệ hình học: Một cột cao gấp đôi cột kia **bắt buộc phải đại diện cho giá trị lớn gấp đôi**.
  - *(Quy tắc này cũng áp dụng tương tự cho **Biểu đồ miền - Area Chart** vì phần diện tích tô màu bên dưới đường kẻ cũng đại diện cho độ lớn giá trị).*
- **Hậu quả khi cắt cụt trục tung (Truncated $y\text{-axis}$):**
  - Nếu trục tung bắt đầu từ $300$ thay vì $0$ (với các giá trị khoảng $310\text{–}430$), cột $310$ sẽ trông như biến mất hoàn toàn, phóng đại giả tạo sự chênh lệch (thủ thuật thường dùng để thao túng kết quả thăm dò bầu cử).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 59 PDF / Trang 128 Sách):</b> Chèn <b>Figure 6.2: Start your bar chart at zero</b> — Đối chiếu trực diện biểu đồ bên trái (<i>Good: Y-axis starts at 0</i>, 3 cột A, B, C chênh nhau vừa phải) và bên phải (<i>Bad: Y-axis starts at 300</i>, cột B gần như bẹp dí so với cột A).
</div>

---



## NGOẠI LỆ QUAN TRỌNG: BIỂU ĐỒ ĐƯỜNG (LINE CHART) KHÔNG CẦN GỐC $0$

Trái ngược với biểu đồ cột, quy tắc gốc $0$ **không bắt buộc** đối với Biểu đồ Đường (Line Chart):

- **Giải thích từ chuyên gia Alberto Cairo:**
  - Biểu đồ đường truyền tải thông tin qua **vị trí tương đối (position)** và **góc nghiêng/độ dốc (angle/slope)** của các đoạn thẳng nối tiếp nhau, chứ không phải chiều cao tính từ đáy.
- **Khi nào thu hẹp trục tung của Biểu đồ Đường lại tốt hơn?**
  - Nếu dữ liệu chỉ dao động trong khoảng hẹp từ $90$ đến $100$ (qua các tháng Jan, Feb, Mar):
    - Nếu ép trục tung bắt đầu từ $0$: Đường biểu diễn sẽ nằm bẹp thành một đường ngang gần như phẳng lì ở sát đỉnh đồ thị, **che giấu mất sự biến động thực tế**.
    - Nếu thu hẹp trục tung về khoảng $[90, 100]$: Độ dốc thay đổi được thể hiện rõ nét và phục vụ câu chuyện dữ liệu tốt hơn (miễn là ghi chú nhãn trục rõ ràng để không đánh lừa người xem).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 60–61 PDF / Trang 129–130 Sách):</b> Ghép <b>Figure 6.3</b> và <b>Figure 6.4</b> để thấy rõ: Với Line chart, thu hẹp trục $y$ từ $[0, 100]$ về $[90, 100]$ giúp làm rõ xu hướng tăng từ tháng 1 đến tháng 3 thay vì một đường thẳng nằm ngang vô hồn.
</div>

---



## QUY TẮC BẤT DI BẤT DỊCH 2: BIỂU ĐỒ TRÒN (PIE CHART) PHẢI ĐÚNG $100\%$

Biểu đồ tròn là loại đồ thị gây tranh cãi nhiều nhất vì mắt người ước lượng diện tích góc quạt kém hơn nhiều so với chiều dài thanh thẳng. Nếu sử dụng Pie Chart, phải tuân thủ nghiêm ngặt:

1. **Tổng các phần bắt buộc phải bằng đúng $100\%$ (Parts of a whole):**
   - Nếu tổng khác $100\%$, biểu đồ tròn hoàn toàn vô nghĩa (tác giả gọi đây là *"một tội ác trong trực quan hóa"*).
   - *Ví dụ bẫy khảo sát:* Khảo sát *"Bạn thích Mèo hay Chó?"* nhưng cho phép chọn phương án thứ 3 là *"Tôi thích cả hai"* hoặc cho phép chọn nhiều đáp án $\rightarrow$ Tổng tỷ lệ sẽ vượt $100\%$, **tuyệt đối không được vẽ biểu đồ tròn!**
2. **Quy tắc thiết kế Biểu đồ Tròn chuẩn xác:**
   - **Số lượng lát cắt:** Càng ít càng tốt, **tối đa không quá $5\text{ lát cắt}$**.
   - **Quy tắc Kim đồng hồ (12 o'clock rule):** Đặt lát cắt lớn nhất bắt đầu từ vạch **12 giờ** và sắp xếp các lát cắt tiếp theo giảm dần theo **chiều kim đồng hồ (clockwise)**.
   - **Giải pháp thay thế tốt hơn:** Khi có nhiều hơn 5 danh mục hoặc cần so sánh chính xác, hãy chuyển sang **Biểu đồ cột chồng (Stacked Bar)** hoặc **Biểu đồ thanh ngang (Bar Chart)**.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 62–63 PDF / Trang 131–132 Sách):</b> Chèn <b>Figure 6.6</b> (So sánh 3 hình tròn: <i>OK</i> bắt đầu ở hướng 12h vs. <i>Bad</i> đặt lệch góc vs. <i>Everything is wrong</i> quá nhiều lát cắt lộn xộn) và <b>Figure 6.7</b> (<i>Consider using bar charts instead of pies</i>).
</div>

---



## THẨM MỸ ĐỒ THỊ (1): LOẠI BỎ "RÁC ĐỒ HỌA" & TỐI ƯU BỐ CỤC

Mục tiêu của thiết kế là giúp người đọc hiểu câu chuyện nhanh nhất, không phải phô diễn hiệu ứng:

- **1. Loại bỏ "Rác đồ họa" (Avoid Chart Junk):**
  - Bắt đầu từ nền sáng/trắng tinh giản; tự hỏi xem từng chi tiết thêm vào có làm tăng khả năng đọc (readability) hay không.
  - **Tuyệt đối tránh:** Hiệu ứng khối **3D giả tạo**, bóng đổ (drop shadows), đường viền quá dày, hoặc nền xám rối mắt. *(Chỉ dùng không gian 3D khi biểu diễn dữ liệu có thực sự 3 trục tọa độ $x, y, z$ như bản đồ mật độ địa hình).*
- **2. Đừng bắt khán giả phải "nghiêng đầu" đọc nhãn (Bar vs. Column):**
  - Khi nhãn danh mục ở trục hoành quá dài (như tên các con sông hoặc tên món ăn) khiến chữ bị xoay nghiêng $45^\circ$ hoặc dựng đứng $90^\circ$ $\rightarrow$ Hãy xoay biểu đồ $90^\circ$ thành **Biểu đồ Thanh ngang (Horizontal Bar Chart)** để chữ nằm ngang tự nhiên!
- **3. Sắp xếp các phần tử có trật tự logic (Logical Ordering):**
  - Với dữ liệu phân loại: Sắp xếp theo **giá trị từ cao xuống thấp** (để so sánh thứ hạng) hoặc theo **bảng chữ cái A–Z** (để tra cứu nhanh), không bao giờ để thứ tự ngẫu nhiên.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 62–64 PDF / Trang 131–133 Sách):</b> Ghép 3 hình: <b>Figure 6.5</b> (Loại bỏ cột 3D đổ bóng loè loẹt), <b>Figure 6.8</b> (Xoay ngang biểu đồ tên các con sông để không phải nghiêng cổ đọc), và <b>Figure 6.9</b> (Sắp xếp thanh theo Alphabetical / Values sorted thay vì Random order).
</div>

---



## THẨM MỸ ĐỒ THỊ (2): NGUYÊN TẮC SỬ DỤNG MÀU SẮC & TỐI GIẢN HÓA

Đừng dùng màu sắc chỉ để trang trí — hãy dùng màu sắc để dẫn dắt sự chú ý:

1. **3 Quy tắc chọn bảng màu (Color Palette):**
   - **Đơn sắc (Monochromatic):** Trong đa số trường hợp, một tông màu duy nhất là đủ. Chỉ dùng màu nổi để nhấn mạnh (highlight) đường/cột quan trọng, còn lại hãy để màu xám trung tính.
   - **Hài hòa theo vòng tròn màu:** Dùng các cặp **màu bổ túc (Complementary)** đối diện nhau (như Xanh dương – Cam) để phân tách rõ các nhóm, hoặc **màu tương đồng (Analogous)** đứng cạnh nhau.
   - **Ưu tiên tông màu trầm/đất (Earthier tones):** Chọn xanh navy hoặc xanh ô-liu thay vì xanh neon hay đỏ tươi chói mắt.
2. **3 Câu hỏi kiểm tra tính tiếp cận (Accessibility Checklist):**
   - *Có xung đột ý nghĩa văn hóa không?* (Tránh dùng màu đỏ cho lợi nhuận tích cực hoặc màu xanh lá tươi vui cho tỷ lệ tử vong).
   - *Người mù màu (Color-blindness) có đọc được không?* (Tránh đặt Đỏ và Xanh lá cạnh nhau; kiểm tra bằng công cụ giả lập như *Color Oracle*).
   - *Khi in trắng đen (Grayscale) có phân biệt được không?* (Đảm bảo các màu có độ sáng tối - brightness khác nhau).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 65–66 PDF / Trang 134–135 Sách):</b> Chèn <b>Figure 6.10</b> (Cách dùng màu xanh-cam làm nổi bật 2 đường chính trên nền các đường xám) và <b>Figure 6.11</b> (Đối chiếu biểu đồ <i>A bit too cluttered</i> nhiều vạch kẻ ngang với bản <i>De-cluttered</i> tinh gọn, đưa số trực tiếp vào đầu cột).
</div>

---



<!-- _class: lead -->
# 03. CÁC NHÓM BIỂU ĐỒ THỰC CHIẾN
### CHOOSING THE RIGHT CHART FOR YOUR DATA STORY

<div class="pill">Từ so sánh danh mục, phân bố tần suất đến tương quan đa biến</div>

---



## NHÓM 1: BIỂU ĐỒ SO SÁNH DANH MỤC (GROUPED, SPLIT & STACKED BAR)

Cùng là biểu đồ Cột/Thanh nhưng cách tổ chức bảng dữ liệu sẽ tạo ra 3 câu chuyện khác nhau:

| Loại biểu đồ | Mục đích kể chuyện | Cấu trúc dữ liệu & Case Study thực tế trong sách |
| :--- | :--- | :--- |
| **1. Cột ghép**<br>*(Grouped Column/Bar)* | So sánh trực tiếp các phân nhóm **đứng cạnh nhau (side-by-side)** trên cùng một danh mục. | **Case Study:** Tỷ lệ béo phì ở người trưởng thành Mỹ theo độ tuổi và giới tính (2017–2018).<br>Đặt cột `Men` và `Women` cạnh nhau ở từng nhóm tuổi (`20-39`, `40-59`, `60+`) để thấy sự khác biệt giới tính trong từng độ tuổi. |
| **2. Thanh tách cụm**<br>*(Split Bar/Column)* | So sánh các danh mục **đặc thù riêng của từng nhóm** trong các cụm tách biệt. | **Case Study:** So sánh lượng Calo của các món ăn tại *Starbucks* và *McDonald's*.<br>Vì món *Mocha Frappuccino* chỉ có ở Starbucks và *Big Mac* chỉ có ở McDonald's, bảng dữ liệu **để trống (blank) có chủ đích** các ô chéo nhau để tách thành 2 cụm màu riêng biệt. |
| **3. Cột chồng**<br>*(Stacked Column/Bar)* | So sánh **tỷ trọng các phần trong một tổng thể ($100\%$)** giữa nhiều quốc gia/đối tượng. | **Case Study:** Tỷ lệ dân số theo mức cân nặng (*Overweight, Normal, Underweight*) tại 7 quốc gia (Mỹ, Nam Phi, Ý, Iran, Brazil, Hàn Quốc, Ấn Độ).<br>Thay thế hoàn hảo cho 7 biểu đồ tròn rời rạc! |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 68, 73, 75 PDF / Trang 137, 142, 144 Sách):</b> Ghép bộ 3 biểu đồ: <b>Figure 6.13</b> (Grouped Column - Béo phì Mỹ), <b>Figure 6.23</b> (Split Bar ngang - Calo Starbucks vs McDonald's), và <b>Figure 6.25</b> (Stacked Column - Mức cân nặng 7 nước với phần màu đỏ Overweight nổi bật ở đỉnh).
</div>

---



## NHÓM 2: BIỂU ĐỒ PHÂN BỐ TẦN SUẤT (HISTOGRAM)

Rất nhiều người nhầm lẫn **Histogram** với **Biểu đồ cột (Column Chart)** vì hình dáng bên ngoài giống nhau, nhưng bản chất toán học của chúng hoàn toàn khác biệt:

- **Sự khác biệt cốt lõi giữa Histogram và Column Chart:**
  1. **Loại dữ liệu:** Column Chart biểu diễn *dữ liệu phân loại rời rạc* (táo, chuối, cam); còn Histogram biểu diễn **sự phân bố tần suất của dữ liệu số liên tục** bằng cách gom các giá trị rơi vào từng khoảng chia (**buckets / bins**).
  2. **Khoảng cách giữa các cột:** Column Chart có khe hở ngăn cách giữa các danh mục; còn các cột của Histogram **nằm sát khít nhau** để thể hiện tính liên tục của dãy số.
- **Case Study: Nguồn cung Calo trung bình/người/ngày của 174 quốc gia (FAO, 2017):**
  - Thay vì vẽ 174 cột riêng lẻ không thể đọc nổi, Histogram chia thành các khoảng (bins) mỗi $150\text{–}250\text{ kcal}$.
  - **Phát hiện ngay hình dáng phân bố:** Hầu hết các quốc gia tập trung quanh ngưỡng **$2.800\text{ kcal/ngày}$**, chỉ có 8 quốc gia thiếu hụt dưới $2.000\text{ kcal}$ ở đuôi bên trái và 11 quốc gia vượt quá $3.500\text{ kcal}$ ở đuôi bên phải.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 77 PDF / Trang 146 Sách):</b> Chèn <b>Figure 6.28: Regular histogram chart</b> (Biểu đồ phân bố lượng cung Calo của 174 quốc gia với các ô gạch trắng chia từng nước bên trong mỗi cột bucket).
</div>

---



## NHÓM 3: BIỂU ĐỒ CHUỖI THỜI GIAN — LINE CHART VS. STACKED AREA CHART

Khi làm việc với dữ liệu liên tục theo thời gian (Time-series), việc chọn giữa **Biểu đồ Đường (Line)** và **Biểu đồ Miền chồng (Stacked Area)** phụ thuộc vào câu chuyện bạn muốn kể:

### Case Study: Nguồn cung Thịt Bò, Thịt Lợn và Thịt Gà bình quân đầu người tại Mỹ (1910–2017, USDA)

- **1. Khi dùng Biểu đồ Đường (Line Chart):**
  - *Điểm mạnh:* Cho thấy rõ sự cạnh tranh và giao cắt thứ hạng giữa từng loại thịt riêng lẻ.
  - *Câu chuyện:* Lượng thịt gà tăng trưởng bền bỉ suốt thế kỷ 20 và chính thức **vượt qua cả thịt lợn lẫn thịt bò vào khoảng năm 2000**.
  - *Hạn chế:* Rất khó nhìn ra **tổng lượng thịt tiêu thụ** của cả 3 loại cộng lại tăng hay giảm.
- **2. Khi dùng Biểu đồ Miền chồng (Stacked Area Chart):**
  - *Điểm mạnh:* Là sự kết hợp giữa **Line Chart** (biến thiên theo thời gian) và **Pie Chart** (tỷ trọng các phần trong tổng thể).
  - *Câu chuyện kép:* Cho thấy đồng thời **tổng lượng thịt bình quân đầu người tăng mạnh** sau cuộc Đại suy thoái 1930 (độ cao tổng của miền), và phần diện tích của **thịt gà ngày càng chiếm tỷ trọng lớn** từ sau năm 1970.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 82–83 PDF / Trang 151–152 Sách):</b> Đặt song song <b>Figure 6.33 (Line chart)</b> và <b>Figure 6.34 (Stacked area chart)</b> của cùng bộ dữ liệu Beef, Pork, Chicken (1910–2017) để khán giả thấy ngay sự khác biệt trực quan.
</div>

---



## NÂNG CẤP BIỂU ĐỒ ĐƯỜNG: ANNOTATED LINE & FILTERED LINE CHART

Làm thế nào để biểu đồ đường không bị "câm lặng" thiếu bối cảnh, hoặc không biến thành một "đĩa mì Ý" (*spaghetti chart*) rối rắm khi có hàng trăm đường?

### 1. Biểu đồ Đường có Chú thích Bối cảnh (Annotated Line Chart)
- Trả lời câu hỏi *"So what?" (Vậy thì sao?)* ngay trên mặt phẳng đồ thị bằng 2 công cụ: **Chú thích văn bản (Text Annotations)** và **Tô sáng vùng thời gian (Range Highlights)**.
- **Case Study: Tỷ lệ Thất nghiệp tại Mỹ (2000–2020):**
  - Tô dải nền màu xám dọc theo các giai đoạn suy thoái kinh tế chính thức và gắn nhãn trực tiếp tại 2 đỉnh nhọn: *"Great Recession (2008–2010)"* và đỉnh lịch sử *"Covid Pandemic (2020)"*.

### 2. Biểu đồ Đường có Bộ lọc Tương tác (Filtered Line Chart)
- **Case Study: Tỷ lệ người dùng Internet của hơn 200 quốc gia (1995–2018, World Bank):**
  - Nếu vẽ tất cả 200 quốc gia lên cùng một đồ thị, nó sẽ biến thành một "đĩa mì Ý" hỗn loạn.
  - **Giải pháp:** Mặc định chỉ hiển thị $3\text{–}4$ quốc gia tiêu biểu (VD: *Brazil, Cuba, Nhật Bản, Anh*) với màu sắc tương phản rõ rệt, và cung cấp **danh sách ô tích chọn (Checkboxes Filter)** bên cạnh để người đọc tự bật/tắt quốc gia họ muốn khám phá.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 85 & 104 PDF / Trang 154 & 173 Sách):</b> Ghép <b>Figure 6.35</b> (Biểu đồ thất nghiệp Mỹ có dải xám Great Recession & Covid Pandemic) và <b>Figure 6.57</b> (Biểu đồ Internet Access 1995–2018 có bảng фильтр chọn từng nước bên phải).
</div>

---



## NHÓM 4: BIỂU ĐỒ KHOẢNG CÁCH (RANGE CHART / DUMBBELL PLOT)

Khi mục tiêu chính của bạn là **nhấn mạnh khoảng cách chênh lệch hoặc sự bất bình đẳng (inequality gaps)** giữa hai nhóm, **Range Chart** hiệu quả hơn biểu đồ cột ghép rất nhiều.

- **Cơ chế thị giác:** Thay vì vẽ 2 cột dài từ mốc $0$, Range Chart vẽ 2 chấm tròn ở 2 đầu mút và nối chúng bằng một thanh ngang chuyển sắc (gradient), buộc mắt người tập trung hoàn toàn vào **độ dài của khoảng cách ở giữa**.
- **Case Study: Khoảng cách thu nhập theo Giới tính và Trình độ học vấn tại Mỹ (ACS 2019):**
  - So sánh thu nhập trung vị (Median earnings) của Nam giới (chấm đỏ) và Nữ giới (chấm xanh) qua 5 bậc học vấn (từ *Chưa tốt nghiệp THPT* đến *Sau đại học*).
  - **Phát hiện chấn động từ biểu đồ:**
    1. Ở tất cả mọi cấp độ học vấn, nam giới luôn kiếm được cao hơn nữ giới khoảng **$1,5\text{ lần}$**, và khoảng cách tuyệt đối càng giãn rộng ở bậc học cao.
    2. Một người đàn ông chỉ có bằng **Cử nhân Đại học ($\$69\text{k}$)** kiếm được nhiều tiền hơn cả một người phụ nữ có bằng **Thạc sĩ/Tiến sĩ ($\$64\text{k}$)**!

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 89 PDF / Trang 158 Sách):</b> Chèn <b>Figure 6.39: Earnings by Gender by Education Level in the US, 2019</b> (Biểu đồ Range chart hiển thị rõ các cặp điểm Women - Men: <code>20k–31k</code>, <code>26k–39k</code>, <code>32k–47k</code>, <code>48k–69k</code>, <code>64k–94k</code>).
</div>

---



## NHÓM 5: BIỂU ĐỒ PHÂN TÁN (SCATTER CHART) — TƯƠNG QUAN 2 BIẾN

**Scatter Chart (Biểu đồ phân tán)** là công cụ chuẩn mực nhất để kiểm tra mối liên hệ (correlation) giữa **hai biến số định lượng liên tục** đặt trên trục hoành ($X$) và trục tung ($Y$).

- **Case Study 1 — Tương quan Nghịch (Negative Correlation): Tuổi thọ vs. Tỷ lệ sinh toàn cầu (World Bank, 2018):**
  - Trục $X$: Tuổi thọ trung bình (*Life Expectancy*) | Trục $Y$: Tỷ lệ sinh số con/phụ nữ (*Fertility*).
  - *Quy luật đám mây điểm:* Các chấm quốc gia dốc từ góc trên bên trái (Nigeria, Congo: sinh $5\text{–}6\text{ con}$, tuổi thọ $54\text{–}60$) xuống góc dưới bên phải (Nhật Bản, Pháp: sinh $1,4\text{–}1,9\text{ con}$, tuổi thọ $>82$).
  - *Lưu ý tư duy:* Đây là tương quan, không được kết luận nhân quả rằng "đẻ ít giúp sống thọ hơn"!
- **Case Study 2 — Tương quan Thuận (Positive Correlation): Thu nhập hộ gia đình vs. Điểm thi học khu tại Connecticut (Stanford SEDA):**
  - Trục $X$: Thu nhập hộ gia đình trung vị | Trục $Y$: Điểm thi Toán & Tiếng Anh lớp 6 (so với chuẩn quốc gia).
  - *Quy luật:* Đám mây điểm vươn dốc lên từ trái sang phải $\rightarrow$ Trẻ em ở các học khu giàu có đạt trình độ vượt trước hàng năm học so với các học khu nghèo.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 93 & 99 PDF / Trang 162 & 168 Sách):</b> Ghép 2 biểu đồ <b>Figure 6.44</b> (Tương quan nghịch: Fertility vs Life Expectancy) và <b>Figure 6.51</b> (Tương quan thuận: Median Household Income vs Grade Levels tại Connecticut).
</div>

---



## NHÓM 6: BIỂU ĐỒ BONG BÓNG (BUBBLE CHART) — ĐA BIẾN "TRÊN MỘT MẶT PHẲNG"

Tác giả gọi **Bubble Chart** là *"Scatter chart on steroids"* (Biểu đồ phân tán siêu cấp) vì nó có khả năng nén từ **4 đến 5 chiều dữ liệu (dimensions)** vào trong một khung hình duy nhất:

| Chiều dữ liệu (Dimension) | Kênh mã hóa thị giác (Visual Encoding) | Ví dụ từ Dữ liệu Ngân hàng Thế giới (World Bank 2018) |
| :--- | :--- | :--- |
| **Biến thứ 1 (Định danh)** | Nhãn tên / Tooltip của từng chấm | Tên quốc gia (`Country`: Mỹ, Trung Quốc, Ấn Độ, Nigeria...) |
| **Biến thứ 2 (Định lượng)** | Tọa độ trên **Trục hoành ($X$)** | Tuổi thọ trung bình (`Life Expectancy`: $54\text{–}85\text{ tuổi}$) |
| **Biến thứ 3 (Định lượng)** | Tọa độ trên **Trục tung ($Y$)** | Tỷ lệ sinh (`Fertility`: $1,4\text{–}6,0\text{ con/phụ nữ}$) |
| **Biến thứ 4 (Định lượng)** | **Kích thước bong bóng (Bubble Size)** | Quy mô dân số (`Population`: Hai quả bóng khổng lồ màu vàng của Trung Quốc và Ấn Độ $\sim 1,35\text{–}1,39\text{ tỷ dân}$) |
| **Biến thứ 5 (Phân loại)** | **Màu sắc bong bóng (Bubble Color)** | Khu vực địa lý (`Region`: Châu Á, Châu Âu, Bắc Mỹ, Châu Phi...) |
| *(Biến thứ 6 - Mở rộng)* | *Chuyển động theo thời gian (Animation)* | *Sự dịch chuyển của các bong bóng qua các thập kỷ (như bài diễn thuyết TED Talk huyền thoại của GS. Hans Rosling - Gapminder).* |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 96 PDF / Trang 165 Sách):</b> Chèn <b>Figure 6.48: Bubble chart — Fertility, Life Expectancy, and Population in nations, 2018</b> (Thể hiện rõ kích thước và màu sắc các bong bóng đại diện cho từng châu lục).
</div>

---



## BẢNG TỔNG HỢP LỰA CHỌN BIỂU ĐỒ NHANH (CHEAT SHEET)

| Khi câu chuyện dữ liệu của bạn cần... | Loại biểu đồ tối ưu nhất | Lưu ý thiết kế sống còn |
| :--- | :--- | :--- |
| **So sánh giá trị giữa các danh mục** | **Bar / Column Chart** (Grouped, Split) | Bắt buộc trục giá trị bắt đầu từ **$0$**. Nếu nhãn chữ dài, phải dùng **Horizontal Bar**. |
| **Xem tỷ trọng thành phần trong tổng thể ($100\%$)** | **Stacked Bar / Column** hoặc **Pie Chart** | Pie Chart chỉ dùng khi $\le 5\text{ lát cắt}$, xếp từ hướng **12 giờ** theo chiều kim đồng hồ. |
| **Xem hình dáng phân bố của dãy số liên tục** | **Histogram** | Chia khoảng (buckets/bins) hợp lý, các cột **sát khít nhau** không có khe hở. |
| **Theo dõi xu hướng biến động theo thời gian** | **Line Chart** / **Annotated Line** / **Stacked Area** | Line Chart **không bắt buộc gốc $0$**. Dùng Annotation để giải thích các đỉnh/đáy lịch sử. |
| **Nhấn mạnh khoảng cách / Bất bình đẳng giữa 2 nhóm** | **Range Chart (Dumbbell Plot)** | Hiển thị số ở cả 2 đầu mút của thanh nối để thấy rõ độ chênh lệch. |
| **Tìm mối tương quan giữa 2 đến 4 biến số** | **Scatter Plot** ($2\text{ biến}$) / **Bubble Chart** ($4\text{ biến}$) | Dùng kích thước (Size) cho biến định lượng và màu sắc (Color) cho biến phân loại vùng/nhóm. |

---



<!-- _class: lead -->
# TỔNG KẾT PHẦN 2
### NGUYÊN TẮC VÀNG KHI TRỰC QUAN HÓA BIỂU ĐỒ

1. **Giải phẫu chuẩn mực:** Kết hợp *Tiêu đề kể chuyện* + *Tiêu đề phụ kỹ thuật*, luôn minh bạch nguồn dữ liệu (`Source/Notes`) và sai số (`Error bars`).
2. **Tuân thủ kỷ luật thị giác:** Gốc $0$ cho biểu đồ Cột/Thanh; Tổng $100\%$ (tối đa 5 phần từ góc 12h) cho biểu đồ Tròn; tuyệt đối nói không với "Rác đồ họa" 3D.
3. **Chọn đúng biểu đồ cho đúng câu chuyện:** Phối hợp linh hoạt từ Bar, Histogram, Line có chú thích đến Range Chart và Bubble Chart đa chiều để dẫn dắt người xem khám phá sự thật.

<div class="pill">Tiếp theo: Phần 3 — Trực quan hóa Không gian (Map Your Data - Chương 7)</div>
---


<!-- _class: lead -->
# TRỰC QUAN HÓA KHÔNG GIAN
# MAP YOUR DATA

<div class="pill">Tư Duy Thiết Kế Bản Đồ & Phân Tích Dữ Liệu Địa Lý (Chương 7)</div>

**Phần 3 — Bài Thuyết Trình Trực Quan Hóa Dữ Liệu**
Dựa trên tác phẩm *Hands-On Data Visualization* (Jack Dougherty & Ilya Ilyankou)

<!-- 
[Ghi chú thuyết trình]:
Chào mọi người. Sau khi đã nắm vững cách làm sạch dữ liệu và vẽ biểu đồ ở 2 phần trước, Phần 3 sẽ đưa chúng ta bước vào không gian địa lý: Map Your Data (Chương 7). Bản đồ có sức hút thị giác cực lớn vì nó gắn liền với cảm thức về nơi chốn, nhưng đây cũng là nơi người làm dữ liệu dễ mắc phải những sai lầm nghiêm trọng nhất.
-->

---


## NỘI DUNG TRÌNH BÀY (OUR CONTENTS)

**01. Bản chất Dữ liệu Không gian & Giải phẫu Bản đồ**
- Khi nào nên (và không nên) vẽ bản đồ?
- Giải phẫu bản đồ tương tác: Lớp nền (Raster vs. Vector) & Lớp dữ liệu (Point, Polyline, Polygon)
- Phân biệt rạch ròi Dữ liệu Điểm (Point) và Dữ liệu Vùng (Polygon)

**02. Nguyên lý Thiết kế Bản đồ Thực chiến**
- Quy tắc 1: Chỉ biểu diễn 1 biến số trên bản đồ, không chồng chéo 2 biến
- Quy tắc 2: Chọn đơn vị địa lý nhỏ hơn cho bản đồ phân vùng (Bài toán MAUP)

**03. Thiết kế Bản đồ Phân vùng màu (Choropleth Map) & Chuẩn hóa**
- Chọn bảng màu theo bản chất dữ liệu (ColorBrewer): Tuần tự, Phân kỳ, Định tính
- Chọn kiểu phân khoảng (Steps vs. Continuous) & 3 phương pháp nội suy (Linear, Quantiles, Jenks)
- Quy tắc sống còn: Bắt buộc chuẩn hóa dữ liệu bản đồ (Tránh bẫy "Bản đồ mật độ dân số")

---


<!-- _class: lead -->
# 01. BẢN CHẤT DỮ LIỆU KHÔNG GIAN
### DECONSTRUCTING A MAP & SPATIAL DATA TYPES

<div class="pill">"Chỉ vì dữ liệu có yếu tố địa lý không có nghĩa là bạn bắt buộc phải vẽ bản đồ."</div>

---


## KHI NÀO NÊN (VÀ KHÔNG NÊN) VẼ BẢN ĐỒ?

Ngày nay, hầu hết dữ liệu đều có thể gắn tọa độ địa lý (từ địa chỉ nhà cho tới vị trí chụp một bức ảnh). Tuy nhiên, trước khi bắt tay vào vẽ bản đồ, hãy tự hỏi:

<div class="box">
<b>Câu hỏi cốt lõi:</b> <i>"Vị trí địa lý và quy luật phân bố không gian (spatial pattern) có thực sự quan trọng đối với câu chuyện của bạn không?"</i>
</div>

- **Khi nào Bản đồ là lựa chọn tối ưu?**
  - Khi người xem cần nhìn thấy **khoảng cách tương đối** giữa các địa điểm, **sự tập trung theo cụm (clusters)**, hoặc **xu hướng lan tỏa theo vùng địa lý** (ví dụ: tâm dịch, vùng ngập lụt, sự phân hóa thu nhập Đông – Tây).
- **Khi nào Biểu đồ thông thường (Chart) kể chuyện tốt hơn Bản đồ?**
  - Nếu chỉ muốn so sánh thứ hạng cao thấp giữa các tỉnh/bang $\rightarrow$ **Biểu đồ thanh ngang (Bar Chart)** chính xác hơn.
  - Nếu muốn xem tốc độ tăng giảm theo thời gian giữa các vùng $\rightarrow$ **Biểu đồ đường (Line Chart)** rõ ràng hơn.
  - Nếu muốn tìm mối liên hệ giữa 2 biến số của các vùng $\rightarrow$ **Biểu đồ phân tán (Scatter Chart)** hiệu quả hơn.

---


## GIẢI PHẪU BẢN ĐỒ TƯƠNG TÁC (1): LỚP NỀN RASTER VS. VECTOR

Một bản đồ tương tác trên web (*slippy map* / *tiled map*) gồm hai phần chính: **Lớp bản đồ nền (Basemap tiles)** ở dưới và **Lớp dữ liệu (Data layers)** phủ lên trên.

| Đặc điểm | Bản đồ nền Raster (Raster Tiles) | Bản đồ nền Vector (Vector Tiles) |
| :--- | :--- | :--- |
| **Bản chất** | Tập hợp các bức ảnh chụp từ vệ tinh hoặc máy bay (Aerial photo imagery) ghép lại theo ô lưới. | Được dựng từ các tọa độ toán học mô tả đường phố, tòa nhà, sông ngòi (như OpenStreetMap). |
| **Khi phóng to (Zoom in)** | Bị giới hạn bởi độ phân giải ảnh gốc; **càng phóng to càng bị vỡ hạt và mờ nhòe (fuzzy)**. | Tái tính toán theo tỷ lệ hiển thị; **giữ nguyên độ sắc nét tuyệt đối** ở mọi mức độ thu phóng. |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 5 PDF / Trang 183 Sách):</b> Chèn <b>Figure 7.1</b> so sánh trực quan lớp nền Raster của Esri World Imagery (bên trái - bị nhòe khi phóng to) và lớp nền Vector của OpenStreetMap (bên phải - sắc nét).
</div>

---


## GIẢI PHẪU BẢN ĐỒ TƯƠNG TÁC (2): 3 KIỂU HÌNH HỌC KHÔNG GIAN

Lớp dữ liệu phủ trên bản đồ nền được cấu thành từ 3 thực thể hình học cơ bản (đều dựa trên cặp tọa độ Vĩ độ, Kinh độ - $\text{Latitude}, \text{Longitude}$):

1. **Điểm (Point):**
   - Đại diện cho một vị trí cụ thể duy nhất bằng một cặp tọa độ $(x, y)$.
   - *Ví dụ:* Tọa độ $(40.69, -74.04)$ đánh dấu vị trí Tượng Nữ thần Tự do tại New York.
2. **Đa tuyến / Đường gấp khúc (Polyline):**
   - Chuỗi các điểm nối tiếp nhau tạo thành tuyến đường hoặc mạng lưới có nhiều nhánh (*poly-lines*).
   - *Ví dụ:* Tuyến đường sắt, lộ trình xe buýt, dòng sông, đường mòn đi bộ.
3. **Đa giác / Vùng khép kín (Polygon):**
   - Tập hợp các đoạn thẳng nối khép kín tạo thành một hình bao quanh ranh giới địa lý.
   - *Ví dụ:* Diện tích chân tòa nhà, khu vực điều tra dân số (Census tract), ranh giới tỉnh/bang hoặc quốc gia.
- **Các thành phần bổ trợ bắt buộc:** Tiêu đề, Chú giải (Legend), Nút thu phóng ($+/-$), Thước tỷ lệ (Scale), Mũi tên chỉ hướng Bắc (North arrow), Hộp thông tin (Tooltip/Popup) và Nguồn dữ liệu.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 6 PDF / Trang 184 Sách):</b> Chèn <b>Figure 7.2</b> giải phẫu các thành phần của một bản đồ tương tác (Polygon, Point/Marker, Polyline, Tooltip, Legend, Scale, North arrow).
</div>

---


## PHÂN BIỆT DỮ LIỆU ĐIỂM (POINT) VS. DỮ LIỆU VÙNG (POLYGON)

Nhầm lẫn giữa dữ liệu Điểm và Vùng là lỗi phổ biến ở người mới bắt đầu. Hãy xét 8 dữ liệu tại bang California dưới đây:

| STT | Dữ liệu địa lý | Bản chất | Lý do & Cách biểu diễn chuẩn |
| :---: | :--- | :---: | :--- |
| 1–4 | - Tọa độ `36.48, -118.56`<br>- Địa chỉ `2800 E Observatory Rd`<br>- Ngã tư `Haight & Ashbury St`<br>- Công viên `Balboa Park, San Diego` | **POINT**<br>*(Dữ liệu Điểm)* | Chỉ định các tọa độ hoặc địa điểm cụ thể $\rightarrow$ Vẽ **Bản đồ Điểm (Point Map)** hoặc **Bản đồ Ký hiệu (Symbol Point Map)**. |
| 5–8 | - Khu điều tra dân số `Census tract 4087`<br>- Thành phố `City of Los Angeles`<br>- Quận `San Diego County`<br>- Tiểu bang `State of California` | **POLYGON**<br>*(Dữ liệu Vùng)* | Đại diện cho các đường biên giới hành chính khép kín $\rightarrow$ Vẽ **Bản đồ Phân vùng màu (Choropleth Map)**. |

<div class="box">
💡 <b>3 Ngoại lệ linh hoạt tùy theo câu chuyện dữ liệu:</b><br>
1. <b>Biến Vùng thành Điểm:</b> Tìm tâm điểm (centroid) của thành phố Los Angeles để vẽ vòng tròn biểu diễn tốc độ tăng dân số.<br>
2. <b>Biến Điểm thành Vùng:</b> Vẽ công viên Balboa Park dưới dạng đa giác rộng $1,8\text{ dặm vuông}$ nếu kể câu chuyện về tỷ lệ đất công cộng.<br>
3. <b>Gộp Điểm thành Vùng (Pivot Points to Polygons):</b> Cộng tổng số giường bệnh của từng bệnh viện (Points) để tô màu năng lực y tế của toàn Quận (Polygon).
</div>

---


## HỆ SINH THÁI CÁC LOẠI BẢN ĐỒ TRỰC QUAN HÓA

Tùy thuộc vào định dạng dữ liệu và mục tiêu truyền tải, ta có 6 nhóm bản đồ thông dụng:

- **1. Bản đồ Điểm với biểu tượng tùy chỉnh (Point Map with Custom Icons):**
  - Đánh dấu vị trí cụ thể (như bảo tàng, công viên) kèm cửa sổ Popup chứa ảnh và thông tin chi tiết.
- **2. Bản đồ Điểm ký hiệu (Symbol Point Map / Proportional Symbol):**
  - Dùng hình tròn hoặc hình vuông có **kích thước và màu sắc biến thiên** theo giá trị số (ví dụ: Bản đồ biến động dân số 300 thành phố lớn của Mỹ giai đoạn 2010–2019).
- **3. Bản đồ Phân vùng màu (Choropleth Map):**
  - Tô màu các đa giác (quốc gia, tỉnh, huyện) theo thang giá trị để làm nổi bật quy luật không gian.
- **4. Bản đồ Nhiệt (Heat Point Map):**
  - Biểu diễn mật độ tập trung dày đặc của các điểm dưới dạng vùng nóng (hotspots).
- **5. Bản đồ Hành trình kể chuyện (Story Map) & Đa tuyến (Polyline Map):**
  - Dẫn dắt người xem đi qua từng địa điểm theo trình tự cuộn trang hoặc hiển thị mạng lưới giao thông.
- **6. Bản đồ Dữ liệu mở Thời gian thực (Current / Live Map):**
  - Kết nối trực tiếp với kho dữ liệu mở để tự động cập nhật điểm mới theo từng ngày.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 2 & 31 PDF / Trang 180 & 209 Sách):</b> Ghép các hình thu nhỏ từ <b>Table 7.1</b> và bản đồ <b>Figure 7.34</b> (Symbol Point Map: <i>US City Population Change from 2010 to 2019</i>).
</div>

---


<!-- _class: lead -->
# 02. NGUYÊN LÝ THIẾT KẾ BẢN ĐỒ THỰC CHIẾN
### CORE MAP DESIGN PRINCIPLES

<div class="pill">Tránh quá tải thị giác và lựa chọn độ phân giải địa lý tối ưu</div>

---


## QUY TẮC 1: CHỈ BIỂU DIỄN 1 BIẾN SỐ TRÊN BẢN ĐỒ, ĐỪNG NHỒI NHÉT 2 BIẾN!

Người mới làm trực quan hóa thường nghĩ: *"Vẽ được 1 biến lên bản đồ đã tốt, chồng thêm biến thứ 2 lên cùng bản đồ đó chắc chắn sẽ tốt gấp đôi!"* $\rightarrow$ **Sai lầm nghiêm trọng!**

- **Bài toán thực tế:** Muốn tìm mối quan hệ giữa **Thu nhập (Income)** và **Trình độ đại học (Education)** tại 8 quận.
  - *Bản đồ (a):* Choropleth Map tô màu xanh theo mức thu nhập $\rightarrow$ **Tốt** (thấy rõ vùng Tây Bắc giàu hơn).
  - *Bản đồ (b):* Symbol Map vẽ vòng tròn cam theo tỷ lệ có bằng đại học $\rightarrow$ **Tốt** (nhìn riêng từng biến).
  - ❌ *Bản đồ (c) — Chồng (b) lên trên (a):* Vừa tô màu nền đa giác, vừa đè hình tròn to nhỏ lên trên $\rightarrow$ **Quá tải thị giác (Overloaded)!** Mắt người không thể giải mã nổi mối liên hệ giữa màu nền và diện tích hình tròn.
- ✅ **Giải pháp chuẩn xác:**
  - Dùng **Biểu đồ phân tán — Scatter Chart (d)** để thể hiện trực diện mối tương quan giữa 2 biến, hoặc đặt bản đồ Choropleth (a) đứng cạnh Scatter Chart (d).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 9 PDF / Trang 187 Sách):</b> Chèn <b>Figure 7.3</b> gồm 4 hình (a) Good: Choropleth, (b) Good: Symbol map, (c) Bad: Symbol map on top of choropleth, (d) Good: Scatter chart.
</div>

<!-- 
[Ghi chú thuyết trình]:
Hãy nhìn vào hình (c) trong Figure 7.3. Khi bạn đặt các chấm tròn màu cam đè lên các ô màu xanh đậm nhạt khác nhau, người đọc sẽ bị rối loạn. Nếu mục tiêu chính là chỉ ra mối tương quan giữa thu nhập và học vấn, hãy dũng cảm bỏ bản đồ đi và dùng Scatter Chart ở hình (d)!
-->

---


## QUY TẮC 2: CHỌN ĐƠN VỊ ĐỊA LÝ NHỎ HƠN CHO BẢN ĐỒ CHOROPLETH

Trong địa lý học, hiện tượng này được gọi là **Bài toán Đơn vị Diện tích Có thể Thay đổi (Modifiable Areal Unit Problem — MAUP)**: Cách bạn chia nhỏ hay gộp lớn ranh giới lãnh thổ sẽ làm thay đổi hoàn toàn nhận thức của người xem.

- **Case Study: Giá nhà điển hình tại vùng Đông Bắc nước Mỹ (Dữ liệu Zillow, 9/2020):**
  - **Bản đồ Trái (Cấp Tiểu bang — State level):** Gom toàn bộ dữ liệu vào một lát cắt lớn. Chỉ thấy bang Massachusetts có màu đậm hơn các bang xung quanh, nhưng **che giấu hoàn toàn sự chênh lệch nội bộ**.
  - **Bản đồ Phải (Cấp Quận/Hạt — County level):** Chia thành các đơn vị nhỏ hơn. Lập tức làm lộ rõ **các cụm giá nhà đắt đỏ quanh vùng đô thị New York, Long Island và Boston** so với các vùng nông thôn giá rẻ ngay trong cùng một bang!
- **Lời khuyên thiết kế:**
  - Khi phân vân, **hãy ưu tiên cấp địa lý nhỏ hơn (smaller geographies)** kèm đường viền bang rõ ràng để người đọc nhìn thấy cả bức tranh vĩ mô lẫn sự đa dạng vi mô (nhưng đừng nhỏ tới mức từng căn nhà riêng lẻ vì sẽ gây nhiễu).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 10 PDF / Trang 188 Sách):</b> Chèn <b>Figure 7.4</b> đặt song song 2 bản đồ giá nhà Zillow: Cấp Tiểu bang (bên trái - đơn điệu) và Cấp Quận/Hạt (bên phải - chi tiết, sắc nét).
</div>

---


<!-- _class: lead -->
# 03. THIẾT KẾ BẢN ĐỒ CHOROPLETH & CHUẨN HÓA
### COLORS, INTERVALS, INTERPOLATION & NORMALIZATION

<div class="pill">Làm chủ màu sắc, phương pháp phân khoảng và chuẩn hóa dữ liệu không gian</div>

---


## CHỌN BẢNG MÀU CHOROPLETH KHỚP VỚI DỮ LIỆU (COLORBREWER)

Dựa trên công cụ chuẩn mực **ColorBrewer** (do Cynthia Brewer phát triển), việc chọn màu cho bản đồ Choropleth không phải theo sở thích cá nhân mà phải tuân theo **3 cấu trúc dữ liệu**:

1. **Bảng màu Tuần tự (Sequential Palettes):**
   - *Đặc điểm:* Chuyển sắc độ từ nhạt sang đậm (1 tông màu hoặc đa sắc chuyển tiếp như Vàng $\rightarrow$ Cam $\rightarrow$ Đỏ).
   - *Ứng dụng:* Dữ liệu số liên tục từ **thấp đến cao** (Thu nhập, lượng mưa, mật độ). Màu đậm thường đại diện cho giá trị cao.
2. **Bảng màu Phân kỳ (Diverging Palettes):**
   - *Đặc điểm:* Có **một màu trung tính sáng ở chính giữa** (mốc $0$, mức trung bình hoặc trung vị) và **2 tông màu đối lập đậm dần về hai cực** (ví dụ: Cam đậm $\leftrightarrow$ Trắng $\leftrightarrow$ Tím đậm).
   - *Ứng dụng:* Nhấn mạnh sự phân cực **cao hơn hoặc thấp hơn một ngưỡng chuẩn** (Mức thay đổi dân số âm/dương, thu nhập so với mức trung bình quốc gia).
3. **Bảng màu Định tính (Qualitative Palettes):**
   - *Đặc điểm:* Các màu sắc tách biệt hoàn toàn, không có thứ tự đậm nhạt.
   - *Ứng dụng:* Dữ liệu **phân loại danh mục** (Loại đất: đất ở, đất thương mại, công viên, mặt nước).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 12 & 13 PDF / Trang 190 & 191 Sách):</b> Ghép <b>Figure 7.6</b> (3 dải màu Sequential, Diverging, Qualitative) và <b>Figure 7.7</b> (2 bản đồ thu nhập đầu người của Mỹ: 7.7a dùng Sequential xanh dương nhấn mạnh vùng cực đại Đông Bắc; 7.7b dùng Diverging Cam-Tím nhấn mạnh sự phân hóa giữa miền Nam nghèo và hai bờ Đông-Tây giàu có).
</div>

---


## PHÂN KHOẢNG MÀU: BẬC THANG (STEPS) VS. LIÊN TỤC (CONTINUOUS)

Khi mã hóa các con số thành màu sắc trên bản đồ, bạn có hai lựa chọn hiển thị thanh thang đo:

| Tiêu chí | Phân khoảng Bậc thang (Steps / Classes) | Dải màu Liên tục (Continuous Gradient) |
| :--- | :--- | :--- |
| **Hình thái** | Chia thành các ô màu rời rạc như bậc cầu thang (thường từ $3$ đến $7\text{ bậc}$). | Chuyển màu mượt mà như một con dốc không có vạch ngăn cách. |
| **Ưu điểm** | - Lý tưởng khi cần chỉ rõ các vùng nằm **trên hoặc dưới một ngưỡng cụ thể** (VD: vùng ngập nếu nước biển dâng $1\text{m}$).<br>- Giúp mắt người dễ đối chiếu màu trên bản đồ với chú giải (Legend). | - Phản ánh trung thực các **khác biệt tinh tế (subtle nuances)** giữa các vùng lân cận.<br>- Tránh việc hai vùng có giá trị sát nút nhau bị đẩy sang hai màu hoàn toàn khác biệt. |
| **Lưu ý thiết kế** | Ít bậc quá sẽ làm bản đồ thô kệch; nhiều bậc quá ($>7$) mắt người không phân biệt nổi các sắc độ kế cận. | Cần kết hợp với phương pháp nội suy phù hợp để không bị chìm màu ở khoảng giữa. |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 14 PDF / Trang 192 Sách):</b> Chèn <b>Figure 7.9</b> minh họa sự khác biệt giữa thanh màu <i>Steps</i> (bậc thang) và <i>Continuous</i> (dải chuyển sắc).
</div>

---


## 3 PHƯƠNG PHÁP NỘI SUY / CHIA NHÓM DỮ LIỆU (INTERPOLATION)

Trước khi chọn cách chia nhóm màu, **hãy vẽ biểu đồ Histogram** để xem dữ liệu phân bố đối xứng đều đặn hay bị lệch đuôi (skewed). Từ đó chọn 1 trong 3 thuật toán nội suy:

1. **Tuyến tính (Linear / Equal Interval):**
   - Chia đều khoảng cách từ giá trị nhỏ nhất đến lớn nhất theo một đường thẳng.
   - *Phù hợp khi:* Dữ liệu có **phân bố chuẩn đối xứng**, hoặc khi bạn muốn **làm nổi bật các giá trị cực đoan (outliers)** ở hai đầu.
2. **Phân vị (Quantiles — Quartiles, Quintiles, Deciles):**
   - Chia dữ liệu sao cho **mỗi nhóm màu chứa số lượng đơn vị địa lý bằng nhau** (chia 4, chia 5 hoặc chia 10).
   - *Phù hợp khi:* Dữ liệu **bị lệch nặng về một phía (skewed)**; giúp tận dụng tối đa dải màu để phô diễn sự đa dạng ở nhóm giữa. *(Biến thể: **Rounded values** làm tròn các mốc số thập phân cho dễ đọc).*
3. **Điểm gãy tự nhiên (Jenks Natural Breaks):**
   - Thuật toán tối ưu hóa nhằm **gom các giá trị gần nhau vào cùng một nhóm** và **tối đa hóa khoảng cách giữa các nhóm khác nhau**.
   - *Phù hợp khi:* Cần một **sự thỏa hiệp cân bằng** giữa Linear và Quantiles trên dữ liệu lệch, vừa thấy được sự đa dạng nội bộ vừa giữ được các điểm cực trị.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 16 & 17 PDF / Trang 194 & 195 Sách):</b> Ghép <b>Figure 7.12</b> (Histogram phân bố lệch vs. phân bố đều) và <b>Figure 7.13</b> của Datawrapper Academy (Minh họa cách điều chỉnh khoảng màu để <i>"See all the differences in the data"</i> thay vì để bản đồ quá sáng hoặc quá tối).
</div>

---


## QUY TẮC SỐNG CÒN: BẮT BUỘC CHUẨN HÓA DỮ LIỆU BẢN ĐỒ CHOROPLETH!

<div class="box">
⚠️ <b>Cảnh báo kinh điển:</b> Nếu bạn quên chuẩn hóa dữ liệu mà đưa thẳng <b>số đếm thô (raw counts)</b> lên bản đồ Choropleth, bạn sẽ vô tình vẽ lại một <b>bản đồ mật độ dân số</b> hoàn toàn vô nghĩa thay vì hiện tượng bạn muốn nghiên cứu!
</div>

### Case Study: Bản đồ đại dịch Covid-19 tại Mỹ (Tính đến 26/06/2020 — *New York Times*)

| Bản đồ (a): Tổng số ca nhiễm thô (Total Cases) | Bản đồ (b): Số ca nhiễm trên đầu người (Cases Per Capita) |
| :--- | :--- |
| - **Hiện tượng hiển thị:** California, Texas, Florida, Illinois và New York có màu xanh đậm nhất.<br>- **Sai lầm:** Đây đơn giản là 5 bang đông dân nhất nước Mỹ! Đông dân hơn thì hiển nhiên tổng số ca dương tính cộng dồn phải cao hơn. | - **Công thức chuẩn hóa:** $\frac{\text{Tổng số ca nhiễm}}{\text{Dân số tiểu bang}}$ (Chia theo phân nhóm Jenks).<br>- **Sự thật lộ diện:** California, Texas và Florida thực chất có tỷ lệ nhiễm thấp hơn nhiều ở thời điểm đó. **Tâm dịch thực sự đầu tiên** tập trung dày đặc tại **New York, New Jersey, Massachusetts** và vùng **Louisiana / Mississippi**! |

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 18 PDF / Trang 196 Sách):</b> Chèn <b>Figure 7.14</b> đặt cạnh nhau: <b>(a) Covid-19 Total Cases</b> và <b>(b) Covid-19 Cases Per Capita</b> để thấy sự biến mất của màu xanh đậm ở California và Texas sau khi chuẩn hóa.
</div>

---


## BẢN ĐỒ DỮ LIỆU MỞ THỜI GIAN THỰC & BÀI HỌC LÀM SẠCH KHÔNG GIAN

Khi kết nối trực tiếp bản đồ với các cổng dữ liệu mở của chính phủ (như nền tảng Socrata / NYC OpenData), bản đồ sẽ tự động cập nhật theo thời gian thực nhưng đòi hỏi bộ lọc chặt chẽ:

- **Ví dụ thực tế: Bản đồ các vụ tai nạn giao thông chết người tại New York trong 365 ngày qua**
  - Để bản đồ luôn hiển thị đúng và sạch, người thiết kế phải thiết lập **3 bộ lọc (Filters) tự động**:
    1. *Lọc theo mức độ nghiêm trọng:* `NUMBER OF PERSONS KILLED > 0` (chỉ lấy các vụ có người tử vong).
    2. *Lọc thời gian động (Relative Date):* `CRASH DATE = Last 365 days` (tự động cuốn chiếu theo ngày hiện tại).
    3. *Lọc bỏ lỗi tọa độ "Đảo Null" (Null Island):* Rất nhiều vụ tai nạn chưa rõ vị trí bị hệ thống gán tọa độ $(0, 0)$ ngoài Đại Tây Dương $\rightarrow$ Bắt buộc thêm bộ lọc **`LATITUDE > 0`** để chỉ giữ lại các điểm nằm ở Bắc Bán Cầu (khu vực New York).
- **Rủi ro của bản đồ trực tuyến phụ thuộc bên thứ ba:**
  - Nếu cơ quan nhà nước ngừng cập nhật kho dữ liệu, đổi tên cột, hoặc ngừng hỗ trợ nền tảng lưu trữ, bản đồ nhúng trên web của bạn sẽ lập tức bị hỏng (break).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 53 & 54 PDF / Trang 231 & 232 Sách):</b> Ghép <b>Figure 7.63</b> (Bản đồ thô chưa lọc bị nhảy điểm ra giữa Đại Tây Dương tại Null Island) và <b>Figure 7.61</b> (Bản đồ nền tối hoàn chỉnh hiển thị từng điểm tai nạn tại Manhattan sau khi áp dụng 3 bộ lọc).
</div>

---


<!-- _class: lead -->
# TỔNG KẾT PHẦN 3
### NGUYÊN TẮC VÀNG KHI TRỰC QUAN HÓA KHÔNG GIAN

1. **Chọn đúng hình thái:** Chỉ vẽ bản đồ khi yếu tố địa lý mang lại thông tin mới; phân biệt rõ **Point** (vị trí/ký hiệu) và **Polygon** (ranh giới/vùng tô màu).
2. **Đơn giản & Chi tiết:** Không chồng 2 biến khác loại lên cùng 1 bản đồ; ưu tiên đơn vị địa lý nhỏ (cấp Quận/Hạt thay vì cấp Bang) để tránh che khuất biến động nội bộ (MAUP).
3. **Làm chủ Choropleth:** Phối màu đúng chuẩn *ColorBrewer* (Sequential, Diverging, Qualitative), kiểm tra phân bố bằng Histogram trước khi chọn nội suy (*Linear, Quantiles, Jenks*) và **luôn luôn chuẩn hóa số đếm thô sang tỷ lệ (Per Capita / $\%$) build-in**.

<div class="pill">Tiếp theo: Phần 4 — Đạo đức Dữ liệu & Nghệ thuật Kể chuyện (Chương 14 & 15)</div>
---

<!-- _class: lead -->
# ĐẠO ĐỨC DỮ LIỆU &
# NGHỆ THUẬT KỂ CHUYỆN

<div class="pill">Phát Hiện Sự Lừa Dối, Giảm Thiểu Định Kiến & Truyền Cảm Hứng Hành Động (Chương 14, 15)</div>

**Phần 4 — Bài Thuyết Trình Trực Quan Hóa Dữ Liệu**
Dựa trên tác phẩm *Hands-On Data Visualization* (Jack Dougherty & Ilya Ilyankou)

<!-- 
[Ghi chú thuyết trình]:
Chào mọi người. Ở phần cuối cùng này, chúng ta sẽ tổng kết toàn bộ hành trình bằng hai chủ đề quan trọng bậc nhất: Làm thế nào để phát hiện những chiêu trò "nói dối" tinh vi bằng biểu đồ/bản đồ cũng như giảm thiểu định kiến dữ liệu (Chương 14), và cuối cùng là cách kết nối mọi thứ lại thành một câu chuyện dữ liệu truyền cảm hứng hành động (Chương 15).
-->

---

## NỘI DUNG TRÌNH BÀY (OUR CONTENTS)

**01. Chương 14 (Phần A): Cách Phát Hiện "Sự Lừa Dối" Trong Trực Quan Hóa**
- Ba phân loại đồ thị: Sai (Wrong), Đánh lừa (Misleading) và Trung thực (Truthful)
- Các thủ thuật bóp méo biểu đồ: Cắt trục tung, kéo giãn tỷ lệ khung hình (Aspect Ratio), bẫy hai trục tung (Dual-Axis)
- Sự thật đằng sau hai bản đồ đối lập nhưng cùng trung thực

**02. Chương 14 (Phần B): Nhận Diện & Giảm Thiểu Định Kiến (Bias)**
- 4 nhóm định kiến dữ liệu: Chọn mẫu, Nhận thức (Cognitive), Thuật toán (Algorithmic) & Liên nhóm (Intergroup)
- 4 nhóm định kiến không gian: Diện tích (Map Area), Phép chiếu (Projection), Lãnh thổ tranh chấp & Loại trừ (Exclusion)

**03. Chương 15: Nghệ Thuật Kể Chuyện Dữ Liệu (Data Storytelling)**
- Công thức **Tell — Show — Why** & Xây dựng bảng phân cảnh (Storyboard)
- Thu hút sự chú ý bằng màu sắc, chú thích trực tiếp & Minh bạch hóa sự bất định (Uncertainty)

---

<!-- _class: lead -->
# 01. PHÁT HIỆN "SỰ LỪA DỐI" TRONG ĐỒ THỊ
### CHAPTER 14: DETECT LIES IN CHARTS AND MAPS

<div class="pill">"Muốn bắt kẻ gian, trước hết phải hiểu mánh khóe của kẻ gian."</div>

---

## BA PHÂN LOẠI TRỰC QUAN HÓA: SAI, ĐÁNH LỪA & TRUNG THỰC

Trực quan hóa dữ liệu không phải là một môn khoa học nhị phân chỉ có một đáp án đúng duy nhất, mà là một **kỹ năng diễn giải dựa trên bằng chứng**. Mọi đồ thị đều rơi vào 1 trong 3 nhóm:

1. **Sai (Wrong):**
   - Bóp méo số liệu thực tế hoặc **vi phạm các quy tắc thiết kế cứng rắn bất khả xâm phạm**.
   - *Ví dụ:* Biểu đồ cột/thanh không bắt đầu từ gốc $0$ (Truncated baseline), hoặc biểu đồ tròn có tổng các lát cắt khác $100\%$.
2. **Đánh lừa / Gây hiểu lầm (Misleading):**
   - Về mặt kỹ thuật **không vi phạm quy tắc thiết kế**, số liệu hoàn toàn chính xác, nhưng lại **cố tình che giấu hoặc bóp méo hình thái xuất hiện của dữ liệu** một cách vô lý (giống như trò đánh lạc hướng của ảo thuật gia).
   - *Ví dụ:* Kéo giãn trục tung quá mức hoặc bóp méo tỷ lệ khung hình (Aspect Ratio) trên biểu đồ đường.
3. **Trung thực (Truthful):**
   - Hiển thị dữ liệu chính xác và tuân thủ các nguyên tắc thiết kế.
   - *Lưu ý:* Có thể có **nhiều hơn một cách biểu diễn trung thực** cho cùng một bộ dữ liệu, tùy thuộc vào góc nhìn mà tác giả muốn làm nổi bật.

---

## MÁNH KHÓE 1: PHÓNG ĐẠI & THU NHỎ BIẾN ĐỘNG QUA TRỤC TUNG ($Y\text{-AXIS}$)

Cùng một con số nhưng việc thao túng điểm đầu và điểm cuối của trục tung sẽ tạo ra hai thông điệp trái ngược:

### A. Phóng đại sự thay đổi (Exaggerating Change) — Cắt cụt gốc $0$ của Biểu đồ Cột
- **Dữ liệu thực tế:** GDP của Mỹ Quý 2/2019 là $\$21,54\text{ nghìn tỷ}$, sang Quý 3/2019 tăng nhẹ lên $\$21,75\text{ nghìn tỷ}$ $\rightarrow$ Mức tăng thực tế chỉ đạt **$0,96\%$** (chưa tới $1\%$).
- **Thủ thuật:** Thay vì để trục tung từ $0$, kẻ thao túng cắt trục bắt đầu từ mốc $\$21.500\text{ tỷ}$ đến $\$21.800\text{ tỷ}$ $\rightarrow$ Cột Quý 3 cao gấp hơn $5\text{ lần}$ cột Quý 2! *(Đồ thị này **SAI / Wrong** vì vi phạm quy tắc gốc $0$ của biểu đồ cột).*

### B. Làm lu mờ sự thay đổi (Diminishing Change) — Kéo dài trục tung Biểu đồ Đường
- **Dữ liệu thực tế (NASA):** Nhiệt độ bề mặt Trái Đất (1880–2019) đã tăng khoảng **$+1^\circ\text{C}$** so với nền nhiệt chuẩn 1951–1980 (gây tan băng và nước biển dâng).
- **Thủ thuật của những kẻ phủ nhận biến đổi khí hậu:** Đổi thang đo trục tung từ $[-0.5^\circ\text{C}, +1.5^\circ\text{C}]$ thành **$[-5^\circ\text{C}, +5^\circ\text{C}]$** $\rightarrow$ Đường tăng nhiệt độ bị ép bẹp dí thành một đường thẳng gần như nằm ngang! *(Về kỹ thuật là không sai với Line Chart, nhưng cực kỳ **Đánh lừa / Misleading**).*

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 62 & 64 PDF / Trang 396 & 398 Sách):</b> Ghép <b>Figure 14.1</b> (GDP Mỹ: Zero baseline <i>Truthful</i> vs. Truncated baseline <i>Wrong</i>) và <b>Figure 14.2 + 14.3</b> (Nhiệt độ toàn cầu bị làm phẳng lì khi kéo trục tung từ $-5$ đến $5$).
</div>

---

## MÁNH KHÓE 2: BÓP MÉO TỶ LỆ KHUNG HÌNH (WARPING ASPECT RATIO)

**Tỷ lệ khung hình (Aspect Ratio)** là tỷ lệ giữa Chiều rộng chia cho Chiều cao ($\text{Width} : \text{Height}$). Kéo giãn chiều ngang hoặc chiều dọc sẽ làm thay đổi hoàn toàn góc dốc của biểu đồ đường:

- **1. Kéo giãn chiều ngang quá mức ($5.7 : 1$):**
  - Biểu đồ nhiệt độ NASA mặc định có tỷ lệ $1.6 : 1$ ($600 \times 370\text{ px}$). Khi kéo bẹt thành $1090 \times 191\text{ px}$ ($5.7 : 1$), độ dốc biến mất, tạo cảm giác khí hậu hoàn toàn ổn định.
- **2. Nghịch lý khi áp dụng máy móc quy tắc của Alberto Cairo:**
  - Cairo từng gợi ý tỷ lệ khung hình nên khớp với $\%$ thay đổi (VD: tăng $33\% = 1/3 \rightarrow$ vẽ khung hình $3:1$). Nhưng chính Cairo cũng cảnh báo quy tắc này sẽ thất bại ở 2 thái cực:
    - *Nếu tính theo mức tăng biến thiên nhiệt độ* (từ $-0.5^\circ\text{C}$ lên $+1^\circ\text{C}$, tức tăng $300\% = 3/1$) $\rightarrow$ Khung hình $1:3$ **cao vút như tòa tháp**, phóng đại quá đà!
    - *Nếu tính theo nhiệt độ tuyệt đối của Trái Đất* (tăng từ $13^\circ\text{C}$ lên $14^\circ\text{C}$, tức tăng $8\% \approx 1/12$) $\rightarrow$ Khung hình $12:1$ **dẹt mỏng như sợi chỉ**, làm lu mờ thảm họa khí hậu!

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 65, 66, 67 PDF / Trang 399–401 Sách):</b> Đặt cạnh nhau 3 biến thể của cùng 1 biểu đồ nhiệt độ: <b>Figure 14.4</b> (Kéo ngang $5.7:1$), <b>Figure 14.5</b> (Kéo dọc $1:3$) và <b>Figure 14.6</b> (Kéo ngang $12:1$).
</div>

---

## MÁNH KHÓE 3: CÁI BẪY BIỂU ĐỒ HAI TRỤC TUNG (DUAL-AXIS CHARTS)

Các chuyên gia trực quan hóa luôn khuyên **tránh xa biểu đồ hai trục tung** vì người thiết kế có thể tùy ý co giãn 2 thang đo độc lập để ép 2 đường cắt nhau hoặc tách rời nhau theo ý muốn.

- **Case Study: Kết hợp Nhiệt độ Toàn cầu và GDP Mỹ (1929–2019) trên cùng một đồ thị**
  - **Bản thiết kế đánh lừa (Figure 14.9):** Đặt trục Nhiệt độ bên trái (kéo giãn từ $0$ đến $10^\circ\text{C}$) và trục GDP bên phải (từ $\$0$ đến $\$25.000\text{ tỷ}$).
  - **3 tầng thao túng tâm lý trong cùng 1 biểu đồ:**
    1. *Thang đo vô lý:* Ép đường nhiệt độ nằm bẹp dưới đáy trong khi đường GDP vút cao $\rightarrow$ Tạo ảo giác *"Kinh tế cứ tăng trưởng rực rỡ còn biến đổi khí hậu chẳng đáng bận tâm"*.
    2. *Dữ liệu không tương đương:* Dùng GDP danh nghĩa chưa điều chỉnh lạm phát (so sánh đồng đô-la năm 1929 với năm 2019).
    3. *Màu sắc ngược nghĩa:* Dùng màu xanh dương mát mẻ (cool blue) cho đường nhiệt độ nóng lên và màu đỏ cho GDP!
- ✅ **Giải pháp thay thế trung thực:** Dùng **Biểu đồ phân tán nối điểm theo thời gian (Connected Scatter Chart)** với trục hoành là **GDP thực (Real GDP - cố định theo giá năm 2012)** và trục tung là **Mức tăng nhiệt độ** $\rightarrow$ Cho thấy rõ kinh tế Mỹ tăng trưởng tỷ lệ thuận với sự nóng lên toàn cầu!

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 69 & 70 PDF / Trang 403 & 404 Sách):</b> Đối chiếu <b>Figure 14.9</b> (Biểu đồ 2 trục tung Misleading) và <b>Figure 14.10</b> (Connected Scatter Chart trung thực).
</div>

---

## SỰ THẬT ĐẰNG SAU HAI BẢN ĐỒ ĐỐI LẬP: CẢ HAI ĐỀU TRUNG THỰC!

Xét dữ liệu **Bất bình đẳng thu nhập toàn cầu** (Tỷ phần thu nhập quốc gia trước thuế nằm trong tay nhóm **$1\%$ giàu nhất** — Mỹ chiếm **$20,5\%$**, Brazil chiếm **$28,3\%$**):

| Bản đồ 1: Dải màu Liên tục, Nội suy Tuyến tính (Continuous, Linear) | Bản đồ 2: Chia 3 Bậc màu, Điểm gãy Tự nhiên (3 Steps, Jenks Natural Breaks) |
| :--- | :--- |
| - Xếp thẳng từ mức thấp nhất ($5\%$) đến cao nhất ($31\%$).<br>- **Nước Mỹ ($20,5\%$) có màu xanh trung bình**, trông khá ôn hòa và tương đồng với đa số các quốc gia khác. | - Chia thế giới thành 3 nhóm phân tầng rõ rệt.<br>- **Nước Mỹ ($20,5\%$) rơi vào nhóm cao nhất ($\ge 19\%$)** và nổi bật với **màu xanh đậm nhất** cùng nhóm với Brazil và Nga! |

<div class="box">
🔍 <b>Giải mã bằng Histogram (Figure 14.14):</b> Tại sao cả hai bản đồ đều trung thực? Khi vẽ Histogram, phần lớn các nước cụm lại ở khoảng $10\%\text{–}16\%$, chỉ có vài nước ngoại lai (outliers) vọt lên mức $30\%$. Mỹ ($20,5\%$) nằm ở <i>giữa khoảng cách địa lý từ cực tiểu đến cực đại</i> (nên Bản đồ 1 tô màu trung bình), nhưng lại nằm ở <i>nhóm đầu nếu xét theo mật độ phân cụm</i> (nên Bản đồ 2 tô màu đậm).
</div>

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 73, 74, 75 PDF / Trang 407–409 Sách):</b> Ghép bộ 3 hình: <b>Figure 14.12</b> (Bản đồ Continuous Linear), <b>Figure 14.13</b> (Bản đồ 3 Steps Natural Breaks) và <b>Figure 14.14</b> (Histogram chỉ mũi tên vào vị trí <code>US 20.5% in this bin</code>).
</div>

---

<!-- _class: lead -->
# 02. NHẬN DIỆN & GIẢM THIỂU ĐỊNH KIẾN
### RECOGNIZE AND REDUCE DATA & SPATIAL BIAS

<div class="pill">Từ định kiến nhận thức, thuật toán cho tới định kiến bản đồ học</div>

---

## 4 NHÓM ĐỊNH KIẾN DỮ LIỆU CẦN NHẬN DIỆN (DATA BIASES) — PHẦN 1

Định kiến (Bias) là sự thiên vị không công bằng cho một góc nhìn hoặc một nhóm xã hội. Ngoài **Định kiến chọn mẫu (Sampling bias)** đã học ở Chương 5, ta phải cảnh giác với:

### 1. Định kiến Nhận thức (Cognitive Biases) — Sự đánh lừa của bộ não
- **Thiên vị xác nhận (Confirmation bias):** Xu hướng chỉ tin vào những dữ liệu khớp với định kiến có sẵn của bản thân $\rightarrow$ *Cách trị:* Chủ động tìm kiếm các dữ liệu và cách diễn giải phản biện lại giả thuyết của mình.
- **Thiên vị khuôn mẫu (Pattern bias):** Não người luôn cố tìm kiếm quy luật ngay cả trong những con số hoàn toàn ngẫu nhiên (nhiễu/noise) $\rightarrow$ *Cách trị:* Dùng kiểm định thống kê.
- **Thiên vị đóng khung (Framing bias — David Spiegelhalter):**
  - Cách dùng từ tích cực hay tiêu cực làm thay đổi hoàn toàn đánh giá rủi ro: Bệnh viện báo cáo **"Tỷ lệ tử vong $5\%$"** nghe đáng sợ hơn nhiều so với **"Tỷ lệ sống sót $95\%$"** (dù hai con số là một!).
  - Nếu nói thêm số đếm thô: *"Có 20 trên 400 bệnh nhân đã chết"* còn gây ám ảnh mạnh hơn nữa vì não bộ hình dung ra những con người cụ thể.

---

## 4 NHÓM ĐỊNH KIẾN DỮ LIỆU (PHẦN 2): THUẬT TOÁN & LIÊN NHÓM

### 2. Định kiến Thuật toán (Algorithmic Biases)
Khi hệ thống máy tính củng cố sự bất bình đẳng xã hội dưới vỏ bọc "toán học khách quan":
- **Hệ thống tòa án Mỹ (Điều tra của *ProPublica*, 2016):** Thuật toán dự đoán nguy cơ tái phạm (COMPAS) dự báo sai rằng bị cáo Da đen sẽ tái phạm với **tỷ lệ cao gần gấp đôi** so với bị cáo Da trắng (ngay cả khi có cùng tiền án).
- **Thẻ tín dụng Apple Card & Goldman Sachs (2019):** Thuật toán xét duyệt tự động cấp hạn mức tín dụng cho nam giới **cao gấp $10$ đến $20\text{ lần}$** nữ giới (dù là vợ chồng sở hữu chung tài sản và cùng điểm tín dụng).

### 3. Định kiến Liên nhóm & Công bằng Chủng tộc (Intergroup Biases — Schwabish & Feng, Urban Institute)
- **Thứ tự sắp xếp nhãn:** Đừng mặc định xếp nhóm `"White"` (Da trắng) hoặc `"Men"` (Nam giới) lên đầu tiên như một "chuẩn mực gốc"; hãy sắp xếp theo câu chuyện dữ liệu.
- **Ghi nhận các nhóm bị bỏ sót:** Chủ động nêu rõ nếu dữ liệu thiếu nhóm phi nhị nguyên giới (non-binary/transgender).
- **Tránh lối nhìn "Quy kết thiếu hụt" (Deficit-based perspective):** Thay vì gộp các chủng tộc vào 1 biểu đồ khiến nhóm yếu thế bị phán xét theo chuẩn của nhóm đặc quyền, hãy cân nhắc tách thành các biểu đồ nhỏ (Small multiples) so sánh từng nhóm với **mức trung bình chung của quốc gia/tiểu bang**.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 78 & 79 PDF / Trang 412 & 413 Sách):</b> Đặt cạnh nhau <b>Figure 14.15</b> (Biểu đồ gộp truyền thống) và <b>Figure 14.16</b> (Biểu đồ 6 khung tách biệt của Urban Institute so sánh từng nhóm với mức trung bình quốc gia).
</div>

---

## 4 NHÓM ĐỊNH KIẾN KHÔNG GIAN TRÊN BẢN ĐỒ (SPATIAL BIASES) — PHẦN 1

Khi làm việc với bản đồ, mắt người luôn bị thao túng bởi kích thước hình học của lãnh thổ:

### 1. Định kiến Diện tích Bản đồ (Map Area Bias) — "Đất đai không đi bầu cử, con người mới đi bầu!"
- Mắt người tự động chú ý vào các vùng có diện tích rộng lớn và bỏ qua các vùng nhỏ bé.
- **Ví dụ Bầu cử Tổng thống Mỹ:** Bang nông thôn **Wyoming** có diện tích lớn gấp **$80\text{ lần}$** bang đô thị **Rhode Island**, nhưng Wyoming chỉ có chưa tới $600.000\text{ dân}$ ($3\text{ phiếu đại cử tri}$), trong khi Rhode Island có hơn $1\text{ triệu dân}$ ($4\text{ phiếu đại cử tri}$). Bản đồ địa lý thông thường phóng đại tầm ảnh hưởng chính trị của các bang ít dân!

### 2. Định kiến Phép chiếu Bản đồ (Projection Bias)
- Khi trải phẳng quả địa cầu 3D lên mặt phẳng 2D, phép chiếu phổ biến nhất trên web là **Web Mercator** đã **phóng đại kích thước của Bắc Mỹ và Châu Âu**, đồng thời **thu nhỏ bất công Châu Phi và Trung Mỹ** nằm gần xích đạo.

### ✅ Giải pháp khắc phục cho cả 2 định kiến trên: Bản đồ Cartogram!
- Thay thế ranh giới địa lý truyền thống bằng **Cartogram (Bản đồ Lục giác / Hexagon Map hoặc Ô vuông Dân số / Population Squares)**: Quy đổi diện tích mỗi bang/quốc gia tỷ lệ thuận với **quy mô dân số** hoặc **số phiếu đại cử tri**.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 81 & 82 PDF / Trang 415 & 416 Sách):</b> Ghép <b>Figure 14.17</b> (Bản đồ bầu cử Mỹ 2020 truyền thống vs. Cartogram lục giác) và <b>Figure 14.18</b> (World Population Square Map).
</div>

---

## 4 NHÓM ĐỊNH KIẾN KHÔNG GIAN (PHẦN 2): TRANH CHẤP & LOẠI TRỪ

### 3. Định kiến Lãnh thổ Tranh chấp (Disputed Territory Bias)
- Các tập đoàn bản đồ thương mại thay đổi đường biên giới tùy theo địa chỉ IP của người xem để chiều lòng chính quyền sở tại và bảo vệ lợi nhuận.
- **Ví dụ thực tế (*Washington Post*, 2020):** Sau khi Nga sáp nhập bán đảo Crimea từ Ukraine năm 2014, nếu truy cập Google Maps từ địa chỉ IP tại Nga, biên giới Crimea hiển thị bằng **nét liền** (thuộc Nga); nếu truy cập từ nơi khác trên thế giới, nó hiển thị bằng **nét đứt** (vùng tranh chấp).
- *Giải pháp:* Tham khảo các nền tảng cộng đồng mã nguồn mở như *OpenStreetMap* hoặc các dự án bản đồ bản địa như *Native Land*.

### 4. Định kiến Loại trừ trên Bản đồ (Map Exclusion Bias)
- Xóa sổ sự tồn tại của hàng triệu con người thông qua hành vi **bỏ sót (act of omission)** do thiết lập mặc định của công cụ.
- **Ví dụ tại Mỹ:** Nhiều bản đồ "Hoa Kỳ" chỉ vẽ đúng 50 tiểu bang và **bỏ qua hoàn toàn Thủ đô Washington D.C.** ($>700.000\text{ dân}$) cùng **Puerto Rico** ($>3\text{ triệu công dân Mỹ}$) và các lãnh thổ hải ngoại (Guam, Samoa thuộc Mỹ, Quần đảo Virgin) — nơi đa số cư dân là người Da đen, gốc La-tinh và người bản địa Thái Bình Dương!
- *Giải pháp:* Luôn chọn bản đồ tích hợp (`USA > States and Territories`) hoặc ghi chú rõ trong phần thuyết minh nếu công cụ không hỗ trợ.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 83 PDF / Trang 417 Sách):</b> Chèn <b>Figure 14.19</b> hiển thị tùy chọn bản đồ bao gồm đầy đủ D.C., Puerto Rico, Guam và các vùng lãnh thổ hải ngoại.
</div>

---

<!-- _class: lead -->
# 03. NGHỆ THUẬT KỂ CHUYỆN DỮ LIỆU
### CHAPTER 15: TELL AND SHOW YOUR DATA STORY

<div class="pill">Công thức Tell — Show — Why: Dẫn dắt nhận thức và thúc đẩy hành động</div>

---

## TRIẾT LÝ KỂ CHUYỆN: "TELL — SHOW — WHY"

Trong văn chương, người ta thường khuyên *"Show, don't tell"* (Hãy miêu tả hành động, đừng kể lể). Nhưng trong trực quan hóa dữ liệu, nguyên tắc vàng là **"TELL AND SHOW"**:

<div class="box">
<b>Đừng bao giờ</b> ném ra một loạt biểu đồ rồi để mặc khán giả tự đoán ý nghĩa! Biểu đồ không tự lên tiếng — bạn chính là người dẫn đường chỉ cho khán giả thấy <b>"khu rừng tổng thể" (the forest)</b> và điểm xuyết <b>"một vài cái cây đặc biệt" (special trees)</b> làm ví dụ.
</div>

### Công thức 3 bước cho mọi trang trình bày dữ liệu:
1. **TELL (Nói rõ phát hiện chính ở phía trên đồ thị):**
   - Tóm tắt thông điệp quan trọng nhất bằng **1 câu tiêu đề sắc gọn (Headline sentence)** ngay phía trên bảng/biểu đồ/bản đồ.
2. **SHOW (Trình chiếu bằng chứng thị giác ở giữa):**
   - Đưa ra biểu đồ hoặc bản đồ đã được thiết kế trung thực, tinh gọn làm bằng chứng thuyết phục.
3. **WHY (Giải thích tại sao nó quan trọng ở phía dưới đồ thị):**
   - Phát hiện này làm thay đổi tư duy, thói quen hay thúc đẩy chúng ta **hành động (take action)** như thế nào?

---

## XÂY DỰNG BẢNG PHÂN CẢNH DỮ LIỆU (DATA STORYBOARD)

Để bài thuyết trình có mạch logic tự nhiên đối với người nghe lần đầu tiếp cận, hãy sắp xếp kịch bản theo **Storyboard**:

- **4 Bước phác thảo khởi đầu (Sketch Your Data Story):**
  1. Xác định **Vấn đề thực tiễn (Problem)** thúc đẩy dự án.
  2. Chuyển hóa vấn đề thành **Câu hỏi nghiên cứu (Researchable Question)**.
  3. Lên kế hoạch **Tìm kiếm và thu thập dữ liệu (Find Data)**.
  4. Phác thảo **Ý tưởng trực quan hóa (Visualize)**.
- **3 Lời khuyên tránh lỗi sơ đẳng khi sắp xếp mạch truyện:**
  - *Luôn nêu Vấn đề và Câu hỏi trước khi đưa ra Đáp án* (não người tiếp nhận theo trình tự nhân quả này).
  - *Tóm tắt luận điểm (Insight) trước khi chiếu biểu đồ chứng minh*.
  - *Đảm bảo Câu hỏi nghiên cứu và Kết luận cuối cùng khớp nhau* (hãy mạnh dạn sửa lại câu hỏi ban đầu nếu dữ liệu dẫn bạn tới khám phá mới thú vị hơn!).

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 87 & 88 PDF / Trang 421 & 422 Sách):</b> Ghép <b>Figure 15.1</b> (Bản phác thảo tay 4 bước Storyboard) và <b>Figure 15.2</b> (2 biểu đồ kết quả khảo sát 3.000 độc giả áp dụng chuẩn cấu trúc: Câu tóm tắt <i>Tell</i> ở đỉnh + Đồ thị <i>Show</i> ở giữa + Hành động sửa sách <i>Why</i> màu xanh ở đáy).
</div>

---

## LÀM NỔI BẬT Ý NGHĨA BẰNG MÀU SẮC & CHÚ THÍCH TRỰC TIẾP

Đừng dừng lại ở biểu đồ mặc định — hãy dùng **màu sắc tương phản** và **chú thích (Annotations)** để hướng mắt người đọc vào đúng thông điệp cốt lõi:

### Case Study: Sản lượng Nhựa Toàn cầu từ 1950 đến 2015 (*Our World In Data*)
- **Bước 1 — Biểu đồ đường mặc định (Figure 15.3):**
  - Chỉ cho thấy sản lượng nhựa hàng năm tăng đều đặn theo thời gian $\rightarrow$ **Chưa đủ sức nặng!**
- **Bước 2 — Khám phá thông điệp lớn & Tái thiết kế thành Biểu đồ Miền tách cột (Figure 15.5):**
  - Phân tích tổng tích lũy cho thấy: **Hơn một nửa ($59\%$) tổng lượng nhựa từng được sản xuất trong toàn bộ lịch sử nhân loại mới chỉ được tạo ra từ năm 2000 trở lại đây (trong 15 năm cuối)!**
  - **Kỹ thuật biến hình đồ thị:**
    1. Tách dữ liệu thành 2 cột: `Before 2000` và `Since 2000` (giữ chung mốc năm 2000 để miền nối liền nhau).
    2. Chuyển từ Line Chart sang **Area Chart (Biểu đồ miền)** để thể hiện *tổng khối lượng tích lũy* dưới đường cong.
    3. Tô **màu xám nhạt** cho giai đoạn trước năm 2000 và **màu xanh đậm nổi bật** cho giai đoạn từ năm 2000, kèm dòng chữ chú thích trực tiếp **`59% of all plastic ever manufactured`** ngay trong vùng màu xanh!

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 90 & 92 PDF / Trang 424 & 426 Sách):</b> Đặt song song <b>Figure 15.3</b> (Line chart mặc định nhạt nhòa) và <b>Figure 15.5</b> (Area chart tô màu xanh-xám làm nổi bật $59\%$ lượng nhựa sản xuất từ năm 2000).
</div>

<!-- 
[Ghi chú thuyết trình]:
Hãy nhìn sự lột xác từ Figure 15.3 sang Figure 15.5. Cùng một bộ dữ liệu sản lượng nhựa, nhưng chỉ bằng cách chuyển sang biểu đồ miền (Area chart), tô màu xám cho quá khứ và màu xanh đậm cho giai đoạn từ năm 2000 kèm con số 59%, biểu đồ lập tức truyền tải một thông điệp môi trường cực kỳ mạnh mẽ ngay từ cái nhìn đầu tiên!
-->

---

## MINH BẠCH NGUỒN GỐC, SỰ BẤT ĐỊNH & ĐỊNH DẠNG KỂ CHUYỆN MỚI

Một câu chuyện dữ liệu chỉ thực sự thuyết phục khi người kể xây dựng được **niềm tin và sự minh bạch (Credibility)**:

1. **4 Nguyên tắc xây dựng uy tín cho tác phẩm dữ liệu:**
   - Trình bày dữ liệu trung thực, cảnh báo người đọc nếu có nguy cơ suy diễn quá đà.
   - Ghi rõ nguồn gốc dữ liệu (Source links) và ghi nhận công sức của các cộng sự (Credits).
   - Lưu trữ lại toàn bộ quá trình xử lý (qua các tab bảng tính hoặc kho mã nguồn GitHub) để bất kỳ ai cũng có thể kiểm chứng và tái lập.
   - **Thừa nhận giới hạn và sự bất định (Disclose Uncertainty):** Dùng thanh sai số (Error bars) hoặc tách cột để vẽ **Đường nét liền (Solid line)** cho *Dữ liệu thực tế đã quan sát (Observed data)* và **Đường nét đứt (Dashed line)** cho *Dữ liệu dự báo tương lai (Projected data)*.
2. **Vượt ra khỏi trang giấy tĩnh — Các định dạng kể chuyện hiện đại:**
   - **Trang web tương tác (Interactive Web / Iframes):** Kết hợp bài viết dẫn dắt với đồ thị sống động.
   - **Video Screencast thuyết minh:** Quay màn hình tương tác trực tiếp với dữ liệu kèm giọng đọc phân tích.
   - **Data Walk (Đi bộ cùng dữ liệu):** In các biểu đồ khổ lớn trưng bày trong không gian cộng đồng để các bên liên quan cùng đi qua, thảo luận và đối chiếu với trải nghiệm sống thực tế của họ.

<div class="img-guide">
🖼️ <b>Hình minh họa từ sách (Trang 93 PDF / Trang 427 Sách):</b> Chèn <b>Figure 15.6</b> minh họa kỹ thuật tách cột <code>pre-2020</code> và <code>post-2020</code> để vẽ đường nét liền (Observed) nối tiếp đường nét đứt (Projected).
</div>

---

<!-- _class: lead -->
# TỔNG KẾT TOÀN BỘ HÀNH TRÌNH
### TỪ DỮ LIỆU THÔ ĐẾN CÂU CHUYỆN TRUYỀN CẢM HỨNG

- **Phần 1 — Nền tảng Dữ liệu (Ch. 3, 4, 5):** Săn tìm dữ liệu có định hướng, bảo vệ quyền riêng tư, làm sạch dữ liệu bẩn và chuẩn hóa để tạo ra những phép so sánh công bằng.
- **Phần 2 — Trực quan hóa Biểu đồ (Ch. 6):** Tuân thủ quy tắc gốc $0$ và tổng $100\%$, loại bỏ rác đồ họa và chọn đúng loại biểu đồ cho từng câu chuyện.
- **Phần 3 — Trực quan hóa Không gian (Ch. 7):** Phân biệt Point/Polygon, thiết kế bảng màu & phân khoảng Choropleth hợp lý và luôn chuẩn hóa dữ liệu bản đồ.
- **Phần 4 — Đạo đức & Kể chuyện (Ch. 14, 15):** Tỉnh táo trước các chiêu trò bóp méo đồ thị, giảm thiểu định kiến và kể chuyện theo công thức **Tell — Show — Why**.

<div class="pill">THANK YOU FOR WATCHING! — Q&A</div>