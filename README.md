

   
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
  
   Khi thực hiện commit, trong repository sẽ ghi lại sự khác biệt từ lần commit trước với trạng thái hiện tại. 
  Các commit ghi nối tiếp với nhau theo thứ tự thời gian do đó chỉ cần theo vết các commit thì có thể biết được lịch sử thay đổi trong quá khứ.
  
  ## 4. Clone
  
   Nếu bạn muốn có một bản sao của một kho chứa Git có sẵn, có thể là một dự án mà bạn tham gia- thì hãy thực hiện clone. 
  **Clone** sẽ tạo ra một bản sao của gần như tất cả những gì mà máy chủ đang lưu trữ. 
  Bạn sẽ có được tát cả lịch sử đã xảy ra trên repository và hoàn toàn có thể quay lại, undo lại từ bất kỳ thời điểm commit nào. 
  Và một điểm nữa là nếu ổ cứng máy bị hư, bạn có thể sử dụng bất kỳ bản sao trên bất kỳ máy khách nào để khôi phục lại máy chủ.

   Bạn có thể **clone** từ bất kỳ kho chứa nào, nó sẽ sao chéo luôn các thiết lập về repository và sẽ tự động taoj một master branch trên máy tính của bạn.

   Trên Github, có một cách khác để sao chép kho từ người khác là thực hiện **_fork_** trên repository bạn cần. 
   Điểm khác của fork là bạn có thể đóng góp thêm vào repository gốc bằng cách thực hiện pull request. 
   Khi máy chủ của repository nơi bạn fork nhận được yêu cầu sẽ xem xét chỉnh sửa của bạn, nếu thấy hay sẽ tiến hành merge nội dung chỉnh sửa của bạn vào source gốc.
   
   ## 5. Push
   
   Lệnh **push** được sử dụng để đưa nội dung kho lưu trữ cục bộ lên server. 
   **Push** là các bạn chuyển giao các commit từ kho lưu trữ cục bộ của bạn lên server.

   ## 6. Pull
   
   Lệnh này sẽ tự động lấy toàn bộ dữ liệu từ repository trên server và gộp vào branch hiện tại bạn đang làm việc.
   
   ## 7. Fetch
   
   Lệnh này sẽ truy cập vào repository trên server và kéo toàn bộ dữ liệu mà bạn chưa có từ repository trên server về.
   Sau đó, bạn có thể tích hợp dữ liệu vào branch bất kỳ lúc nào.
   
   ## 8. Merge & Rebase
   **Merge** được dùng để gộp nhánh, tức là lấy _snapshot_ (ảnh chụp) mới nhất của mỗi branch rồi kết hợp lại với nhau.
   Như vậy, mỗi khi merge một feature branch về master branch thì đơn giản là nó sẽ tạo ra một merge commit ở master branch.
   
   **Rebase** cũng là cách để bạn tích hợp các thay đổi từ nhánh này sang nhánh khác.
   Tuy nhiên, điểm khác biệt là nếu cần tích hợp feature branch vào master branch thì nó sẽ sao chép tất cả các thay đổi từ nhánh feature đặt lên trước nhánh master lần lượt theo thứ tự.
  ## 9. Stash
   Lệnh này được sử dụng khi muốn lưu lại các thay đổi **chưa commit**, thường rất hữu dụng khi thay đổi sang một branch khác mà lại đang làm dở ở branch hiện tại.
 ## 10. Tag
   Tag là chức năng đặt tên một cách đơn giản của Git, nó cho phép ta xác định một cách rõ ràng các phiên bản mã nguồn (code) của dự án. 
   Ta có thể coi tag như một branch không thay đổi được. 
   Một khi nó được tạo (gắn với 1 commit cụ thể) thì ta không thể thay đổi lịch sử commit ấy được nữa.
   
   Có 2 loại tag là **lightweight** và **annotated**
   
   * Lightweight tag
     * Temporary tag là cái không thể thay đổi
     * Có thể đăth tên
   * Annotated tag
     * Có thể đính kèm tên và email của người thực hiện và ngày
     * Có thể đặt tên
     * Có thể đính kèm bình luận
     * Có thể đính kèm chữ ký
     
**Annotated tag** sẽ trở nên quan trọng khi có kế hoạch đánh dấu commit quan trọng.
Thông thường dùng để đánh dấu commit để release và cũng có thể thêm những chú thích bên cạnh.

Mặt khác **lightweight tag** thì chủ yếu được dùng trên không gian local làm việc tạm thời.
## 11. Upstream
Upstream đề cập đến nơi bạn push các thay đổi của mình, thường là nhánh chính (master branch).
*******************
Nguồn tham khảo:
1. Viblo.asia (viblo.asia/p/nhung-lenh-git-co-ban-can-nho-V3m5W1OyZO7)
2. (https://csc.edu.vn/lap-trinh-va-csdl/tin-tuc/kien-thuc-lap-trinh/Git-la-gi--Nhung-khai-niem-co-ban-khi-lam-viec-tren-Git-4133)
3. (https://backlog.com/git-tutorial/vn/intro/intro1_2.html)
