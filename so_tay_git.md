# 1. Cài đặt
- Tải git về cho OSX: http://git-scm.com/download/mac
- Tải git về cho Windows: https://gitforwindows.org/
- Tải git về cho Linux: http://book.git-scm.com/download/linux
# 2. Tạo một repository mới
Để tạo 1 repository mới, bạn hãy mở cửa sổ lệnh và gõ dòng lệnh sau: 
git init
# 3. Sao chép (clone) một repository
- Để clone 1 repository có sẵn ở trên máy cục bộ, bạn hãy sử dụng dòng lệnh sau:
        git clone /đường-dẫn-đến/repository/
- Nếu repository đó ở máy chủ khác thì bạn hãy gõ dòng lệnh sau:
git clone tênusername@địachỉmáychủ:/đường-dẫn-đến/repository
# 4. Quy trình làm việc
Thư mục cục bộ của bạn bao gồm ba "trees" được duy trì bởi git.
Đầu tiên là Thư Mục Đang Làm Việc (Working Directory) có chứa các tập tin hiện tại.
Thứ hai là Chỉ Mục (Index) đóng vai trò như staging area.
Cuối cùng là HEAD trỏ đến commit gần đây nhất của bạn.
# 5. Thêm (add) & commit
Bạn có thể đề xuất thay đổi (thêm nó vào chỉ mục Index) bằng cách:
```bash
git add <tên-tập-tin>
git add *
```
Đây là bước đầu tiên trong quy trình git cơ bản. Để thật sự commit những thay đổi, bạn sử dụng
```bash
git commit -m "Ghi chú Commit"
```
Bây giờ thì tập tin đã được commit đến HEAD, nhưng chưa phải trên thư mục remote.
# 6. Đẩy (push) các thay đổi
Thay đổi của bạn hiện đang nằm tại HEAD của bản sao cục bộ đang làm việc. Để gửi những thay đổi đó đến repository remote, bạn thực thi:
git push origin master
Thay đổi master bằng bất cứ nhánh nào mà bạn muốn đầy những thay đổi đến.
Nếu bạn chưa clone một repository hiện có và muốn kết nối repository của bạn đến máy chủ remote, bạn phải thêm nó với
git remote add origin <máy-chủ>
Bây giờ bạn đã có thể đẩy các thay đổi của mình vào máy chủ đã chọn
# 7. Nhánh (Branch)
Các nhánh (branches) được dùng để phát triển tính năng tách riêng ra từ những nhánh khác. Nhánh master là nhánh "mặc định" khi bạn tạo một repository. Sử dụng các nhánh khác tri đang trong giai đoạn phát triển và merge trở lại nhánh master một khi đã hoàn tất.
