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

\begin{align}f(x) = \text{sign} \left(\sum_i^N \alpha_i~y_i~K(x_i, x)\right).\end{align}


