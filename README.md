# Sorting Algorithm Performance Benchmark System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 🎯 Proje Amacı

Bu proje, 5 temel sıralama algoritmasının (Quick, Merge, Heap, Shell, Radix) teorik karmaşıklıklarını pratik performans ölçümleriyle karşılaştıran bir analiz platformudur. **Big-O notasyonunun** gerçek dünya verileri (Random, Reverse, Partial) üzerindeki yansımalarını analiz eder.

## 🚀 Özellikler

- **Hybrid Quick Sort:** Küçük veri setlerinde Insertion Sort'a geçen optimize edilmiş yapı.

- **Knuth Shell Sort:** $O(n^{1.5})$ karmaşıklığı için Knuth Sequence kullanımı.

- **Memory Efficient Merge Sort:** Slicing yerine indeks tabanlı bellek yönetimi.

- **Robust Radix Sort:** Negatif sayıları destekleyen özel implementasyon.

- **Gerçek Zamanlı Analiz:** `tracemalloc` ve `time.perf_counter` ile mikrosaniye hassasiyetinde ölçüm.

## 📊 Benchmark Metodolojisi

Sistem aşağıdaki parametrelerde stres testi uygular:

| Parametre | Değerler |
|-----------|----------|
| **Veri Boyutu** | 1.000, 10.000, 100.000 |
| **Veri Tipi** | Random, Reverse Sorted, Partially Sorted |
| **Tekrar Sayısı** | Her test için 3 koşum ortalaması (Noise reduction) |

## 🛠 Kurulum ve Çalıştırma

> 💡 **Hızlı Başlangıç:** Detaylı adım adım kılavuz için `QUICK_START.md` dosyasına bakın.

1. **Virtual Environment Oluşturun (Önerilen):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # macOS/Linux
   # veya
   venv\Scripts\activate  # Windows
   ```

2. **Bağımlılıkları Yükleyin:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Benchmark'ı Başlatın (Backend):**

   ```bash
   python main.py
   ```

   Sonuçlar `results/` klasörüne CSV olarak kaydedilir.

4. **Arayüzü Açın (GUI):**

   ```bash
   python gui/app.py
   ```

**Not:** macOS'ta Homebrew Python (`/opt/homebrew/bin/python3`) kullanıyorsanız, tkinter desteği için sistem Python'unu (`/usr/local/bin/python3`) kullanmanız önerilir.

## 📈 Sonuçlar (Özet)

- **Hız Şampiyonu:** Radix Sort (Integer verilerde).
- **Stabilite:** Merge Sort (Her senaryoda tutarlı).
- **Bellek Verimliliği:** Iterative Heap Sort.

---

**Geliştirici:** Berna | Computer Engineering Senior Student

