> Mục lục
>> I. Git là gì?

>> II. Lợi ích của Git

>> III. Flow cơ bản trong Git

>> IV. Các thuật ngữ cơ bản

>> V. Các lệnh git cơ bản

   
# I. Git là gì?
 **Git** là phần mềm hỗ trợ quản lý việc viết code, là hệ thống thuộc dạng **VCS** (Version Controll System).
 Nó cung cấp cho mỗi lập trình viên kho lưu trữ (**repository**) riêng chứa toàn bộ lịch sử thay đổi.

**VCS** là hệ thống giúp lập trình viên có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (**clone**) từ  kho chứa mã nguồn (**repository**).
Mỗi thay đổi vào mã nguồn trên local sẽ có thể ủy thác (**commit**) rồi đưa lên server nơi đặt kho chứa chính.
## II. Lợi ích của Git
  * Lưu trữ các phiên bản khác nhau của mã nguồn dự án phần mềm
  * Khôi phục lại mã nguồn từ một phiên bản bất kỳ
  * Dễ dàng so sánh giữa các phiên bản
  * Phát hiện được người gây ra lỗi phát sinh
  * Khôi phục lại tập tin đã mất
  * Dễ dàng thử nghiệm, mở rộng tính năng của dự án mà không làm ảnh hưởng đến phiên bản chính (**master branch**)
 
### III. Flow cơ bản trong Git
   * Clone project từ server về Local Repository
   * Check-out một nhánh từ Local Repository về Working space
   * Làm việc (thêm, sửa, xóa) tại Working space
   * Add: Xác nhận sự thay đổi của các file (đưa đến vùng Staging Area)
   * Commit: Cập nhật sự thay đổi lên Local Repository
  
 Về cơn bản, tại bước này, bạn đã hoàn thành một chu trình (**flow**) sử dụng Git. 
 Lúc này, nếu như bạn muốn cập nhật sự thay đổi này lên server thì bạn sẽ dùng lệnh *push* để đẩy chúng lên server.
#### IV. Các thuật ngữ cơ bản
