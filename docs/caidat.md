# Cài đặt Xpenology

Trang này sẽ hướng dẫn bạn cách để bạn tự cài đặt Xpenology lên phần cứng của bạn.

## Lựa chọn phần cứng

Để cài đặt Xpenology, có một số yêu cầu phần cứng tối thiểu cần được đáp ứng. Dưới đây là các yêu cầu phần cứng tối thiểu thông thường để cài đặt Xpenology:

- CPU:CPU hỗ trợ kiến trúc x86 hoặc x86-64. Đa số CPU hiện đại đều tương thích.
- RAM: Tối thiểu 1GB RAM, tuy nhiên, nếu bạn định sử dụng nhiều ứng dụng hoặc dịch vụ, nên có ít nhất 2GB RAM hoặc hơn.
- Ổ cứng: Một ổ cứng để cài đặt Xpenology. Nếu bạn có ý định sử dụng RAID hoặc cung cấp lưu trữ mạng, bạn có thể cần nhiều ổ cứng hơn. Ổ cứng có thể là ổ cứng thông thường (HDD) hoặc ổ cứng rắn (SSD).
- Card mạng: Một card mạng tương thích với Xpenology. Đa số card mạng thông dụng được hỗ trợ.
- Thiết bị USB hoặc ổ đĩa: Bạn sẽ cần một thiết bị USB hoặc ổ đĩa để tạo đĩa khởi động hoặc USB bootable để cài đặt Xpenology.

## Lựa chọn platform

Xpenology có thể chạy trên nhiều loại phần cứng khác nhau. Việc lựa chọn platform nó giống như việc bạn lựa mua phần cứng Synology thật vậy. Nhưng vì phần cứng bạn đã có sẵn, thế nên bạn cần phải lựa chọn platform cho gần giống với phần cứng của bạn nhất. Dưới đây là các platform phổ biến của Xpenology: 

|DSM Platform|DS918+|DS3622xs+|DS920+|DS1621+|DS3617xs|DVA3221|DS3615xs|
|:----------------------------:|-------------------------------------------------------|------------------------------------------------------|------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------|-----------------------------------------------------|-------------------------------------------------|
|Architecture|apollolake|broadwellnk|geminilake|v1000|broadwell|denverton|bromolow|
|QuickSync Transcoding|Yes|No|Yes|No|No|No|No|
|NVMe Cache Support|Yes|Yes|Yes|Yes|Yes (as of 7.0)|Yes|No|
|RAIDF1 Support|No|Yes|No|No|Yes|No|Yes|
|Oldest CPU Supported|Haswell *|any x86-64|Haswell **|any x86-64|any x86-64|Haswell *|any x86-64|
|Max CPU Threads|8|24|8|16|24 (as of 7.0)|16|16|
|Key Note|Nên dùng|Nên dùng cho CPU nhiều core|Nên dùng|AMD Ryzen|DS3622xs+|nVIDIA GPU|DS3622xs+|

Tóm lại, lựa chọn platform chỉ gói gọn trong những ý sau:

- Nếu bạn dùng CPU AMD chọn DS1621+
- Nếu bạn dùng CPU nhiều hơn 8 core, CPU Intel thế hệ thứ 3 hoặc cũ hơn chọn DS3622xs+
- Nếu bạn có gắn GPU GTX 1650 và cần dùng các tính năng AI chọn DVA3221
- Nếu bạn cần 8 license camera cho Surveillance Station chọn DVA1622
- Nếu không có nhu cầu gì đặc biệt, hoặc chạy DSM trong hệ thống ảo hoá chọn DS920+

Sau khi đã lựa chọn được platform hãy ghi nhớ platform phù hợp nhất với phần cứng của bạn để đi vào bước tiếp theo.

## Lựa chọn loader
Để chạy được DSM phiên bản mới nhất (hiện tại đang là DMS 7.2), bạn cần một trong các loader dưới đây: 

### ARC Redpill Loader
Đây là loader được phát triển gần đây nhất, là một bản được phát triển thêm từ ARPL được đề cập bên dưới. Loader này ngoài những tính năng của ARPL nó còn có thêm một số add on hữu dụng.

Download: <https://github.com/AuxXxilium/arc/releases>

### Automated Redpill Loader (ARPL)
Đây là một loader với giao diện build khá dễ sử dụng. 

Download: <https://github.com/fbelavenuto/arpl/releases>

Nhưng ARPL trong thời gian gần đây không còn được cập nhật liên tục và đều đặn, một trong những người phát triển loader này đã fork thành một bản lodaer khác với tên là ARPL i18n. Với những anh em mới bắt đầu với Xpenology mình thấy đây là loader dễ sử dụng và ổn định nhất, mọi người nên chọn loader này để build Xpenology cho mình.

Download: <https://github.com/wjz304/arpl-i18n/releases>

### TinyCore RedPill Loader (TCRP)
Đây là loader đầu tiên được phát triển từ bộ loader Redpill, bạn có thể customize rất nhiều thứ với loader này. Nhưng đổi lại nó lại không có giao diện dễ sử dụng như các loader kể trên. 

Download: <https://github.com/pocopico/tinycore-redpill/releases>

## Cài đặt Xpenology

Đến đây mới là bước quan trọng, thành bại là ở đây.

### Ghi loader ra USB hoặc SSD

Sau khi chọn được 1 trong các loader được giới thiệu ở trên, bạn vào github của loader và download bản release mới nhất của loader đó. File download về thường được nén lại, bạn cần giải nén ra và lấy được file có đuôi .img. 

Tìm một phần mềm ghi file .img ra USB hoặc SSD. Mình hay dùng <https://etcher.balena.io/#download-etcher>(balenaEtcher)