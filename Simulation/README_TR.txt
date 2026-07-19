XL7015 LTspice dosyaları

1) XL7015.lib ve XL7015.asy dosyalarını, devrenizin .asc dosyasıyla aynı klasöre koyun.
2) LTspice'ı kapatıp yeniden açın.
3) F2 -> Top Directory açılır menüsünden proje klasörünü seçin.
4) XL7015 sembolünü yerleştirin.
5) Şemaya şu komutu ekleyin:
   .include XL7015.lib

Pin sırası:
1 VIN
2 SW
3 GND
4 FB
5 EN

5 V örnek dış devre:
VIN: 24 V
CIN: 33uF (VIN-GND)
L1: 100uH (SW-VOUT)
D1: S310, anot GND, katot SW
COUT: 100uF (VOUT-GND)
R2: 10k (VOUT-FB)
R1: 3.3k (FB-GND)
CFF: 33nF (VOUT-FB)
EN: GND
Yük: örneğin 50 ohm (yaklaşık 100 mA)
Transient: .tran 0 30m 0 100n startup

Not:
Bu dosya resmi üretici modeli değildir. Temel PWM ve regülasyon davranışını görmek
için hazırlanmış basitleştirilmiş eğitim modelidir; gerçek verim, geçici rejim,
korumalar ve kararlılık doğrulaması için datasheet ölçümleri esas alınmalıdır.
