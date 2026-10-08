# BÁO CÁO BÀI TẬP: VIẾT USER STORY, ACCEPTANCE CRITERIA VÀ THEO DÕI TRÊN TRELLO (RIKKEICARE)

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## Bước 1. Viết User Story cho R5

Yêu cầu R5 từ đề bài: 'Phòng khám muốn tự cập nhật giá các gói khám.' Hiện tại admin RikkeiCare đang cập nhật hộ qua email.

User Story hoàn chỉnh cho R5 được viết theo cấu trúc chuẩn Agile:

Là một quản lý phòng khám, tôi muốn tự cập nhật giá các gói khám của mình, để không phải phụ thuộc vào admin RikkeiCare cập nhật hộ qua email, giúp tiết kiệm thời gian và đảm bảo giá luôn chính xác theo thời gian thực.

- Giải thích lựa chọn vai trò: Tôi chọn vai trò 'quản lý phòng khám' thay vì 'admin RikkeiCare' vì đây là người trực tiếp chịu trách nhiệm về dịch vụ và bảng giá của phòng khám họ. Việc để họ tự cập nhật sẽ giảm tải cho đội ngũ admin trung tâm, đồng thời trao quyền chủ động vận hành đúng với tinh thần phân quyền sản phẩm.

## Bước 2. Viết phần Then cho 2 AC của R5

Xây dựng tiêu chí nghiệm thu (Acceptance Criteria) theo mẫu Given - When - Then cho yêu cầu R5:

- AC 1 (Thành công): Given quản lý phòng khám đã đăng nhập vào hệ thống, When nhập giá mới cho một gói khám rồi nhấn nút 'Lưu', Then hệ thống lưu thành công giá mới vào cơ sở dữ liệu, hiển thị thông báo cập nhật thành công và cập nhật ngay lập tức giao diện hiển thị bảng giá cho bệnh nhân.
- AC 2 (Thất bại): Given quản lý phòng khám để trống ô giá hoặc nhập định dạng chữ cái không hợp lệ, When nhấn nút 'Lưu', Then hệ thống từ chối lưu, giữ nguyên giá cũ và hiển thị thông báo lỗi 'Vui lòng nhập giá hợp lệ bằng số lớn hơn 0'.

## Bước 3. Thẻ R5 đã sẵn sàng chưa?

Xét theo Definition of Ready (DoR) gồm 4 điều kiện của nhóm:

1. Có User Story đủ 3 vế: Đã có (Vai trò - Tính năng - Lợi ích).

2. Có tiêu chí nghiệm thu: Đã có 2 AC rõ ràng cho trường hợp thành công và thất bại.

3. Đã được ước lượng: Thẻ đã được team ước lượng là 3 story points.

4. Đủ nhỏ để làm xong trong 1 Sprint: Hoàn toàn phù hợp để hoàn thành trong 1 Sprint.

- Kết luận: Thẻ R5 HOÀN TOÀN ĐỦ ĐIỀU KIỆN để kéo sang cột 'Ready for Sprint'. Lý do là thẻ đã thỏa mãn 100% các tiêu chí trong Definition of Ready, đội ngũ phát triển không còn điểm mù nghiệp vụ nào khi nhận thẻ này vào Sprint.

## Bước 4. Hoàn thiện thẻ R5 trên Trello

Sau khi thẻ R5 được chọn vào Sprint, ta tiến hành cấu hình chi tiết thẻ trên Trello theo đúng quy ước của nhóm:

| Thuộc tính thẻ Trello | Giá trị cấu hình cho R5 |
| --- | --- |
| Tiêu đề thẻ | R5: Quản lý phòng khám tự cập nhật giá các gói khám |
| Nhãn (Label) | Xanh dương (Feature) vì đây là tính năng mới bổ sung cho hệ thống |
| Người phụ trách (Members) | Dev Backend & Dev Frontend phụ trách tính năng quản lý |
| Hạn hoàn thành (Due Date) | Ngày thứ 5 của Sprint (Đảm bảo tiến độ sớm) |
| Vị trí trong cột | Đặt ở ĐẦU CỘT Sprint Backlog (vì đây là việc ưu tiên cao nhất, cần làm trước tiên) |
| Checklist nghiệm thu | 1. Tạo API cập nhật giá khám
2. Xây dựng giao diện form nhập giá
3. Viết Unit Test cho validation giá tiền |

## Bước 5. Đọc Burndown Chart

Phân tích dữ liệu Burndown Chart của Sprint (Sprint dài 10 ngày, tổng cam kết 30 points, R5 chiếm 3 points):

- a) Ngày 6 nhóm nhanh hay chậm so với đường lý tưởng, lệch bao nhiêu point?: Theo đường lý tưởng, mỗi ngày giảm 3 point, vậy đến ngày 6 số point lý tưởng còn lại là: 30 - (6 * 3) = 12 point. Thực tế ngày 6 nhóm còn lại 20 point. Vậy nhóm đang CHẬM hơn so với đường lý tưởng và lệch: 20 - 12 = 8 point.
- b) Một bạn báo thẻ R5 'xong 80%' và muốn trừ luôn 3 point khỏi biểu đồ. Có nên không, vì sao?: TUYỆT ĐỐI KHÔNG NÊN. Trong Agile/Scrum, một User Story chỉ được tính là hoàn thành (Done) khi thỏa mãn toàn bộ Definition of Done (DoD), nghĩa là đã code xong, đã test qua QA, không còn lỗi và sẵn sàng phát hành. 'Xong 80%' vẫn tính là 0 point hoàn thành vì chưa mang lại giá trị sử dụng thực tế cho người dùng. Việc trừ point non sẽ làm sai lệch Burndown Chart, che giấu rủi ro tiến độ thực tế của Sprint.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `bt2.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
