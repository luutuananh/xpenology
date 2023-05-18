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

| DSM Platform|DS918+|DS3622xs+ |DS920+|DS1621+ |DS3617xs |DVA3221|DS3615xs |
|:----------------------------:|-------------------------------------------------------|------------------------------------------------------|------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------|-----------------------------------------------------|-------------------------------------------------|
| Architecture|apollolake |broadwellnk |geminilake|v1000 |broadwell|denverton|bromolow |
| Drive Slot Mapping |sataportmap\
diskidxmap|sataportmap\
diskidxmap |device tree |device tree|sataportmap\
diskidxmap |sataportmap\
diskidxmap|sataportmap\
diskidxmap |
|QuickSync Transcoding |Yes |No |Yes|No|No |No|No |
|NVMe Cache Support|Yes |Yes|Yes|Yes |Yes (as of 7.0) |Yes |No |
|RAIDF1 Support|No|Yes|No |No|Yes|No|Yes|
| Oldest CPU Supported |Haswell *|any x86-64|Haswell **|any x86-64|any x86-64|Haswell *|any x86-64|
| Max CPU Threads|8 |24 |8|16|24 (as of 7.0)|16|16 |
| Key Note|currently bestfor most users |best for verylarge installs |see slot mappingtopic below |AMD Ryzen, seeslot mapping topic |obsoleteuse DS3622xs+|AI/Deep LearningnVIDIA GPU |obsoleteuse DS3622xs+| 


## Lựa chọn loader

## Cài đặt Xpenology