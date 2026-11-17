# Báo cáo QC — G003

## 1. Mục đích, dữ liệu và phiên bản

- Mục đích và giới hạn sử dụng: Huấn luyện mô hình phát hiện đối tượng 2D phục vụ camera giao thông đường phố; chỉ sử dụng trên tập dữ liệu ảnh đô thị ban ngày/ban đêm đại diện trong tập 40 ảnh.
- Nguồn và phép sử dụng dữ liệu: 40 ảnh đường phố giấy phép Creative Commons (xem data/ATTRIBUTION.csv).
- Manifest và checksum nhãn cuối: batch_manifest.json (SHA-256: b247880f311a74ae499d946e856a16982ac6c86af1589b76cfa21dcc63539553)
- Guideline và taxonomy khi gán / khi bàn giao: Khi gán dùng taxonomy v1.0 và guideline_v1.0_agreed.md; khi bàn giao dùng guideline_v1.1_calibrated.md và giữ nguyên taxonomy v1.0.

## 2. Phân công và đồng thuận trước calibration

- Lượt hoàn thành / được giao: 120 / 120 (100% trên 40 ảnh, 5 thành viên gán độc lập).
- Số cặp box ghép, IoU TB, đồng thuận lớp và mẫu số: 777 cặp box ghép; IoU trung bình 0.844; đồng thuận lớp 89.3% trên mẫu số 777 cặp box ghép.
- Box chưa ghép, loại do ignore, bất đồng vùng ignore: Chưa ghép A/B là 260/248; loại do ignore là 0; bất đồng ignore là 0.
- Ca hai người có thể cùng sai sau khi đối chiếu tham chiếu: img_002.jpg (xe chở xe: hai người cùng gán sót box car con trên sàn hoặc chỉ gán 1 box truck); kiểm bằng cách rà soát theo quy tắc R-03/R-10.

## 3. Calibration và kiểm lại

- Ca đã xử lý, rule ID, bản sửa và người xác nhận: Đã xử lý 1261 ca bất thường được ghi chi tiết trong submission/qc/calibration_decisions.csv (người chốt: 343; người review: 069).
- Tác động v1.1 lên nhãn và ảnh: Làm rõ quy tắc R-10, ranh giới rider và xe, loại bỏ vật nhỏ < 20 px; phạm vi kiểm lại mở rộng cả lô (40 ảnh).
- Tham chiếu bằng chứng khi Rework: Vòng 1 giải quyết các ca nghi vấn can_review và rà soát lỗi; vòng 2 duyệt toàn bộ 40 ảnh sạch lỗi.

## 4. Kết quả duyệt

- Vòng QC: 2
- Người review và ngày: 343, 2026-11-17
- Đã duyệt / cả lô: 40 / 40 ảnh
- Ảnh lỗi / ảnh đã duyệt: 0 / 40 (0.0%)
- Annotation đối tượng hiện có bị lỗi / annotation đối tượng đã duyệt: 0 / 481 (0.0%)
- Vật bỏ sót, ảnh và vùng: Không có vật bỏ sót trên 40 ảnh đã duyệt.
- Ca khó / phần còn lại, lỗi lặp và ví dụ: Đã duyệt 36/36 ca khó (0 lỗi), 4/4 ảnh còn lại (0 lỗi) theo phiếu round-02/qc_review.csv.
- Một lỗi máy chặn được và một lỗi cần người đọc ảnh: Lỗi máy chặn: kích thước box < 20px hoặc sai schema; lỗi người đọc: phân biệt người đi bộ vs người điều khiển (rider) bị che khuất và phân biệt xe chở xe.

## 5. Quyết định bàn giao

- Quyết định: Release
- Lý do, người nhận và phạm vi sử dụng: Đạt toàn bộ tiêu chuẩn kiểm tra QC vòng 2 với tỉ lệ lỗi 0.0% trên cả 40 ảnh; bàn giao cho đội ngũ phát triển mô hình giao thông để huấn luyện object detection 2D.
- Nếu còn việc: Không còn tồn đọng; toàn bộ ca nghi vấn can_review đã được xử lý triệt để.
- Kiểm ngược từ báo cáo tới ảnh, rule và nhãn: C001, submission/qc/calibration_decisions.csv dòng 2, img_001.jpg person giữ box đạt R-10.
