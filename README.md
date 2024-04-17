Chúng tôi cung cấp một tập lệnh dự đoán có thể chuyển đổi một tệp âm thanh cụ thể hoặc thậm chí là một danh sách các tệp âm thanh. Hãy xem xét các đối số dưới đây, đặc biệt là đối số ```-f TEST_FILEPATH``` và đối số ```-s HUGGINGFACE_FOLDER```:
```cmd
sử dụng: inference.py [-h] -f TEST_FILEPATH [-s HUGGINGFACE_FOLDER] [-d DEVICE_ID]

CÁC ĐỐI SỐ DỰ ĐOÁN ASR

tuỳ chọn đối số:
  -h, --help            Hiển thị trợ giúp này và thoát
  -f TEST_FILEPATH, --test_filepath TEST_FILEPATH
                        Có thể là đường dẫn đến tệp âm thanh của bạn (.wav, .mp3) hoặc một tệp văn bản (.txt) chứa danh sách các đường dẫn tệp âm thanh.
  -s HUGGINGFACE_FOLDER, --huggingface_folder HUGGINGFACE_FOLDER
                        Thư mục bạn lưu trữ các tệp huggingface.Lựa chọn giữa "DuyTa/ZH_Hanzi" và "DuyTa/ZH_pinyn"

  -d DEVICE_ID, --device_id DEVICE_ID
                        Thiết bị bạn muốn kiểm tra mô hình của mình trên nếu CUDA có sẵn. Nếu không, sử dụng CPU. Giá trị mặc định: 0
```
# Chuyển văn bản từ một tệp âm thanh(Pinyin mode):
```cmd
python inference.py \
    -f path/to/your/audio/file.wav(.mp3) \
    -s DuyTa/ZH_pinyn

# output example:
>>> transcript: nà shì kāi shuō kǒu lìng
```
# Chuyển văn bản từ một tệp âm thanh(Hanzi mode):
```cmd
python inference.py \
    -f path/to/your/audio/file.wav(.mp3) \
    -s DuyTa/ZH_Hanzi
```


# Chuyển văn bản từ một tệp các file âm thanh :
```cmd
python inference.py \
    -f path/to/your/new.txt \
    -s DuyTa/ZH_Hanzi hoặc (DuyTa/ZH_pinyn)
```