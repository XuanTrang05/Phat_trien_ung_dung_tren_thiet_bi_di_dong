# Phat_trien_ung_dung_tren_thiet_bi_di_dong
MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419
BÀI TẬP LỚN:
1. Viết phần mềm trên công cụ Mit App inventor
   (tập trung vào quy trình tạo ra phần mềm)
   app có 3 screen:
   + about về bản thân+nút gọi sang 2 screen còn lại
   + giải 1 bài toán đơn giản
   + sử dụng webview: hiển thị 1 trang web có sẵn, hỗ trợ giao diện điện thoại
   mô tả: thanh công cụ có gì? kéo thả + thay đổi thuộc tính: làm ntn, để làm gì?
          block: mô tả bản chất việc kéo thả block ntn?
                 ưu điểm gì so với viết code? nhược điểm?
                 copy paste block ? (backpack)
2. Viết app sử dụng Android Studio
   + Android manifest.xml  => mô tả gì? app cần quyền để do-st: khai báo ntn? để làm gì?
   + vòng đời của 1 ứng dụng android.
     code tự sinh sau khi tạo 1 project: có sẵn hàm onCreate: tại sao???
   + Code: java language. 
     app cần check xem có quyền để do-st? : code ntn? ý nghĩa?
     giao diện: (res/layout) mô tả bằng file XML + UI Design review
        + thuộc tính text, hoặc các thuộc tính khác: giá trị hardcode => lưu vào nới khác, tham chiếu tới nó:
          cú pháp của việc tham chiếu là gì?
          ưu điểm của việc tham chiếu này?
          OS hỗ trợ auto việc lấy giá trị tham chiếu theo LOCATION, LANGUAGE, THEME
          việc hỗ trợ auto này giúp app làm được điều gì?	
        + đối tượng chứa: gộp các đối tượng con lại: cùng 1 quy luật sắp xếp để hiển thị 
          các đối tượng con nằm kề nhau theo chiều dọc | hoặc ngang, gravity
     code tương tác với layout: vd hiển thị text
          mong muốn text hiển thị phù hợp với thiết lập LOCATION, LANGUAGE, THEME của người dùng
          thì làm ntn? (tránh hardcode)
     event (sự kiện) người dùng tác động vào app: CLICK vào button, click vào text,...
          với 1 sự kiện nào đó, muốn chạy 1 đoạn code để do-st
          thì LAYTOUT cần làm gì?
              CODE viết như nào (2 cách)
---------------------------
     trong app có các thư mục đặc biệt: Assets
     khi sử dụng Window Explorer để copy các files + folder vào trong Assets
     thì khi compiler: mọi file này đều đi theo app, nằm trong app
     trong app có thể truy cập được đến các file này
     cú pháp truy cập vào là gì?
     lợi ích của việc app có sẵn các files (offline cũng có)?
     ứng dụng: app hướng dẫn việc X

==> tạo app1 sử dụng cơ chế Dữ liệu chuẩn bị trước trong Assets
         format dữ liệu: tuỳ ý, nội dung tuỳ ý
         công cụ để hiển thị dữ liệu: tuỳ ý
         có cần phải tiền xử lý trước khi hiển thị ko: tuỳ ý.
         SV TỰ ĐẶT RA VẤN ĐỀ => TỰ GIẢI QUYẾT VẤN ĐỀ
         MÔ TẢ ĐƯỢC DỮ LIỆU CÓ ĐẶC THÙ GÌ
                    DÙNG THUẬT TOÁN NÀO ĐỂ XỬ LÝ DỮ LIỆU (NẾU CẦN)
                    DÙNG ĐỐI TƯỢNG NÀO ĐỂ HIỂN THỊ DỮ LIỆU.
                    (ĐỘ SÁNG TẠO LÀ KO GIỚI HẠN)
------------------------
APP2 (android studio):  tạo app tương đương với Mit App inventor
  app có 3 activity
  + activity1: about: about+nút gọi sang 2 activity còn lại
  + activity2: giải toán đơn giản (tuỳ ý). mỗi khi giải xong bài toán: gọi api tại https://k58kmt.tdh.io.vn/api
    để gửi bài toán lên đó
    {app_by:mã số sv, input: {a:1,b:2,c:3,name:"hello tắc kè"},output:{ketluan:"vô nghiệm", abc:"xyz", nghiem:3.14}}
    nhận lại json: {ok:1, stt:1234}
  + activity3: 
    dùng web-view để truy cập từ 
    1 trang web https://k58kmt.tdh.io.vn?masv=mã sv của bạn
=======================
    vết để lại: mô tả quá trình làm bài tập ra file .md => upload github
    kèm hình ảnh minh hoạ quá trình làm.

    print ra giấy đóng quyển, nộp bm.
## BÀI LÀM
# 1. Viết phần mềm trên công cụ Mit App inventor
- Tạo Project
   > - Vào appinventor.mit.edu → Create Apps! → đăng nhập Google
   > - Click Projects → Start new project → đặt tên ví dụ BaiTapLon
<img width="953" height="1079" alt="image" src="https://github.com/user-attachments/assets/d9591091-833c-4f18-b89d-bc41b0960e4f" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d8be158f-814a-4cb1-b76e-26ef64e0cd7e" />

- Tạo Screen1 (About bản thân)
- Kéo Label ->  Đổi nội dung -> Bên phải: Properties -> Tìm: Text -> đổi thành thông tin cá nhân ( làm y hệt như vậy với 2 label còn lại)
- Tạo Button: Kéo: Button -> Text:  giải toán ( button Web view cũng làm tương tự)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f5ab36fc-006e-4fe1-b990-28e4d295edfe" />

Nút mở Screen2

- THIẾT KẾ SCREEN 2 (GIẢI PHƯƠNG TRÌNH ax+b=0)
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/74356cac-35f1-4c00-83e3-b51674de5618" />

- Viết Block giải toán
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/610a0748-64e4-42ae-8988-0ca2e22de123" />

- THIẾT KẾ SCREEN 3
- ở phần url sẽ để https://www.google.com , để test thử xem phần mit app có hoạt động không
- Kéo thêm 1 dòng chữ (Label) từ cột User Interface bên trái thả vào màn hình, đặt nó nằm phía trên hoặc phía dưới cái WebViewer đó. Thay đổi chữ hiển thị của nút bấm thành: "bài tập của xuân trang".
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e5c40280-2ab1-4ff1-ac0a-da6409528b2f" />
- kết quả test
- Nút bấm chứa tên vẫn nằm ở đó, còn ô phía dưới thì hiển thị trang Google! Điều này chứng tỏ app của bạn hoạt động

<img width="1179" height="2556" alt="image" src="https://github.com/user-attachments/assets/16915861-6068-4a8f-b14b-c33bfcdee65a" />

cat > /mnt/user-data/outputs/MoTa_MITAppInventor.md << 'EOF'
# Mô tả công cụ MIT App Inventor

## Thanh công cụ Designer — có gì?

Giao diện Designer gồm 4 khu vực chính:

### Palette (bên trái)
- Chứa toàn bộ các component sẵn có, chia theo nhóm:
  - **User Interface**: Button, Label, TextBox, Image, CheckBox...
  - **Layout**: HorizontalArrangement, VerticalArrangement, TableArrangement
  - **Media**: Camera, Player, Sound...
  - **Connectivity**: Web, BluetoothClient...
  - **Sensors**: LocationSensor, AccelerometerSensor...
- Mục đích: là kho component để lập trình viên chọn và kéo vào giao diện

### Viewer (ở giữa)
- Mô phỏng màn hình điện thoại Android
- Lập trình viên kéo component từ Palette thả vào đây để bố trí giao diện
- Hiển thị trực quan giao diện sẽ trông như thế nào trên điện thoại thật

### Components (bên phải trên)
- Hiển thị cây phân cấp tất cả component đang có trong screen
- Dùng để chọn nhanh một component, đổi tên (Rename) hoặc xoá (Delete)
- Thể hiện quan hệ cha-con giữa các component (ví dụ Button nằm trong VerticalArrangement)

### Properties (bên phải dưới)
- Hiển thị toàn bộ thuộc tính của component đang được chọn
- Ví dụ: Text, FontSize, FontBold, BackgroundColor, Width, Height, Visible...
- Mục đích: tuỳ chỉnh ngoại hình và hành vi của component mà không cần viết code

---

## Kéo thả + thay đổi thuộc tính — làm như thế nào, để làm gì?

### Cách kéo thả component:
1. Tìm component cần dùng trong **Palette** bên trái
2. Giữ chuột trái vào component đó
3. Kéo sang vùng **Viewer** ở giữa rồi thả ra
4. Component xuất hiện trên giao diện, đồng thời xuất hiện trong cây **Components**

### Cách thay đổi thuộc tính:
1. Click vào component trong **Viewer** hoặc trong **Components**
2. Bảng **Properties** bên phải tự động hiển thị thuộc tính của component đó
3. Thay đổi giá trị trực tiếp: gõ chữ vào ô Text, chọn màu ở BackgroundColor, tick vào FontBold...
4. Giao diện trong Viewer cập nhật ngay lập tức

### Để làm gì?
- Xây dựng giao diện người dùng (UI) một cách trực quan
- Không cần viết XML hay code để tạo layout
- Thấy ngay kết quả sau mỗi thay đổi → dễ chỉnh sửa, dễ thử nghiệm

> 📸 *[Chèn ảnh màn hình Designer tại đây]*

---

## Block — Bản chất việc kéo thả block là gì?

### Bản chất:
- Mỗi **block** là một lệnh lập trình được biểu diễn bằng **hình khối màu sắc**
- Các block có **hình dạng khớp nhau theo kiểu dữ liệu**: block số chỉ ghép được vào ô nhận số, block boolean chỉ ghép được vào ô điều kiện → không thể ghép sai kiểu
- Lập trình viên **kéo block từ danh sách bên trái** (Built-in hoặc tên component) rồi **thả vào vùng làm việc** ở giữa
- Các block ghép lại với nhau như **xếp hình LEGO**: block con lồng vào block cha để tạo thành cấu trúc lệnh hoàn chỉnh
- Kết quả là một **chương trình chạy được** mà không cần gõ một dòng code nào

### Ưu điểm so với viết code:
| Tiêu chí | Block | Viết code |
|---|---|---|
| Lỗi cú pháp | Không có (không thể ghép sai) | Thường xuyên xảy ra |
| Dễ học | Rất dễ, phù hợp người mới | Cần học ngôn ngữ lập trình |
| Trực quan | Thấy ngay cấu trúc logic | Phải đọc hiểu từng dòng |
| Tốc độ làm | Nhanh với app đơn giản | Chậm hơn nhưng linh hoạt hơn |

### Nhược điểm so với viết code:
- Khó xử lý logic phức tạp (nhiều vòng lặp lồng nhau, đệ quy...)
- Không thể dùng thư viện ngoài
- Khó tái sử dụng code, khó quản lý khi app lớn
- Không có tính năng debug nâng cao
- Hiệu năng thấp hơn so với app viết bằng code thật

## Backpack — Copy Paste Block giữa các Screen

### Backpack là gì?
- Backpack (cái ba lô) là **vùng lưu trữ tạm thời** cho block, nằm ở **góc trên bên phải** màn hình Blocks
- Biểu tượng trông như một chiếc ba lô màu xanh lá

### Cách dùng:
1. Kéo block muốn copy vào **biểu tượng Backpack** → block được lưu vào đó
2. Chuyển sang **Screen khác** (click tên screen ở thanh trên)
3. Kéo block từ **Backpack** ra vùng làm việc → block được dán sang screen mới
4. Block gốc ở screen cũ vẫn còn nguyên

### Dùng để làm gì?
- **Tái sử dụng logic** giữa các screen mà không cần làm lại từ đầu
- Ví dụ: block kiểm tra dữ liệu nhập vào giống nhau ở Screen2 và Screen3 → copy qua Backpack thay vì làm lại
- Tiết kiệm thời gian khi nhiều screen có logic tương tự nhau









    
