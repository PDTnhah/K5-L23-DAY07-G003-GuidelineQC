# Ghi chú cá nhân — 105

> Copy file này thành `submission/individual_notes/<mã>.md`. Mỗi thành viên một file, ngắn gọn (khoảng một trang), tự viết.

## 1. Pha 1: ba ca khó tôi tìm ra trong 40 ảnh
| Ảnh | v0 không trả lời được gì | Quyết định ban đầu của tôi |
|---|---|---|
| `img_008` *(thay bằng mã ảnh thực tế)* | Guideline v0 không quy định rõ xe tải lớn chở theo các xe máy hoặc xe nhỏ ở phía sau thì có phải gán nhãn cho các xe bên trên hay không. | Vẫn vẽ bounding box (`motorcycle` hoặc `car`) cho các phương tiện được chở bên trên nếu thấy rõ hình dạng phương tiện, vì chúng vẫn là đối tượng giao thông xuất hiện trong ảnh. |
| `img_015` *(thay bằng mã ảnh thực tế)* | Không đề cập cách xử lý với tượng trưng bày, ma-nơ-canh (mannequin) hoặc tượng người ven đường. | Quyết định **không gán nhãn** (`person`) cho ma-nơ-canh hoặc tượng vì chúng không phải là người thật tham gia giao thông. |
| `img_027` *(thay bằng mã ảnh thực tế)* | Không hướng dẫn xử lý các đối tượng xuất hiện qua hình ảnh phản chiếu trên kính cửa sổ hoặc gương chiếu hậu. | Quyết định **bỏ qua (không gán nhãn)** các vật thể chỉ là hình ảnh phản chiếu qua kính/gương để tránh làm nhiễu dữ liệu huấn luyện thực tế. |

## 2. Pha 2: chỗ tôi bất đồng với nhóm
- Chỗ nào bản của tôi khác bản của bạn? Cuối cùng nhóm chốt gì, tôi đồng ý / chưa đồng ý vì sao?
  *(Điền sau khi họp nhóm ở Pha 2)*

## 3. Pha 3: ảnh tôi đã gán
- Số ảnh được giao: … Số box đã vẽ: … Số lần tôi tick `can_review`: …
- Ca nào tôi lưỡng lự nhất khi gán (ảnh, vì sao)?
  *(Điền sau khi hoàn thành gán nhãn ở Pha 3)*

## 4. Pha 4–5: tôi lệch ở đâu
- Trong `calibration_candidates.csv`, các ca có tên tôi: tôi lệch vì guideline mơ hồ hay vì tôi chưa nắm quy tắc?
- Quyết định calibration nào tôi thấy quan trọng nhất?
  *(Điền sau khi chạy IAA và Calibration ở Pha 4–5)*

## 5. Dùng AI
- Công cụ nào, cho việc gì, bạn kiểm tra kết quả thế nào? (Ghi "không dùng" nếu không dùng.)
  *(Ví dụ: Sử dụng Gemini để rà soát cấu trúc Markdown và tổng hợp các trường hợp đặc biệt cho guideline; đã đối chiếu lại trực tiếp với 40 ảnh thực tế trên CVAT và quy định của dự án).*

## 6. Bài học
- Một điều tôi sẽ làm khác khi viết guideline lần sau:
  *(Điền sau khi hoàn thành toàn bộ bài lab)*