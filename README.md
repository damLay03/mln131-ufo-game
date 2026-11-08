# UFO xâm lăng: game ôn tập MLN131, Nhóm 6

Game kết bài cho phần thuyết trình *Xây dựng gia đình Việt Nam trong thời kỳ quá độ lên chủ nghĩa xã hội*. Toàn bộ game nằm trong một file `index.html`, chạy offline, không cần cài đặt hay mạng.

## Cách chạy

- **Offline:** tải repo về, mở `index.html` bằng Chrome hoặc Edge.
- **Online:** bật GitHub Pages (Settings → Pages → Branch `main`, thư mục `/root`), rồi mở link Pages.

Lần đầu bấm vào trang để trình duyệt cho phát âm thanh. Nên bấm **Toàn màn hình** khi chiếu.

## Luật chơi

1. Dán danh sách lớp vào màn hình đầu, mỗi dòng một tên, rồi chọn số giây cho mỗi câu (mặc định 20).
2. UFO bay ngẫu nhiên và chiếu tia vào một người. Người đó trả lời câu hỏi của người ngoài hành tinh.
3. Trả lời **đúng** thì được an toàn và nhận kẹo. **Sai hoặc hết giờ** thì bị hút lên UFO.
4. Sau mỗi câu, game hiện đáp án và mời thành viên phụ trách phần đó nói thêm.
5. Hết 7 câu: **hơn 50% đúng** thì UFO chán nản bỏ đi và thả mọi người về. Ngược lại, UFO thống trị Trái Đất.

## Phím tắt cho người điều khiển

| Phím | Tác dụng |
|---|---|
| `Space` | UFO đi săn / sang câu tiếp |
| `D` | Đúng |
| `S` | Sai |
| `G` | Hiện gợi ý |
| `P` | Tạm dừng đồng hồ |
| `R` | Người này vắng, chọn người khác |

## Sửa câu hỏi

Mở `index.html`, tìm `const QUESTIONS`. Mỗi câu có:

- `q`: câu hỏi
- `hint`: gợi ý
- `a`: đáp án
- `by`: thành viên giải thích

Câu chọc khi bị bắt nằm ở `ABDUCT_LINES`, câu khen khi trả lời đúng nằm ở `SAFE_LINES`.

Nên giữ số câu là số lẻ để không thể hòa đúng 50%. Nếu hòa đúng 50% thì game tính UFO thắng.

Danh sách tên chỉ lưu trong trình duyệt của máy đang chơi, không đưa lên repo.
