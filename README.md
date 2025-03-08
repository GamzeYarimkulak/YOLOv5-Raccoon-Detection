# YOLOv5 ile Rakun Tespiti Projesi

Bu repo, YOLOv5 modelini kullanarak **rakun tespiti** üzerine yapılan çalışmaları içermektedir. Proje, nesne tespiti ve görüntü işleme alanında rakunların tespiti için model eğitimi ve değerlendirme süreçlerini kapsamaktadır.

## Proje İçeriği

### 1. Rakun Tespiti
- **Veri Kümesi**: Roboflow'dan alınan rakun veri kümesi kullanılmıştır.
- **Amaç**: Doğal yaşam alanlarında rakunları tespit etmek.
- **Model**: YOLOv5n (Nano) modeli kullanılmıştır.
- **Eğitim Süreci**: 
  - Toplam epoch: 100
  - Batch size: 16
  - Optimizasyon: AdamW

## Kurulum

1. Projeyi klonlayın:
   ```bash
   git clone https://github.com/GamzeYarimkulak/YOLOv5-Raccoon-Detection.git
   cd YOLOv5-Raccoon-Detection
   ```

2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install -r requirements.txt
   ```

3. YOLOv5'i yükleyin:
   ```bash
   git clone https://github.com/ultralytics/yolov5.git
   cd yolov5
   pip install -r requirements.txt
   ```

## Veri Kümesi Hazırlığı
- **Rakun Veri Kümesi**: [Roboflow Raccoon Dataset](https://roboflow.com/) 

Veri kümesi `datasets/` klasörüne yerleştirilmeli ve `train` ile `val` klasörleri oluşturulmalıdır.

## Eğitim

Eğitim sürecini başlatmak için aşağıdaki komutu çalıştırabilirsiniz:
```bash
python train.py --img 640 --batch 16 --epochs 100 --data datasets/raccoon.yaml --weights yolov5n.pt --name raccoon_detection
```

## Sonuçlar
- **mAP@0.5**: %85 (Rakun Tespiti)


## İletişim
Gamze Yarımkulak  
[GitHub](https://github.com/GamzeYarimkulak)  
[LinkedIn](https://www.linkedin.com/in/gamze-yarimkulak-355a6933a/)



