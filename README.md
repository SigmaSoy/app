# SigmaSoy

## Overview

Repositori ini berisi materi dan dokumentasi untuk tahap awal perancangan proyek "SigmaSoy" yang bertujuan untuk mengembangkan sistem cerdas untuk memantau kualitas dan kuantitas biji kedelai. Pada tahap ini, fokus utama adalah pengumpulan dan persiapan data, serta perencanaan arsitektur sistem.

## Tujuan Proyek

Tujuan utama proyek ini adalah:

*   Mengembangkan sistem pengawasan kedelai berbasis AI yang mampu secara otomatis mendeteksi dan mengklasifikasikan kualitas biji kedelai (good, broken, moldy).
*   Mengimplementasikan fitur *Visual Question Answering* (VQA) untuk menghitung jumlah biji kedelai.
*   Mengintegrasikan model deteksi dan VQA dengan platform BLIV untuk visualisasi data dan *monitoring*.
*   Mendukung pengambilan keputusan yang lebih baik di seluruh rantai pasok kedelai.
*   Berkontribusi pada kemandirian pangan nasional dengan meningkatkan efisiensi pengelolaan sumber daya kedelai lokal.

## Tahap Awal Perancangan (Tahap Proposal)

Pada tahap ini, kami telah melakukan:

1.  **Identifikasi Masalah:**
    *   Menganalisis permasalahan ketergantungan impor kedelai di Indonesia dan inefisiensi dalam rantai pasok domestik.
    *   Menyoroti pentingnya sistem pengawasan kualitas dan kuantitas biji kedelai yang akurat dan efisien.
2.  **Perumusan Tujuan:**
    *   Menetapkan tujuan yang jelas dan terukur untuk pengembangan sistem.
    *   Mengidentifikasi manfaat sistem bagi berbagai pemangku kepentingan (petani, pedagang, industri, pemerintah).
3.  **Perancangan Solusi:**
    *   Merancang arsitektur sistem yang menggabungkan teknologi AI (*object detection* dan VQA), platform BLIV, dan Google Vertex AI.
    *   Menentukan metode dan algoritma yang akan digunakan untuk pelatihan model.
    *   Memilih model *pretrained* untuk *object detection* (EfficientDet/YOLOv5/8/11) dan VQA (PaLI-Gemma/Florence).
4.  **Pengumpulan Data Awal:**
    *   Mengamankan dataset citra biji kedelai dalam format COCO JSON dari Roboflow.
    *   Memisahkan data menjadi *training*, *validation*, dan *test set*.
    *   Menyiapkan format data yang akan digunakan.

## Gambaran Rangkaian Proyek

Berikut adalah gambaran rangkaian proyek yang akan dilakukan:

1.  **Tahap Proposal (Tahap Ini):**
    *   Identifikasi masalah, perumusan tujuan, perancangan solusi, pengumpulan data awal.
2.  **Pengolahan dan Persiapan Data:**
    *   Melakukan *data cleaning*, *pre-processing*, dan augmentasi data.
    *   Menggunakan fitur *Data Pipeline* BLIV untuk manajemen data.
3.  **Pelatihan Model AI:**
    *   Melatih model *object detection* dan VQA di Vertex AI.
    *   Melakukan *hyperparameter tuning* untuk mengoptimalkan performa model.
    *   Mengevaluasi model dengan metrik yang sesuai.
4.  **Implementasi dan Integrasi:**
    *   Mengintegrasikan model dengan platform BLIV.
    *   Mengembangkan *dashboard* untuk visualisasi data dan monitoring.
    *   Menguji dan memvalidasi sistem secara menyeluruh.
5.  **Deployment dan Peningkatan:**
    *   Melakukan *deployment* sistem yang telah dikembangkan.
    *   Mengumpulkan *feedback* pengguna dan melakukan peningkatan berkelanjutan.

## Struktur Repositori

Berikut adalah struktur *repository* saat ini:
```
├── data/
│ ├── train/ # Data latih
│ │ ├── *.jpg # Citra latih
│ │ └── *.json # File anotasi COCO JSON untuk data latih
│ ├── test/ # Data testing
│ │ ├── *.jpg # Citra uji
│ │ └── *.json # File anotasi COCO JSON untuk data uji
│ ├── valid/ # Data validasi
│ │ ├── *.jpg # Citra validasi
│ │ └── *.json # File anotasi COCO JSON untuk data validasi
├── docs/ # Untuk menyimpan dokumentasi proyek/app
│ └── placeholder
├── model/
│ └── placeholder # File placeholder untuk menyimpan model yang sudah dilatih.
└── README.md # File ini
```
