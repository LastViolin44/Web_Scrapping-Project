# 🔍 DergiPark Scraper & Article Analysis System

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Flask](https://img.shields.io/badge/Flask-2.0-green)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green)
![BeautifulSoup](https://img.shields.io/badge/Scraping-Bs4-yellow)

## 🚀 Proje Hakkında
Bu proje, akademik araştırmalar için geliştirilmiş, **Python Flask** tabanlı gelişmiş bir web kazıma (web scraping) ve veri analiz aracıdır. Kullanıcının belirlediği anahtar kelimelerle **DergiPark** veritabanını tarar, makaleleri analiz eder, meta verilerini (Özet, Yazar, Referanslar vb.) ayrıştırır ve yapılandırılmış bir şekilde **MongoDB** veritabanına kaydeder.

Sadece veri çekmekle kalmaz, **NLP tabanlı yazım denetimi** ve **gelişmiş filtreleme motoru** ile araştırmacıların literatür taramasını otomatize eder.

### 🌟 Temel Özellikler

* **Akıllı Arama & Typo Correction:** Kullanıcı arama terimlerini yanlış yazsa bile (örn: `~artifcal`), entegre `SpellChecker` modülü ile otomatik düzeltme yapar ve doğru sonuçları getirir.
* **Derinlemesine Veri Kazıma:** Sadece listeleme sayfalarını değil, her makalenin detay sayfasını ziyaret ederek;
    * Makale Özeti (Abstract)
    * Yazar Bilgileri
    * Yayın Tarihi & DOI
    * Referans Listesi
    * PDF Bağlantılarını ayrıştırır.
* **NoSQL Veritabanı Entegrasyonu:** Çekilen veriler, tekrarı önleyen (duplicate check) mekanizmalarla MongoDB üzerinde saklanır.
* **Gelişmiş Filtreleme Paneli:** Kaydedilen veriler üzerinde şu kriterlere göre sorgulama yapılabilir:
    * 📅 Tarih Aralığı
    * 🔢 Alıntı Sayısı (Simülasyon)
    * 📝 Anahtar Kelime & İçerik Arama
* **Dosya Yönetimi:** Makalelerin PDF versiyonlarını yerel diske indirip arşivler.

## 🛠️ Mimari ve Teknolojiler

Proje **ETL (Extract, Transform, Load)** prensiplerine göre tasarlanmıştır:

1.  **Extract (Veri Toplama):** `Requests` ve `BeautifulSoup4` kullanılarak dinamik HTML parse edilir.
2.  **Transform (Dönüştürme):** Ham metin verileri, tarih formatları ve yazar isimleri temizlenir (`datetime` dönüşümleri).
3.  **Load (Yükleme):** Temizlenen veriler JSON formatında `MongoDB` koleksiyonlarına işlenir.

| Teknoloji | Kullanım Amacı |
|-----------|----------------|
| **Flask** | Backend API ve Web Arayüzü Yönetimi |
| **MongoDB** | Esnek veri şeması ile makale verilerinin saklanması |
| **BeautifulSoup4** | HTML Parsing ve DOM Navigasyonu |
| **SpellChecker** | Arama terimlerindeki yazım hatalarının düzeltilmesi |
| **HTML/CSS** | Kullanıcı dostu arama ve listeleme arayüzü |

## ⚙️ Kurulum ve Çalıştırma

Projeyi yerel ortamınızda çalıştırmak için aşağıdaki adımları izleyin:

### Gereksinimler
* Python 3.x
* MongoDB (Yerel veya Atlas servisi çalışır durumda olmalı)

### Adım 1: Repoyu Klonlayın
```bash
git clone [https://github.com/mehmetalik1r/Web_Scrapping-Project.git](https://github.com/mehmetalik1r/Web_Scrapping-Project.git)
cd Web_Scrapping-Project# 🔍 DergiPark Scraper & Article Analysis System

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Flask](https://img.shields.io/badge/Flask-2.0-green)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green)
![BeautifulSoup](https://img.shields.io/badge/Scraping-Bs4-yellow)

## 🚀 Proje Hakkında
Bu proje, akademik araştırmalar için geliştirilmiş, **Python Flask** tabanlı gelişmiş bir web kazıma (web scraping) ve veri analiz aracıdır. Kullanıcının belirlediği anahtar kelimelerle **DergiPark** veritabanını tarar, makaleleri analiz eder, meta verilerini (Özet, Yazar, Referanslar vb.) ayrıştırır ve yapılandırılmış bir şekilde **MongoDB** veritabanına kaydeder.

Sadece veri çekmekle kalmaz, **NLP tabanlı yazım denetimi** ve **gelişmiş filtreleme motoru** ile araştırmacıların literatür taramasını otomatize eder.

### 🌟 Temel Özellikler

* **Akıllı Arama & Typo Correction:** Kullanıcı arama terimlerini yanlış yazsa bile (örn: `~artifcal`), entegre `SpellChecker` modülü ile otomatik düzeltme yapar ve doğru sonuçları getirir.
* **Derinlemesine Veri Kazıma:** Sadece listeleme sayfalarını değil, her makalenin detay sayfasını ziyaret ederek;
    * Makale Özeti (Abstract)
    * Yazar Bilgileri
    * Yayın Tarihi & DOI
    * Referans Listesi
    * PDF Bağlantılarını ayrıştırır.
* **NoSQL Veritabanı Entegrasyonu:** Çekilen veriler, tekrarı önleyen (duplicate check) mekanizmalarla MongoDB üzerinde saklanır.
* **Gelişmiş Filtreleme Paneli:** Kaydedilen veriler üzerinde şu kriterlere göre sorgulama yapılabilir:
    * 📅 Tarih Aralığı
    * 🔢 Alıntı Sayısı (Simülasyon)
    * 📝 Anahtar Kelime & İçerik Arama
* **Dosya Yönetimi:** Makalelerin PDF versiyonlarını yerel diske indirip arşivler.

## 🛠️ Mimari ve Teknolojiler

Proje **ETL (Extract, Transform, Load)** prensiplerine göre tasarlanmıştır:

1.  **Extract (Veri Toplama):** `Requests` ve `BeautifulSoup4` kullanılarak dinamik HTML parse edilir.
2.  **Transform (Dönüştürme):** Ham metin verileri, tarih formatları ve yazar isimleri temizlenir (`datetime` dönüşümleri).
3.  **Load (Yükleme):** Temizlenen veriler JSON formatında `MongoDB` koleksiyonlarına işlenir.

| Teknoloji | Kullanım Amacı |
|-----------|----------------|
| **Flask** | Backend API ve Web Arayüzü Yönetimi |
| **MongoDB** | Esnek veri şeması ile makale verilerinin saklanması |
| **BeautifulSoup4** | HTML Parsing ve DOM Navigasyonu |
| **SpellChecker** | Arama terimlerindeki yazım hatalarının düzeltilmesi |
| **HTML/CSS** | Kullanıcı dostu arama ve listeleme arayüzü |

## ⚙️ Kurulum ve Çalıştırma

Projeyi yerel ortamınızda çalıştırmak için aşağıdaki adımları izleyin:

### Gereksinimler
* Python 3.x
* MongoDB (Yerel veya Atlas servisi çalışır durumda olmalı)

### Adım 1: Repoyu Klonlayın
```bash
git clone [https://github.com/mehmetalik1r/Web_Scrapping-Project.git](https://github.com/mehmetalik1r/Web_Scrapping-Project.git)
cd Web_Scrapping-Project
