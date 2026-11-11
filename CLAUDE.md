# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Kho này là gì

Kho chứa hồ sơ xin việc / xin học của chủ kho: CV, 자소서 (bài tự giới thiệu tiếng Hàn), câu trả lời nhà tuyển dụng. Không có mã, không có lệnh build, lint hay test.

Tại thời điểm tạo tệp này (11/11/2026) kho chưa có tệp nào khác. Đơn đang làm, hạn nộp và các bản nháp nằm trong gói bàn giao chủ kho giữ ngoài kho; đầu phiên hỏi chủ kho dán gói đó nếu cần.

Trước khi đọc hay ghi thu_vien/, đọc thu_vien/HUONG_DAN_THU_VIEN.md.

## Kho đang PUBLIC

Mọi thứ commit lên đây ai cũng đọc được. Không commit: số điện thoại, email, ngày sinh, thu nhập, nợ, số dư tài khoản, chuyện nhập quốc tịch, giấy tờ cá nhân. Gói bàn giao hồ sơ (có các thông tin trên) chỉ giữ ngoài kho; muốn đưa vào thì chủ kho chuyển kho sang Private trước.

## Luật viết văn bản thay chủ kho (bản 11/11/2026, rút từ hồ sơ AIGEN câu 1–2)

V1. Ý lõi trước, chuyện sau. Trước khi viết, hỏi Thiên và chốt bằng 1–2 câu: "nguyên tắc tư duy / giá trị mà bài này chứng minh là gì?". Câu chuyện chỉ là bằng chứng cho ý lõi; mỗi đoạn phải phục vụ nó. Câu đầu = ý chính; cuối = bài học hoặc việc đang làm, không hứa chung chung.
Bằng chứng: câu 2 có 3 bản "luận điểm, luận cứ đẹp nhưng trống rỗng"; chỉ đạt khi có ý lõi "phần giữ giá trị cốt lõi quyết, phần khác chỉ báo tin" (11/11 14:35).

V2. Trả lời đúng từng ý của đề. Chép nguyên văn câu hỏi, tách thành các ý (tên câu hỏi cũng là một ý: "질문한" ⇒ phải có câu hỏi thật), gán mỗi đoạn cho một ý, đưa bảng đối chiếu trước nháp. Thiếu một ý là bài hỏng, dù viết hay.
Bằng chứng: câu 1 bản 10/11 bị chấm "5 hoặc 0 điểm" vì không trả lời "주변에서 당연하게 여기던 일".

V3. Kể quá trình nghĩ, không kể kết quả thay đổi. Theo thứ tự đã xảy ra: thấy mâu thuẫn → truy nguyên nhân → thử → lặp lại hay không → tìm điểm chung → rút nguyên tắc → kiểm lại. Cấm kiểu "đã đổi cái này, sửa cái kia". Thiên kể bằng lời mình trước; Claude không dựng chuyện từ số kỹ thuật.
Bằng chứng: câu 2 bản 14:21 bị nhận xét "chỉ nói chung chung đã thay đổi nay kia, không có quá trình tư duy"; câu 1 qua 4 bản dựng từ số vẫn lệch, Thiên kể bằng lời thì 1 bản đạt (11/11).

V4. Viết cho người ngoài: khung trước, số sau, ví von đời thường. Đặt khung vật lý trước khi đưa số (xe 16 cm, khe 50 cm, rồi mới tới "còn trống 11 cm"). Số viết dễ đọc ("6번 중 4번"). Khái niệm kỹ thuật thì so với con người (mắt lái xe; người quyết theo giá trị cốt lõi). Bỏ hết thuật ngữ, nhưng không "trẻ con hóa". Trả lời trước câu người đọc chắc chắn hỏi ("sao tự nhiên lại hỏi?", "AI làm hết à?").
Bằng chứng: "돌아오는 길 도착이 0/6" và "좁은 문 앞에서 막혔다" bị nhận xét là người đọc không hình dung được.

V5. Thật trước, hay sau. Mỗi số, mỗi lời trích phải có nguồn và khớp đúng giai đoạn nó đo. Tách số đo trên đồ thật với số tính hoặc giả lập. Chỗ nào tự suy, tự diễn lại thì liệt kê ⚠ cuối bài, hỏi trước khi dán. Thiếu dữ kiện thì soạn lệnh để Thiên lấy từ chat nguồn, không đoán.
Bằng chứng: hai lệnh hỏi chat ros2 ngày 10/11 mới ra được số 11 cm, 14 cm, 8 cm và dòng thời gian 9/11.

V6. Mỗi bài đúng 1 chuyện; các bài không lặp chuyện (chỉ nhắc nửa câu). Cùng chuyện thì cùng số, cùng vai.

V7. Không viết như đi xin; "vì sao cần chương trình" = mình thiếu gì + chương trình bù đúng chỗ nào.

## Đếm chữ (luôn bằng máy)

Giới hạn form tính cả dấu cách. Chừa lề ≥ 3 % (800 ⇒ ≤ 776; 1 000 ⇒ ≤ 970), kiểm cả hai kiểu đếm xuống dòng:

```bash
python3 -c "import sys;t=open(sys.argv[1],encoding='utf-8').read().rstrip('\n');print(len(t),len(t)+t.count('\n'))" bai.txt
```

Số thứ nhất: xuống dòng = 1 ký tự; số thứ hai: xuống dòng = 2 ký tự. Cả hai phải ≤ ngưỡng.

## Việc không quay lại được

Bấm nộp đơn, gửi thư cho nhà tuyển dụng: dừng trước bước đó, chờ chủ kho xác nhận bằng lời.
