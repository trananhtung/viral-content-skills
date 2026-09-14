# Viral Content Skills

Hai skill AI viết và chấm nội dung, dựng trên hai cuốn sách nghiên cứu về việc tại sao một ý tưởng được nhớ và được chia sẻ:

- **[Contagious: Why Things Catch On](https://jonahberger.com/books/contagious/)** của Jonah Berger, khung **STEPPS**: Social Currency, Triggers, Emotion, Public, Practical Value, Stories.
- **[Made to Stick](https://heathbrothers.com/books/made-to-stick/)** của Chip Heath và Dan Heath, khung **SUCCESs**: Simple, Unexpected, Concrete, Credible, Emotional, Stories.

Chạy được trên **Claude** (Claude Code, Claude.ai, Claude API) và **ChatGPT** (Custom GPT, Projects, hoặc chat thường).

*[English version](README.en.md)*

## Có gì trong này

| Skill | Làm gì |
|-------|--------|
| [`viral-content-creator`](skills/viral-content-creator/SKILL.md) | Biến một ý tưởng thô thành nội dung đăng được: bài post, kịch bản video, quảng cáo, email, landing page. Nó tìm thông điệp cốt lõi trước, rồi mới chọn đòn bẩy STEPPS và SUCCESs. Trả về nội dung, phần giải thích ngắn vì sao chọn như vậy, và vài phương án mở bài khác. |
| [`viral-content-evaluator`](skills/viral-content-evaluator/SKILL.md) | Chấm nội dung 0–5 trên 12 tiêu chí, mỗi điểm phải kèm câu trích dẫn làm bằng chứng. Kiểm tra 8 lỗi chí mạng, rồi kết luận Đăng được, Sửa lại, hoặc Làm lại, kèm danh sách sửa ưu tiên. |

```
skills/
├── viral-content-creator/
│   ├── SKILL.md                          # quy trình: brief → khung → cốt lõi → dựng → tự kiểm
│   └── references/
│       ├── contagious-stepps.md          # STEPPS: tâm lý học, chiến thuật, ví dụ
│       └── made-to-stick-success.md      # SUCCESs: tâm lý học, chiến thuật, ví dụ
├── viral-content-evaluator/
│   ├── SKILL.md                          # quy trình: bối cảnh → đọc lạnh → chấm → lỗi → kết luận
│   └── references/
│       └── scoring-rubric.md             # mốc 0–5, trọng số theo mục tiêu, ngưỡng kết luận
chatgpt/
├── content-creator-prompt.md             # bản prompt độc lập cho ChatGPT
└── content-evaluator-prompt.md           # bản prompt độc lập cho ChatGPT
```

## Vì sao nó hiệu quả

### Kẻ thù là lời nguyền của tri thức

Elizabeth Newton cho một nhóm người gõ nhịp một bài hát ai cũng biết, rồi hỏi họ đoán bao nhiêu phần trăm người nghe sẽ nhận ra. Họ đoán 50%. Con số thật là 2,5%. Người gõ nghe được giai điệu trong đầu mình; người nghe chỉ nghe những tiếng gõ rời rạc.

Bạn viết về sản phẩm của mình đúng như vậy. Bạn biết quá rõ nên bạn nói bằng khái niệm trừu tượng, còn người đọc chỉ nhận được tiếng gõ. Cả hai cuốn sách đều xoay quanh việc kéo người viết ra khỏi cái bẫy đó, và hai skill này biến việc kéo ra thành một quy trình bắt buộc thay vì một lời khuyên.

### Dính và lan là hai việc khác nhau

Nội dung dính mà không ai chia sẻ thì chết lặng lẽ. Nội dung được chia sẻ mà không ai nhớ thì chỉ là tiếng ồn. Hai khung giải hai bài toán khác nhau, nên skill chạy mọi bản nháp qua cả hai.

Vài cơ chế mà quy trình dựa vào:

**Cái quyết định chia sẻ là mức kích thích.** Berger phân tích khoảng 7.000 bài trên New York Times. Bài gây kinh ngạc có khả năng lọt danh sách được gửi nhiều nhất cao hơn 30%. Tức giận và lo âu, dù là cảm xúc tiêu cực, cũng làm tăng chia sẻ. Buồn bã thì giảm 16%. Trục quyết định là mức kích thích, không phải cảm xúc dễ chịu hay khó chịu. Đó là lý do "chúng tôi vui mừng thông báo" giết chết một bài post: nó tạo ra sự hài lòng êm ả, và hài lòng êm ả không khiến ai bấm nút chia sẻ.

**Tần suất gợi nhắc đánh bại sự thú vị.** Nghiên cứu của Berger cho thấy sản phẩm "thú vị" không nhận được nhiều truyền miệng hơn sản phẩm nhàm chán tính trên tổng thể. Thú vị mua được cuộc trò chuyện đầu tiên; một tác nhân kích hoạt thường xuyên mới mua được cuộc trò chuyện thứ một trăm. Cheerios được nhắc trên Twitter nhiều hơn Disney World, vì bữa sáng diễn ra mỗi ngày còn chuyến đi Disney thì vài năm một lần.

**Một người cụ thể đánh bại một con số thống kê.** Trong nghiên cứu ở Carnegie Mellon, người đọc câu chuyện về bé gái tên Rokia quyên góp trung bình 2,38 đô. Người đọc số liệu về nạn đói quyên 1,14 đô. Nhóm đọc cả hai, tức là câu chuyện có kèm số liệu, chỉ quyên 1,43 đô. Thống kê đẩy người đọc sang chế độ phân tích và dập tắt cảm xúc. Skill xử lý mâu thuẫn này bằng một quy tắc rõ ràng thay vì để người viết tự đoán.

**Thương hiệu phải nằm trong mạch truyện.** Quảng cáo Roller Babies của Evian lập kỷ lục lượt xem, trong khi thị phần và doanh số giảm khoảng 25%. Ai cũng kể lại được đám trẻ trượt patin mà không cần nhắc tới nước khoáng. Ngược lại, bạn không kể được "Will It Blend?" mà bỏ chiếc máy xay ra khỏi câu chuyện. Evaluator kiểm tra đúng điều này bằng cách viết lại nội dung thành một câu chủ ngữ, hành động, kết quả, rồi xem thương hiệu còn sót lại trong câu đó không.

**Công khai hành vi xấu sẽ nhân rộng hành vi xấu.** Các chiến dịch chống ma túy quảng bá con số bao nhiêu thanh thiếu niên đang dùng ma túy đã làm tăng mức sử dụng. Người ta bắt chước cái họ thấy người khác làm. Với nội dung thay đổi hành vi, đây là cái bẫy dễ sập nhất, vì con số phổ biến luôn là con số gây sốc nhất trong brief.

### Vì sao tách làm hai skill

Người viết bài luôn là người kém khách quan nhất về bài đó, vì lời nguyền tri thức tác động mạnh nhất lên chính tác giả. Nên evaluator nhận brief, bản kiểm kê bằng chứng, và bản nháp, nhưng **không** nhận phần "vì sao nó hiệu quả" của creator. Phần đó chính là lời biện hộ mà evaluator có nhiệm vụ kiểm chứng độc lập.

Mỗi điểm số bắt buộc phải kèm một câu trích dẫn từ nội dung, hoặc một ghi chú rằng nội dung không hề chạm tới tiêu chí đó. Không có điểm nào được cho bằng cảm tính.

Tám lỗi chí mạng ghi đè lên phép tính điểm. Một bài có thể đạt 4,8 trên 5 mà vẫn bị chặn, nếu nó chôn thông tin quan trọng nhất xuống dưới, bịa bằng chứng, hoặc đẩy thương hiệu ra khỏi câu chuyện.

Vòng lặp có giới hạn: viết, chấm, sửa một lần, chấm lại tối đa một lần, rồi dừng. Điểm số không bao giờ là giấy phép để bịa thêm dữ kiện cho đẹp bảng.

## Cài đặt cho Claude

### Claude Code

```bash
git clone https://github.com/trananhtung/viral-content-skills.git
mkdir -p ~/.claude/skills
cp -r viral-content-skills/skills/viral-content-creator ~/.claude/skills/
cp -r viral-content-skills/skills/viral-content-evaluator ~/.claude/skills/
```

Muốn giới hạn trong một dự án thì chép vào `.claude/skills/` của dự án đó. Sau đó cứ yêu cầu bình thường bằng tiếng Việt hay tiếng Anh, ví dụ "viết bài LinkedIn giới thiệu tính năng mới" hoặc "xem lại cái tweet này trước khi tôi đăng", Claude sẽ tự gọi skill. Gọi thẳng thì dùng `/viral-content-creator`.

### Claude.ai và Claude Desktop

Nén từng thư mục skill (thư mục chứa `SKILL.md`) thành file zip, rồi tải lên ở **Settings → Capabilities → Skills**.

### Claude API và Agent SDK

Truyền thư mục skill qua tính năng skills của Agent SDK, hoặc dán thẳng nội dung `SKILL.md` cùng các file reference vào system prompt.

## Cài đặt cho ChatGPT

Thư mục `chatgpt/` chứa bản độc lập, đã nhúng sẵn nội dung khung nên không cần file đính kèm:

- **Dùng nhanh:** dán cả file làm tin nhắn đầu tiên của cuộc trò chuyện, rồi đưa yêu cầu nội dung.
- **ChatGPT Projects:** dán vào phần custom instructions của project.
- **Custom GPT:** tải file lên làm Knowledge file, đặt Instructions là "Follow the workflow in content-creator-prompt.md for every content request." Làm tương tự với bản evaluator.

## Ví dụ câu lệnh

```
Viết một chuỗi tweet ra mắt app quản lý chi tiêu giá 19 đô cho freelancer. Mục tiêu: đăng ký dùng thử.
```

```
Chấm bài LinkedIn này giúp tôi, đối tượng là CTO, mục tiêu là độ nhận biết:
[dán bản nháp vào đây]
```

```
Email này chỉ đạt 2% tỷ lệ mở. Chẩn đoán giúp tôi và viết lại dòng tiêu đề.
```

## Kết quả mẫu

Nội dung thật do hai skill tạo ra cho một cửa hàng đang hoạt động ([lunavows.com](https://lunavows.com)):

- [`examples/instagram-caption-ring-dish.md`](examples/instagram-caption-ring-dish.md): caption Instagram, mục tiêu chia sẻ
- [`examples/meta-ad-embroidered-sweatshirt.md`](examples/meta-ad-embroidered-sweatshirt.md): quảng cáo Meta, mục tiêu chuyển đổi
- [`examples/email-gothic-tapestry.md`](examples/email-gothic-tapestry.md): email marketing, mục tiêu chuyển đổi
- [`examples/evaluation-report-sample.md`](examples/evaluation-report-sample.md): một bảng chấm đầy đủ từ evaluator

## Đối chứng

Ba brief được viết hai lần, một lần bởi agent dùng `viral-content-creator`, một lần bởi agent nhận đúng brief đó nhưng không có skill. Cả sáu bài được chấm mù bởi các agent đánh giá độc lập không biết bài nào là bài nào. Một bài thông báo doanh nghiệp rỗng tuếch được trộn vào cùng nhóm làm mẫu đối chứng.

| Brief | Có skill | Không skill | Chênh |
|---|---|---|---|
| Caption Instagram (chia sẻ) | 3,8 | 3,4 | +0,4 |
| Quảng cáo Meta (chuyển đổi) | 3,6 | 3,1 | +0,5 |
| Email marketing (chuyển đổi) | 3,8 | 3,0 | +0,8 |
| **Trung bình** | **3,73** | **3,17** | **+0,57** |
| Bài đối chứng rỗng | — | 0,9 | — |

Mức tăng lớn nhất nằm ở Simple, Unexpected, Emotion và Story vehicle, đều +1,0. Bài đối chứng đạt 0,9 trong khi nội dung thật đạt 3,0 đến 3,8, cho thấy thang điểm có phân biệt chứ không khen đều mọi thứ nó đọc.

### Độ ổn định

Bảy văn bản đó được chấm lại bởi một nhóm giám khảo độc lập thứ hai sau khi sửa thang điểm. Điểm gần như không đổi, dịch chuyển tuyệt đối trung bình 0,10 điểm, cao nhất 0,2, và khoảng cách giữa bài có skill và bài không skill giữ ở +0,60. Xét theo từng tiêu chí, hai nhóm giám khảo trùng khớp chính xác 79% số lần và chênh không quá một điểm ở 100% số lần. Bài đối chứng đạt 0,9, 0,9 và 0,8 qua ba lần chạy độc lập.

Một thang điểm mà kết luận thay đổi tùy người chấm thì chưa đủ tư cách làm tiêu chuẩn.

> **Lưu ý:** các con số đối chứng và độ ổn định ở trên được tạo ra dưới thang điểm v1. Thuật toán kết luận đã thay đổi trong bản sửa lỗi bám sách (bỏ ngưỡng điểm tối thiểu theo từng tiêu chí, hạ mức kích thích thấp từ lỗi chí mạng xuống thành điểm yếu tính điểm, thêm hai lỗi chí mạng), nên không so sánh trực tiếp được với điểm chấm hôm nay. Phép thử phân biệt đã chạy lại trên thang điểm hiện tại và vẫn giữ nguyên, xem bảng dưới.

### Kiểm chứng thang điểm mới

Năm brief tiếng Anh (bài LinkedIn B2B, kịch bản TikTok, email gây quỹ, mở đầu blog, chiến dịch an toàn giao thông) được creator viết rồi chấm mù bởi các agent đánh giá riêng, không nhìn thấy phần lập luận của creator. Sau đó hai bài đối kháng được dựng riêng để thử hai lỗi chí mạng mới, và hai bài hiệu chuẩn kiểm tra xem khả năng phân biệt có sống sót qua thay đổi thang điểm không.

| Phép thử | Thang v1 | Thang hiện tại |
|---|---|---|
| Bài doanh nghiệp rỗng (đối chứng) | 0,3 Làm lại | 0,24 Làm lại |
| Bài LinkedIn người viết tay, chất lượng tốt | 4,1 Đăng được | 4,1 Đăng được |
| Bài LinkedIn B2B, mục tiêu nhận biết | 3,9 Sửa lại | 3,8 Sửa lại |
| Chiến dịch an toàn giao thông, đổi hành vi | 3,93 Sửa lại | **4,3 Đăng được** |
| Quảng cáo Reels có thương hiệu tách rời được | — | 2,6 Sửa lại, **lỗi lan truyền vô giá trị nổ** |
| Chiến dịch mở đầu bằng "84% người trẻ nhắn tin khi lái" | — | 2,9 Sửa lại, **lỗi bằng chứng xã hội phản tác dụng nổ** |

Bài an toàn giao thông tăng 0,37 vì creator giờ nhận được cơ chế tác nhân kích hoạt (tần suất, độ mạnh liên kết, và kích hoạt ở nơi hành động khả thi) cùng cảnh báo bằng chứng xã hội ngay trong quy trình, thay vì chôn trong file reference. Nó tự bỏ con số 84% và nói rõ lý do. Bài LinkedIn giảm 0,1 vì phép thử N/A chặt hơn: một cơ chế khả thi mà không dùng thì bị chấm điểm thấp chứ không được miễn. Hai lỗi mới chỉ nổ đúng trên hai bài dựng ra để thử chúng, và được xem xét rồi bác bỏ chính xác trên bốn bài hợp lệ.

### Những con số này là gì và không là gì

Các mốc 0–5, trọng số theo mục tiêu, và ngưỡng 4,0 với 2,5 là **quy ước biên tập** giúp nhiều người chấm ra kết quả giống nhau. Không cuốn sách nào đưa ra chúng. Chúng không phải xác suất đo được rằng một bài sẽ lan truyền, và không kết quả nào ở đây được đối chiếu với phản ứng thật của khán giả. Mọi điểm số trong repo này là một model chấm bài viết của một model khác.

## Ghi công và giấy phép

STEPPS và SUCCESs là công trình trí tuệ của **Jonah Berger** và **Chip Heath cùng Dan Heath**. Repo này là một bản chắt lọc độc lập, mang tính giáo dục, chuyển các ý tưởng đó thành chỉ dẫn mà AI dùng được. Nó không sao chép văn bản của sách, không liên kết và không được hai tác giả bảo trợ. Nếu thấy hữu ích, hãy mua sách, hai cuốn đều xứng đáng.

Nội dung repo phát hành theo [giấy phép MIT](LICENSE).
