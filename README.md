# UNIFIED LEGAL KNOWLEDGE & COMPLIANCE ARCHITECTURE (VLK-001 · GLICE-0.1)

**Trạng thái tài liệu:** LOCKED SPECIFICATION (DRAFT v1.0.0)  
**Ngày khóa cấu trúc:** 2026-11-25  
**Phạm vi:** Hệ thống tri thức pháp luật Việt Nam (VLK-001) & Khung khám phá tuân thủ pháp lý toàn cầu (GLICE v0.1)  
**Lưu ý pháp lý:** Tài liệu tham chiếu cấu trúc tri thức và tuân thủ pháp lý; không phải ý kiến tư vấn pháp lý chính thức.

---

## Mục lục

1. [Tuyên bố cốt lõi & Nguyên tắc vận hành](#tuyên-bố-cốt-lõi--nguyên-tắc-vận-hành)
2. [Phần I: Kiến trúc hệ thống 6 lớp (VLK-001)](#phần-i-kiến-trúc-hệ-thống-6-lớp-vlk-001)
3. [Phần II: Hệ thống phân loại lĩnh vực & phân ngành pháp luật](#phần-ii-hệ-thống-phân-loại-lĩnh-vực--phân-ngành-pháp-luật)4. [Phần III: Hệ thống nguồn pháp lý & Kiểm chứng hiệu lực](#phần-iii-hệ-thống-nguồn-pháp-lý--kiểm-chứng-hiệu-lực)
5. [Phần IV: Bộ máy phân tích quy định & Đồ thị quan hệ pháp luật](#phần-iv-bộ-máy-phân-tích-quy-định--đồ-thị-quan-hệ-pháp-luật)
6. [Phần V: Lộ trình phổ cập 12 giai đoạn & Tiêu chuẩn hoàn thành phân hệ](#phần-v-lộ-trình-phổ-cập-12-giai-đoạn--tiêu-chuẩn-hoàn-thành-phân-hệ)
7. [Phần VI: Kiến trúc dữ liệu chuẩn (40 cột GLICE + Bảng quan hệ VLK)](#phần-vi-kiến-trúc-dữ-liệu-chuẩn-40-cột-glice--bảng-quan-hệ-vlk)
8. [Phần VII: Kiểm định chất lượng, Khởi động `LAW-000` & Trạng thái triển khai](#phần-vii-kiểm-định-chất-lượng-khởi-động-law-000--trạng-thái-triển-khai)

---

## Tuyên bố cốt lõi & Nguyên tắc vận hành

Hệ thống được thiết kế để chuyển hóa văn bản pháp luật từ dạng liệt kê tĩnh sang **hệ thống tri thức vận hành có khả năng kiểm chứng**, đáp ứng 6 năng lực cốt lõi:

1. Phân loại toàn diện các lĩnh vực và phân ngành pháp luật.
2. Truy xuất quy định từ nguồn gốc và văn bản chính thức.
3. Xác định chính xác tình trạng hiệu lực và lịch sử sửa đổi tại một thời điểm pháp lý cụ thể.
4. Kết nối quy định với chủ thể, hành vi, quyền, nghĩa vụ, chế tài và hậu quả pháp lý.
5. Phân tích tình huống thực tế và đánh giá rủi ro tuân thủ.
6. Cập nhật, đối chiếu và kiểm chứng khi có văn bản mới hoặc thay đổi chính sách.

### Chuỗi suy luận pháp lý chuẩn

Mọi vấn đề pháp lý và tình huống tuân thủ phải được truy xuất theo chuỗi:

`SỰ KIỆN / HÀNH VI → CHỦ THỂ → QUAN HỆ PHÁP LUẬT → CĂN CỨ PHÁP LÝ → ĐIỀU KIỆN ÁP DỤNG → QUYỀN / NGHĨA VỤ / CẤM ĐOÁN → HẬU QUẢ / CHẾ TÀI → CƠ CHẾ GIẢI QUYẾT & THỰC THI`

Không kết luận hợp pháp hay vi phạm chỉ dựa trên tên gọi của hành vi; phải kiểm tra đầy đủ yếu tố cấu thành, hiệu lực, phạm vi và quy tắc áp dụng.

---

## Phần I: Kiến trúc hệ thống 6 lớp (VLK-001)

- **L0 — LEGAL FOUNDATION:** Hiến pháp, nguyên tắc pháp quyền, chủ quyền, quyền con người, quyền công dân.
- **L1 — LEGAL STRUCTURE:** Hệ thống pháp luật, ngành luật, nguồn luật, văn bản quy phạm pháp luật (VBQPPL) và điều ước/văn kiện quốc tế.
- **L2 — LEGAL DOMAINS:** Các cụm ngành, lĩnh vực và phân ngành điều chỉnh.
- **L3 — LEGAL RULES:** Điều, khoản, điểm, điều kiện áp dụng, ngoại lệ, hành vi bị cấm, chế tài và hậu quả pháp lý.
- **L4 — LEGAL OPERATIONS:** Cơ quan có thẩm quyền, thủ tục, hồ sơ, thực thi, kiểm tra/giám sát và giải quyết tranh chấp.
- **L5 — LEGAL INTELLIGENCE:** Phân tích tình huống, kiểm tra tính hợp pháp, đánh giá tuân thủ, kiểm chứng hiệu lực, quản trị rủi ro và cập nhật tri thức.

---

## Phần II: Hệ thống phân loại lĩnh vực & phân ngành pháp luật

Hệ thống kết hợp cây phân loại chuyên sâu **8 cụm / 32+ phân hệ** (tối ưu cho pháp luật Việt Nam) với khả năng mở rộng đa tài phán (Global Jurisdiction).

### A. Nhà nước và nền tảng pháp lý

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `LAW-001` | Hiến pháp | Tổ chức quyền lực nhà nước, quyền con người, quyền công dân |
| `LAW-002` | Lý luận nhà nước và pháp luật | Bản chất, chức năng, nguồn luật, nguyên tắc pháp luật |
| `LAW-003` | Luật tổ chức bộ máy nhà nước | Quốc hội, Chính phủ, Tòa án, Viện kiểm sát, chính quyền địa phương |
| `LAW-004` | Luật hành chính | Quản lý hành chính nhà nước, thủ tục và quyết định hành chính |
| `LAW-005` | Luật cán bộ, công chức, viên chức | Tuyển dụng, bổ nhiệm, nghĩa vụ, kỷ luật, trách nhiệm công vụ |
| `LAW-006` | Luật bầu cử và dân chủ | Bầu cử, trưng cầu ý dân, quyền tham gia quản lý nhà nước |

### B. Quyền cá nhân và quan hệ xã hội

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `LAW-007` | Luật dân sự | Chủ thể, giao dịch dân sự, đại diện, thời hiệu, nghĩa vụ |
| `LAW-008` | Luật tài sản | Quyền sở hữu, chiếm hữu, quyền khác đối với tài sản |
| `LAW-009` | Luật hợp đồng | Giao kết, thực hiện, sửa đổi, chấm dứt, vi phạm hợp đồng |
| `LAW-010` | Luật hôn nhân và gia đình | Kết hôn, quan hệ vợ chồng, cha mẹ và con, tài sản gia đình |
| `LAW-011` | Luật thừa kế | Thừa kế theo di chúc, thừa kế theo pháp luật, phân chia di sản |
| `LAW-012` | Luật lao động | Quan hệ lao động, hợp đồng lao động, tiền lương, an toàn lao động |
| `LAW-013` | Luật an sinh xã hội | Bảo hiểm xã hội, bảo hiểm y tế, bảo hiểm thất nghiệp, trợ cấp |
| `LAW-014` | Luật giáo dục | Quyền học tập, hệ thống giáo dục, quản lý giáo dục |

### C. Kinh tế, tài chính và tài sản

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `LAW-015` | Luật doanh nghiệp | Thành lập, loại hình, quản trị, tổ chức lại, giải thể doanh nghiệp |
| `LAW-016` | Luật thương mại | Mua bán hàng hóa, cung ứng dịch vụ, xúc tiến thương mại, trung gian |
| `LAW-017` | Luật đầu tư | Đầu tư kinh doanh trong nước và đầu tư nước ngoài, ưu đãi/hỗ trợ |
| `LAW-018` | Luật tài chính công | Ngân sách nhà nước, đầu tư công, quản lý tài sản công, nợ công |
| `LAW-019` | Luật thuế | Thuế thu nhập, thuế GTGT, thuế tiêu thụ đặc biệt, quản lý thuế |
| `LAW-020` | Luật ngân hàng | Tiền tệ, hoạt động ngân hàng, tín dụng, thanh toán, ngoại hối |
| `LAW-021` | Luật chứng khoán | Chào bán, niêm yết, giao dịch chứng khoán, công bố thông tin |
| `LAW-022` | Luật bảo hiểm | Kinh doanh bảo hiểm, hợp đồng bảo hiểm và các cơ chế bảo hiểm |
| `LAW-023` | Luật cạnh tranh | Hành vi hạn chế cạnh tranh, tập trung kinh tế, cạnh tranh không lành mạnh |
| `LAW-024` | Luật phá sản | Mất khả năng thanh toán, phục hồi, thủ tục phá sản |
| `LAW-025` | Luật đất đai | Quyền sử dụng đất, quy hoạch, giao đất, cho thuê đất, thu hồi, bồi thường |
| `LAW-026` | Luật nhà ở và kinh doanh bất động sản | Sở hữu/phát triển nhà ở, dự án và giao dịch bất động sản |

### D. Trật tự, an ninh và trách nhiệm pháp lý

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `LAW-027` | Luật hình sự | Tội phạm, yếu tố cấu thành tội phạm, hình phạt, biện pháp tư pháp |
| `LAW-028` | Luật xử lý vi phạm hành chính | Vi phạm hành chính, hình thức xử phạt, biện pháp khắc phục hậu quả |
| `LAW-029` | Luật tố tụng hình sự | Khởi tố, điều tra, truy tố, xét xử, thẩm quyền và thủ tục hình sự |
| `LAW-030` | Luật thi hành án | Thi hành án dân sự, thi hành án hình sự, cưỡng chế thi hành |
| `LAW-031` | Luật an ninh quốc gia | Bảo vệ an ninh chính trị, kinh tế, tư tưởng, văn hóa, xã hội |
| `LAW-032` | Luật quốc phòng | Quốc phòng toàn dân, khu vực phòng thủ, nghĩa vụ quân sự |

### E. Công nghệ, dữ liệu và sở hữu trí tuệ

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `TECH-001` | Luật công nghệ thông tin | Hoạt động ứng dụng và phát triển CNTT, hạ tầng và dịch vụ số |
| `TECH-002` | Luật an ninh mạng | Bảo vệ an ninh mạng, phòng chống tội phạm và đe dọa trên không gian mạng |
| `TECH-003` | Luật dữ liệu và bảo vệ dữ liệu cá nhân | Thu thập, lưu trữ, xử lý, chia sẻ, chuyển giao dữ liệu và dữ liệu cá nhân |
| `TECH-004` | Luật giao dịch điện tử | Giá trị pháp lý của thông điệp dữ liệu, chữ ký điện tử, giao dịch số |
| `TECH-005` | Luật sở hữu trí tuệ | Quyền tác giả, quyền liên quan, sáng chế, nhãn hiệu, kiểu dáng, bí mật |
| `TECH-006` | Luật AI và công nghệ mới | Quản trị rủi ro, trách nhiệm và khung pháp lý cho trí tuệ nhân tạo/công nghệ mới |
| `TECH-007` | Luật viễn thông | Hạ tầng mạng, dịch vụ viễn thông, tài nguyên viễn thông, quản lý thuê bao |
| `TECH-008` | Luật xuất bản và báo chí | Hoạt động xuất bản, báo chí, phát thanh, truyền hình và thông tin điện tử |

### F. Tài nguyên và phát triển

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `ENV-001` | Luật môi trường | Bảo vệ môi trường, đánh giá tác động môi trường, kiểm soát ô nhiễm |
| `ENV-002` | Luật tài nguyên nước | Quản lý, khai thác, sử dụng và bảo vệ nguồn nước |
| `ENV-003` | Luật khoáng sản | Thăm dò, khai thác, chế biến và quản lý tài nguyên khoáng sản |
| `ENV-004` | Luật lâm nghiệp | Quản lý, bảo vệ, phát triển và sử dụng rừng |
| `ENV-005` | Luật năng lượng | Điện lực, năng lượng tái tạo, tiết kiệm và sử dụng năng lượng hiệu quả |
| `ENV-006` | Luật xây dựng | Quy hoạch xây dựng, cấp phép, thi công, giám sát và nghiệm thu công trình |
| `ENV-007` | Luật giao thông vận tải | Đường bộ, đường sắt, hàng hải, hàng không và an toàn giao thông |
| `ENV-008` | Luật nông nghiệp và thủy sản | Trồng trọt, chăn nuôi, lâm ngư nghiệp, thủy sản và an toàn thực phẩm |

### G. Tư pháp và giải quyết tranh chấp

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `JUST-001` | Tố tụng dân sự | Trình tự, thủ tục giải quyết vụ việc dân sự tại Tòa án |
| `JUST-002` | Tố tụng hành chính | Khiếu kiện và giải quyết vụ án hành chính tại Tòa án |
| `JUST-003` | Trọng tài thương mại | Giải quyết tranh chấp thương mại bằng hội đồng trọng tài |
| `JUST-004` | Hòa giải | Hòa giải cơ sở, hòa giải thương mại, hòa giải/đối thoại tại Tòa án |
| `JUST-005` | Luật luật sư và công chứng | Hành nghề luật sư, dịch vụ pháp lý, công chứng và chứng thực |
| `JUST-006` | Trợ giúp pháp lý | Hỗ trợ pháp lý miễn phí cho người thuộc diện được trợ giúp |
| `JUST-007` | Án lệ và thực tiễn xét xử | Lập luận xét xử, án lệ và hướng dẫn áp dụng thống nhất pháp luật |

### H. Quan hệ quốc tế và lĩnh vực đặc thù

| Mã | Phân hệ | Nội dung trọng tâm |
| :--- | :--- | :--- |
| `INT-001` | Công pháp quốc tế | Chủ thể công pháp, chủ quyền, điều ước quốc tế, trách nhiệm quốc gia |
| `INT-002` | Tư pháp quốc tế | Xung đột pháp luật, thẩm quyền và quan hệ dân sự có yếu tố nước ngoài |
| `INT-003` | Luật thương mại quốc tế | Cam kết WTO, FTA, thương mại xuyên biên giới, phòng vệ thương mại |
| `INT-004` | Luật đầu tư quốc tế | Hiệp định đầu tư, bảo hộ nhà đầu tư, giải quyết tranh chấp đầu tư |
| `INT-005` | Luật ngoại giao và lãnh sự | Quan hệ ngoại giao, cơ quan đại diện, quyền ưu đãi và miễn trừ |
| `INT-006` | Luật hàng hải và hàng không quốc tế | Vận tải quốc tế, điều ước hàng hải/hàng không, giới hạn trách nhiệm |

> **Quy tắc phân loại:** Một số phân hệ là lĩnh vực nghiên cứu liên ngành (không nhất thiết tương ứng 1–1 với một đạo luật duy nhất). Một sự kiện thực tế có thể đồng thời chịu sự điều chỉnh của nhiều phân hệ.

---

## Phần III: Hệ thống nguồn pháp lý & Kiểm chứng hiệu lực

### 1. Phân loại nguồn & Giá trị sử dụng

| Loại nguồn | Cách sử dụng trong hệ thống |
| :--- | :--- |
| Hiến pháp | Nền tảng pháp lý cao nhất |
| Bộ luật, luật, nghị quyết của Quốc hội | Quy phạm pháp luật thuộc thẩm quyền lập pháp của Quốc hội |
| Pháp lệnh, nghị quyết của UBTVQH; Nghị định; Quyết định; Thông tư | Quy phạm pháp luật ban hành đúng thẩm quyền và hình thức theo luật |
| Điều ước quốc tế | Áp dụng theo quy định pháp luật về điều ước quốc tế và phạm vi tham gia |
| Án lệ | Nguồn tham khảo và áp dụng theo cơ chế công bố, lựa chọn án lệ |
| Bản án, quyết định | Phân tích thực tiễn xét xử và giải quyết vụ việc |
| Công văn hướng dẫn / văn bản hành chính cá biệt | Phải kiểm tra thẩm quyền và tính chất; không mặc nhiên là VBQPPL |
| Tài liệu học thuật, giáo trình, bình luận | Hỗ trợ giải thích và nghiên cứu; không thay thế văn bản gốc |

### 2. Nguồn tra cứu chính thức (Việt Nam)

- **Cơ sở dữ liệu quốc gia về văn bản pháp luật:** `https://vbpl.vn/` (ưu tiên tra cứu văn bản, hiệu lực, lịch sử sửa đổi, văn bản liên quan).
- **Cổng thông tin điện tử Chính phủ / Văn bản Chính phủ:** `https://vanban.chinhphu.vn/`
- **Quốc hội Việt Nam:** `https://quochoi.vn/`
- **Tòa án nhân dân tối cao:** `https://www.toaan.gov.vn/`
- **Viện kiểm sát nhân dân tối cao:** `https://vksndtc.gov.vn/`
- **Cổng thông tin khung khám phá tuân thủ (GLICE):** `https://sites.google.com/view/legalintelligencecompliancedis`

### 3. Mốc văn bản nền tảng Việt Nam đã ghi nhận (cần xác minh chi tiết theo từng điều khoản)

| Văn bản / Số hiệu | Vai trò / Mốc hiệu lực ghi nhận |
| :--- | :--- |
| Hiến pháp 2013 (sửa đổi, bổ sung năm 2025) | Nền tảng hiến định |
| Nghị quyết `203/2025/QH15` | Sửa đổi, bổ sung Hiến pháp (ghi nhận hiệu lực từ `16/06/2025`) |
| Văn bản hợp nhất `52/VBHN-VPQH` | Văn bản hợp nhất Hiến pháp (ghi nhận ban hành `21/07/2025`) |
| Luật `64/2025/QH15` | Luật Ban hành VBQPPL (ghi nhận hiệu lực từ `01/04/2025`) |
| Luật `87/2025/QH15` | Sửa đổi, bổ sung Luật Ban hành VBQPPL (ghi nhận hiệu lực từ `01/07/2025`) |
| Văn bản hợp nhất `54/VBHN-VPQH` | Bản hợp nhất Luật Ban hành VBQPPL (ghi nhận xác thực `11/08/2025`) |

> **Lưu ý kiểm chứng bắt buộc:** Không sử dụng nguyên trạng một điều khoản của văn bản gốc nếu điều khoản đó đã được sửa đổi, bổ sung hoặc bãi bỏ bởi văn bản sau (ví dụ: đối chiếu phần sửa đổi của Luật `87/2025/QH15` khi đọc Luật `64/2025/QH15`).

### 4. Sáu trạng thái hiệu lực (`Validity Engine`)

- `VALID` *(Còn hiệu lực)*: Đang có hiệu lực tại thời điểm kiểm tra.
- `PARTIALLY_VALID` *(Hiệu lực một phần)*: Một số điều, khoản, điểm hoặc phạm vi đã hết hiệu lực, bị sửa đổi hoặc bãi bỏ.
- `NOT_YET_EFFECTIVE` *(Chưa có hiệu lực)*: Đã ban hành nhưng ngày có hiệu lực chưa tới.
- `EXPIRED` *(Hết hiệu lực)*: Đã hết hiệu lực toàn bộ do hết thời hạn, bị thay thế hoặc bãi bỏ.
- `SUSPENDED` *(Tạm ngưng áp dụng)*: Tạm ngưng hiệu lực hoặc tạm ngưng áp dụng theo quyết định có thẩm quyền.
- `UNVERIFIED` *(Chưa xác minh)*: Chưa đủ nguồn chính thức để kết luận; không dùng làm căn cứ pháp lý kết luận.

### 5. Quy trình xác minh & Quy tắc chống lỗi pháp lý

**6 bước xác minh:**
1. Xác định văn bản gốc (số hiệu, cơ quan ban hành, ngày ban hành, toàn văn).
2. Kiểm tra thuộc tính (ngày có hiệu lực, phạm vi điều chỉnh, hiệu lực theo không gian/đối tượng).
3. Kiểm tra lịch sử pháp lý (sửa đổi, bổ sung, thay thế, đình chỉ, bãi bỏ).
4. Đối chiếu văn bản hợp nhất và văn bản gốc để xác định chính xác nguồn sửa đổi.
5. Kiểm tra văn bản hướng dẫn thi hành (nghị định, thông tư) và điều khoản chuyển tiếp.
6. Chốt thời điểm pháp lý (thời điểm xảy ra sự kiện, xác lập/thực hiện giao dịch, hoặc thời điểm giải quyết vụ việc).

**Quy tắc chống lỗi:**
- Không lấy ngày ban hành thay cho ngày có hiệu lực.
- Không coi văn bản hợp nhất là văn bản quy phạm pháp luật ban hành mới độc lập.
- Không coi văn bản hướng dẫn hành chính là có giá trị pháp lý cao hơn luật.
- Không kết luận văn bản hết hiệu lực toàn bộ khi chỉ một phần bị sửa đổi/bãi bỏ.
- Không dùng kết quả tìm kiếm phổ thông thay thế văn bản nguồn chính thức.
- Không áp dụng hồi tố khi không có căn cứ pháp luật cho phép.
- Khi có xung đột văn bản, đối chiếu thẩm quyền, thứ bậc hiệu lực pháp lý, thời điểm ban hành, phạm vi điều chỉnh và nguyên tắc xử lý xung đột.

---

## Phần IV: Bộ máy phân tích quy định & Đồ thị quan hệ pháp luật

### 1. Cấu trúc đối tượng quy định (`LEGAL RULE OBJECT`)

Mỗi quy định (điều, khoản, điểm) được chuẩn hóa theo các trường:
- **IDENTITY:** Số hiệu, tên văn bản, điều, khoản, điểm.
- **SOURCE:** Cơ quan ban hành, URL nguồn chính thức, bản gốc/bản hợp nhất.
- **VALIDITY:** Ngày ban hành, ngày có hiệu lực, ngày hết hiệu lực, trạng thái hiệu lực.
- **SUBJECT:** Cơ quan, tổ chức, cá nhân hoặc đối tượng chịu sự điều chỉnh/được bảo hộ.
- **CONDITION:** Điều kiện, ngưỡng hoặc phạm vi để quy định phát sinh hiệu lực áp dụng.
- **RIGHT:** Quyền được ghi nhận hoặc bảo vệ.
- **OBLIGATION:** Nghĩa vụ phải thực hiện.
- **PROHIBITION:** Hành vi bị nghiêm cấm hoặc hạn chế.
- **EXCEPTION:** Trường hợp ngoại lệ, miễn trừ hoặc loại trừ.
- **CONSEQUENCE:** Hậu quả pháp lý, chế tài xử lý, trách nhiệm bồi thường/hành chính/hình sự.
- **ENFORCEMENT:** Cơ quan có thẩm quyền, trình tự/thủ tục, hồ sơ thực thi hoặc giải quyết tranh chấp.
- **RELATION:** Quan hệ sửa đổi, bổ sung, thay thế, dẫn chiếu, quy định chi tiết hoặc hướng dẫn.

### 2. Đồ thị quan hệ pháp luật (`Knowledge Graph`)

Thay vì tách rời từng đạo luật, mô hình ánh xạ một chủ thể trung tâm (ví dụ: **DOANH NGHIỆP**) qua các trục quan hệ:
- **Sở hữu:** Thành viên/cổ đông, vốn, tài sản, quyền tài sản.
- **Quản trị:** Cơ cấu tổ chức, người đại diện theo pháp luật, điều hành, kiểm soát.
- **Tài chính:** Kế toán, thuế, ngân hàng, dòng tiền, nghĩa vụ tài chính.
- **Nhân sự:** Hợp đồng lao động, tiền lương, BHXH/BHYT/BHTN, an toàn lao động.
- **Thương mại:** Hợp đồng, mua bán/dịch vụ, đối tác, khách hàng, tranh chấp.
- **Công nghệ & Dữ liệu:** Dữ liệu, dữ liệu cá nhân, an ninh mạng, sở hữu trí tuệ.
- **Tuân thủ & Trách nhiệm:** Điều kiện kinh doanh, giấy phép, chế tài hành chính/dân sự/hình sự, quản trị rủi ro.

Các đồ thị tương tự áp dụng cho: Cá nhân, Hộ gia đình, Tổ chức tín dụng, Cơ quan nhà nước, Tổ chức xã hội, Nhà đầu tư, Chủ sở hữu tài sản, Chủ thể/bên xử lý dữ liệu, Chủ thể giao dịch xuyên biên giới.

---

## Phần V: Lộ trình phổ cập 12 giai đoạn & Tiêu chuẩn hoàn thành phân hệ

### 1. Lộ trình 12 giai đoạn (`Curriculum Engine`)

| Giai đoạn | Chủ đề trọng tâm | Mục tiêu năng lực cốt lõi |
| :--- | :--- | :--- |
| `00` | Nhập môn pháp luật (`LAW-000`) | Nắm vững 7 khái niệm nền tảng và cách đọc luật |
| `01` | Hiến pháp (`LAW-001`) | Hiểu cấu trúc quyền lực nhà nước và quyền/nghĩa vụ cơ bản |
| `02` | Hệ thống văn bản (`LAW-002` & Nguồn) | Biết đọc, phân tầng, truy xuất và kiểm chứng hiệu lực văn bản |
| `03` | Dân sự (`LAW-007` – `LAW-011`) | Hiểu chủ thể, giao dịch, nghĩa vụ, hợp đồng, tài sản, thừa kế |
| `04` | Hành chính (`LAW-003` – `LAW-006`) | Hiểu quản lý hành chính nhà nước, thủ tục và khiếu nại/tố tụng |
| `05` | Hình sự (`LAW-027`, `LAW-029`) | Hiểu tội phạm, cấu thành, trách nhiệm hình sự và tố tụng |
| `06` | Tố tụng & Giải quyết tranh chấp (`JUST-001` – `JUST-007`) | Hiểu cơ chế xét xử, trọng tài, hòa giải, thi hành án |
| `07` | Kinh tế – Doanh nghiệp (`LAW-015` – `LAW-017`, `LAW-023` – `LAW-024`) | Hiểu pháp lý doanh nghiệp, thương mại, đầu tư, cạnh tranh, phá sản |
| `08` | Tài chính – Tài sản (`LAW-018` – `LAW-022`, `LAW-025` – `LAW-026`) | Hiểu ngân sách, thuế, tín dụng, đất đai, bất động sản |
| `09` | Công nghệ – Dữ liệu (`TECH-001` – `TECH-008`) | Hiểu giao dịch điện tử, dữ liệu, an ninh mạng, SHTT, công nghệ mới |
| `10` | Tài nguyên – Phát triển & Lĩnh vực khác (`ENV-001` – `ENV-008`, `LAW-012` – `LAW-014`, `LAW-028`, `LAW-030` – `LAW-032`) | Bao phủ lao động, an sinh, môi trường, xây dựng, giao thông, an ninh/quốc phòng |
| `11` | Pháp luật quốc tế (`INT-001` – `INT-006`) | Hiểu quan hệ pháp luật có yếu tố nước ngoài và xuyên biên giới |

**5 phương pháp học tập mỗi giai đoạn:**
1. Nắm 20% nguyên lý nền tảng để hiểu 80% cấu trúc phân hệ.
2. Đọc văn bản pháp luật gốc/chính thức.
3. Phân tích tình huống thực tế theo chuỗi suy luận.
4. Đối chiếu văn bản sửa đổi, hướng dẫn và văn bản liên quan.
5. Tự kiểm tra năng lực giải thích, dẫn nguồn và áp dụng.

### 2. Tiêu chuẩn hoàn thành một phân hệ

Một phân hệ được coi là hoàn thành khi người học/hệ thống có thể:
- Xác định đúng phạm vi điều chỉnh và đối tượng áp dụng.
- Giải thích rõ các khái niệm cốt lõi.
- Truy xuất đúng căn cứ pháp luật đến điều, khoản, điểm và dẫn nguồn chính xác.
- Phân biệt rõ quyền, nghĩa vụ, hành vi bị cấm, điều kiện và ngoại lệ.
- Xác định cơ quan có thẩm quyền, hậu quả pháp lý và cơ chế giải quyết.
- Kiểm chứng hiệu lực văn bản tại thời điểm áp dụng và giải quyết được tình huống thực tế cơ bản.

---

## Phần VI: Kiến trúc dữ liệu chuẩn (40 cột GLICE + Bảng quan hệ VLK)

### 1. Schema 40 cột chuẩn (`C01–C40` | Excel `A–AN`)

| Cột | Excel | Trường dữ liệu (EN / VI) | Mô tả chuẩn hóa |
| :--- | :--- | :--- | :--- |
| `C01` | `A` | Record ID / Mã bản ghi | Mã định danh duy nhất cho từng văn bản hoặc điều khoản |
| `C02` | `B` | Jurisdiction / Tài phán & Khu vực | Quốc gia, vùng lãnh thổ, liên minh siêu quốc gia hoặc hệ thống điều ước |
| `C03` | `C` | Legal Domain / Lĩnh vực pháp luật | Lĩnh vực cấp cao (công pháp, tư pháp, hình sự, thuế, lao động, dữ liệu, môi trường, SHTT, thương mại...) |
| `C04` | `D` | Legal Subdomain / Phân ngành pháp luật | Phân ngành chuyên biệt phục vụ lọc và lập ma trận nghĩa vụ |
| `C05` | `E` | Instrument Type / Loại văn bản | Hiến chương, luật, nghị định, thông tư, công ước, hiệp định, quy định, chỉ thị, quyết định... |
| `C06` | `F` | Document Number / Số hiệu & Mã đăng ký | Số hiệu văn bản, số công báo, ký hiệu điều ước hoặc mã định danh chính thức |
| `C07` | `G` | Official Title / Tên gọi chính thức | Tên gọi chính thức (ưu tiên giữ nguyên văn gốc kết hợp bản dịch/chú giải khi cần) |
| `C08` | `H` | Issuing Authority / Cơ quan ban hành & Lưu chiểu | Cơ quan lập pháp, hành pháp, tư pháp, tổ chức quốc tế hoặc cơ quan lưu chiểu |
| `C09` | `I` | Promulgation Date / Ngày ban hành & Ký kết | Ngày thông qua, ký kết hoặc ban hành (`YYYY-MM-DD`), ghi rõ bản chất mốc ngày |
| `C10` | `J` | Effective Date / Ngày có hiệu lực & Áp dụng | Ngày có hiệu lực hoặc bắt đầu áp dụng (`YYYY-MM-DD`), ghi rõ theo từng giai đoạn/tài phán |
| `C11` | `K` | Expiry / Termination / Ngày hết hiệu lực & Chấm dứt | Ngày hết hiệu lực/chấm dứt hoặc ghi nhận sau khi kiểm tra |
| `C12` | `L` | Legal Status / Tình trạng hiệu lực | Trạng thái hiệu lực chuẩn hóa (`VALID`, `PARTIALLY_VALID`, `NOT_YET_EFFECTIVE`, `EXPIRED`, `SUSPENDED`, `UNVERIFIED` hoặc theo tài phán) |
| `C13` | `M` | Amendment History / Lịch sử sửa đổi | Văn bản sửa đổi, bổ sung, đính chính, nghị định thư, bản hợp nhất và lịch sử bãi bỏ |
| `C14` | `N` | Part / Chapter / Phần & Chương | Phần hoặc Chương chứa quy định |
| `C15` | `O` | Section / Mục & Tiểu mục | Mục hoặc Tiểu mục (nếu có) |
| `C16` | `P` | Article / Điều | Điều / Section / Clause |
| `C17` | `Q` | Clause / Khoản & Đoạn | Khoản hoặc đoạn văn bản thuộc Điều |
| `C18` | `R` | Point / Điểm & Tiểu khoản | Điểm hoặc tiểu khoản chi tiết |
| `C19` | `S` | Source Page / Số trang nguồn | Số trang ấn phẩm hoặc PDF chính thức khi đã kiểm chứng; nếu không có ghi `N/A` |
| `C20` | `T` | Source Line / Số dòng nguồn | Số dòng khi văn bản có đánh số dòng ổn định và kiểm chứng được; nếu không có ghi `N/A` (không tự tạo số dòng) |
| `C21` | `U` | Legal Subject / Chủ thể & Đối tượng pháp lý | Chủ thể, cá nhân, tổ chức hoặc đối tượng được bảo hộ/điều chỉnh |
| `C22` | `V` | Regulated Conduct / Hành vi bị điều chỉnh | Hành vi, hoạt động, giao dịch hoặc quyết định chịu sự điều chỉnh |
| `C23` | `W` | Compliance Obligation / Tóm tắt nghĩa vụ tuân thủ | Tóm tắt ngắn gọn, vận hành được về nghĩa vụ tuân thủ chính |
| `C24` | `X` | Official Source / Nguồn chính thức | Liên kết URL nguồn sơ cấp chính thức của cơ quan ban hành/lưu chiểu |
| `C25` | `Y` | Legislative Purpose / Mục đích lập pháp & Điều ước | Mục tiêu ban hành hoặc mục tiêu điều ước; phân biệt lời mở đầu/mục tiêu với quy phạm thi hành |
| `C26` | `Z` | Legal Principle / Nguyên tắc pháp lý | Các nguyên tắc pháp lý chi phối việc diễn giải và áp dụng quy định |
| `C27` | `AA` | Applicability / Điều kiện & Phạm vi áp dụng | Điều kiện áp dụng, ngưỡng phạm vi, yếu tố kích hoạt tài phán và trường hợp loại trừ |
| `C28` | `AB` | *(Mở rộng chuẩn hóa)* Rights & Permissions / Quyền & Quyền hạn | Quyền được trao, quyền được bảo hộ hoặc thẩm quyền cho phép thực hiện hành vi |
| `C29` | `AC` | *(Mở rộng chuẩn hóa)* Prohibitions & Restrictions / Cấm đoán & Hạn chế | Hành vi bị cấm, điều kiện hạn chế hoặc nghĩa vụ không thực hiện |
| `C30` | `AD` | *(Mở rộng chuẩn hóa)* Exceptions & Exemptions / Ngoại lệ & Miễn trừ | Các trường hợp ngoại lệ, miễn trừ hoặc áp dụng đặc thù |
| `C31` | `AE` | *(Mở rộng chuẩn hóa)* Sanctions & Remedies / Chế tài & Biện pháp khắc phục | Hình thức xử phạt, chế tài hành chính/dân sự/hình sự và biện pháp khắc phục hậu quả |
| `C32` | `AF` | *(Mở rộng chuẩn hóa)* Enforcement Authority / Cơ quan thực thi & Giám sát | Cơ quan nhà nước hoặc thiết chế có thẩm quyền kiểm tra, thực thi, xử lý |
| `C33` | `AG` | *(Mở rộng chuẩn hóa)* Procedure & Filing / Thủ tục & Hồ sơ tuân thủ | Trình tự, thủ tục, hồ sơ, thời hạn hoặc yêu cầu báo cáo/đăng ký |
| `C34` | `AH` | *(Mở rộng chuẩn hóa)* Dispute Resolution / Cơ chế giải quyết tranh chấp | Khiếu nại, khởi kiện hành chính, Tòa án dân sự/kinh tế, trọng tài, hòa giải |
| `C35` | `AI` | *(Mở rộng chuẩn hóa)* Related Instruments / Văn bản liên quan & Dẫn chiếu | Văn bản hướng dẫn thi hành, văn bản liên quan, điều khoản chuyển tiếp |
| `C36` | `AJ` | *(Mở rộng chuẩn hóa)* Precedents & Case Notes / Án lệ & Thực tiễn áp dụng | Án lệ liên quan, hướng dẫn xét xử hoặc ghi chú thực tiễn áp dụng |
| `C37` | `AK` | *(Mở rộng chuẩn hóa)* Risk Level / Mức độ rủi ro tuân thủ | Phân mức rủi ro (`LOW`, `MEDIUM`, `HIGH`, `CRITICAL`) theo mức độ chế tài và tác động |
| `C38` | `AL` | *(Mở rộng chuẩn hóa)* Verification Status / Trạng thái kiểm chứng | Trạng thái đối chiếu nguồn (`VERIFIED`, `PARTIAL`, `PENDING`, `DISPUTED`) |
| `C39` | `AM` | *(Mở rộng chuẩn hóa)* Verified At / Ngày kiểm chứng | Ngày thực hiện kiểm chứng dữ liệu (`YYYY-MM-DD`) |
| `C40` | `AN` | *(Mở rộng chuẩn hóa)* Notes & Audit Trail / Ghi chú & Nhật ký kiểm tra | Ghi chú phân tích, nguồn đối chiếu bổ sung và lịch sử cập nhật |

### 2. Các bảng dữ liệu quan hệ cốt lõi (`VLK Data Tables`)

- `legal_documents`: Danh mục văn bản và siêu dữ liệu hiệu lực.
- `legal_articles`: Chi tiết điều, khoản, điểm và nội dung quy phạm.
- `legal_domains`: Danh mục cụm ngành, lĩnh vực và phân hệ.
- `legal_subjects`: Danh mục chủ thể và đối tượng pháp lý.
- `legal_rights`: Quyền và quyền hạn pháp lý.
- `legal_obligations`: Nghĩa vụ và yêu cầu tuân thủ.
- `legal_sanctions`: Chế tài và biện pháp khắc phục hậu quả.
- `legal_relations`: Quan hệ sửa đổi, bổ sung, thay thế, dẫn chiếu, hướng dẫn giữa các văn bản/điều khoản.
- `legal_cases`: Tình huống thực tế, vụ việc và bản án/quyết định.
- `legal_precedents`: Án lệ và lập luận áp dụng.
- `legal_sources`: Danh mục nguồn chính thức và độ tin cậy.
- `legal_versions`: Lịch sử phiên bản và thay đổi nội dung.
- `verification_logs`: Nhật ký kiểm chứng hiệu lực và nguồn.

### 3. Bản ghi mẫu chuẩn (`JSON Seed Record`)

```json
{
  "schema_version": "VLK-001 + GLICE-0.1 (LOCKED)",
  "snapshot_date": "2026-11-25",
  "record_id": "VN-LAW-64-2025-DOC",
  "jurisdiction": "VN",
  "classification": {
    "domain": "LEGAL_SYSTEM",
    "subdomain": "LAW-002_LEGAL_NORMATIVE_DOCUMENTS"
  },
  "document": {
    "instrument_type": "LAW",
    "number": "64/2025/QH15",
    "title": "Luật Ban hành văn bản quy phạm pháp luật",
    "issuing_authority": "Quốc hội",
    "promulgation_date": "2025-02-19",
    "effective_date": "2025-04-01",
    "expiry_date": null,
    "status": "PARTIALLY_VALID",
    "amended_by": [
      "87/2025/QH15"
    ],
    "consolidated_reference": "54/VBHN-VPQH",
    "official_source": "https://vbpl.vn/"
  },
  "verification": {
    "status": "VERIFIED",
    "verified_at": "2026-11-17",
    "method": "Official source cross-check",
    "notes": "Bản ghi mẫu khởi tạo; cần đối chiếu từng điều khoản cụ thể và phần sửa đổi theo Luật 87/2025/QH15 trước khi áp dụng."
  }
}
```

---

## Phần VII: Kiểm định chất lượng, Khởi động `LAW-000` & Trạng thái triển khai

### 1. Năm chỉ số kiểm soát chất lượng

| Chỉ số | Tiêu chuẩn vận hành |
| :--- | :--- |
| **Source Traceability** | Mỗi quy định truy xuất được nguồn gốc rõ ràng |
| **Validity Verification** | Có trạng thái hiệu lực, mốc thời gian áp dụng và ngày kiểm chứng |
| **Amendment Coverage** | Theo dõi đầy đủ lịch sử sửa đổi, bổ sung, thay thế, bãi bỏ |
| **Legal Classification** | Gắn đúng lĩnh vực, phân ngành và đồ thị quan hệ |
| **Application Accuracy** | Kết luận tình huống và tuân thủ có căn cứ, điều kiện và giới hạn rõ ràng |

> **Nguyên tắc kiểm định:** Không đặt mục tiêu hoàn thiện 100% dữ liệu khi chưa có nguồn xác minh đầy đủ; mọi khoảng trống dữ liệu phải được gắn cờ (`UNVERIFIED` / thiếu dữ liệu) thay vì suy đoán.

### 2. Khởi động Module nền tảng `LAW-000 · Legal Literacy`

7 khái niệm nền tảng cần nắm vững trước khi đi sâu vào các phân hệ:
1. Nhà nước
2. Pháp luật
3. Quy phạm pháp luật
4. Quan hệ pháp luật
5. Sự kiện pháp lý
6. Vi phạm pháp luật
7. Trách nhiệm pháp lý

**Ví dụ áp dụng chuỗi vận hành (Cá nhân ký hợp đồng mua bán tài sản):**
- **Sự kiện pháp lý:** Hai bên xác lập/thực hiện giao dịch mua bán tài sản.
- **Chủ thể:** Bên mua, bên bán (và các bên liên quan nếu có).
- **Quan hệ pháp luật:** Quan hệ dân sự (có thể giao thoa thương mại, đất đai, nhà ở tùy chủ thể và loại tài sản).
- **Căn cứ pháp lý:** Quy định về giao dịch dân sự, hợp đồng, quyền sở hữu và luật chuyên ngành tương ứng.
- **Điều kiện áp dụng:** Năng lực pháp luật/năng lực hành vi của chủ thể, quyền định đoạt tài sản, sự tự nguyện, mục đích/nội dung hợp pháp, hình thức giao dịch và điều kiện riêng của tài sản.
- **Quyền & Nghĩa vụ:** Quyền yêu cầu giao tài sản/thanh toán; nghĩa vụ chuyển giao quyền sở hữu/tài sản và thanh toán đúng thỏa thuận.
- **Hậu quả & Giải quyết tranh chấp:** Trách nhiệm do vi phạm nghĩa vụ, giao dịch vô hiệu hoặc bồi thường thiệt hại; giải quyết qua thương lượng, hòa giải, Tòa án hoặc Trọng tài (nếu đủ điều kiện).

### 3. Trạng thái triển khai & Thứ tự thực hiện tiếp theo

| Hạng mục | Trạng thái hiện tại |
| :--- | :--- |
| Kiến trúc tổng thể & phân loại ngành luật | Đã thống nhất cấu trúc khung |
| Nguồn pháp lý nền tảng & cơ chế kiểm chứng hiệu lực | Đã xác lập quy trình & 6 trạng thái |
| Kho dữ liệu toàn văn & phân tích từng điều khoản | Đang khởi tạo / chưa nhập đầy đủ |
| Tự động cập nhật & cảnh báo thay đổi | Chưa triển khai |

**Thứ tự triển khai ưu tiên:**
1. Hoàn thiện tài liệu và bộ khung `LAW-000` (tư duy pháp lý, chuỗi suy luận, cách đọc điều khoản).
2. Hoàn thiện `LAW-001` (Hiến pháp, cấu trúc quyền lực, quyền con người/quyền công dân).
3. Hoàn thiện `LAW-002` & quy trình nguồn/hiệu lực (hệ thống văn bản, thẩm quyền, hiệu lực, sửa đổi/hợp nhất).
4. Nạp dữ liệu hạt nhân theo schema 40 cột và quan hệ sửa đổi cho các phân hệ ưu tiên.
5. Mở rộng dần sang toàn bộ các phân hệ còn lại và kiểm chứng liên tục.

**Tiêu chí năng lực đầu ra:** Một người hoàn thành lộ trình và sử dụng hệ thống có thể tiếp cận một quy định/văn bản mới, xác định đối tượng và phạm vi điều chỉnh, kiểm tra hiệu lực, truy xuất quy định liên quan và giải thích cách áp dụng vào tình huống thực tế có căn cứ.

---

## 3. Hai cơ chế nội tại: Trích xuất từng dòng dễ hiểu & Nhảy định vị trong cụm

### Cơ chế 1: Trích xuất & Giải nghĩa từng dòng cho người thiếu hiểu biết pháp lý
Dùng khi cần bóc tách từng dòng/đoạn quy định cụ thể để người không chuyên đọc hiểu chính xác mà không làm sai lệch ý nghĩa pháp lý:
1. **Neo tọa độ chuẩn (`Locator`):** Xác định rõ `C06` (Số hiệu văn bản), `C16–C18` (Điều/Khoản/Điểm), `C19–C20` (Số trang/Số dòng nếu nguồn chính thức có đánh số ổn định; không có thì ghi `N/A`, không tự bịa số dòng).
2. **Gắn cờ hiệu lực & kiểm chứng:** Hiển thị `C12` (`VALID`, `PARTIALLY_VALID`...) và `C38` (`VERIFIED`, `UNVERIFIED`...) ngay tại dòng trích xuất.
3. **Bóc tách 4 lớp dễ hiểu (không suy diễn ngoài văn bản):**
   - **Nguyên văn dòng/đoạn:** Trích đúng câu chữ cần xem.
   - **Hiểu nôm na (Plain Language):** Diễn đạt lại bằng ngôn ngữ đời thường, giải thích thuật ngữ chuyên ngành nếu có.
   - **Bạn cần chú ý gì (`C21–C23`, `C28–C30`):** Ai là đối tượng chịu tác động, được làm gì, bị cấm gì, có ngoại lệ nào không.
   - **Nếu làm sai sẽ sao (`C31–C33`):** Chế tài, mức xử phạt hoặc hậu quả pháp lý và thủ tục/cơ quan liên quan.

### Cơ chế 2: Nhảy đến vị trí luật trong cụm phân hệ (`Intra-Cluster Jump`)
Dùng để di chuyển nhanh tới đúng điểm quy định nằm bên trong một cụm phân hệ (ví dụ cụm `A–H` ở Phần II):
1. **Khóa ngữ cảnh cụm (`Cluster Anchor`):** Chọn cụm (`C03` Legal Domain) và phân hệ đích (`C04` Legal Subdomain, ví dụ `LAW-009`, `LAW-025`, `TECH-003`...).
2. **Định vị điểm nhảy (`Jump Target`):** Nhảy trực tiếp theo đường dẫn:
   `Cụm (A–H) → Phân hệ (Mã luật/lĩnh vực) → Văn bản (C06) → Vị trí điều khoản (C16 Điều / C17 Khoản / C18 Điểm)`
3. **Chuyển nhanh trong cùng cụm (`Lateral & Relation Jump`):** Từ vị trí hiện tại, cho phép nhảy ngang sang:
   - Các điều khoản/văn bản khác **cùng phân hệ** đang bổ sung hoặc hướng dẫn thi hành (`C35` / `legal_relations`).
   - Các phân hệ khác **cùng cụm** có liên quan trực tiếp tới cùng sự kiện/hành vi.
