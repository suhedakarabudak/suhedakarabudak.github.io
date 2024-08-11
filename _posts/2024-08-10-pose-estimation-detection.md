---
layout: post
title: "Yapay Zeka ile Squat Performansınızı Otomatik Olarak Değerlendirin"
subtitle: ""
author: "Şuheda Karabudak"
header-style: text
tags:
  - İstatistik
  - Aykırı değer
  - Outliers
  - Veri
---


Squat, fitness dünyasında en temel ve etkili egzersizlerden biri olarak bilinir. Ancak, doğru yapılmadığında sakatlanma riskini artırabilir. Bu nedenle, doğru formda squat yapmanın önemi büyüktür. Bu blog yazısında, squat hareketinin analizini gerçekleştiren ve doğru formda yapılıp yapılmadığını tespit eden bir sistem geliştirme sürecini adım adım açıklayacağım. Bu projede Medipipe kütüphanesi, Streamlit ve FastAPI kullanarak bir squat analizi uygulaması geliştirdim.



Projenin Adımları
-- 

**1.Adım : Medipipe Kütüphanesi ve Pose Estimation**

Medipipe, Google tarafından geliştirilen, gerçek zamanlı makine öğrenimi uygulamalarını kolaylaştıran güçlü bir kütüphanedir. Pose Estimation, vücut eklemlerinin (örneğin, dirsek, diz, omuz) konumlarını belirleyen bir tekniktir. Bu projede, squat hareketini analiz etmek için Medipipe'in Pose Estimation modelini kullandım. Model, video üzerinden kullanıcının vücut eklemlerinin x, y ve z koordinatlarını çıkarır. 

![Streamlit Arayüzü](https://github.com/user-attachments/assets/5045fa45-4249-4216-9618-cc9c95a00afa)


**2.Adım: Streamlit Kütüphanesi ile Arayüz Oluşturma**

Bu proje gerçek zamanlı olacağı için kullanıcın görebileceği,videolarını yükleyebileceği bir arayüze ihtiyaç vardır.Bunu da Streamlit kütüphanesini kullanarak yapabiliriz. Streamlit, veri bilimi ve makine öğrenimi projeleri için hızlı bir şekilde interaktif web uygulamaları oluşturmayı sağlayan bir kütüphanedir. Kullanıcı dostu arayüzü ile kullanıcıların squat videolarını yüklemelerini ve bu videoların analiz edilmesini sağladım.

**Streamlit Arayüzü:**
- Video Yükleme: Kullanıcılar, squat hareketlerini içeren videolarını arayüze yükleyebilir.

- Video Analizi: Yüklenen video, Medipipe Pose Estimation kullanılarak analiz edilir. Her karedeki vücut eklemlerinin koordinatları (x, y, z) çıkarılır.
  
- Sonuçların İndirilmesi: Kullanıcılar, analiz sonuçlarını bir dosya olarak indirebilir.


![](https://github.com/user-attachments/assets/f86f8b64-8bad-49db-8279-c5d9edfd343b)

**3.Adım: FastAPI ile Makine Öğrenmesi Modelinin Entegrasyonu**

Yukarıdaki adımları yaparak squat pozisyonun doğru yapılıp,yapılmadığını anlayabiliriz. Bu projeye ek olarak makine öğrenmesi algoritmalarını kullanarak bunu veri bilimi ile destekleyerek bir model geliştirip Fastapi entegrasyon sağlayabiliriz.

**FastAPI**, modern ve yüksek performanslı bir API geliştirme framework’üdür. Bu projede, squat hareketinin doğru yapılıp yapılmadığını belirleyen bir makine öğrenimi modeli geliştirdim ve FastAPI ile entegre ettim.Yarattığımız makine öğrenmesi modellerini yaratmak veri bilimi döngüsünün sadece çok küçük bir kısmını oluşturuyor. Modellerimizi canlıya alamadığımız sürece herhangi bir katma değer yaratamamış oluruz. Bu yüzden model yaratmaktan çok yaratılan modeli canlıya alma işi çok kıymetli. 

- Veri Seti Oluşturma: Farklı squat videolarından Medipipe kullanarak elde ettiğim koordinatları kullanarak, doğru ve yanlış squat örneklerinden oluşan bir veri seti hazırladım.
  
- Model Eğitimi: Bu veri setini kullanarak, squat formunu sınıflandıran bir makine öğrenimi modeli eğittim.Bu modeli eğitirken bir çok makaleden destek aldım.Veri setlerini ayrı ayrı elde ettim.
  
- API Entegrasyonu: Modeli FastAPI üzerinden bir servise dönüştürdüm, böylece Streamlit uygulaması bu servise istekte bulunarak analiz sonuçlarını alabilir.

![Screenshot from 2024-08-10 01-02-31](https://github.com/user-attachments/assets/9df97a60-0a2f-461c-9184-b0a5a396cd5b)
Bu görselde FastAPI sunduğu web arayüzünü görüyoruz.

Üst Kısımda: Kullanıcını hangi squat videosunu analiz edilmesini istiyorsa onu yüklüyor.

Ortada: Kullanıcının bu dosyayı bir sunucuya gönderip tahmin yapması için bir POST isteği gönderilmiş. Bu istek, video dosyasını sunucuya gönderiyor.

Alt Kısımda: Sunucu, dosyayı işleyip yanıt olarak "predictions" (tahminler) adıyla bir liste döndürmüş. Bu listede birçok "Correct" (Doğru) sonucu var, yani tahminlerin hepsi doğru olarak değerlendirilmiş.

Özetle: Kullanıcı bir video dosyasını sunucuya yüklüyor, sunucu bu videoyu analiz edip sonuçları geri döndürüyor.

Proje Akışı
-- 
1. Video Yükleme: Kullanıcı, Streamlit arayüzünden squat videosunu yükler. 

2. Koordinatların Çıkarılması: Medipipe Pose Estimation modeli, videodaki her karedeki vücut eklemlerinin x, y, z koordinatlarını çıkarır.

3. Makine Öğrenimi Analizi: Bu koordinatlar, FastAPI üzerinden çalışan makine öğrenimi modeline gönderilir.

4. Sonuçların Görüntülenmesi: Model, squat hareketinin doğru olup olmadığını analiz eder ve sonucu Streamlit arayüzüne geri gönderir.

5. Sonuçların İndirilmesi: Kullanıcı, analiz sonuçlarını isterse bir dosya olarak indirebilir.

Sonuç
-- 

Bu projede, squat analizini otomatikleştiren bir sistem geliştirdim. Medipipe kütüphanesi ile vücut eklemlerinin koordinatlarını çıkardım.Buradan elde ettiğim ham verileri kullanarak  makine öğrenmesi modeli ile doğru ve yanlış squatları belirledim ve bu sistemi FastAPI ile bir servise entegre ettim. Sonuç olarak, kullanıcıların squat formunu analiz edebileceği, interaktif ve kullanışlı bir proje ortaya koydum.

Bu tür projeler, fitness ve sağlık alanında daha güvenli ve etkili egzersizler yapılmasına olanak sağlar. Makine öğrenimi ve pose estimation tekniklerinin birleşimi, daha da gelişmiş analizler ve uygulamalar için büyük bir potansiyele sahiptir.



https://github.com/user-attachments/assets/1bc21e0e-f325-4545-8141-bf625756d73b

[Bu videoyu izleyin](https://drive.google.com/file/d/1OsIYYOlfW9zmPDxc9Xr-8n0XUQh2QEC_/view?usp=drive_link)




[Bu videoyu izleyin](https://github.com/user-attachments/assets/44856077-b86d-4870-8eba-c9cf12530385)

