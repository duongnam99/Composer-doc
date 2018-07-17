# Trainee Colombo 2018
## Composer 
- thực hiện: Dương Minh Nam 
### Global Options  
Các option dưói đây có thể dùng trong mọi lệnh:  
    - --verbose (-v): Tăng độ dài cho thông báo  
    - --help (-h): Hiển thị thông tin trợ giúp
    - --quiet (-q): Không hiển thị message 
    - --no-interacion (-n): Không hỏi câu hỏi
    - --no-plugins: tắt plugins
    - --working-dir (-d): nếu đưọc chỉ định, dùng thư mục đó là thư mục làm việc
    - --profile: Hiển thị thông tin về thời gian và bộ nhớ sử dụng 
    - --ansi: đầu ra là ANSI 
    - --no-ansi: tắt đầu ra là ANSI
    - --version (-V): hiển thị version.
### Exit Codes:
    - 0: OK
    - 1: Lỗi không xác định
    - 2: Lỗi dependency solving
### Init  
Có thể tạo file composer.json một cách thủ công, tuy nhiên cách dễ dàng hơn là dùng lệnh: 
```php composer.phar init```
#### Options:  
    - --name: tên package
    - --description: mô tả  
    - --author: tên tác gỉa
    - --type: loại package
    - --hompage:  homepage của package
    - --require: packge yêu cầu với phiên bản bắt buộc. format `foo/bar:1.0.0`
    - --require-dev: yêu cầu phát triển
    - --stability (-s): gía trị cho trường `minimum-stability`
    - --license(-l): giấy phép của package
    - --repository: cung cấp 1 hoặc nhiều repo. chúng sẽ đưọc lưu trong composer.json 
### Install 
Lệnh `install` đọc file composer.json, bắt các dependencies, cài đặt vào folder `vendor`  
```php composer.phar install```  
Nếu chưa có file composer.json, Composer sẽ khởi tạo sao khi cài dependency
#### Options
    - --prefer-source/--prefer-dist: cài đặt từ `source` hoặc `dist`, phiên bản ổn định mặc định là `dist` 
    - --dry-run: mô phỏng cài thử xem chuyện gì xảy ra
    - --dev: cài đặt theo `require-dev` ( mặc định )
    - --no-dev: tương tự
    - --no-autoloader / --no-scripts / --no-progress / --no-suggest
    - --classmap-authoritative (-a): tự động load class từ class map
### Update
cài phiên bản mới nhất của dependencies và update file `composer.lock`:  
```php composer.phar update```

Chỉ update 1 vài package  
```
php composer.phar update vendor/package vendor/package2
```

Update 1 loạt  
```
php composer.phar update vendor/*
```
#### Óptions ( tương tự update)  

### Require:  
```php composer.phar require
```

### Remove
```
php composer.phar remove vendor/package vendor/package2
```

### Search  
tìm kiếm package
```
php composer.phar search monolog
```

### Show : 
List all of the available packages:  
```
php composer.phar show
```

