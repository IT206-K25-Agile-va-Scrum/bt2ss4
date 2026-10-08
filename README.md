# BÀI TẬP B2 - SESSION 4: VIẾT USER STORY, ACCEPTANCE CRITERIA VÀ THEO DÕI TRÊN TRELLO (RIKKEICARE)

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## Bước 1. Viết User Story cho R5

Yêu cầu ban đầu R5: 'Phòng khám muốn tự cập nhật giá các gói khám.' Hiện admin RikkeiCare đang cập nhật hộ qua email.

User Story được viết lại hoàn chỉnh theo chuẩn:

'Là một quản lý phòng khám, tôi muốn tự động cập nhật giá các gói khám của mình trên hệ thống, để bệnh nhân luôn thấy mức giá chính xác nhất mà không cần qua bên trung gian RikkeiCare.'

Giải thích lý do chọn vai trò 'Quản lý phòng khám' thay vì 'Admin RikkeiCare':

Thứ nhất, xét về nghiệp vụ cốt lõi, quản lý phòng khám là người nắm quyền quyết định trực tiếp về chiến lược giá dịch vụ y tế của cơ sở mình. Việc để admin RikkeiCare cập nhật hộ vừa chậm trễ, vừa dễ xảy ra sai sót khi truyền tải thông tin qua email.

Thứ hai, dưới góc độ tự động hóa và phân quyền (Role-Based Access Control), hệ thống RikkeiCare cần trao quyền chủ động cho đối tác để tối ưu hiệu suất vận hành, giảm tải công việc cho bộ phận quản trị hệ thống trung tâm.

- Đảm bảo đủ 3 vế chuẩn Scrum: Vai trò (Ai), Mong muốn (Làm gì), Mục đích (Để làm gì).
- Phù hợp với mô hình phân quyền đối tác của ứng dụng đặt lịch khám.

## Bước 2. Viết phần Then cho 2 AC của R5

Hoàn thiện các tiêu chí nghiệm thu theo mẫu Given - When - Then đối với yêu cầu R5:

| Mã AC | Trạng thái | Mô tả tiêu chí (Given - When - Then) |
| --- | --- | --- |
| AC 1 | Thành công (Happy Path) | Given quản lý phòng khám đã đăng nhập hệ thống, When nhập giá mới hợp lệ cho một gói khám rồi nhấn 'Lưu', Then hệ thống cập nhật thành công, hiển thị thông báo 'Đã lưu thay đổi' và giá mới được hiển thị ngay trên ứng dụng cho bệnh nhân. |
| AC 2 | Thất bại (Edge Case) | Given quản lý phòng khám để trống ô giá hoặc nhập giá trị âm, When nhấn 'Lưu', Then hệ thống báo lỗi 'Giá gói khám không được để trống hoặc nhỏ hơn 0' và giữ nguyên giá cũ, không cho phép lưu vào cơ sở dữ liệu. |

## Bước 3. Thẻ R5 đã sẵn sàng chưa?

Xét theo Definition of Ready (DoR) của nhóm gồm 4 điều kiện:

1. Có User Story đủ 3 vế: Đã có (Đạt).

2. Có tiêu chí nghiệm thu (AC): Đã có 2 AC rõ ràng cho trường hợp thành công và thất bại (Đạt).

3. Đã được ước lượng (Estimated): Chưa rõ trong đề bài liệu thẻ này đã được team gán story point chưa (Giả sử Product Owner chưa cho team ước lượng).

4. Đủ nhỏ để làm xong trong 1 Sprint: Có thể đánh giá là vừa vặn cho 1 Sprint (3 point), nhưng vì chưa qua buổi lập kế hoạch ước lượng cùng development team, thẻ R5 CHƯA THỂ kéo sang cột 'Ready for Sprint'.

Kết luận: Thẻ R5 CHƯA ĐỦ ĐIỀU KIỆN để kéo sang cột 'Ready for Sprint' do thiếu bước ước lượng thống nhất từ team kỹ thuật, tránh tình trạng đẩy thẻ mù mờ vào Sprint gây tắc nghẽn tiến độ.

- Definition of Ready là lá chắn bảo vệ Sprint Backlog khỏi các yêu cầu chưa chín muồi.
- Cần buổi Refinement nhỏ để team chốt số Story Point trước khi đưa vào cột Ready.

## Bước 4. Hoàn thiện thẻ R5 trên Trello

Giả sử thẻ R5 đã đạt đủ DoR và được chọn vào Sprint Backlog. Dưới đây là cách thiết lập chi tiết thẻ trên Trello:

- Nhãn (Labels): Màu Xanh dương (Feature - Tính năng mới dành cho đối tác phòng khám).

- Người phụ trách (Assignee): Developer phụ trách module Quản lý phòng khám (Ví dụ: Nam Backend).

- Hạn hoàn thành (Due Date): Ngày thứ 5 của Sprint.

- Vị trí trong cột: Do R5 là tính năng được ưu tiên cao nhất, thẻ được đặt ở VỊ TRÍ CAO NHẤT (trên cùng) của cột Sprint Backlog.

- Checklist hoàn thành:

- [x] Thiết kế API cập nhật giá gói khám cho Quản lý phòng khám.
- [x] Viết Unit Test kiểm tra các trường hợp nhập giá hợp lệ và không hợp lệ (AC1, AC2).
- [ ] Kiểm thử giao diện trên ứng dụng và nghiệm thu với Product Owner.

## Bước 5. Đọc Burndown Chart

Thông số dữ liệu đầu vào:

- Tổng số ngày Sprint: 10 ngày.

- Tổng cam kết: 30 point (thẻ R5 chiếm 3 point).

- Đường lý tưởng giảm đều 3 point/ngày (Ví dụ Ngày 2 còn 24 point, Ngày 4 còn 18 point theo đường lý thuyết chuẩn).

- Thực tế theo bảng dữ liệu: Ngày 0 = 30 point, Ngày 2 = 26 point, Ngày 4 = 23 point, Ngày 6 = 20 point.

a) Ngày 6 nhóm nhanh hay chậm so với đường lý tưởng, lệch bao nhiêu point?

- Theo đường lý tưởng (Ideal Line): Đến ngày 6, số point còn lại đáng lẽ phải là: 30 - (6 * 3) = 12 point.

- Thực tế trên biểu đồ ngày 6: Nhóm còn lại 20 point.

- Kết luận: Nhóm đang CHẬM HƠN so với đường lý tưởng.

- Mức độ lệch: 20 - 12 = 8 point (tương đương chậm hơn khoảng gần 3 ngày làm việc so với kế hoạch ban đầu).

b) Một bạn báo thẻ R5 'xong 80%' và muốn trừ luôn 3 point khỏi biểu đồ. Có nên không, vì sao?

- TẢI TUYỆT ĐỐI KHÔNG NÊN.

- Giải thích kỹ thuật: Trong Scrum, một Product Backlog Item (PBI) chỉ được tính là hoàn thành (Done) khi thỏa mãn toàn bộ Definition of Done (DoD) như đã viết code, test qua QA, code review và deploy lên môi trường Staging. Việc ước lượng theo phương pháp nhị phân (Binary Tracking) nghĩa là chưa xong 100% thì point vẫn giữ nguyên là 3, không có khái niệm 'xong 80% trừ 2.4 point'. Nếu trừ non, Burndown Chart sẽ phản ánh sai lệch thực trạng dự án, che giấu các rủi ro kỹ thuật tiềm ẩn.

- Burndown Chart phản ánh khối lượng công việc CÒN LẠI thực tế có thể bàn giao.
- Nguyên tắc Scrum: Không nghiệm thu nửa vời (No partial points for unfinished stories).

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `bt2.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
