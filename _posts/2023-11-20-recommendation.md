---
layout: post
title: "Öneri Sistemleri Hakkında"
subtitle: "Dijital çağda, öneri sistemleri adeta dedektif gibi çalışarak kullanıcıların izlerini takip ediyor ve en sevdikleri içerikleri önlerine seriyor. Bu yazıda, teknolojinin detektifleri olarak kabul edilen öneri sistemlerinin sırlarına bir göz atacağız. Kullanıcıların sanal dünyada iz bıraktığı her adımda, bu algoritmalar nasıl esrarengiz bir şekilde ortaya çıkıyor? 🕵️‍♂️🔍"
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

![](https://miro.medium.com/v2/resize:fit:640/format:webp/0*GtWBC5QD3rbFPZSG.jpg)

**1-Association Rule Learning(Birliktelik Kuralı):** Bu yöntem, özellikle birbirleriyle ilişkilendirilebilecek öğeler arasındaki ilişkileri incelemek için kullanılır. Temelde, bir öğe kümesindeki bir öğenin varlığının, diğer bir öğenin varlığını tahmin etmeye yönelik kuralları tanımlar.
ARL özellikle perakende sektöründe ürün önerileri, pazarlama stratejileri, stok yönetimi gibi birçok alanda kullanılır. Veri madenciliği ve büyük veri analitiği bağlamında sıkça tercih edilen bir tekniktir. Apriori algoritması, FP-Growth algoritması gibi algoritmalar, bu tür öğrenme yöntemlerinde yaygın olarak kullanılan örnek algoritmalar arasındadır.

![](https://cdn.sanity.io/images/oaglaatp/production/a2fc251dcb1ad9ce9b8a82b182c6186d5caba036-1200x800.png?w=1200&h=800&auto=format)

**2-Content-Based Filtering (İçerik Tabanlı Filtreleme) :** Kullanıcının tercihlerine benzer başka öğeler önermek için bir öğenin (bu içerik kısmıdır) özelliklerini veya özelliklerini kullanır. Bu yaklaşım, öğe ve kullanıcı özelliklerinin benzerliğine, bir kullanıcı ve etkileşime girdiği öğeler hakkındaki bilgilere dayalı olarak, yeni bir şeyin olasılığını modellemeye dayanır. 

**3-Collabarative Filtering (İşbirlikçi Filtreleme):** Bu tavsiye sistemleri, kullanıcının daha önce satın aldığı ürünler veya bu ürünlere verilen derecelendirmeler ve diğer kullanıcılar tarafından alınan benzer kararlar gibi geçmiş davranışlarından bir model oluşturur. Buradaki fikir şu ki, eğer bazı insanlar geçmişte film seçimi gibi benzer kararlar ve satın almalar yapmışsa, o zaman gelecekte başka seçimler üzerinde de anlaşmaya varma olasılıkları yüksektir. Örneğin, işbirlikçi bir filtreleme önericisi sizin ve başka bir kullanıcının benzer film zevklerini paylaştığınızı biliyorsa, bu diğer kullanıcının zaten beğendiğini bildiği bir filmi size önerebilir.

Kullanım Durumları ve Etkileyici Uygulamalar
--

**1. E-Ticaret ve Perakende: Kişiselleştirilmiş Mağazacılık**
E-Ticaret devleri, kişiselleştirilmiş alışveriş deneyimleri sunarak kullanıcı sadakatini artırıyor. Örneğin, bir kullanıcı bir eşarp satın aldığında, algoritmalar onun geçmiş tercihlerini analiz eder ve tamamlayıcı bir ürün olan şapka gibi önerilerde bulunur. Amazon, Walmart ve Target gibi platformlar, "Görünümü Tamamla" veya "Ayrıca Beğenebilirsin" bölümleri aracılığıyla kullanıcıların ilgi alanlarına yönelik ürünleri başarıyla önerir. Akıllı öneri sistemleri, web ürünleri için dönüşüm oranlarında %22,66 gibi etkileyici artışlar sağlar.

**2. Medya ve Eğlence: Kişiselleştirilmiş İçerik**
Medya ve eğlence sektörü, yapay zeka tabanlı öneri motorlarını kullanarak kullanıcıların ilgi alanlarına en uygun içerikleri önerir. Google ve Facebook, reklam önerilerinde bireyin satın alma davranışlarını analiz ederek kişiselleştirilmiş reklamlar sunar. Netflix ise büyük bir başarıyla, kullanıcıların izleme geçmişlerine dayanarak kişiselleştirilmiş film ve dizi önerileri sunar. Bu sayede kullanıcılar, kendi tercihlerine uygun içerikleri daha hızlı keşfeder.

![Screenshot from 2023-12-06 13-49-58](https://github.com/suhedakarabudak/suhedakarabudak.github.io/assets/100937634/6c1e0205-137d-4bad-bc06-b6e9e23a41f5)

**3. Kişiselleştirilmiş Bankacılık**
Dijital bankacılık, müşterilere daha iyi hizmet sunmak ve finansal kararlarını desteklemek amacıyla kişiselleştirilmiş öneriler sağlar. Algoritmalar, müşterinin mali durumu, harcama alışkanlıkları ve geçmiş tercihleri gibi verileri analiz eder. Bu bilgiler, kullanıcılara uygun kredi kartı teklifleri, yatırım fırsatları veya tasarruf planları gibi kişiselleştirilmiş bankacılık hizmetleri sunmak için kullanılır. Bu, milyonlarca kullanıcının verileri bir araya getirildiğinde güçlü bir etki yaratır ve müşteri memnuniyetini artırır.

**4. Seyahat ve Turizm: Özelleştirilmiş Tatil Paketleri**
Seyahat ve turizm endüstrisi, kullanıcıların tercihlerine dayalı olarak özelleştirilmiş tatil paketleri sunarak müşteri memnuniyetini maksimize eder. Bir kullanıcının geçmiş seyahat deneyimleri, konaklama tercihleri ve aktivite ilgi alanları analiz edilerek, kişiselleştirilmiş seyahat önerileri yapılır. Bu, online seyahat platformlarının kullanıcıların beklentilerine daha iyi yanıt vermesini sağlar ve seyahat planlama sürecini kolaylaştırır.


Kaynakça
--

