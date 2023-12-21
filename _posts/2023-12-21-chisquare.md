---
layout:       post
title:        ""
author:       "Şuheda Karabudak"
header-style: text
catalog:      true
tags:
    - Veri
    - Rutin
    - Stres
    - Alışkanlık
---


![Neutral Beige Minimalist Company Organizational Chart](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/21033f81-866f-42d2-99c8-e9cd556341d9)

> Bu yazımda,istatistiksel testlerden ki-kare dağılımından bahsedeceğim.

Ki-Kare Dağılımı
--
İstatistikte önemli diğer bir sürekli dağılım ki-kare dağılımıdır.Normal dağılım istatistikte önemli bir dağılım olduğu için,normal dağılımlı kitlelerden alınan örneklemler üzerinden tanımlı istatistiklerin örneklem dağılımları çok önemlidir.Normal dağılımdan alınan örneklemler için en çok kullanılan örneklem dağılımlarından biri de **ki-kare** dağılımıdır.

Ki-kare Dağılımın Özellikleri Ve Varsayımları
--

- Ki kare değişkeni 0 ile sonsuz arasında dağılım gösteren tek taraflı bir değişkendir.
- Ortalaması μ ve standart sapması σ olan normal dağılan bir popülasyondan çekilen her bir değeri X değeri için (X-μ)/σ şeklinde hesaplanark k tane bağımsız Z değerinin karelerinin toplamının gösterdiği dağılı ki-kare dağılımı oluşur.
![Screenshot from 2023-12-21 14-28-41](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/a271af0e-2a2d-47c2-bb24-9667f525e0cf)

- Gruplar bibirinden bağımsız olmalıdır.BAğımlı gruplara ki-kare testi yerine Mc-Nemar testi uygulanır.
- Ki kare dağılımı süreklidir.Beklenen frekanslardan herhangi biri 5'den küçük ise dağılım kesikli ya da çarpık olur.Bu yüzden test sonucu elde edilen ki-kare değeri ki-kare dağılımına uygunluk göstermez. Böyle durumlarda aşağıdaki yollar uygulanır.
  
   - **2x2 çapraz tablo:** Fisher'in kesin ki-kare testi

   - **2xc,rx2 ya da rxc çapraz tablo:** Ki-kare testi uygulamak isteniyorsa satır ya da sütun birleştirilerek 5'den küçük değerin ortadan kaldırılmasına çalışılır.

![](https://ars.els-cdn.com/content/image/3-s2.0-B9780120887705500678-f28-03-9780120887705.jpg)

Ki-kare Dağılımını Hangi Durumlarda Kullanırız ?
--

- Değişkenlerin tümü kategorik olduğunda
  
- Bağımsızlık kontrolü
  
- Gruplar arası fark konrtolü
  
- Uyum iyiliği testi

Ki-kare Testinin Uygulanması
--
Nitel yapıdaki iki değişkenin birlikte dağılımını veren RxC boyutlu çapraz tabloların analizinde  ki-kare testi uygulanmaktadır.Burada R(r) satırdaki değişkenin düzey sayısını C(c) ise sütundaki değişkenin düzey sayısını ifade etmektedir.
RxC boyutlu çapraz tabloların analizinde araştırmanın hedefine bağlı olarak iki temel analiz söz konusudur.Bunlardan **1.Bağımsızlık Kontrolü**, **2.Gruplar Arası Fark Kontrolüdür**

Bağımsızlık kontrolünde,satır ve sütun değişkenler arasında ilişkinin analizi söz konusu iken,gruplar arası fark kontrolünde bir değişken bakımından diğer değişkenin düzeyleri arasında fark olup olmadığı incelenmektedir.Bu iki analiz arasındaki farklılıklar olsa da iki analizde de aynı ki-kare testi kullanılmaktadır.Farklılıklar kurulacak olan Ho hipotezi ve Ho reddedilği takdirde izlenecek olan yoldur.


