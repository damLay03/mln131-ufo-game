# UFO xâm lăng: game ôn tập MLN131, Nhóm 6

Game kết bài cho phần thuyết trình *Xây dựng gia đình Việt Nam trong thời kỳ quá độ lên chủ nghĩa xã hội*. Toàn bộ game nằm trong một file `index.html`, chạy offline, không cần cài đặt hay mạng.

**Chơi online:** https://mln131-ufo-game.vercel.app

## Cách chạy

- **Online:** mở https://mln131-ufo-game.vercel.app
- **Offline:** tải repo về, mở `index.html` bằng Chrome hoặc Edge.

Lần đầu bấm vào trang để trình duyệt cho phát âm thanh. Nên bấm **Toàn màn hình** khi chiếu.

## Luật chơi

1. Dán danh sách lớp vào màn hình đầu, mỗi dòng một tên, rồi chọn số giây cho mỗi câu (mặc định 20).
2. UFO bay ngẫu nhiên và chiếu tia vào một người. Người đó chọn đáp án cho câu hỏi trắc nghiệm của người ngoài hành tinh. Người điều khiển bấm vào phương án người đó chọn.
3. Chọn **đúng** thì được an toàn và nhận kẹo. Chọn **sai hoặc hết giờ** thì bị hút lên UFO.
4. Sau mỗi câu, game hiện đáp án đúng, phần giải thích và mời thành viên phụ trách nói thêm.
5. Hết câu hỏi: **hơn 50% đúng** thì UFO chán nản bỏ đi và thả mọi người về. Ngược lại, UFO thống trị Trái Đất.

## Phím tắt cho người điều khiển

| Phím | Tác dụng |
|---|---|
| `Space` | UFO đi săn / sang câu tiếp |
| `A` `B` `C` `D` hoặc `1` `2` `3` `4` | Chọn phương án |
| `G` | Hiện gợi ý |
| `P` | Tạm dừng đồng hồ |
| `R` | Người này vắng, chọn người khác |

## Sửa câu hỏi ngay trong game

Ở màn hình đầu, bấm **Sửa câu hỏi**. Bạn có thể:

- sửa nội dung câu hỏi, các phương án (2 đến 6 phương án), gợi ý, giải thích và người nói thêm;
- bấm ô tròn cạnh phương án để đánh dấu đáp án đúng;
- thêm, xóa, đổi thứ tự câu hỏi;
- **Xuất file** để tải bộ câu hỏi về dạng `.json`, **Nhập file** để nạp lại;
- **Khôi phục mặc định** để quay về bộ câu hỏi gốc.

Bấm **Lưu và quay lại** để áp dụng. Câu hỏi đã sửa chỉ lưu trong trình duyệt của máy đang dùng. Muốn chiếu trên máy khác thì xuất file trên máy này, rồi nhập file trên máy kia.

Bộ câu hỏi mặc định nằm trong `index.html`, ở `const DEFAULT_QUESTIONS`. Mỗi câu có `q` (câu hỏi), `options` (các phương án), `correct` (số thứ tự phương án đúng, đếm từ 0: 0 là A, 1 là B…), `hint`, `explain`, `by`.

Câu chọc khi bị bắt nằm ở `ABDUCT_LINES`, câu khen khi trả lời đúng nằm ở `SAFE_LINES`.

Nên giữ số câu là số lẻ để không thể hòa đúng 50%. Nếu hòa đúng 50% thì game tính UFO thắng.

Danh sách tên chỉ lưu trong trình duyệt của máy đang chơi, không đưa lên repo.
