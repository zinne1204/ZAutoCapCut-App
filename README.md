# HƯỚNG DẪN SỬ DỤNG PHẦN MỀM ZAUTOCAPCUT
**Dành cho nhà sáng tạo nội dung & biên tập video**

---

## 🌟 1. GIỚI THIỆU
**ZAutoCapCut** là công cụ giúp bạn tự động dựng các video CapCut hoàn chỉnh chỉ trong vài giây. Bạn không cần phải kéo thả từng bức ảnh, canh chỉnh từng câu phụ đề hay đặt hiệu ứng thủ công nữa.

### ✨ Những việc phần mềm làm tự động cho bạn:
* ✅ **Tự động khớp hình ảnh theo giọng đọc:** Canh chuẩn từng bức ảnh tương ứng với từng câu thoại theo kịch bản.
* ✅ **Tự động tạo chuyển động ảnh (Ken Burns):** Thu phóng, lia góc camera (Zoom in, Zoom out, Pan lên/xuống/trái/phải) giúp video chuyển động mượt mà, cuốn hút.
* ✅ **Tự động tạo phụ đề viền nổi:** Phụ đề hiển thị đẹp mắt, rõ chữ, chống chìm trên mọi nền video.
* ✅ **Hỗ trợ 2 chế độ làm việc:** Dựng từng video lẻ (1-Click) hoặc dựng hàng loạt hàng chục video cùng lúc.
* ✅ **Tích hợp công cụ Xóa Logo / Watermark thông minh:** Tẩy sạch logo hoặc chữ thừa trên ảnh/video.

---

## 📁 2. CHUẨN BỊ THƯ MỤC VIDEO
Để phần mềm tự động nhận diện tất cả trong **1 click**, bạn chỉ cần chuẩn bị một thư mục video chứa các file sau:

```text
📁 Thư_Mục_Video/
├── 🎵 voice.mp3           (File âm thanh giọng đọc: .mp3, .wav, .m4a)
├── 📝 sub-chuan.srt       (File phụ đề: .srt)
├── 📄 scenes.txt          (File kịch bản phân cảnh: mỗi dòng là nội dung 1 ảnh)
└── 🖼️ image/ (hoặc để ảnh trực tiếp trong thư mục)
    ├── 1.jpg
    ├── 2.png
    ├── 3.jpeg
    └── ... (các ảnh theo thứ tự)
```

<details>
<summary><b>🔍 BẤM VÀO ĐÂY ĐỂ XEM CHI TIẾT: "SCENES (KỊCH BẢN PHÂN CẢNH)" LÀ GÌ & CÁCH DÙNG</b></summary>

### 📌 1. Khái niệm cơ bản
* **Scenes (Phân cảnh)** là danh sách các câu thoại / nội dung kịch bản tương ứng với từng bức ảnh hoặc video clip.
* **Quy tắc cốt lõi:** **`1 Scene = 1 Bức ảnh (hoặc 1 Video Clip)`**.

### ⚙️ 2. Cách phần mềm xử lý Scenes thông minh:
1. **So khớp chữ với SRT (Fuzzy Matching):** Phần mềm đọc từng câu trong Scenes và đối chiếu với file phụ đề `.srt` để tìm chính xác mốc thời gian (bắt đầu từ giây thứ mấy đến giây thứ mấy).
2. **Co giãn thời lượng ảnh chuẩn xác:** Bức ảnh tương ứng sẽ hiển thị vừa khớp đúng thời lượng câu thoại đó được đọc.
3. **Tự động lấp khoảng lặng (Smart Gap Filling):** Tự động kéo dài ảnh che kín các khoảng dừng thở giữa các câu, đảm bảo video chuyển động mượt mà, **100% không bao giờ bị đen màn hình**.

### 📝 3. Các định dạng viết Scenes được hỗ trợ:
* **Cách 1 (Đánh số thứ tự - Khuyên dùng):**
  ```text
  1. Ngày xửa ngày xưa ở một ngôi làng nhỏ ven rừng.
  2. Có một chàng tiều phu nghèo sống hiền lành, chất phác.
  3. Một hôm khi đang đốn củi thì lưỡi rìu rơi xuống dòng sông sâu.
  ```
* **Cách 2 (Mỗi câu 1 dòng):**
  ```text
  Ngày xửa ngày xưa ở một ngôi làng nhỏ ven rừng.
  Có một chàng tiều phu nghèo sống hiền lành, chất phác.
  Một hôm khi đang đốn củi thì lưỡi rìu rơi xuống dòng sông sâu.
  ```
* **Cách 3 (Cách nhau bằng dòng trống - Cho đoạn văn dài):**
  ```text
  Ngày xửa ngày xưa ở một ngôi làng nhỏ ven rừng. Người dân nơi đây sống rất yên bình.

  Có một chàng tiều phu nghèo ngày ngày vác rìu đi đốn củi kiếm sống.

  Một hôm khi đang đốn củi thì lưỡi rìu tuột khỏi cán rơi xuống dòng nước xiết.
  ```

### 📁 4. Tên file quy ước để tool tự nhận diện (1-Click):
Đặt tên file kịch bản trong thư mục là một trong các tên: `scenes.txt`, `kichban.txt`, `kịch_bản.txt`, `script.txt`, `prompt.txt`.

</details>

---

## 🚀 3. HƯỚNG DẪN DỰNG 1 VIDEO ĐƠN LẺ (SINGLE MODE)

### 👉 Cách nhanh nhất (1 Click):
1. Mở phần mềm, chọn thẻ **"Dự án đơn lẻ"**.
2. Bấm nút: **`📁 Chọn Thư Mục Dự Án (Tự động điền tất cả các mục bên dưới)`**.
3. Chọn thư mục video bạn đã chuẩn bị.
   - *Phần mềm sẽ tự động nhận diện Tên video, Âm thanh, Phụ đề, Danh sách ảnh và Kịch bản phân cảnh.*
4. Chọn Khung hình mong muốn:
   - **16:9:** Video ngang (YouTube, Facebook...).
   - **9:16:** Video dọc (TikTok, YouTube Shorts, Reels...).
5. Bấm nút màu xanh: **`Tạo Dự Án CapCut`**.
6. Mở phần mềm **CapCut Desktop** lên $\rightarrow$ Dự án đã xuất hiện ngay đầu danh sách, bạn chỉ việc bấm vào để xem lại hoặc xuất video.

---

## ⚡ 4. HƯỚNG DẪN DỰNG HÀNG LOẠT (BATCH MODE)

Khi bạn có nhiều tập phim hoặc nhiều video cần làm cùng lúc (ví dụ 10, 20 hoặc 50 video):

### Cấu trúc thư mục gom chung:
```text
📁 Thu_Muc_Tong/
├── 📁 Video_Tap_01 (chứa voice, srt, scenes, images)
├── 📁 Video_Tap_02 (chứa voice, srt, scenes, images)
├── 📁 Video_Tap_03 (chứa voice, srt, scenes, images)
└── ...
```

### Các bước thực hiện:
1. Chuyển sang thẻ **"Dựng hàng loạt (Batch)"**.
2. Bấm nút: **`📁 Quét thư mục mẹ`** $\rightarrow$ Chọn `Thu_Muc_Tong`.
   - *Toàn bộ các video con sẽ được tự động đưa vào hàng đợi với trạng thái "SẴN SÀNG".*
3. Cài đặt các tùy chọn chung phía dưới (Khung hình, Chuyển động camera, Màu chữ phụ đề...).
4. Bấm nút lớn màu xanh: **`Bắt đầu dựng`**.
5. Phần mềm sẽ tự động tạo lần lượt từng dự án vào CapCut Desktop mà bạn không cần phải thao tác thêm gì.

---

## ✂️ 5. HƯỚNG DẪN TÍNH NĂNG "VOICE SPLITTER" (CẮT VOICE TỰ ĐỘNG BẰNG AI WHISPER)

Nếu bạn có **1 file âm thanh dài** (ví dụ file thu âm voiceover 5-10 phút) và **1 file kịch bản kịch bản**:

### ✨ Ưu điểm vượt trội:
* 🤖 **AI OpenAI Whisper:** Nhận diện mốc thời gian của từng từ phát âm chuẩn xác 100%.
* 🎯 **Sentence Anchor & Silence Snapping:** Tự động định vị điểm đầu và đuôi câu, tự động tìm điểm giữa của khoảng lặng để cắt file, **đảm bảo 100% không nuốt chữ, không giật tiếng hay bị lặp âm**.
* 📁 **Tự động đánh số thứ tự:** Xuất ra các file `1.wav`, `2.wav`, `3.wav`... sẵn sàng cho tính năng Voice Sync.

### Các bước thực hiện:
1. Bấm vào biểu tượng **"Voice Splitter"** (hình chiếc kéo ✂️ trên thanh bên trái).
2. **Chọn File voice gốc:** Chọn file thu âm giọng đọc dài (`.mp3`, `.wav`, `.m4a`).
3. **Chọn Thư mục xuất file voice:** Chọn thư mục bạn muốn lưu các đoạn voice nhỏ sau khi cắt.
4. **Nhập Kịch bản hoặc SRT:**
   * Dán nội dung các câu phân cảnh vào ô kịch bản (mỗi câu 1 dòng).
   * Hoặc chọn chế độ **Khớp theo phụ đề SRT** nếu bạn đã có sẵn file `.srt`.
5. **Cài đặt AI & Định dạng:**
   * **Mô hình Whisper:** `base` (Khuyên dùng - cân bằng tốc độ và độ chuẩn).
   * **Ngôn ngữ:** `Tiếng Việt (vi)` hoặc `Tự động nhận`.
   * **Định dạng xuất:** Chọn **`wav (Khuyên dùng)`** để có chất lượng âm thanh 100% không độ trễ nén và hiển thị sóng âm tức thì trong CapCut.
6. Bấm **`🔍 PHÂN TÍCH & XEM TRƯỚC`** để kiểm tra danh sách câu thoại và mốc thời gian.
7. Bấm **`✂️ BẮT ĐẦU CẮT VOICE`** $\rightarrow$ Phần mềm sẽ cắt ra toàn bộ các file voice lẻ mượt mà trong vài giây!

---

## 🎙️ 6. HƯỚNG DẪN TÍNH NĂNG "VOICE SYNC" (ĐỒNG BỘ THEO TỪNG ĐOẠN VOICE)

Nếu bạn chia kịch bản bằng **từng file voice riêng lẻ** (ví dụ: `1.wav`, `2.wav`, `3.wav`...) và **từng bức ảnh tương ứng** (`Images_01.png`, `Images_02.png`...):

### Cách hoạt động:
* Phần mềm tự động ghép cặp từng bức ảnh với từng đoạn voice có cùng số thứ tự.
* Trên timeline CapCut, mỗi bức ảnh sẽ tự động **kéo dài đúng bằng thời lượng file voice** tương ứng.

### Các bước thực hiện:
1. Bấm vào biểu tượng **"Voice Sync"** (hình nốt nhạc 🎵 trên thanh bên trái).
2. **Chọn thư mục ảnh/video:** Chọn thư mục chứa toàn bộ ảnh của bạn.
3. **Chọn thư mục voice:** Chọn thư mục chứa toàn bộ các file âm thanh voice lẻ (vừa cắt từ Voice Splitter).
4. **Kiểm tra & Xem trước:** Bấm nút **`🔍 KIỂM TRA & XEM TRƯỚC`** để xem bảng phân cảnh hiển thị chi tiết: `STT | Tên ảnh | Tên file voice | Thời lượng | Vị trí timeline`.
5. Tùy chỉnh kiểu chuyển động camera (Zoom in, Zoom out, Pan góc...) và cường độ mong muốn.
6. Bấm nút **`🚀 TẠO PROJECT CAPCUT`** $\rightarrow$ Timeline hoàn chỉnh sẽ được tạo ngay lập tức!
7. *(Hỗ trợ cả chế độ Dựng hàng loạt Batch cho Voice Sync nếu bạn có nhiều thư mục video con).*

---

## 🎨 7. TÙY CHỈNH HIỆU ỨNG VIDEO

### 1. Phụ Đề (Subtitles):
* **Màu sắc:** Bạn có thể chọn màu Vàng, Xanh, Trắng, Hồng... để làm nổi bật phụ đề.
* **Cỡ chữ & Kiểu chữ:** Tùy chỉnh độ to nhỏ (mặc định 7.0) và bật in đậm/viền chữ để chữ luôn nổi rõ.
* **Vị trí hiển thị:** Đặt ở dưới chân màn hình, giữa màn hình hoặc tầm trung.

### 2. Chuyển Động Camera (Keyframe):
* Tích chọn **"Bật chuyển động ngẫu nhiên"**: Phần mềm sẽ tự động phối hợp nhiều kiểu chuyển động (Zoom vào, Zoom ra, Lia góc lên/xuống/trái/phải) để video sinh động như phim.

### 3. Chuyển Cảnh (Transitions):
* Tích chọn các kiểu hiệu ứng chuyển cảnh bạn thích (nhạt dần, trượt sang, chuyển cảnh đen...) và bật **"Ngẫu nhiên chuyển cảnh"** để cảnh quay tự nhiên hơn.

### 4. Xóa Watermark AI (Tự Động Nhận Diện & Tẩy Logo):
* Bật công tắc **"✨ Xóa watermark AI (Tự động nhận diện)"** trên màn hình Khớp SRT hoặc Voice Sync.
* Phần mềm sẽ tự động quét từng ảnh và video, nhận diện các logo mờ, chữ watermark, sparkle (Gemini, Veo...) và tẩy xóa sạch sẽ bằng AI Inpainting tăng tốc GPU trước khi đưa vào CapCut.
* Các file sạch được tự động lưu và cache trong thư mục `_cleaned_wm`, giúp tối ưu tốc độ cho những lần dựng tiếp theo.

---

## 🔍 8. HƯỚNG DẪN TÍNH NĂNG "UPSCALE AI" (NÂNG NÉT & PHÓNG TO ẢNH BẰNG AI)

Nếu bạn có những bức ảnh chất lượng thấp, ảnh mờ, vỡ hạt hoặc kích thước nhỏ (512x512, 720p) và muốn nâng cấp lên chuẩn 1080p, 2K hoặc 4K siêu sắc nét:

### ✨ Ưu điểm vượt trội:
* 🚀 **7 Mô hình AI chuyên dụng:** Hỗ trợ đầy đủ từ siêu nhẹ đa dụng (`upscayl-lite-4x`), tranh vẽ 2D/Anime (`digital-art-4x`), ảnh AI Midjourney (`ultrasharp-4x`), chi tiết bề mặt (`remacri-4x`) đến ảnh chụp thực tế (`upscayl-standard-4x`).
* ⚡ **Tăng tốc GPU Vulkan:** Chạy mượt mà trên mọi loại card đồ họa NVIDIA, AMD Radeon, Intel Arc / Iris Xe / UHD Graphics và CPU đa luồng.
* 🎚️ **Xem trước tương tác Before / After Slider:** Kéo thanh trượt so sánh trực tiếp độ sắc nét của ảnh trước và sau khi upscale.

### Các bước thực hiện:
1. Bấm vào biểu tượng **"Upscale AI"** (hình mũi tên mở rộng ⤢ trên thanh bên trái).
2. **Kéo thả ảnh hoặc bấm `Chọn file` / `Chọn thư mục`:** Thêm danh sách các ảnh cần nâng nét (tối đa 50 ảnh/lần).
3. **Chọn Cấu hình:**
   * **Mô hình AI:** Chọn 1 trong 7 model phù hợp (Rê chuột vào nút `❓ Hướng dẫn chọn Model` để xem bảng so sánh).
   * **Tỉ lệ phóng to (Scale):** Chọn `2x (200%)`, `3x (300%)` hoặc `4x (400% - Khuyên dùng)`.
   * **Cài đặt nâng cao (`⚙️ Cài đặt`):** Chọn định dạng xuất (PNG, JPG, WEBP), kích thước Tile chống tràn VRAM hoặc bật TTA Mode khử nhiễu 8x.
4. Bấm nút **`🚀 BẮT ĐẦU NÂNG NÉT ẢNH (UPSCALE AI)`**.
5. Bấm vào bất kỳ ảnh nào trong danh sách kết quả bên phải để kéo thanh trượt so sánh độ nét chi tiết Before / After!

---

## 💡 9. MẸO & LƯU Ý KHI SỬ DỤNG

> [!TIP]
> **1. Hãy đóng ứng dụng CapCut trước khi bấm Tạo Dự Án:**
> Để CapCut không khóa dự án khi phần mềm đang lưu dữ liệu mới, bạn nên tắt CapCut Desktop trước khi bấm "Tạo Dự Án". Sau khi phần mềm thông báo hoàn tất, hãy mở CapCut lên.

> [!TIP]
> **2. Mở CapCut lên là có sẵn dự án:**
> Tất cả các video sau khi tạo xong đều tự động xuất hiện ở vị trí đầu tiên trong danh sách dự án gần đây của CapCut Desktop.

> [!NOTE]
> **Công cụ Xóa Watermark độc lập:** Nếu bạn cần xóa watermark chuyên biệt cho hàng loạt ảnh/video độc lập không qua CapCut, vui lòng tham khảo tài liệu [HUONG_DAN_ZWATERMARK.md](file:///d:/ytb/tools/my-auto-capcut/myautocapcut/HUONG_DAN_ZWATERMARK.md) hoặc chạy `python app_watermark.py`.

---

**Chúc bạn tạo ra thật nhiều video triệu view nhanh chóng và dễ dàng với ZAutoCapCut!** 🎬🚀
