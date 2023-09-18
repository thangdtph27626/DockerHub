# Tìm hiểu Docker hub

Chúng ta có thể coi Docker Hub như một dịch vụ của Docker để định vị và phân phối các container cho từng image trong nhóm được chỉ định. Đây là kho lưu trữ hình ảnh vùng chứa toàn diện nhất, với thứ tự của tất cả các nguồn nội dung, bao gồm các dự án nguồn mở, phát triển việc chia sẻ mã nguồn ứng dụng và các nhà phát triển cộng đồng sử dụng vùng chứa .


## Docker Hub là gì?
Docker Hub là Docker Registry, phiên bản được lưu trữ trên đám mây, ứng dụng phía máy chủ mã nguồn mở, có thể mở rộng và không trạng thái. Nó có thể quản lý việc chia sẻ và lưu trữ hình ảnh Docker . Bằng cách sử dụng Docker, các nhà phát triển có thể truy cập nó dưới dạng công khai và tạo không gian kho lưu trữ riêng của họ cũng như tự động hóa các chức năng, nhóm làm việc và webhooks xây dựng ứng dụng tùy chỉnh.

Ví dụ: nhà phát triển được đào tạo DevOps có thể tải xuống hình ảnh vùng chứa hệ thống cơ sở dữ liệu hướng tài liệu MongoDBSQL chính thức từ Docker Hub để thực hành trên một ứng dụng được triển khai trong các vùng chứa.

## Tính năng của Docker Hub

- Repositories: Nó chứa quy trình Đẩy và Kéo cho hình ảnh vùng chứa.
- Teams and Organizations: Nó cho phép nhà phát triển/người dùng truy cập vào kho lưu trữ riêng tư của hình ảnh vùng chứa. 
- Docker Official Images: Nó kéo và sử dụng hình ảnh vùng chứa chất lượng tiêu chuẩn cao do Docker hiển thị.
- Docker Verified Publisher Images: Nó kéo và sử dụng hình ảnh vùng chứa chất lượng tiêu chuẩn cao được cung cấp bởi các nhà cung cấp bên ngoài.
- Builds: Nó cung cấp các cơ chế tự động tạo hình ảnh vùng chứa từ Bitbucket và GitHub và đẩy chúng đến Docker Hub.
- Webhooks: Nó kích hoạt một số hành động nhất định sau khi đẩy thành công vào vùng chứa để kết hợp Docker Hub với các dịch vụ bổ sung.
- Docker triển khai công cụ Docker Hub CLI hiện đang ở giai đoạn thử nghiệm và API (Dịch vụ vi mô) cho phép bạn giao tiếp với Docker Hub. Bạn có thể duyệt tài liệu API Docker Hub để tìm kiếm các điểm cuối chuẩn bị.

##  Tạo kho lưu trữ đầu tiên
Dưới đây là các bước sau xác định các tính năng từng bước để tạo kho lưu trữ đầu tiên: 

### Bước 1: Tạo ID Docker của bạn
Để chia sẻ hình ảnh trên Docker Hub, ID Docker cung cấp cho bạn quyền truy cập và truy cập vào kho lưu trữ của Docker Hub, đồng thời cho phép bạn tìm kiếm hình ảnh từ cộng đồng Docker và nhà xuất bản đã được xác nhận. 
### Bước 2: Tạo kho lưu trữ đầu tiên của bạn
Để tạo một kho lưu trữ:
Vui lòng đăng nhập vào Docker Hub.
Nhấp vào tùy chọn Tạo kho lưu trữ trên trang chào mừng của Docker Hub.
Đặt tên là <your-username>/my-testprivate-repo.
Đặt chế độ hiển thị là Riêng tư theo ảnh chụp màn hình bên dưới.

![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/30a5d447-154b-47b9-ab46-8ddac4625ef2)

Bấm vào tùy chọn Tạo.
Và bạn có thể thấy kho lưu trữ đầu tiên do chính bạn tạo.

### Bước 3: Cài đặt và tải xuống Docker Desktop
Để cài đặt và tải xuống Docker Desktop để đẩy và xây dựng hình ảnh vùng chứa vào Docker Hub:

Cài đặt và tải xuống Docker Desktop. Nếu bạn muốn làm điều đó trong Linux, hãy tải xuống Docker Engine.
Sau đó đăng nhập vào ứng dụng Docker Desktop với sự trợ giúp của ID Docker (như được tạo ở Bước 1).

### Bước 4: 
Đẩy và Xây dựng hình ảnh vùng chứa tới Docker Hub từ hệ thống của bạn.
Tạo Dockerfile và xác định nó vào ứng dụng của bạn theo lệnh dưới đây:
      # cú pháp=docker/dockerfile:1

TỪ hộp của bạn

CMD echo "Xin chào thế giới! Đây là hình ảnh Docker đầu tiên."

Chạy docker build -t <your_username>/my-private-repo để tạo hình ảnh Docker của bạn.
Chạy cái này bên dưới docker:
chạy <your_username>/my-private-repo và kiểm tra hình ảnh Docker của bạn cục bộ.

Vui lòng chạy docker push <your_username>/my-private-repo để đẩy hình ảnh Docker đã tạo của bạn lên Docker Hub.
Sau kho lưu trữ trên theo cú pháp Docker Hub, nó sẽ hiển thị và chạy thành công và tạo một thẻ mới trong Thẻ.
Bây giờ hãy đăng ký tài khoản Docker để tạo kho lưu trữ đầu tiên của bạn.
Bây giờ đã xây dựng hình ảnh vùng chứa Docker trên hệ thống của bạn
Và đẩy nó thành công vào Docker Hub


## Khám phá các image

Trong Docker, chúng ta có thể tìm kiếm hình ảnh bằng cách sử dụng lệnh docker search, lệnh này giúp và lấy hình ảnh tìm kiếm từ kho lưu trữ docker công cộng. 

Trong lệnh docker search, chúng ta có từ khóa TERM để định vị và tìm những hình ảnh khớp với TERM được chỉ định.

Ví dụ: lệnh sau sẽ định vị hình ảnh từ BusyBox 

hình ảnh.

docker tìm kiếm busybox

Sau khi chạy lệnh trên theo ảnh chụp màn hình bên dưới, nó sẽ hiển thị đầu ra với mô tả chi tiết và số sao cũng như trạng thái của hình ảnh là chính thức hoặc tự động.
![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/dbd3f65a-6664-4d56-9fcf-270386490cba)


## Tìm kiếm Docker
Để được trợ giúp tìm kiếm Docker, hãy nhập lệnh bên dưới:

> docker search --help

Tìm kiếm cụm từ 'ubuntu':

> docker search ubuntu

Tìm kiếm Hình ảnh Ubuntu; nó sẽ hiển thị hình ảnh chính thức:

> docker search --filter=is-official=true ubuntu

Đầu ra:
![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/3740a9f1-6d80-4a63-8cec-d8af48febf11)

## Tạo một image

Để tạo hình ảnh Docker, chúng ta cần bắt đầu với hình ảnh hiện có. Chúng ta có thể tùy chỉnh và thay đổi nó theo kịch bản và tạo một hình ảnh mới.

Làm thế nào nó hoạt động?
- Đầu tiên, chúng ta cần khởi tạo hình ảnh cơ sở chính hoặc xác định docker để tạo vùng chứa từ bên trong hình ảnh.
- Sau đó, chúng ta cần cài đặt Docker.
- Tiếp theo, chúng ta cần lấy image cơ sở như webdevops/php-nginx mà chúng ta có thể định vị trong kho Docker Hub - để “kéo” nó, chúng ta cần có ID Docker Hub. Nếu chưa tạo chúng ta có thể tham khảo https://hub.docker.com và tạo tài khoản miễn phí.
- Sau đó đi đến dòng lệnh nơi chúng tôi đã cài đặt Docker và đăng nhập vào Docker Hub:
Cú pháp:

![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/e525c78a-e97f-4ee5-9062-af1779432159)

- Ở đây, chúng ta bắt đầu với image cơ sở và tham khảo Docker để khởi động một container. 
- Hình ảnh docker cung cấp cho webdevops/php-dev một daemon apache chạy trên các cổng 80 và 443.
- Ở đây, cờ -dP xác định cách lấy và đặt vùng chứa, đồng thời nó chạy ở chế độ nền.
![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/834b5020-0455-489d-a685-6969e8da2587)
-Vùng chứa chạy thành công, như minh họa trong hình ảnh đầu ra bên dưới.
![image](https://github.com/thangdtph27626/DockerHub/assets/109157942/f28bb06e-c559-45a2-b2ea-c6944b467ffa)

## Push một Image 

Để đẩy một hình ảnh hoặc kho lưu trữ, dưới đây là cú pháp và các bước chúng ta cần tuân theo:

Sử dụng tính năng đẩy hình ảnh docker, chúng ta có thể chia sẻ hình ảnh từ Docker Hub.

Đẩy một hình ảnh mới vào sổ đăng ký
Đầu tiên, lưu trữ hình ảnh mới nhất bằng cách lấy ID vùng chứa và đặt tên ban đầu của nó. 

Theo tiêu chuẩn, chúng ta chỉ cần tuân theo a-z0-9-_. được phép khi chọn hình ảnh:

Cú pháp
> docker container commit c16378f943fe rhel-httpd:latest
Trong lệnh này, chúng tôi cung cấp cổng 5000 với thông tin chi tiết về tên máy chủ và địa chỉ IP

> docker image tag rhel-httpd:latest registry-host:5000/myadmin/rhel-httpd:latest
> docker image push registry-host:5000/myadmin/rhel-httpd:latest

Dưới đây là lệnh để kiểm tra xem nó hoạt động như thế nào sau khi chạy:

Đẩy tất cả các thẻ của một hình ảnh
Tùy chọn -a (hoặc --all-tags) để đẩy tất cả các thẻ của hình ảnh cục bộ phải là tùy chọn ưu tiên.

Ví dụ sau tạo nhiều thẻ cho một hình ảnh và đẩy tất cả các thẻ đó vào Docker Hub.

 > docker image tag myimage registry-host:5000/testname/testimage:latest
 > docker image tag myimage registry-host:5000/testname/testimage:v1.0.1
 > docker image tag myimage registry-host:5000/testname/testimage:v1.0
 > docker image tag myimage registry-host:5000/testname/testimage:v1
