1. Version control system: Lưu history, back lại version cũ, làm việc nhóm mà không đè lên nhau, gồm:
   + Local version : Lưu ở máy local (tạo ra nhiều version khác nhau để lưu trữ )
   + Centralized version: Lưu ở 1 máy chủ tập trung (Central server)
   + Distributed version (Popular): Lưu ở nhiều máy khác nhau (Git)

2. Git (Command line tool): Three states
   + Working directory: Lưu file mới tạo/ change (Draft)
     -> Git int: Khởi tạo repo mới, chỉ chạy 1 lần
   + Staging area: Vùng chuẩn bị tạo commit (Prepare)
     -> Git add <namefile> : Thêm 1 file vào staging, chạy khi có change
     -> Git add <namefile1> <name file2> : Thêm multiple file vào staging
     -> Git add. : Thêm all file vào staging
     -> Git commit -m"message" : Tạo commit (Có thể tạo commit cho nhiều phiên bản cùng lúc.)
   + Repository: các phiên bản commit (Submitted)
     -> Note: lastest commit sẽ nằm trên cùng
    ===============================================================
   + Cấu hình all repo trên máy tính (--global)
     -> git config --global user.name "tên"
     -> git config --global user.email "email"
     Full flow: int -> add -> commit -> push
   + Cấu hình riêng cho từng repo (không có --global)
     Note: Mở đúng terminal cho thư mục cần cấu hình
     -> git config user.name "tên"
     -> git config user.email "email"
     Full flow: int -> config -> add > commit -> push

   + Check status
     -> git status 
     Đỏ: file đang ở working director
     Xanh: File đang ở staging area
   + Check danh sách commit
     -> git log

   + Commit convention
     -> <type>: <short_description>>
     Type:
         - chore: chỉnh sửa nhỏ lẻ
         - feat: add tính năng mới, tc mới
         - fix: sửa lỗi
3. JavaScript basic
   + In dòng chữ
     -> console.log("nội dung") || Có thể dùng "" or ''
   + Run câu lệnh
     -> node <filename> (nếu là folder -> cd vào folder để run)
   + Comment code
     -> Một dòng: Thêm // trước dòng code 
     -> Nhiều dòng: 
        1. Thêm /* đoạn code */
        2. Bôi đen -> Ctrl/Cmd + /
   + Khai báo biến: <từ khoá> <tên biến> = <giá trị>
     -> Có thể khai báo nhiều lần, thay giá trị đổi tuỳ ý
     1. var <tên biến> = <giá trị>;
        // đời cũ, cho khai báo lại, ít sử dụng
        // không sử dụng
     2. let <tên biến> = <giá trị>;
        // đời mới, không cho khai báo lại đc sd phổ biến
        // Sử dụng khi cần gán lại giá trị
   + Khai báo hằng: <từ khoá> <tên hằng> = <giá trị>
     1. const <tên hằng> = <giá trị>;
        // Chỉ đc khai báo 1 lần, luôn cố định, không thay đổi
        // Default sử dụng
     2. Có thể sd ${biến} để thêm vào chuỗi <giá trị>
        -> const <tên hằng> = `<giá trị>: ${biến}`;
        // `` là backtick
   + Kiểu dữ liệu (Data type)
     1. Primitibe types (Nguyên thuỷ): 
        -> Number
        -> String: nằm trong dấu nháy đơn, nháy kép, backtick ``
        -> Boolean (true/false)
        -> Undeffined, Null, Symbol, BigInt 
     2. Reference types (Tham chiếu): 
        -> Object
     3. Hàm: typeof <variable> || check kiểu dữ liệu
   + Toán tử so sánh 
     1. So sánh bằng: == and ===
        -> == : JS sẽ chuyển 2 vế về cùng kiểu rồi mới so sánh
        -> ===: so sánh ngay lập tức, không chuyển đổi (recommend use)
     2. So sánh không bằng: !
     3. So sánh lớn hơn, nhỏ hơn: >, <, >=, <=
   + Toán tử logic
     1. && (AND) : Tất cả phải đúng
     2. || (OR) : Chỉ cần 1 đúng
   + Toán tử 1 ngôi: 
     1. Prefix: ++x, --x : Tăng trước, trả về sau
     2. Postfix: x++, x-- : trả về trước, tăng sau
   + Toán tử toán học: +, -, *, /
   + Câu điều kiện
     1. if (<điều kiện>)
        { //code.. }
     2. if..else
     3. if..else if..else
     4. switch..case
   + Vòng lặp: 
     1. For (i)
        -> For (<điều kiện khởi tạo>; <điều kiện lặp>; <cập nhật>)
           { //code }
-> Format code: Option + Shifft + F