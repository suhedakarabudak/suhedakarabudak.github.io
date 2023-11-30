---
layout: post
title: "Öneri Sistemleri Hakkında"
subtitle: "P değeri,birçok araştırmacının odak noktası olmuş ve sıkça yanlış yorumlanmış bir istatistiksel ölçüdür.Bu yazıda,p değerinin ne olduğunu,nasıl hesaplandığını ve en önemlisi nasıl doğru bir şekilde yorumlanması gerektiğini ele alacağım."
author: "Şuheda Karabudak"
header-style: text
tags:
  - İstatistik
  - p-değeri
  - Dağılım
  - Veri
  - Örneklem
---

![Recommaster-gif](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/11332841-f1ce-40e9-ba5c-01ec71500ccc)


Öneri(Tavsiye) Sistemleri Nedir ?
--
Arka planda işleyen mantığı anlamak adına bazı sorular akla geliyor.
- Beni nerden tanıyor da bu önerilerde bulunuyor?
- Ürüne tıkladığımda anında benzer ürünler geliyor.Bu kadar hızlı nasıl çalışıyor bu sistem
- Arka planda nasıl bir öneri algoritması var ?
  
**Öneri Sistemleri** etkileşimleri hakkında toplanan verileri kullanarak kişilerin ve ürünlerin tercihlerini, önceki kararlarını ve özelliklerini anlamak üzere eğitilir. Bunlara gösterimler, tıklamalar, beğeniler ve satın almalar dahildir.Tüketicileri kitaplardan videolara, sağlık derslerinden giyime kadar ilgilerini çeken hemen hemen her ürün veya hizmete yönlendirebilirler.

Öneri sistemlerin arkasındaki algoritmalardan bahsetmeden önce her bir öneri sistemi için farklı algoritmalar kullanılır.Bunlardan kısaca bahsedelim.Sizin için belki proje fikri olabilir.

**1-Association Rule Learning:** Bu yöntem, özellikle birbirleriyle ilişkilendirilebilecek öğeler arasındaki ilişkileri incelemek için kullanılır. Temelde, bir öğe kümesindeki bir öğenin varlığının, diğer bir öğenin varlığını tahmin etmeye yönelik kuralları tanımlar.
ARL özellikle perakende sektöründe ürün önerileri, pazarlama stratejileri, stok yönetimi gibi birçok alanda kullanılır. Veri madenciliği ve büyük veri analitiği bağlamında sıkça tercih edilen bir tekniktir. Apriori algoritması, FP-Growth algoritması gibi algoritmalar, bu tür öğrenme yöntemlerinde yaygın olarak kullanılan örnek algoritmalar arasındadır.

**2-Content-Based Filtering:** Kullanıcının tercihlerine benzer başka öğeler önermek için bir öğenin (bu içerik kısmıdır) özelliklerini veya özelliklerini kullanır. Bu yaklaşım, öğe ve kullanıcı özelliklerinin benzerliğine, bir kullanıcı ve etkileşime girdiği öğeler hakkındaki bilgilere dayalı olarak, yeni bir şeyin olasılığını modellemeye dayanır. 

**3-Collabarative Filtering:** Bu tavsiye sistemleri, kullanıcının daha önce satın aldığı ürünler veya bu ürünlere verilen derecelendirmeler ve diğer kullanıcılar tarafından alınan benzer kararlar gibi geçmiş davranışlarından bir model oluşturur. Buradaki fikir şu ki, eğer bazı insanlar geçmişte film seçimi gibi benzer kararlar ve satın almalar yapmışsa, o zaman gelecekte başka seçimler üzerinde de anlaşmaya varma olasılıkları yüksektir. Örneğin, işbirlikçi bir filtreleme önericisi sizin ve başka bir kullanıcının benzer film zevklerini paylaştığınızı biliyorsa, bu diğer kullanıcının zaten beğendiğini bildiği bir filmi size önerebilir.
