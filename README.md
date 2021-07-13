

   
# I. Git là gì?
 **Git** là phần mềm hỗ trợ quản lý việc viết code, là hệ thống thuộc dạng **VCS** (Version Controll System).
 Nó cung cấp cho mỗi lập trình viên kho lưu trữ (**repository**) riêng chứa toàn bộ lịch sử thay đổi.

**VCS** là hệ thống giúp lập trình viên có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (**clone**) từ  kho chứa mã nguồn (**repository**).
Mỗi thay đổi vào mã nguồn trên local sẽ có thể ủy thác (**commit**) rồi đưa lên server nơi đặt kho chứa chính.
# II. Lợi ích của Git
  * Lưu trữ các phiên bản khác nhau của mã nguồn dự án phần mềm
  * Khôi phục lại mã nguồn từ một phiên bản bất kỳ
  * Dễ dàng so sánh giữa các phiên bản
  * Phát hiện được người gây ra lỗi phát sinh
  * Khôi phục lại tập tin đã mất
  * Dễ dàng thử nghiệm, mở rộng tính năng của dự án mà không làm ảnh hưởng đến phiên bản chính (**master branch**)
 
# III. Flow cơ bản trong Git
   * Clone project từ server về Local Repository
   * Check-out một nhánh từ Local Repository về Working space
   * Làm việc (thêm, sửa, xóa) tại Working space
   * Add: Xác nhận sự thay đổi của các file (đưa đến vùng Staging Area)
   * Commit: Cập nhật sự thay đổi lên Local Repository
  
 Về cơn bản, tại bước này, bạn đã hoàn thành một chu trình (**flow**) sử dụng Git. 
 Lúc này, nếu như bạn muốn cập nhật sự thay đổi này lên server thì bạn sẽ dùng lệnh *push* để đẩy chúng lên server.
# IV. Các thuật ngữ cơ bản
  ## 1. Repository-Kho lưu trữ

  Repository là nơi lưu trữ, quản lý tất cả những thông tin cần thiết (thư mục, tập tin, ảnh, video, dữ liệu...),cũng như sửa đổi và lịch sử của toàn bộ dự án.
  Khi tạo mới repository, bạn nên tạo thêm tập tin README hoặc một tập thông tin giới thiệu về dự án của bạn.
  
  Có hai loại repository là local repository và remote repository.
  Remote repository là repository để chia sẻ giữa nhiều người và bố trí trên server chuyên dụng.
  Local repository là repository bố trí trên máy của bản thân mình, dành cho một người dùng sử dụng.
  ## 2. Branch- Nhánh

  Branch được dùng để phân nhánh và ghi lại luồng của lịch sử. 
  Branch đã phân nhánh sẽ không ảnh hưởng đến branch khác nên có thể tiến hành nhiều thay đổi đồng thời trong cùng một reposoitory.
  
  Hơn nữa, branch đã phân nhánh có thể chỉnh sửa, tổng hợp lại thành một branch bằng việc hợp lại (merge) với branch khác.
  
  Khi tiến hàng commit lần đầu tiên trong repository thì Git sẽ tạo ra một có tên là master (nhánh chính).
  Vì thế những lần commit sau sẽ được thêm vào **branch master** (nhánh chính) cho đến khi chuyển đổi branch.
  ## 3. Commit
  
  Một commit đại diện cho một thời điểm cụ thể trong lịch sử dự án của bạn. 
  Sử dụng lệnh commit kết hợp với lệnh **git add** để cho git biết những thay đổi bạn muốn lưu vào local repository.
