# 🍏 Apple Color Classification using YOLOv8

## 📖 Overview
Proyek ini menggunakan **YOLOv8** untuk mengklasifikasikan warna apel berdasarkan citra. Model ini telah dilatih untuk membedakan apel berdasarkan warna seperti **merah, hijau, dan kuning**. Model ini dapat digunakan dalam industri pertanian atau ritel untuk klasifikasi apel secara otomatis.

---

## 🚀 Features
✅ Deteksi dan klasifikasi warna apel dalam gambar atau video  
✅ Visualisasi hasil deteksi dengan bounding box dan label warna  
✅ Dapat digunakan dalam sistem otomatisasi di bidang pertanian dan ritel  

---

---

## 🛠 Installation

### 1️⃣ Clone Repository
```bash
git clone https://github.com/username/Apple_Color_Classification.git
cd Apple_Color_Classification
```

### 2️⃣ Install Dependencies
Pastikan Python sudah terinstal, lalu jalankan:
```bash
pip install ultralytics opencv-python matplotlib
```

### 3️⃣ Download YOLO Model
Model YOLO yang digunakan harus diunduh terlebih dahulu:
```bash
mkdir models
mv best.pt models/
```

---

## 🖼️ How to Use

### 🔹 Run Classification on an Image
```python
from ultralytics import YOLO
import cv2
import matplotlib.pyplot as plt

model = YOLO("models/best.pt")
image_path = "dataset/apple_sample.jpg"
results = model(image_path)

# Menampilkan gambar hasil deteksi
result_image = results[0].plot()
plt.imshow(cv2.cvtColor(result_image, cv2.COLOR_BGR2RGB))
plt.show()
```

### 🔹 Run Classification on a Video
```python
model = YOLO("models/best.pt")
results = model("dataset/apple_video.mp4", save=True)
```

---

## 📊 Expected Output
Setelah menjalankan kode di atas, Anda akan mendapatkan:
✅ Gambar dengan bounding box dan label warna apel  
✅ Jumlah total apel berdasarkan warnanya  
![Output](https://github.com/Amrina22/apple-color-classification/blob/main/apple-color-classification.jpg)

---

## 📝 Notes
- Pastikan model YOLO telah dilatih dengan dataset yang mencakup berbagai kondisi pencahayaan dan sudut pengambilan gambar.
- Jika klasifikasi kurang akurat, bisa menyesuaikan parameter **confidence threshold** atau melakukan **augmentasi data**.

---

## 🤝 Contributors
- **[Your Name]** - Developer & AI Engineer
- Dataset Referensi: [Apple color](https://universe.roboflow.com/tugas-akhir-70fw5/apel-mrg3l)

Jika Anda ingin berkontribusi, silakan buat **pull request** atau hubungi saya! 🚀

