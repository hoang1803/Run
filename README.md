# Run
## 1. Hướng dẫn cài đặt:

### a.Yêu cầu cần có:
* Code::Blocks.
* SDL2_ttf, SDL2_mixer, SDL2_image, SDL2.

### b. Hướng dẫn cài đặt:

#### i) Cài đặt Code::Blocks:

* [Bấm vào đây](http://www.codeblocks.org/downloads/binaries/#imagesoswindows48pnglogo-microsoft-windows), rồi chọn tải bản **codeblocks-20.03mingw-setup.exe** về máy.
* Sau khi đã tải xuống, bạn hãy vào thư mục chữa file setup trên, bấm vào nó, và click **Next** cho đến khi cài đặt xong.

#### ii) Cài đặt SDL2:

* [Bấm vào đây](https://bitly.com.vn/c7wowi), rồi tải file **SDL2-setting.zip** về máy của bạn.
* Sau đó, bạn giải nén ra và cho những thứ trong đó vào thư mục nào đấy.
* Sau đó, bạn bật Code::Blocks lên, chọn **Setting** -> **Compiler** -> **Linker settings**, sau đó copy **-lmingw32 -lSDL2main -lSDL2 -lSDL2_image
-lSDL2_mixer -lSDL2_ttf** sau vào trong **Other linker options**.
![image](https://user-images.githubusercontent.com/100293832/170075373-d5b8fbc1-4e0b-43b5-ba40-251208b89608.png)


* Lưu ý: Các bước sau đây là cài đặt cho CodeBlock 64 bit. Với CodeBlock 32 bit, bạn chỉ cần thay thế thư mục **x86….** bằng thư mục **i686…**

* Sau đó, bạn tiếp tục chọn **Search directories**, trong phần **Compiler**, bạn chọn **Add**, và ghi như sau: **Đường dẫn đến folder SDL2\x86_64-w64-mingw32\include\SDL2**, chẳng hạn như tôi để cái file SDL ở ổ D, tôi sẽ điền như sau:
![image](https://user-images.githubusercontent.com/100293832/170077564-94b973fe-3352-4b5c-b163-f1fd9419746a.png)
* Sau đó, trong **Search directories**, bạn chọn **Linker**, chọn **Add**, và ghi lần lượt như sau: **Đường dẫn đến folder SDL2\x86_64-w64-mingw32\lib**, ví dụ:
![image](https://user-images.githubusercontent.com/100293832/170078329-c5fc16d0-3ea4-4964-9f65-a2f0fca9caac.png)
* Cuối cùng, bạn bấm nút **Nút OK** để hoàn tất cài đặt nhé.


#### iii) Cài đặt và chạy game:
* Bước 1: Bạn hãy download folder **Run** về máy.
* Bước 2: Giải nén (nếu có), và sau đó chọn file **Run!!.cbp** và mở lên.
* Bước 3: Bấm phím **F9** để chơi game, hoặc có thể tìm biểu tượng ![image](https://user-images.githubusercontent.com/100293832/170079367-de773ca9-74a3-4016-ae2d-aeb3217f542c.png) trên thanh công cụ.
* Bước 4: Thưởng thức trò chơi.


##### Lưu ý: Trong trường hợp bạn bật file cpp lên và bị như này thì đừng lo, chúng ta sẽ sửa như sau:

![image](https://user-images.githubusercontent.com/100293832/170166857-2f0838e0-7854-4f4d-8be3-0d396bfaf9ff.png)


- Bước 1: Bấm chuột phải vào file main.cpp, rồi chọn **Remove file from project**.

![image](https://user-images.githubusercontent.com/100293832/170166901-9c5b434a-ee0d-4095-9194-e77209298fe0.png)


- Bước 2: Bấm chuột phải vào project **Run!!**, và chọn **Add file**.

![image](https://user-images.githubusercontent.com/100293832/170166935-2d8ed0ea-efd4-4bd7-806e-f16de090a1e9.png)

- Bước 3: Chọn tất cả các file có đuôi **.cpp** hoặc **.h**, sau khi chọn xong bạn bấm **Open** -> Bấm **OK**. Từ đó bạn sẽ có những file đầy đủ như ảnh dưới.

![image](https://user-images.githubusercontent.com/100293832/170167104-0bfa12ad-eb09-4d96-b83e-1a7c233a2b19.png)

- Bước 4: Làm như hướng dẫn ở trên và thưởng thức trò chơi.

## 2. Mô tả chung về trò chơi, các ý tưởng chính:
* Mô tả chung về trò chơi: Bạn sẽ nhập vai vào nhân vật bị mắc kẹt trong rừng rậm, và bạn phải đánh bại các con quái vật trong thời gian nhất định để có thể thoát khỏi khu rừng. 
* Ý tưởng chính: Nhân vật cầm kiếm di chuyển để chém quái vật, có các vật phẩm hồi máu và tăng sức tấn công.

## 3. Các chức năng đã cài đặt, gồm có:
* Hình động của nhân vật và quái.
* Di chuyển map theo nhân vật, sử dụng tileset.
* Có menu ban đầu, menu chọn độ khó và menu chiến thắng/thua cuộc.
* Sử dụng âm thanh.
* Hiển thị máu, sức mạnh, điểm, thời gian còn lại của nhân vật...
* Minh họa: [Click here](https://youtu.be/fJQcZ5sCVV0).

## 4. Các kỹ thuật lập trình được sử dụng trong chương trình:
* Mảng.
* Con trỏ.
* Class, struct.
* SDL2, SDL2_image, SDL2_mixer, SDL2_ttf.
* Sinh số ngẫu nhiên.

## 5. Kết luận, hướng phát triển và các điều tâm đắc rút ra được sau khi hoàn thiện chương trình:
### a. Kết luận:
* Em đã quản lý được nhiều hàm ở nhiều file.
* Học được cách sử dụng đồ họa SDL.
### b. Hướng phát triển:
* Cải thiện đồ họa đẹp hơn.
* Cải thiện va chạm giữa nhân vật, map và quái vật.
* Thêm nhiều màn chơi, bản đồ chơi.
* Thêm nhiều quái vật, boss.
* Thêm các chuyển động, hình động và âm thanh của nhân vật, quái vật.
* Thêm các đồ phụ trợ, bẫy,...
### c. Các điều tâm đắc rút ra được sau khi hoàn thiện chương trình:
* Cần phải biết được đặc tính của từng vật thể mà mình định làm, rồi sau đó nhóm chúng vào từng lớp.
* Để từng lớp ra các file khác nhau để quản lý từng lớp cho dễ dàng.
* Cần đặt tên biến, comment vào code để sau này có xem lại thì còn có thể hiểu được.
