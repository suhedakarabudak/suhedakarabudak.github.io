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

![Screenshot from 2024-08-10 23-28-39](https://github.com/user-attachments/assets/1e875e7b-f56e-4e19-b48d-cffa15a6a374)




Projenin Adımları
-- 

**1.Adım : Medipipe Kütüphanesi ve Pose Estimation**

Medipipe, Google tarafından geliştirilen, gerçek zamanlı makine öğrenimi uygulamalarını kolaylaştıran güçlü bir kütüphanedir. Pose Estimation, vücut eklemlerinin (örneğin, dirsek, diz, omuz) konumlarını belirleyen bir tekniktir. Bu projede, squat hareketini analiz etmek için Medipipe'in Pose Estimation modelini kullandım. Model, video üzerinden kullanıcının vücut eklemlerinin x, y ve z koordinatlarını çıkarır. 


**2.Adım: Streamlit Kütüphanesi ile Arayüz Oluşturma**

Bu proje gerçek zamanlı olacağı için kullanıcın görebileceği,videolarını yükleyebileceği bir arayüze ihtiyaç vardır.Bunu da Streamlit kütüphanesini kullanarak yapabiliriz. Streamlit, veri bilimi ve makine öğrenimi projeleri için hızlı bir şekilde interaktif web uygulamaları oluşturmayı sağlayan bir kütüphanedir. Kullanıcı dostu arayüzü ile kullanıcıların squat videolarını yüklemelerini ve bu videoların analiz edilmesini sağladım.

**Streamlit Arayüzü:**
- Video Yükleme: Kullanıcılar, squat hareketlerini içeren videolarını arayüze yükleyebilir.

- Video Analizi: Yüklenen video, Medipipe Pose Estimation kullanılarak analiz edilir. Her karedeki vücut eklemlerinin koordinatları (x, y, z) çıkarılır.
  
- Sonuçların İndirilmesi: Kullanıcılar, analiz sonuçlarını bir dosya olarak indirebilir.

**3.Adım: FastAPI ile Makine Öğrenmesi Modelinin Entegrasyonu**

Projenin bu kısmı tamamen bana aittir.Yukarıdaki adımları yaparak squat pozisyonun doğru yapılıp,yapılmadığı anlaşılıyor ve bu aslında var olan bir projedir.Bu projeye ek olarak makine öğrenmesi algoritmalarını kullanarak bunu veri bilimi ile destekleyerek bir model geliştirip Fastapi entegre etmektir.

**FastAPI**, modern ve yüksek performanslı bir API geliştirme framework’üdür. Bu projede, squat hareketinin doğru yapılıp yapılmadığını belirleyen bir makine öğrenimi modeli geliştirdim ve FastAPI ile entegre ettim.Yarattığımız makine öğrenmesi modellerini yaratmak veri bilimi döngüsünün sadece çok küçük bir kısmını oluşturuyor. Modellerimizi canlıya alamadığımız sürece herhangi bir katma değer yaratamamış oluruz. Bu yüzden model yaratmaktan çok yaratılan modeli canlıya alma işi çok kıymetli. 

- Veri Seti Oluşturma: Farklı squat videolarından Medipipe kullanarak elde ettiğim koordinatları kullanarak, doğru ve yanlış squat örneklerinden oluşan bir veri seti hazırladım.
  
- Model Eğitimi: Bu veri setini kullanarak, squat formunu sınıflandıran bir makine öğrenimi modeli eğittim.Bu modeli eğitirken bir çok makaleden destek aldım.Veri setlerini ayrı ayrı elde ettim.
  
- API Entegrasyonu: Modeli FastAPI üzerinden bir servise dönüştürdüm, böylece Streamlit uygulaması bu servise istekte bulunarak analiz sonuçlarını alabilir.

Proje Akışı
-- 
1. Video Yükleme: Kullanıcı, Streamlit arayüzünden squat videosunu yükler. 

2. Koordinatların Çıkarılması: Medipipe Pose Estimation modeli, videodaki her karedeki vücut eklemlerinin x, y, z koordinatlarını çıkarır.

3. Makine Öğrenimi Analizi: Bu koordinatlar, FastAPI üzerinden çalışan makine öğrenimi modeline gönderilir.

4. Sonuçların Görüntülenmesi: Model, squat hareketinin doğru olup olmadığını analiz eder ve sonucu Streamlit arayüzüne geri gönderir.

5. onuçların İndirilmesi: Kullanıcı, analiz sonuçlarını isterse bir dosya olarak indirebilir.
