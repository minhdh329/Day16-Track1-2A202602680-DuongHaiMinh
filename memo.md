# Memo Teardown — ChatGPT

**Người thực hiện:** Dương Hải Minh  
**Ngày phân tích:** 02/10/2026  
**Phạm vi:** Các quyết định sản phẩm công khai từ lúc ChatGPT ra mắt đến nay.

> **Cách đọc memo:** Ngày và tính năng dưới đây được lấy từ bài công bố chính thức của OpenAI. Persona, JTBD, nguyên lý và dự đoán là phân tích của memo, không phải dữ liệu nội bộ hay roadmap OpenAI. Bài công bố cho biết công ty giới thiệu gì, nhưng tự nó không chứng minh mức độ sử dụng hoặc hiệu quả kinh doanh.

## §1. Timeline các quyết định sản phẩm lớn

| Thời điểm | Quyết định / cập nhật và nguồn gốc | Context lúc đó | Revert nguyên lý: vì sao đây là quyết định sản phẩm? |
|---|---|---|---|
| **30/11/2022** | Ra mắt ChatGPT như một bản research preview miễn phí, có giao diện hội thoại và mời người dùng phản hồi. [Nguồn](https://openai.com/index/chatgpt/) | ChatGPT được giới thiệu là mô hình hội thoại có thể trả lời câu hỏi tiếp nối, thừa nhận sai sót và từ chối một số yêu cầu. Bài ra mắt cũng nêu các hạn chế như câu trả lời sai và độ nhạy với cách đặt câu hỏi. | **P1 — Triển khai lặp để học từ sử dụng thật:** đưa trải nghiệm cốt lõi đến người dùng, công khai giới hạn và thu phản hồi trước khi hệ thống trưởng thành. Mốc này chọn “thử và học” thay vì chờ một sản phẩm hoàn hảo. |
| **14/03/2023** | GPT‑4 được đưa vào ChatGPT Plus; đồng thời OpenAI công bố API cho nhà phát triển. [Nguồn](https://openai.com/index/gpt-4/) | Mô hình mới được giới thiệu là có năng lực suy luận rộng hơn GPT‑3.5; quyền dùng trong ChatGPT gắn với gói Plus lúc ra mắt. | **P2 — Phân tầng năng lực và đường tiếp cận:** mô hình tốt hơn có thể tạo lý do trả phí, trong khi API mở một đường tích hợp khác cho nhà phát triển. Đây là lựa chọn về phân phối và mô hình kinh doanh, không chỉ là cập nhật benchmark. |
| **06/11/2023** | Ra mắt GPT tùy chỉnh: người dùng có thể kết hợp hướng dẫn, kiến thức và công cụ để tạo phiên bản ChatGPT cho một mục đích; không cần viết code. [Nguồn](https://openai.com/index/introducing-gpts/) | Người dùng đã phải lặp lại prompt và hướng dẫn để ChatGPT phù hợp với từng tác vụ. GPTs đóng gói các thiết lập đó để tái sử dụng và chia sẻ. | **P3 — Đóng gói tác vụ lặp lại, mở rộng sáng tạo cho người dùng:** chuyển từ “người dùng tự prompt lại” sang tạo cấu hình chuyên biệt; cộng đồng có thể tạo và phân phối cách dùng mới. |
| **13/05/2024** | Giới thiệu GPT‑4o: mô hình có thể xử lý văn bản, hình ảnh và âm thanh; khả năng văn bản và hình ảnh bắt đầu triển khai trên ChatGPT, gồm cả gói miễn phí. [Nguồn](https://openai.com/index/hello-gpt-4o/) | Hội thoại văn bản không đủ tự nhiên cho tác vụ cần nói, nghe, nhìn hoặc phản hồi nhanh. OpenAI nêu mục tiêu đưa năng lực GPT‑4 đến nhiều người dùng hơn và cải thiện tốc độ/chi phí. | **P4 — Giảm ma sát tương tác và mở rộng tiếp cận:** làm cho cách đưa đầu vào gần với ngữ cảnh thật hơn; đưa năng lực đa phương thức xuống trải nghiệm phổ thông thay vì chỉ dành cho nhóm trả phí. |
| **31/10/2024** | Ra mắt ChatGPT Search, trả lời bằng thông tin web cập nhật kèm liên kết nguồn. [Nguồn](https://openai.com/index/introducing-chatgpt-search/) | Mô hình kiến thức tĩnh không đủ cho tin tức, thời tiết, thể thao hay câu hỏi cần thông tin mới. Người dùng trước đó phải tự tìm qua nhiều trang rồi tổng hợp. | **P5 — Đưa truy xuất thông tin vào đúng ngữ cảnh và giữ đường kiểm chứng:** người dùng có thể hỏi tiếp trong cùng cuộc trò chuyện, đồng thời mở nguồn để tự đối chiếu. Giá trị không chỉ là câu trả lời, mà còn là giảm bước chuyển giữa chat và tìm kiếm. |
| **02/02/2025** | Ra mắt deep research: agent thực hiện nghiên cứu nhiều bước trên web rồi tạo báo cáo có nguồn. [Nguồn](https://openai.com/index/introducing-deep-research/) | Các câu hỏi phức tạp cần thu thập và tổng hợp nhiều nguồn; một câu trả lời tức thời không thay thế được quá trình nghiên cứu. OpenAI mô tả sản phẩm dành cho công việc tri thức chuyên sâu và người cần báo cáo có thể kiểm chứng. | **P6 — Bán kết quả công việc, không chỉ lượt trả lời:** cho phép giao một mục tiêu dài hơi, chờ hệ thống thực hiện và nhận một đầu ra có cấu trúc. Đổi lại, thời gian chờ và khả năng kiểm tra nguồn trở thành phần cốt lõi của trải nghiệm. |
| **17/07/2025** | Ra mắt ChatGPT agent, kết hợp trình duyệt, công cụ và khả năng thực hiện quy trình nhiều bước; người dùng có thể can thiệp và xác nhận hành động quan trọng. [Nguồn](https://openai.com/index/introducing-chatgpt-agent/) | Deep research giỏi tổng hợp nhưng không thao tác được trên website; Operator có thể thao tác nhưng không phù hợp cho phân tích sâu. Agent kết hợp hai loại năng lực vào một luồng làm việc. | **P7 — Giao việc nhưng giữ quyền kiểm soát:** mở rộng từ nghiên cứu sang hành động thực tế; yêu cầu xác nhận, khả năng tạm dừng và giám sát vì hậu quả của hành động lớn hơn hậu quả của một câu trả lời sai. |
| **03–29/09/2026** | GPT‑6 Astra được định vị cho computer use và công việc chuyên môn; ngày 29/09, GPT‑6.1 Sol được đưa vào ChatGPT Work và Codex như lựa chọn gần Astra với chi phí thấp hơn (chưa có trong ChatGPT Chat tại thời điểm công bố). [Astra](https://openai.com/index/gpt-6-astra/) · [GPT‑6.1 Sol](https://openai.com/index/introducing-gpt-6-1-sol/) | Công việc khác nhau cần mức năng lực, tốc độ và chi phí khác nhau. Astra nhắm tác vụ khó; Sol nhắm công việc lặp lại, coding và nghiệp vụ với chi phí thấp hơn. | **P8 — Ghép năng lực với workload:** không buộc mọi tác vụ dùng mô hình mạnh nhất; cấu hình sản phẩm và mức giá phản ánh giá trị/chi phí của việc cần làm. Với user, lựa chọn này chỉ tốt nếu chất lượng đủ dùng và chi phí dễ dự đoán. |

### Revert nguyên lý: đọc các mốc như một chuỗi quyết định

Đây không đơn thuần là danh sách phiên bản. Có thể đọc chuỗi quyết định như sau:

1. **P1, triển khai lặp:** ra mắt bản preview để học từ tương tác thật.
2. **P2, phân tầng:** tạo khác biệt về năng lực và kênh tiếp cận giữa miễn phí, Plus và API.
3. **P3, chuyên biệt hóa:** cho người dùng đóng gói một tác vụ lặp thành GPT có thể dùng lại.
4. **P4, giảm ma sát:** làm tương tác đa phương thức nhanh và phổ cập hơn.
5. **P5, nối với thế giới thật:** tích hợp tìm kiếm web và liên kết nguồn để trả lời câu hỏi cập nhật.
6. **P6, nâng đơn vị giá trị:** từ trả lời một câu hỏi sang giao một nhiệm vụ nghiên cứu và nhận báo cáo.
7. **P7, hành động có kiểm soát:** agent thao tác được, nhưng cần quyền dừng và xác nhận của người dùng.
8. **P8, hướng tới hoàn thành workflow:** tập trung vào đầu ra chuyên môn và thao tác trên công cụ, không chỉ khả năng trò chuyện.

**Luận điểm:** ChatGPT đang dịch chuyển từ giao diện hội thoại để thử AI thành một giao diện làm việc có thể tìm kiếm, tổng hợp và thực hiện một số bước trong công việc tri thức. Đây là suy luận từ các mốc công khai, không khẳng định rằng mọi người dùng đã dịch chuyển theo cách đó.

## §2. Tệp user và JTBD

Hai phân khúc dưới đây là **persona giả thuyết** được suy ra từ các loại tác vụ mà sản phẩm công bố hỗ trợ. Cần kiểm chứng bằng phỏng vấn, review hoặc dữ liệu sử dụng trước khi coi là sự thật về khách hàng.

| | Early adopter — giai đoạn đầu | Tệp hiện tại tiềm năng — theo hướng sản phẩm mới |
|---|---|---|
| **Người cụ thể** | Frontend developer ở startup nhỏ, dùng VS Code, đọc tài liệu/API và tự tìm lời giải trên web; sẵn sàng thử công cụ mới nhưng biết cần kiểm tra code đầu ra. | Chuyên viên vận hành hoặc tư vấn độc lập trong nhóm nhỏ, thường phải đọc nhiều tài liệu, tìm thông tin mới, rồi tổng hợp thành báo cáo/bảng tính cho đồng nghiệp hoặc khách hàng. |
| **JTBD chính, viết theo việc cần làm** | “Khi tôi mắc ở một lỗi code hoặc cần hiểu nhanh một API, giúp tôi tìm được hướng xử lý và kiểm tra giả thuyết để tôi tiếp tục ship tính năng trong buổi làm việc này.” | “Khi tôi phải biến nhiều tài liệu và thông tin mới thành một báo cáo có thể gửi đi, giúp tôi nghiên cứu, tổng hợp và chuẩn bị bản nháp trong một quy trình, để tôi dành thời gian kiểm chứng và quyết định thay vì ghép thông tin thủ công.” |
| **Cách cũ** | Tìm kiếm nhiều trang, đọc Stack Overflow/tài liệu, thử code, hỏi đồng nghiệp. ChatGPT bản đầu có thể giúp tạo điểm bắt đầu nhưng câu trả lời còn cần kiểm tra. | Mở trình duyệt, tài liệu và bảng tính riêng; tự thu thập nguồn, chép ý, tổng hợp, định dạng và kiểm tra lại. |
| **Mốc tạo khả năng dịch chuyển** | ChatGPT ra mắt hội thoại dễ thử; GPT‑4 nâng năng lực cho người sẵn sàng trả phí; GPTs cho phép đóng gói hướng dẫn/tác vụ. (S1: mốc 1–3) | Search đưa thông tin mới vào chat; deep research tạo báo cáo nhiều nguồn; agent và Astra chuyển dần sang thao tác nhiều bước, computer use và artifact chuyên môn. (S1: mốc 5–8) |
| **Vì sao phân khúc có thể dịch chuyển** | Điểm hấp dẫn ban đầu là nhận câu trả lời nhanh cho một vấn đề hẹp. Nếu câu trả lời sai hoặc không kiểm chứng được, developer quay lại docs và công cụ quen thuộc. | Giá trị tiềm năng chuyển từ “chat hay” sang tiết kiệm thời gian hoàn thành một đầu việc có đầu ra. Đổi lại, độ tin cậy, nguồn dẫn, quyền truy cập và xác nhận thao tác quan trọng hơn. |

**Segment-shift cần thận trọng:** Mốc **Search → deep research → agent (S1, mốc 5–7)** làm cho những tác vụ nghiên cứu và quy trình nhiều bước trở nên khả thi hơn trong cùng sản phẩm. Điều đó hỗ trợ giả thuyết rằng sản phẩm muốn phục vụ thêm người làm công việc tri thức chuyên sâu; nó **không chứng minh** nhóm developer ban đầu đã bị thay thế hay nhóm chuyên viên đã trở thành tệp đông nhất.

### Switching cost — 4 forces

| Lực | Áp vào ChatGPT | Điều có thể khiến user ở lại / rời đi |
|---|---|---|
| **Push — điều đẩy khỏi cách hiện tại** | Người dùng mất thời gian tìm và ghép nhiều nguồn; với workflow công việc, việc chuyển giữa trình duyệt, tài liệu và bảng tính tạo nhiều thao tác lặp. | ChatGPT Search, deep research và agent có thể giảm các bước này (S1, mốc 5–7). Ngược lại, câu trả lời sai, trích dẫn yếu, quota/giá cao hoặc thao tác thiếu tin cậy cũng đẩy người dùng rời sản phẩm. |
| **Pull — điều hút về ChatGPT** | ChatGPT gộp hội thoại, tìm kiếm web có nguồn, nghiên cứu nhiều bước và một số thao tác agent vào cùng luồng (S1, mốc 5–8). | Với persona tư vấn/vận hành, sức hút tiềm năng là bắt đầu từ một yêu cầu rồi nhận bản nháp báo cáo thay vì tự ghép nhiều công cụ. Đây là giả thuyết cần so sánh với cách làm hiện tại; một công cụ chuyên biệt hoặc tích hợp sẵn ở nơi làm việc có thể hút mạnh hơn. |
| **Anxiety — lo ngại khi chuyển** | Lo thông tin sai, dữ liệu nhạy cảm bị dùng không đúng, agent thao tác quá phạm vi hoặc công việc tạo ra không theo mẫu. | Nguồn dẫn ở Search/deep research giúp kiểm tra; khả năng ngắt và xác nhận của agent giảm rủi ro hành động (S1, mốc 5–7). Nhưng AI log, chính sách dữ liệu và khả năng sửa kết quả vẫn cần được đánh giá trong tình huống thật. |
| **Habit — thói quen giữ user / cản chuyển đổi** | Người mới có thói quen tìm Google, dùng mẫu tài liệu và bảng tính hiện có; người đã dùng ChatGPT có thể quen bắt đầu công việc ở giao diện chat. | GPTs giúp tái sử dụng cấu hình (S1, mốc 3); Search và agent mở rộng số việc có thể bắt đầu trong cùng giao diện (S1, mốc 5–7). Thói quen cũ làm chậm chuyển đổi; thói quen mới chỉ giữ user nếu đầu ra ổn định và không tốn nhiều công sửa. |

**Lực giữ chân mạnh nhất — phán đoán:** Habit có thể trở nên mạnh hơn khi GPTs và các công cụ giữ nhiều tác vụ trong cùng giao diện; tuy nhiên, tài liệu công khai chưa đủ để chứng minh switching cost thực tế cao. Với persona hiện tại, tiêu chí quyết định có thể là **độ tin cậy của đầu ra và mức tích hợp vào workflow**, chứ không chỉ số lượng tính năng.

## §3. Ba dự đoán trong 6–12 tháng tới

**Khoảng dự đoán:** 02/10/2026–02/10/2027. Mỗi mục là giả thuyết để theo dõi, không phải roadmap của OpenAI.

### Dự đoán 1 — Agent chuyển từ chạy một lần sang workflow có thể tiếp tục

**Dự đoán:** ChatGPT sẽ làm rõ hơn cách lưu tiến độ, tiếp tục một công việc nhiều bước và bàn giao artifact/ngữ cảnh giữa các phiên hoặc công cụ; người dùng vẫn được yêu cầu xác nhận bước có hậu quả đáng kể.

**Lập luận:** Search và deep research đã mở rộng từ trả lời sang nghiên cứu; agent đưa thao tác web vào quy trình; Astra nhấn mạnh computer use và đầu ra công việc (S1, mốc 5–8). Persona chuyên viên vận hành/tư vấn có nhu cầu lặp lại cùng một loại workflow, nên việc tiếp tục tác vụ có thể có giá trị hơn thêm một chế độ chat mới.

**Dấu hiệu bác bỏ:** Các cập nhật chủ yếu vẫn là agent chạy tác vụ độc lập, không duy trì tiến độ hoặc không giúp bàn giao kết quả sang workflow đang dùng.

### Dự đoán 2 — Phân khúc nhóm làm việc được hỗ trợ bằng tích hợp và quyền kiểm soát

**Dự đoán:** Năng lực nghiên cứu và agent sẽ được đóng gói rõ hơn cho nhóm chuyên môn, với trọng tâm vào nguồn dữ liệu/kết nối công cụ, chia sẻ đầu ra và kiểm soát quyền truy cập.

**Lập luận:** GPTs đã đưa tùy biến từ cá nhân sang chia sẻ; deep research và agent nhắm tới công việc nhiều bước; Astra nhấn mạnh đầu ra chuyên môn (S1, mốc 3, 6–8). Với persona nhóm nhỏ, một báo cáo tốt chưa đủ nếu không thể dùng dữ liệu đúng quyền hoặc chuyển kết quả cho đồng nghiệp.

**Dấu hiệu bác bỏ:** Các bản cập nhật tập trung vào trải nghiệm cá nhân, không cải thiện đáng kể tích hợp, quản trị hay chia sẻ trong nhóm.

### Dự đoán 3 — Giá và hạn mức sẽ phân biệt rõ hơn theo loại workload

**Dự đoán:** Người dùng sẽ gặp nhiều lựa chọn hơn giữa mô hình nhanh/rẻ cho công việc thường xuyên và mô hình mạnh/đắt hơn cho nghiên cứu, coding hoặc agent dài hạn; hạn mức hoặc allowance sẽ gắn rõ hơn với workload.

**Lập luận:** GPT‑4 được định vị trong ChatGPT Plus; GPT‑6 Astra hướng đến công việc khó; GPT‑6.1 Sol được công bố như lựa chọn gần Astra với chi phí thấp hơn cho một số công việc trong ChatGPT Work và Codex. Các mốc này cho thấy năng lực và chi phí được phân tầng (S1, mốc 2, 8; [GPT‑6.1 Sol](https://openai.com/index/introducing-gpt-6-1-sol/)). Với persona chuyên viên, chi phí dự đoán được sẽ ảnh hưởng việc dùng agent thường xuyên.

**Dấu hiệu bác bỏ:** Mô hình và hạn mức được gộp thành trải nghiệm đơn giản, không cần người dùng chọn hoặc trả phí khác nhau theo độ khó/tần suất công việc.

## §4. AI Log

| Việc | AI làm hay người làm? | Kiểm chứng / phán đoán lại |
|---|---|---|
| Dựng timeline 8 mốc | **AI hỗ trợ:** tìm và tổng hợp các bài công bố chính thức về ChatGPT, GPT‑4, GPTs, GPT‑4o, Search, deep research, agent và Astra; rút ra thời điểm, thay đổi được công bố và nguyên lý có thể suy luận. | Đối chiếu ngày và mô tả với link nguồn ngay trong bảng. Nguồn chính thức xác nhận việc OpenAI công bố tính năng, không xác nhận mức adoption hay tác động kinh doanh. |
| Viết nguyên lý, persona và JTBD | **AI đề xuất bản nháp:** suy luận từ loại tác vụ và hướng sản phẩm được công bố; chọn persona cụ thể là developer giai đoạn đầu và chuyên viên vận hành/tư vấn ở hướng workflow hiện tại. | Đây chưa phải nghiên cứu người dùng. Người nộp cần thay persona/JTBD nếu trải nghiệm hoặc quan sát thực tế khác; không trình bày segment-shift như dữ liệu đã đo. |
| Phân tích 4 forces | **AI lập khung ban đầu:** map push, pull, anxiety và habit vào ChatGPT, đồng thời liên kết các lực với mốc GPTs, Search, deep research và agent. | Các lực cạnh tranh được nêu là giả thuyết. Cần hỏi user thật họ đang dùng cách nào, điều gì khiến họ ở lại và điều gì khiến họ chuyển sang công cụ khác. |
| Viết ba dự đoán | **AI đề xuất:** đưa ra giả thuyết về workflow agent, nhóm làm việc và phân tầng chi phí từ timeline. | Đây là phán đoán tương lai, không phải thông tin nội bộ. Tôi cần tự bảo vệ hoặc sửa từng dự đoán và theo dõi các dấu hiệu bác bỏ đã ghi. |

**Giới hạn của phần AI hỗ trợ:** Memo này chưa dùng phỏng vấn người dùng, review cửa hàng, dữ liệu retention, changelog của đối thủ hoặc số liệu nội bộ. Các nguyên lý, persona, 4 forces và dự đoán vì vậy cần được xem là lập luận có nguồn gợi ý, không phải kết luận đã kiểm nghiệm.

## Checklist trước khi nộp

- [x] Điền tên người thực hiện.
- [x] Mở từng link và kiểm tra ngày, claim, khả năng triển khai; giữ lại hoặc bỏ mốc nếu nguồn không xác nhận.
- [x] Chỉnh persona/JTBD theo trải nghiệm hoặc quan sát của mình; JTBD phải nói về việc cần hoàn thành, không phải “cần AI chatbot”.
- [x] Giữ rõ ranh giới giữa nội dung AI tổng hợp và phán đoán của người nộp; xác nhận rằng ba dự đoán là lập luận mình đồng ý chịu trách nhiệm.