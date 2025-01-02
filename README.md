# Araç Takip ve Hız Ölçme Projesi

Bu proje, video üzerinden araç takibi yapmak ve bu araçların hareketlerini izlemek, hızlarını hesaplamak üzerine tasarlanmıştır. Çalışma, YOLO modelini kullanarak nesne algılama, byte tracking algoritmasıyla nesne takibi ve geometrik dönüşümler ile özelleştirilmiş çözümler sunar.

---
## Yapılanlar
- **YOLO ile Nesne Algılama**: YOLO modelini kullanarak videodaki araçlar algılandı.
- **Araç Takibi**: ByteTrack algoritması ile her bir araç takip edildi.
- **Hız Hesaplama**: Araçların belirli bir zaman içerisinde katettiği mesafeden hız tahmini yapıldı.
- **İz Çizgisi (Trace)**: Her bir araç için izleme (trace) çizgileri oluşturuldu.
- **Dönüştürülmüş Perspektif**: Perspektif dönüştürülmesiyle araçların belirli bir geometriye uygun hale getirilmesi sağlandı.

---

## Ekran Görüntüsü
Aşağıda uygulama çalışırken alınan bir ekran görüntüsü bulunmaktadır:

Araç Takip Ekran Görüntüsü
![Hıız Testi](https://github.com/user-attachments/assets/4e3429ca-db3d-4e54-8830-41339c43dc90)


---
## Proje Amacı
Bu projenin amacı:
1. **Araç takibi** yapmak ve videodaki araçları belirlemek.
2. Araç hızlarını tahmin ederek hızını etiketlemek.
3. Araç hareketlerini izleyen bir izleme (trace) sistemi oluşturmak.

---

## Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki yazılımlar ve kütüphaneler gereklidir:

- **Python 3.8+**
- OpenCV
- NumPy
- Ultralytics YOLO
- yolov8n
- Supervision
- ByteTrack

Gereksinimleri kurmak için:
```bash
pip install opencv-python-headless numpy ultralytics supervision

## Kullanım
1. Videonuzu proje dizinine `"vehicles.mp4"` adıyla yerleştirin.
2. Kodda bulunan **SOURCE** ve **TARGET** koordinat ayarlarını, videonuza uygun olacak şekilde ayarlayın.
3. Projeyi çalıştırmak için aşağıdaki kodu çalıştırın:
   ```bash
   python main.py
