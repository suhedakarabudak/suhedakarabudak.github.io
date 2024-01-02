---
layout: post
title: "Ki-Kare Testi"
subtitle: "Veri Dünyasında Bir Adım Öteye: İstatistiksel Ki-Kare Testi 🤓📊"
author: "Şuheda Karabudak"
header-style: text
tags:
  - Data Science
  - Veri
  - Dijital Hayat
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

**Ki-kare testi formulü:**

![Screenshot from 2023-12-27 13-22-58](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/3a19a2df-b47e-4ba2-921b-b77e42e2539d)

**1.RxC Çapraz Tablolarda Bağımsızlık Kontrolü:**
- Çapraz tabloda bir kitleden alınan bir örneklemin düzeylere göre incelenmesinden oluşuyor ise bağımsızlık kontrolü yapılır.
- Test süreci, gruplar arası fark kontrolü ile aynıdır.Ancak hipotez ifadeleri değişir.
- **Hipotezler**
  
                 Ho: Değişkenler arasında ilişki yoktur.
  
  
                 H1: Değişkenler arasında ilişki vardır.
  
biçiminde kurulur.Testin diğer adımları aynıdır.Eğer test sonucu hipotez reddedilirse yani incelenen değişkenler arasında ilişki olduğu söylenebilir.Bu durumda değişkenler arasında ilişki katsayısı hesaplanır.

**İlişki Katsayıları**
- Bağımsızlık kontrolünde hipotez reddedilirse değişkenler arasındaki ilişki katsayısı hesaplanır.Hesaplanan ilişki katsayıları değişkenlerin ordinal(sıralanabilir) ya da nominal(sınıflanabilir) olmasına göre farklılık gösterir.
- Değişkenlerin her ikisi nominal olduğunda (nominal-nominal ) kulanılan ilişki katsayıları;

    - Pearson'n C katsayısı
    - Cramer'in V katsayısı
    - Phi katsayısı
      
- Değişkenlerin her ikiside ordinal ya da nominal- ordinal  olduğunda kullanılan ilişki katsayıları;
    - Gamma
    - Kendall's Tau b
    - Kendall's Tau c
      
**İlişki Katsayısının Önem Kontrolü**
Hesaplanan ilişki katsayılarının istatistiksel olarak anlamlı olup olmadığıda test edilebilir.
θ bir ilişki katsayısını göstersin;

        Ho: θ = 0  şeklinde kurulan yokluk hipozetezi
        
![Screenshot from 2023-12-22 13-29-42](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/d7dd33ab-2066-4ee3-8f73-e00e9abe9e7a)

Yokluk hpotezinin dğruluğu altında Z standart normal dağılım gösterir.Bu durumda |Z| >Zα/2 ise Ho reddedilir. p değeri α ile karşılatırılır.P<α ise ilişki katsayısı önemlidir.


**Örnek**

Türkiye'de evliliklerinde eşlerin eğitim durumlarına önem verdikleri,eş seçimlerinde kendi eğitim durumlarına eşit eğitim durumuna sahip eşler seçme eğilimi gösterdikleri ileri sürülmektedir.Bu savı denetlemek için yapılan bir eğitim düzeyi araştırmasında rasgele seçilen 200 ailede eşlerin eğitim durumlarına göre verileri aşağıdaki gibidir.Eşlerin eğitim durumları birbirinden bağımsız mıdır? %95 güven düzeyinde test ediniz.

![Screenshot from 2023-12-28 18-35-22](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/8c4061f6-b14f-499f-8701-098108b63877)

**Çözüm**

Beklenen Sıklıkları hesaplamak için her göze için ; bulunduğu satır toplamı * bulunduğu sütun toplamı / Genel toplam

![Screenshot from 2023-12-28 18-42-27](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/22cbe353-567d-4787-81a1-b13a40cb2143)

Yukarıdaki toplada beklenen her göze için beklenen frekanslar hesaplanmıştır.

Ki-kare formül yoluyla bulabilirsiniz.Sizlere pythonda nasıl yapılacağını göstereceğim.

```python
import researchpy, pandas ,numpy

df = pandas.DataFrame(numpy.random.randint(3, size= (200, 3)),
                  columns= ['erkek', 'severity', 'kadın'])
                  
researchpy.crosstab(df['erkek'],df['kadın'],test='chi-square')
```

![Screenshot from 2023-12-30 23-13-16](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/6c0a5f1c-2adb-47dd-a7ad-64a769bd7235)


**Sonuç,** yokluk hipotezini değişkenler arasında ilişki yoktur diye kurmuştuk.(Eşlerin eğitim durumları arasında ilişki yoktur.) p-value 0.05'den büyük olduğu için Ho hipotezi reddedilemez olduğunu 0.05 yanılma payıyla söylenebilir.Eğer ki aralarındaki ilişki önemli olsaydı ilişki katsayısını hesaplamamız gerekirdi.

**2-2x2 Çapraz Tabloda Ki-kare Testi:**
Örnek üzerinden anlatacağım.Bir hastanede muayene edilen 176 hastanın sigara içme durumu ile akciğer kanseri olması arasındaki ilişki incelenmek istenmektedir.Hastalara ait veriler aşağıda verilmiş ve gerekli çözümlemeyi yapınız.

![Screenshot from 2024-01-02 12-43-19](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/32575010-d0b8-4c67-84a7-9dd0a53d0aa9)

Beklenen frekansları yine aynı şekilde buluyoruz.

![Screenshot from 2024-01-02 12-51-36](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/f8e6040a-f5f1-49c6-8ae7-8af48d10c6d5)


2x2 çapraz tabloda en az bir gözlenen sıklık 5'ten küçük olduğu için Fisher'in Exact testi ile ilgili değerler yorumlanır.

```python
from scipy.stats import fisher_exact

# Örnek veri seti
#                Kanser Var     Kanser Yok
# Sigara İçiyor:      82             15
# Sigara İçmiyor:      4             75

# İki grup arasındaki ilişkiyi değerlendirmek için Fisher's exact testi
contingency_table = [[82, 15], [4, 75]]

odds_ratio, p_value = fisher_exact(contingency_table)

print("Odds Ratio:", odds_ratio)
print("p-value:", p_value)

Output:
Odds Ratio: 102.5
p-value: 4.5642139755146983e-29
```

          Ho:Sigara içme durumu ve kanser olup olmama arasında ilişki yoktur.
          
          H1:Sigara içme durumu ve kanser olup olmama arasında ilişki vardır.

Fisher kesin olasılık testi sonucuna göre Ho hipotezi reddedilir (p<0.001).Sigara ve Kanser değişkenleri arasında istatistiksel olarak anlamlı bir ilişki bulunmuştur.

Sınıflanabilir kategorik değişkenler arasındaki ilişkininn derecesini incelemek için Phi ve Cramer V ilişki katsayılarının sonuçları verilmiştir.

```python
# Phi katsayısını hesapla
def phi_coefficient(table):
    a = table[0][0]
    b = table[0][1]
    c = table[1][0]
    d = table[1][1]

    return (a*d - b*c) / sqrt((a+b)*(c+d)*(a+c)*(b+d))

phi = phi_coefficient(contingency_table)
print("Phi Coefficient:", phi)
```
**Yorum,** Phi Coefficient: 0.7907649284913115 sigara ve kanser değişkenleri arasında güçlü derecede (%79) ve istatistiksel olarak anlamlı bir ilişki vardır.
Sigara ve Kanser değişkenlerine ait çapraz tabşo üzerinden hesaplan odds oranı 102,5 olarak bulunmuştur.Sigara içen hastaların sigara içmeyenlere göre,kansere yakalanma olasılığı kansere yakalanmama olasılığından 102,5 kat daha fazladır.(Sigara içen hastaların kansere yakalanma riski,sigara içmeyenlere göre 102,5 kat daha fazladır.)
