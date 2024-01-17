---
layout:       post
title:        "Destek Vektör Makinesi Algoritması (Support Vector Machine)"
author:       "Şuheda Karabudak"
header-style: text
catalog:      true
tags:
    - Veri Madenciliği
    - Veri
    -
    - 
---

![](https://i0.wp.com/jeremykun.com/wp-content/uploads/2017/06/svm_solve_by_hand-e1496076457793.gif?resize=802%2C596&ssl=1)

Destek Vektör Makinesi Nedir ?
--
Destek vektör makineleri veya SVM'ler denetimli öğrenme modellerinden biridir.Yani algoritmaları eğitmek için etiketli veri kümlelerini kullanırlar.SVM hem regresyon hem de sınıflandırma problemleri için kullanılabilir ancak genel olarak sınıflandırma problemlerinde en iyi şekilde çalışırlar.

**SVM ile Lojistik Regresyon arasında fark; her iki algoritma da en iyi hiperdüzlemi bulmaya çalışır ancak temel fark lojistik regresyonun olasılıksal bir yaklaşım olması,destek vektör makinesinin istatistiksel yaklaşımlara dayanmasıdır.**


Destek Vektör Makinesi (SVM) Algoritma Türleri
--

**1.Doğrusal SVM:** Veri noktaları doğrusal bir çizgiyle ayrılabiliyorsa Doğrusal SVM kullanırız.

**2.Doğrusal Olmayan SVM:** Veriler doğrusal olarak ayrılamadığında Doğrusal Olmayan SVM'yi kullanabiliriz; bu, veri noktalarının bir sınıfa ayrılamadığı anlamına gelir.Gerçek dünyadaki uygulamaların çoğunda doğrusal olarak ayrılabilir veri noktaları bulamıyoruz, dolayısıyla bunları çözmek için çekirdek hilesini kullanıyoruz.


Destek Vektör Makinesi Algoritmasında Bazı Kavramlar
--

- **Hiperdüzlem:** İki boyutlu uzayda bir düzlem ve genel olarak n boyutlu uzayda bir hiperdüzlem olarak ifade edilir.Sınıfları ayırmak için en iyi hiperdüzlem, veri noktalarının en iyi şekilde ayıran düzlemdir.

- **Destek Vektörler:**  H,perdüzleme en yakın olan veri noktalarıdır.Bu noktalar ,sınıflar arasındaki marjı maksimize etmek için önemlidir.

- **Marj:** Marj,hiperdüzlem ile destek vektörleri araındaki boşluktur.

- **Çekirdek İşlevi(Kernel Trick):** Bunlar hiperdüzlemin şeklini ve karar sınırını belirlemek için kullanılan işlevlerdir.

> Destek Vektör Makinesinin Temel Amacı: iki sınıf arasındaki maksimum mesafe anlamına gelen hiperdüzlemler arasındaki maksimum marjı bularak yapar.


Destek Vektör Makinesi Nasıl Çalışır?
--

![567891](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/9fb7874a-d3a8-4ace-8da8-354ed5459e56)

SVM özellikle iki sınıf arasındaki boşluğu en üst düzeye çıkaran bir hiper düzlemi bulmak üzere eğitilir. Bu hiper düzlem, veri noktalarını sınıflandırmada optimal bir performans sağlar. Margin adı verilen bu boşluk, sınıflar arasındaki uzaklığı temsil eder ve en geniş margin, modelin genelleme yeteneğini artırır.

Birden fazla hiperdüzlem olabilir ancak marjının maksimum olduğu hiperdüzlemin optimal hiperdüzlem olduğunu bulabiliriz. DVM'nin temel amacı, veri noktalarını yüksek hassasiyetle sınıflandırabilen hiperdüzlemleri bulmakt

Destek vektörler, hiper düzlem üzerindeki sınıf sınırlarına en yakın veri noktalarını temsil eder. SVM'nin gücü, bu destek vektörlerin belirlenmesi ve sınıflandırma sürecindeki etkisiyle ortaya çıkar. Optimizasyon süreci, margin'i en üst düzeye çıkaran hiper düzlemi bulurken destek vektörleri de belirler.

Destek Vektör Makinsindeki Çekirdekler
--
SVM'nin en ilginç özelliği doğrusal olmayan bir veri seti ile bile çalışabilmesidir ve bunun için noktaların sınıflandırılmasını kolaylaştıran “Kernel Trick” kullanıyoruz.

![8882023](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/34ad896e-07bb-4f81-8877-5589026df3f3)

Burada noktaları doğru bir şekilde sınıflandırabilecek tek bir çizgi çizemediğimizi veya hiperdüzlem söyleyemediğimizi görüyoruz. Yani yaptığımız şey, veri noktalarını açıkça bölen bir karar sınırı bulmamızı sağlayacak bazı ikinci dereceden fonksiyonları kullanarak bu düşük boyutlu uzayı daha yüksek boyutlu bir uzaya dönüştürmeyi denemektir.Bunu yapmamıza yardımcı olan bu işlevlere Çekirdek adı verilir ve hangi çekirdeğin kullanılacağı tamamen hiperparametre ayarıyla belirlenir.

**Çekirdek Türleri:**

1.Polinom Çekirdek
2.Sigmoid Çekirdek
3.RBF Çekirdeği 
4-Bessel fonksiyon Çekirdeği
5.Anova Çekirdeği

**Doğru Çekirdek Nasıl Seçilir?**

Veri kümeniz için hangi çekirdek fonksiyonunun verimli çalışacağına nasıl karar vereceğiniz konusunda bu şüpheye sahip olduğunuzun farkındayım. Modelin performansı buna bağlı olduğundan iyi bir çekirdek fonksiyonu seçmek gereklidir.

Bir çekirdek seçmek tamamen ne tür bir veri kümesi üzerinde çalıştığınıza bağlıdır. Doğrusal olarak ayrılabilirse, seçmelisiniz. Doğrusal çekirdek fonksiyonu için kullanımı çok kolay olduğundan ve karmaşıklığı diğer çekirdek fonksiyonlarına göre çok daha düşük olduğundan. Verilerinizin doğrusal olarak ayrılabilir olduğuna dair bir hipotezle başlamanızı ve doğrusal bir çekirdek işlevi seçmenizi öneririm.

SVM'nin Avantajları
--
 - Veriler Doğrusal olduğunda SVM daha iyi çalışır
 - Yüksek boyutlarda daha etkilidir
 - Çekirdek numarasının yardımıyla her türlü karmaşık sorunu çözebiliriz
 - SVM aykırı değerlere duyarlı değildir
 - Görüntü sınıflandırma konusunda bize yardımcı olabilir
   
SVM'nin dezavantajları
--
 - İyi bir çekirdek seçmek kolay değil
 - Büyük bir veri kümesinde iyi sonuçlar göstermez
 - SVM hiperparametreleri Maliyet -C ve gamadır. Bu hiper parametrelere ince ayar yapmak o kadar kolay değil.Etkilerini görselleştirmek zordur.


Kaynakça
--
https://www.koshegio.com/support-vector-machine-calculator

https://www.analyticsvidhya.com/blog/2021/10/support-vector-machinessvm-a-complete-guide-for-beginners/

https://datatron.com/what-is-a-support-vector-machine/
