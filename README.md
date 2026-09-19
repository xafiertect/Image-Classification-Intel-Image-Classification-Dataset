# Image Classification — Intel Image Classification Dataset

## Deskripsi
Model klasifikasi gambar CNN Sequential untuk mengklasifikasikan 6 kategori pemandangan:
buildings, forest, glacier, mountain, sea, street.

## Dataset
Intel Image Classification (Kaggle). Seluruh gambar dari folder bawaan `seg_train` dan `seg_test`
digabungkan terlebih dahulu, lalu displit ulang secara mandiri (stratified, seed=42) menjadi:
- Train: 80%
- Validation: 10%
- Test: 10%

Total gambar gabungan: 17034
Total gambar test (hasil split mandiri): 1709

## Arsitektur Model
CNN Sequential dengan 4 blok Conv2D + MaxPooling2D, diikuti Flatten, Dense, Dropout, dan Softmax output.

## Hasil
- Train Accuracy: 86.39%
- Test Accuracy: 87.30%

## Format Model
- SavedModel: `saved_model/`
- TensorFlow Lite: `tflite/model.tflite` (label di `tflite/label.txt`)
- TensorFlow.js: `tfjs_model/`

## Cara Menjalankan
1. Install dependencies: `pip install -r requirements.txt`
2. Load model sesuai format yang dibutuhkan (SavedModel/TFLite/TFJS)
