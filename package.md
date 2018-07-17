# Trainee Colombo 2018
## Creating Composer Package Library
- thực hiện: Dương Minh Nam  

### 1. Tạo cấu trúc thư mục cho project  
Thực thi lệnh dưới đây. 'mylibrary' là tên chung, thay thế bằng bất cứ tên nào bạn muốn.
```
composer create-project buonzz/composer-library-template mylibrary
```
=> folder:  
    - **src**: nơi lưu code, mỗi class sẽ phải nằm trong tập tin riêng của nó trong folder này.  
    - **tests**: mỗi class viết ra trong src cần phải đưọc test trước khi được include vào đâu đó. => Về cơ bản chúng ta có test class để test các class khác 
    - **.gitignore**: ignore file không muốn đưa lên git  
    - **LICENSE**: điều khoản sử dụng  
    - **README.md**: tài liệu cho library  
    - **composer.json**: lưu trữ thông tin về library, như tên package, tác gỉa , dependencies...  
    - **phpunix.xml**: file cấu hình của PHPUnit.  
Đây là cấu trúc thư mục cơ bản nhất để bắt đầu.

### Tùy chính file được tạo  
Không nên đặt nhiều class vào một file php, vì thế tên class và tên file nên giống nhau cho thuận tiện. Nếu muốn viết thêm một class, hãy tạo mới 1 file!  

- **Namespace** nên là tên github, từng class được tạo nên được đặt theo cú pháp `VendorName\PackageName` 
- **Điều chính** branding: thêm mô tả (description) để package có thể dễ dàng tìm tthayas trên packagist.org, thêm tên tác gỉa, validate file composer.json để check valid  
- Viết **Test Class**: mỗi class trong src folder nên nên có test class liên kết với nó, tên nên đặt trùng và thêm đuôi 'test'.  
- run PHPUnit: `vendor/bin/phpunit` 

### Public  
- Nên đặt tên repo trên  github giống tên library  
- push libarary lên repo => vào **Settings** => **Webhooks & Services** => trong tab **Services** ,click **Add Service**, chọn **Packagist**  
- Lấy token, paste vào github
- Vào https://packagist.org/packages/submit , paste link github repo
=> Done !!!
- Sử dụng:
```
composer init
composer require yourusername/yourpackagename
```
