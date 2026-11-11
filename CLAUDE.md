# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Kho này là gì

Kho chứa hồ sơ xin việc / xin học của chủ kho: CV, 자소서 (bài tự giới thiệu tiếng Hàn), câu trả lời nhà tuyển dụng. Không có mã, không có lệnh build, lint hay test.

Tại thời điểm tạo tệp này (11/11/2026) kho chưa có tệp nào khác. Đơn đang làm, hạn nộp và các bản nháp nằm trong gói bàn giao chủ kho giữ ngoài kho; đầu phiên hỏi chủ kho dán gói đó nếu cần.

## Kho đang PUBLIC

Mọi thứ commit lên đây ai cũng đọc được. Không commit: số điện thoại, email, ngày sinh, thu nhập, nợ, số dư tài khoản, chuyện nhập quốc tịch, giấy tờ cá nhân. Gói bàn giao hồ sơ (có các thông tin trên) chỉ giữ ngoài kho; muốn đưa vào thì chủ kho chuyển kho sang Private trước.

## Luật viết văn bản thay chủ kho (chủ kho đã chốt)

1. Trước khi đưa nháp: bảng đối chiếu từng ý của đề. Tên câu hỏi cũng là một ý (vd. "질문한" ⇒ bài phải có một câu hỏi thật).
2. Chủ kho kể chuyện bằng lời mình trước; số kỹ thuật (log, commit, CSV từ dự án khác) chỉ dùng để KIỂM chuyện, không dùng để dựng chuyện. Chỗ Claude suy ra đánh ⚠ đánh số, hỏi trước khi dán.
3. Câu đầu = ý chính; giữa = chuyện + số làm chứng; cuối = bài học hoặc việc đang làm. Không hứa chung chung.
4. Người đọc không biết dự án: lời thường, câu ngắn, hình ảnh đời thường thay thuật ngữ; nhưng không "trẻ con hóa". Trả lời trước câu người đọc chắc chắn hỏi ("sao tự nhiên lại hỏi?", "AI làm hết à?").
5. Mỗi bài đúng 1 chuyện; các bài không lặp chuyện (chỉ nhắc nửa câu). Cùng chuyện thì cùng số, cùng vai.
6. Số đưa vào bài phải khớp đúng giai đoạn nó đo; số từ giả lập không được viết như số đo thật.
7. Không viết như đi xin; "vì sao cần chương trình" = mình thiếu gì + chương trình bù đúng chỗ nào.

## Đếm chữ (luôn bằng máy)

Giới hạn form tính cả dấu cách. Chừa lề ≥ 3 % (800 ⇒ ≤ 776; 1 000 ⇒ ≤ 970), kiểm cả hai kiểu đếm xuống dòng:

```bash
python3 -c "import sys;t=open(sys.argv[1],encoding='utf-8').read().rstrip('\n');print(len(t),len(t)+t.count('\n'))" bai.txt
```

Số thứ nhất: xuống dòng = 1 ký tự; số thứ hai: xuống dòng = 2 ký tự. Cả hai phải ≤ ngưỡng.

## Việc không quay lại được

Bấm nộp đơn, gửi thư cho nhà tuyển dụng: dừng trước bước đó, chờ chủ kho xác nhận bằng lời.
