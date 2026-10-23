# Landing Page Workflow v2 — Phân loại → Strategy → Research → Content → Style → UI → Launch

> Đây là **bản đồ** của workflow. Kit chạy được nằm cùng folder: `CLAUDE.md` (quy tắc cho Claude), `_progress.md` (trạng thái), `_prompts/` (prompt từng step 00–26) và các folder đầu ra. Bắt đầu từ `00-START-HERE.md`.

Workflow dùng chung cho mọi task landing page: tạo mới, làm lại trang cũ, hoặc rebrand.
Gộp ba nguồn:
- **Kit cũ** (repo Landing-page-CC-v2): step và gate, `_progress.md`, đo bằng code, token, master spec, review bản dựng với spec.
- **Cách làm Quân hướng dẫn** trong thread Slack ConvertCore: USP và persona làm input, research insight thật, content trước UI, chốt hướng bằng option, tự review vài vòng trước khi submit.
- **Đề xuất bổ sung** (không có trong thread hay kit): phân loại task A/B/C, audit trang cũ, baseline đo lường, module brand, publish và đo sau launch.

Mỗi nguyên tắc dưới đây đều ghi nguồn để người đọc biết đâu là hướng dẫn đã có, đâu là đề xuất.

---

## 1. Phân loại task — hỏi đầu tiên (Step 00)

AI hỏi trước khi làm bất cứ việc gì. Câu trả lời quyết định step nào chạy, step nào bỏ (bảng ở mục 5).

| Loại | Mô tả | Ví dụ |
|---|---|---|
| **A · Mới hoàn toàn** | Chưa có landing page nào trước đó | Sản phẩm mới ra mắt |
| **B · Làm lại (redesign)** | Đã có trang, giữ nguyên brand | Cải thiện CR của trang đang chạy |
| **C · Rebrand** | Đã có trang hoặc sản phẩm cũ, đổi tên, đổi định vị hoặc đổi nhận diện | PlusBase/PrintBase → ConvertCore · ShopBase → ShopBase v2 tích hợp AI |

**Câu hỏi bắt buộc:**
1. Đã có landing page chưa? Nếu có, gửi link.
2. Brand đã có chưa (logo, palette, guideline)? Giữ nguyên hay làm mới?
3. Nếu có trang cũ: số liệu hiện tại (traffic, CR, scroll depth), feedback đã nhận, những gì bắt buộc giữ (URL, từ khoá SEO, section đang hiệu quả).
4. Phạm vi: một trang hay nhiều trang (Home, trang con, Policy, DMCA…)?
5. Khách hiện tại có đọc trang này không? Nếu có, họ cần nghe điều gì khác với khách mới?

Không trả lời được câu 1 và 2 thì **dừng**. Các câu còn lại dùng default và ghi `ASSUMPTION`.

## 2. Nguyên tắc vận hành (giữ từ kit cũ)

1. **Một step mỗi lượt.** Dừng sau mỗi step, người dùng nói `continue`.
2. **Gate cuối mỗi phase.** Chỉ tính là duyệt khi người có quyền nói bằng lời và `_progress.md` ghi `APPROVED`.
3. **`_progress.md` là nguồn sự thật duy nhất.** Ghi loại task (A/B/C), step, gate, quyết định đã chốt.
4. **Stop-if trước.** Mỗi step có điều kiện dừng. Điều kiện đúng thì báo và dừng, không làm vòng.
5. **Không ngoại suy.** Mọi claim không có trong input hoặc nguồn research ghi `ASSUMPTION`. Câu hỏi chặn việc gắn `[BLOCKER]`.
6. **Đo, không đoán.** Contrast, alias token, số section, độ dài trang, số lần tên cũ còn sót đều tính bằng code. Check chưa chạy ghi `NOT RUN — lý do`.
7. **Mã vĩnh viễn.** `S##` (section), `P##` (trang), `FL##` (flow) không đổi số. Phần bị bỏ giữ mã, ghi `removed`.
8. **Đổi step trước thì step sau `stale`** (mục 6).
9. **Asset dùng đúng như được cung cấp.** Không vẽ lại logo, không trộn bộ icon. Chỉ dùng font và icon có license thương mại.
10. **Lưu đúng tên file đã định.** Chạy lại step thì ghi đè. Không tạo bản `-v2`, `-final`. Không tạo folder ngoài cấu trúc.
11. **Chat summary mỗi step.** File viết chi tiết. Chat tóm tắt bằng heading và bảng, kết bằng "điều này nghĩa là gì cho thiết kế". Câu hỏi chia 🔴 phải trả lời / 🟡 nên trả lời / ⚪ có thì tốt, mỗi câu có default. Chat bằng ngôn ngữ của người dùng, file theo ngôn ngữ của dự án.
12. **End-of-turn block** sau mỗi step: Files · Key result · ASSUMPTIONS · Measured · `_progress.md` · Next.

## 3. Nguyên tắc nội dung và thiết kế

| # | Nguyên tắc | Khi làm | Nguồn |
|---|---|---|---|
| N1 | **USP và persona là input, không phải output** | Con người chuẩn bị trước. AI không tự bịa USP | Quân, reply 10; Hải Hà, reply 8 |
| N2 | **Research để tìm insight thật cho đúng persona** | Reddit, review app store, comment YouTube, forum ngành. Pain point phải có nguồn | Quân, reply 10; Hải Hà, reply 12 |
| N3 | **Content trước, UI sau** | UI chỉ bắt đầu khi content đã qua review | Quân, reply 10 |
| N4 | **USP là trục, pain point là chất liệu** | Không biến trang thành danh sách vấn đề của user | Alice và Hải Hà, reply 19, 22 |
| N5 | **Mỗi section một điểm nhấn** | Có trần số section và ít box | Quân, reply 1, 18; reply 22 |
| N6 | **Chốt hướng bằng option** | 2 option, có pros, cons và flow cho từng persona. Người quyết định chọn | Hải Hà, reply 23; Quân, reply 26 |
| N7 | **Câu chuyện phụ thuộc người đọc đã biết gì** | Khách hiện tại khác khách mới. Chọn option theo người đọc chính | Alice, reply 25 |
| N8 | **Reference phục vụ USP, tránh "me too"** | AI phân tích reference dựa trên USP rồi đề xuất cải tiến | Quân, reply 5, 9 |
| N9 | **Tự review vài vòng trước khi submit** | Default 2 vòng. Con số này là đề xuất, Quân chỉ nói "vài vòng" | Quân, reply 6 |
| N10 | **Reference không phải bằng chứng CR** | Không lấy "trang X chuyển đổi cao" làm lý do nếu không có dữ liệu | Đoạn AI phân tích Quân dán ở reply 11 |
| N11 | **Bắt đầu bằng phương án dễ làm rõ thông điệp** | Ví dụ: nền sáng trước, tối ưu nền tối sau | Quân, reply 1 |

## 4. Vai trò

| Vai trò | Việc | Ví dụ trong thread |
|---|---|---|
| **Strategy owner** | Cung cấp USP và persona, chốt option, duyệt UI cuối | Quân |
| **Content reviewer** | Review content kỹ | Alice |
| **Builder** | Chạy workflow, dựng UI | Hải Hà |
| **Publisher** | Đưa trang lên môi trường thật | Xuan Bac Ho (setup publish từ Claude Design) |
| **AI** | Research, viết nháp, phân tích, dựng | Không tự quyết hướng |

Gán lại tên người cho từng dự án và ghi vào `_progress.md`.

## 5. Các phase và step

Ký hiệu: 🧑 con người làm hoặc quyết · 🤖 AI làm · 🚦 gate · **[A] [B] [C]** loại task áp dụng.

### Phase 0 · Phân loại & Strategy 🧑
| Step | Loại | Việc | Output |
|---|---|---|---|
| 00 | A B C | **Phân loại task**: 5 câu hỏi ở mục 1. Ghi loại A/B/C và phạm vi trang | `01-strategy/00-project-type.md` |
| 01 | A B C | **Strategy pack**: USP (kèm bằng chứng nếu có), persona mục tiêu (chính và phụ), Business Model Canvas hoặc tóm tắt tương đương, mục tiêu trang (North Star). **C:** thêm định vị mới và lý do đổi. **B:** kiểm tra pack cũ còn đúng không | `01-strategy/01-strategy-pack.md` |

🚦 **Gate 0:** Strategy owner xác nhận loại task và strategy pack. Thiếu USP hoặc persona thì không sang Phase 1.

### Phase 1 · Intake & Audit 🤖
| Step | Loại | Việc | Output |
|---|---|---|---|
| 02 | A B C | **Intake**: kiểm tra brief, strategy pack, logo, font, icon, moodboard. Báo thiếu gì, rủi ro license | `03-research/02-intake.md` |
| 03 | A B C | **Phân tích brief và khoá frame**: thiết bị (desktop, mobile, responsive), khổ, light hay dark, ngôn ngữ, danh sách trang `P##`. Câu hỏi cho client gắn `[BLOCKER]` | `03-research/03-brief-analysis.md` |
| 04 | B C | **Audit trang cũ**: kiểm kê section và content, cái gì hiệu quả, cái gì không (có số thì ghi số), feedback đã nhận, SEO (URL, từ khoá, meta), những gì bắt buộc giữ. **C:** thêm danh sách tài sản brand cũ và mọi chỗ xuất hiện tên cũ | `03-research/04-audit.md` |
| 05 | A B C | **Đo lường**: **A:** kế hoạch đo (sự kiện CTA, công cụ, mốc kỳ vọng). **B C:** số liệu nền của trang cũ cộng kế hoạch đo. Không có số thì ghi `NOT AVAILABLE`, không đoán | `03-research/05-measurement.md` |

🚦 **Gate 1:** frame lock và kết quả audit.

### Phase 2 · Research 🤖
| Step | Loại | Việc | Output |
|---|---|---|---|
| 06 | A B C | **Định vị và đối thủ**: 3–5 đối thủ trực tiếp, cách họ định vị, chỗ dễ bị "me too", khác biệt của mình. **C:** so định vị cũ và mới | `03-research/06-positioning.md` |
| 07 | A B C | **Voice of customer** theo từng persona: top pain point, câu chữ khách dùng, link nguồn, mức độ lặp lại. **B:** nhấn vào lý do trang cũ chưa thuyết phục. **C:** thêm khách cũ nghĩ gì về brand cũ | `03-research/07-voc.md` |
| 08 | A B C | **Reference theo khía cạnh** (mục 8). Chọn reference và nêu học cái gì | `03-research/08-reference-analysis.md` |

Quy tắc VoC: có link nguồn, không kết luận định lượng từ vài bình luận, ý không có nguồn ghi `ASSUMPTION`.

🚦 **Gate 2:** Strategy owner xác nhận pain point và định vị không lệch USP.

### Phase 3 · Brand (module) 🧑 + 🤖
Bắt buộc với **C**. Chạy với **A** khi chưa có brand. Bỏ với **B**.

| Step | Loại | Việc | Output |
|---|---|---|---|
| 09 | A C | **Định vị và thông điệp**: positioning statement, thứ bậc thông điệp (1 thông điệp chính, 3 thông điệp phụ), giọng văn. **C:** thông điệp chuyển đổi cho khách cũ (ví dụ "X giờ là Y — điều gì giữ nguyên, điều gì mới") | `04-brand/09-messaging.md` |
| 10 | A C | **Nhận diện**: logo, palette gốc, font. Logo do con người hoặc team brand cung cấp. AI không tự vẽ logo | `04-brand/10-identity.md` + `02-assets/` |

🚦 **Gate 3:** Strategy owner duyệt thông điệp và nhận diện. Bỏ gate này khi module tắt.

### Phase 4 · Narrative & Structure 🤖 + 🧑
| Step | Loại | Việc | Output |
|---|---|---|---|
| 11 | A B C | **Hai option kể chuyện**: thứ tự thông điệp, pros, cons, flow cho từng persona, option nào hợp người đọc nào (khách mới hay khách hiện tại) | `03-research/11-narrative-options.md` |

🚦 **Gate 4 (Quyết định):** Strategy owner **chọn option bằng lời**. Chưa chọn thì không chạy step 12.

| Step | Loại | Việc | Output |
|---|---|---|---|
| 12 | A B C | **Sitemap và section list** theo option đã chọn. Mỗi section: mục đích, một điểm nhấn, persona phục vụ. Đặt trần số section. **B C:** bảng **giữ / sửa / bỏ** cho từng section cũ, có lý do. **Nhiều trang:** sitemap `P##` trước | `03-research/12-sections.md` |

### Phase 5 · Content 🤖 + 🧑
| Step | Loại | Việc | Output |
|---|---|---|---|
| 13 | A B C | **Content brief từng section**: thông điệp chính, pain point dùng (có nguồn), bằng chứng, CTA, độ dài tối đa | `05-content/13-content-brief.md` |
| 14 | A B C | **Copy toàn trang** cộng SEO cơ bản cho từng trang (title, meta description, H1). **B C:** giữ từ khoá và URL đã liệt kê trong audit | `05-content/14-copy.md` |
| 15 | A B C | **Tự review content** theo checklist mục 9 (default 2 vòng) | ghi trong `14-copy.md` |

🚦 **Gate 5:** Content reviewer duyệt section list và copy. **Không bắt đầu UI khi chưa qua gate này.**

### Phase 6 · Visual Direction 🤖
| Step | Loại | Việc | Output |
|---|---|---|---|
| 16 | A C | **Palette** từ logo và nhận diện, kiểm tra contrast bằng code. **B:** dùng palette hiện có, chỉ bổ sung màu thiếu | `03-research/16-palette.md` |
| 17 | A B C | **Moodboard theo section**, dựa trên reference ở step 08. Người dùng lưu ảnh tham chiếu, AI đọc lại | `03-research/17-moodboard.md` |
| 18 | A B C | **Proof sections**: khoảng 5 section chủ chốt, dùng đúng copy đã duyệt, đúng các thiết bị trong frame lock | `06-proof-ui/proof.html` |

🚦 **Gate 6:** duyệt hướng visual.

### Phase 7 · Design System & Spec 🤖
| Step | Loại | Việc | Output |
|---|---|---|---|
| 19 | A B C | **Token** Primitive và Semantic từ proof. **B:** ánh xạ vào token hiện có nếu đã có | `07-tokens/*.json` |
| 20 | A B C | **Master spec** cộng image prompts: dùng copy đã duyệt, không viết lại. Thêm hành vi responsive và sự kiện đo lường cho CTA | `08-claude-design-input/` |

🚦 **Gate 7:** duyệt token và spec. Người dùng tạo ảnh hoặc nói `skip images`.

### Phase 8 · Build & Review 🤖 + 🧑
| Step | Loại | Việc | Output |
|---|---|---|---|
| 21 | A B C | **Build** trong Claude Design hoặc công cụ dự án dùng | `09-final-ui/final-ui.html` |
| 22 | A B C | **Tự review UI** theo checklist mục 9 (default 2 vòng), sửa trước khi submit | `09-final-ui/22-self-review.md` |
| 23 | A B C | **So bản dựng với spec**: số section, token, điểm nhấn, đo bằng code | `09-final-ui/23-spec-check.md` |

🚦 **Gate 8:** Strategy owner review. Feedback quay về đúng chỗ theo loại:

| Feedback về… | Quay về |
|---|---|
| Lỗi hiển thị, khoảng cách, box, header | Step 22 |
| Câu chữ, độ dài, thứ tự trong section | Phase 5 |
| Thứ tự section, trang quá dài, quá nhiều điểm nhấn | Step 12 |
| Chưa rõ USP, giống đối thủ ("me too"), sai hướng kể chuyện | Phase 2 hoặc Gate 4 |

Quay về phase nào thì các step sau phase đó thành `stale`.

### Phase 9 · Launch 🧑 + 🤖
| Step | Loại | Việc | Output |
|---|---|---|---|
| 24 | A B C | **Pre-launch checklist**. **A:** trang legal cơ bản, email support, nơi lưu dữ liệu form. **B:** thêm redirect URL, giữ SEO. **C:** thêm quét tên cũ (kết quả phải bằng 0, đo bằng lệnh), cập nhật pháp nhân và form legal | `10-launch/24-prelaunch.md` |
| 25 | A B C | **Publish hoặc bàn giao** cho publisher (Claude Design publish, hoặc module handoff cho dev) | `10-launch/25-publish.md` |
| 26 | A B C | **Đo sau launch** (tuỳ chọn): so với kế hoạch đo hoặc baseline ở step 05 sau số ngày đã định | `10-launch/26-results.md` |

🚦 **Gate 9** (sau step 25): Strategy owner duyệt launch. Step 26 chạy sau, khi hết khoảng thời gian đọc kết quả đã đặt ở step 05.

### Module tuỳ chọn (từ kit cũ, mặc định tắt)
Figma import, component, prototype, handoff cho dev. Bật khi dự án yêu cầu.

## 6. Bảng bật/tắt theo loại task

| Step | A · Mới | B · Làm lại | C · Rebrand |
|---|---|---|---|
| 04 Audit trang cũ | — | ✅ | ✅ cộng tài sản brand cũ |
| 05 Đo lường | Kế hoạch đo | Baseline + kế hoạch | Baseline + kế hoạch |
| 09–10 Module brand | Khi chưa có brand | — | ✅ bắt buộc |
| 12 Section list | Viết mới | Giữ / sửa / bỏ | Giữ / sửa / bỏ + section chuyển đổi brand nếu cần |
| 16 Palette | ✅ | Chỉ bổ sung | ✅ từ nhận diện mới |
| 19 Token | Tạo mới | Ánh xạ vào token cũ | Tạo mới |
| 24 Pre-launch | Legal cơ bản | + redirect, SEO | + redirect, SEO, quét tên cũ, pháp nhân |

Step không có trong bảng thì chạy cho cả ba loại.

## 7. Khi đổi step trước thì step sau `stale`

| Đổi… | Stale |
|---|---|
| Loại task (step 00) | Toàn bộ |
| Strategy pack (USP, persona) | Từ Phase 1 trở đi |
| Frame lock, phạm vi trang | Từ step 12 trở đi |
| Audit, VoC, định vị | Brand, narrative, content và mọi thứ sau |
| Thông điệp hoặc nhận diện brand | Narrative, content, visual và mọi thứ sau |
| Option đã chọn | Section list, content, UI |
| Copy | Proof, spec, UI |
| Palette, moodboard | Proof, token, spec, UI |

Sửa lỗi nhỏ không đổi quyết định (chính tả, câu chữ) không làm stale gì.

## 8. Các khía cạnh khi research reference (step 08)

| Khía cạnh | Câu hỏi | Ví dụ trong thread |
|---|---|---|
| Định vị | Họ nói giá trị chính thế nào, có minh hoạ bằng giao diện thật không? | Replo, GemPages |
| Sắp xếp thông tin | Thứ tự section ra sao, bằng chứng đặt ở đâu so với CTA? | Shopify, Ridge |
| Trust | Use case, kết quả, security, privacy được trình bày thế nào? | Vanta, Anthropic, Cursor |
| Màu sắc | Màu nào tạo cảm giác tin cậy, khác đối thủ? | Vanta (Quân nêu ví dụ màu tím) |
| Khác biệt | Reference này có làm mình giống đối thủ không? | Nhận xét "me too" của Quân |

Danh sách ví dụ ở cột phải lấy từ đoạn AI phân tích mà Quân dán ở reply 11, cộng GemPages và Replo do Hải Hà chọn. Đây là ví dụ, chưa phải danh sách đã thẩm định. Thêm khía cạnh layout và motion nếu dự án cần.

## 9. Checklist tự review

**Content (step 15):**
- [ ] Mỗi section có đúng một thông điệp chính.
- [ ] Hero trả lời được: dành cho ai → giải quyết gì → thấy sản phẩm chạy → bước tiếp theo.
- [ ] USP xuất hiện xuyên suốt, không bị loãng bởi phần user problems.
- [ ] Mỗi pain point dùng có nguồn từ VoC.
- [ ] Không dùng reference làm bằng chứng CR.
- [ ] Số section không vượt trần.
- [ ] **B C:** mọi thứ "bắt buộc giữ" trong audit vẫn còn.
- [ ] **C:** khách cũ hiểu được điều gì giữ nguyên, điều gì mới.

**UI (step 22):**
- [ ] Không quá nhiều box, không quá nhiều điểm nhấn.
- [ ] Header và logo hài hoà.
- [ ] Trang không dài quá trần.
- [ ] Không giống đối thủ ("me too" test).
- [ ] Đúng các thiết bị trong frame lock.
- [ ] Contrast, token, hex ngoài `:root` đều đo bằng code.

## 10. Cấu trúc thư mục

```
00-START-HERE.md
00-workflow-map.md           file này
CLAUDE.md                    quy tắc cho AI
_progress.md                 loại task, step, gate, quyết định
_prompts/                    prompt gốc cho từng step
01-strategy/                 phân loại task, strategy pack
02-assets/                   logo, font, icon, moodboard, images
03-research/                 step 02–08, 11–12, 16–17
04-brand/                    step 09–10 (khi module bật)
05-content/                  content brief, copy
06-proof-ui/                 proof sections
07-tokens/                   token
08-claude-design-input/      master spec, image prompts, prompt cho Claude Design
09-final-ui/                 bản dựng cuối, báo cáo review
10-launch/                   pre-launch, publish, kết quả sau launch
```

## 11. Khác kit cũ ở đâu

| Mục | Kit cũ | Bản này |
|---|---|---|
| Loại task | Chỉ một luồng: tạo mới từ brief | Phân loại A mới / B làm lại / C rebrand, bật/tắt step theo loại |
| Đầu vào | Brief của client | Brief **và** strategy pack (USP, persona) do con người chuẩn bị |
| Trang cũ | Không xét | Audit, baseline, bảng giữ / sửa / bỏ |
| Research | Phân tích brief, thị trường, đối thủ | Thêm VoC từ Reddit, review, YouTube, forum, có nguồn |
| Brand | Giả định đã có logo | Module brand cho C và A chưa có brand |
| Chốt hướng | Không có | Hai option, người quyết định chọn bằng lời |
| Content | Nằm trong master spec ở cuối | Phase riêng, qua review trước UI |
| Reference | Moodboard theo section | Phân tích theo khía cạnh, kèm kiểm tra khác biệt |
| Review | Check cuối mỗi step, Step 13 so bản dựng với spec | Giữ các check đó, thêm tự review nhiều vòng trước khi gửi người duyệt, và feedback quay về đúng phase |
| Người duyệt | Một người dùng | Phân vai: strategy owner, content reviewer, builder, publisher |
| Phạm vi | Một sản phẩm, nhiều màn hình app | Một hoặc nhiều trang (`P##`) |
| Launch | Không có (dừng ở handoff dev) | Pre-launch theo loại, publish, đo sau launch |
| Figma, handoff | Bắt buộc | Module tuỳ chọn |

## 12. Chưa chốt (cần bạn quyết)

1. Trần số section và trần độ dài trang là bao nhiêu? Thread chỉ nói "trang quá dài", không có con số.
2. Gate 4 (chọn option) do một người chốt hay cả nhóm?
3. Số vòng tự review mặc định: giữ 2 hay đổi?
4. Frame mặc định: desktop only như kit cũ, hay responsive?
5. Có giữ module Figma và handoff làm mặc định không?
6. ~~Bộ prompt, `CLAUDE.md`, `_progress.md`~~ — đã viết (xem folder kit). Các mặc định đã dùng, có thể đổi: trần 10 section · 9.000 px desktop · 4 box mỗi section · 1 CTA mỗi section (Step 12), 2 vòng tự review.
