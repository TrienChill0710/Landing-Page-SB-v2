# 🎒 Start Here — Landing Page Kit

Kit này chạy workflow tạo landing page cho **mọi task**: làm mới hoàn toàn, làm lại trang cũ, hoặc rebrand.
Copy cả folder cho mỗi dự án mới.

## 1. Trước khi bắt đầu — bạn chuẩn bị

| Folder | Bạn thêm gì | Bắt buộc? |
|---|---|---|
| `01-strategy/` | **Strategy pack**: USP, persona mục tiêu, Business Model Canvas (hoặc tóm tắt), mục tiêu của trang. Mẫu: `01-strategy/strategy-pack-template.md` | **Có** — thiếu USP hoặc persona thì dừng ở Step 01 |
| `02-assets/logo/` | Logo (SVG/PNG), thêm bản cho nền tối nếu cần | Loại B, C: có. Loại A: nếu đã có |
| `02-assets/fonts/` | Font, hoặc `font-name.txt` ghi một font mã nguồn mở | Có (trước Step 16) |
| `02-assets/icons/` | Icon SVG, hoặc `icon-library.txt` ghi một thư viện mở | Có (trước Step 16) |
| `02-assets/moodboard/` | 2–4 ảnh UI bạn thích | Nên có |
| Brief | Brief của client, hoặc 5–10 dòng tự viết, đặt trong `01-strategy/` | Có |
| Trang cũ (loại B, C) | Link trang đang chạy, số liệu, feedback đã nhận | Có với B, C |

Chỉ dùng font và icon được phép dùng thương mại.

## 2. Các folder theo thứ tự workflow

```
00-START-HERE.md           bạn đang ở đây
00-workflow-map.md         toàn bộ playbook (đọc cái này để hiểu workflow)
CLAUDE.md                  quy tắc cho Claude — đừng sửa
_progress.md               dự án đang ở đâu — Claude tự cập nhật
_prompts/                  prompt gốc cho từng step (00–26) — đừng sửa
01-strategy/               phân loại task + strategy pack     ← bạn + Claude
02-assets/                 logo · font · icon · moodboard · ảnh ← bạn
03-research/               research, structure, palette        ← Claude
04-brand/                  messaging + identity (module Brand) ← Claude
05-content/                content brief + copy                ← Claude
06-proof-ui/               proof sections                      ← Claude
07-tokens/                 token Primitive + Semantic          ← Claude
08-claude-design-input/    master spec + prompt cho Claude Design ← Claude
09-final-ui/               bản dựng + báo cáo review           ← bạn export, Claude review
10-launch/                 pre-launch, publish, kết quả        ← bạn + Claude
```

## 3. Cách bắt đầu

1. Mở project này trong Claude Code (hoặc Cowork).
2. Gõ: **`Read Folder`**
3. Claude đọc `_progress.md`, báo dự án đang ở đâu, rồi hỏi bạn có bắt đầu **Step 00** không.
4. Step 00 hỏi 5 câu để phân loại: **A mới · B làm lại · C rebrand**. Kit tự bật hoặc tắt các step theo loại.
5. Sau mỗi step Claude dừng. Bạn nói `continue`. Cuối mỗi phase có **gate**: người có quyền duyệt nói `approved`.

## 4. Hành trình

| Phase | Steps | Gate sau phase |
|---|---|---|
| 0 · Type & strategy | 00 Project type · 01 Strategy pack | **0** |
| 1 · Intake & audit | 02 Intake · 03 Brief & frame lock · 04 Audit trang cũ (B, C) · 05 Measurement | **1** |
| 2 · Research | 06 Positioning · 07 Voice of customer · 08 Reference | **2** |
| 3 · Brand (module) | 09 Messaging · 10 Identity | **3** |
| 4 · Narrative | 11 Hai option kể chuyện → **bạn chọn** · 12 Sitemap & section list | **4** (sau step 11) |
| 5 · Content | 13 Content brief · 14 Copy · 15 Tự review content | **5** |
| 6 · Visual | 16 Palette · 17 Moodboard · 18 Proof sections | **6** |
| 7 · System & spec | 19 Tokens · 20 Master spec | **7** |
| 8 · Build & review | 21 Build · 22 Tự review UI · 23 So với spec | **8** |
| 9 · Launch | 24 Pre-launch · 25 Publish · 26 Kết quả | **9** (sau step 25) |

**Content đi trước UI.** Chưa qua Gate 5 thì chưa làm Step 16 trở đi.

## 5. Vai trò

Ghi vào `_progress.md` ở Step 00: **Strategy owner** (chốt hướng, duyệt UI), **Content reviewer** (duyệt copy), **Builder** (chạy workflow), **Publisher** (đưa trang lên).

**AI là engine. Bạn là director.** 🎬
