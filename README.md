# 🐰 Project ALICE: Nasdaq (NQ) Macro-Aware Decision Support System

Project ALICE, Nasdaq (NDX/NQ) piyasası için özel olarak tasarlanmış, Piyasa Arası Analiz (Intermarket Analysis) ve Akıllı Para Konseptlerini (SMC) birleştiren gelişmiş bir algoritmik karar destek sistemidir.

Sıradan indikatörlerin aksine, Alice sadece fiyatın kendisine bakmaz; Dolar Endeksi (DXY), Tahvil Faizleri (US10Y) ve Volatilite (VIX) gibi makroekonomik verileri de analiz ederek "Piyasa Rejimini" tespit eder.

## 🧠 Nasıl Çalışır? (The Logic)

Bu proje, Hibrit Zeka yaklaşımıyla geliştirilmiştir. Strateji ve piyasa okuma mantığı bir insan trader (Domain Expert) tarafından kurgulanmış, kodlama süreci ise AI asistanlığı ile optimize edilmiştir.

### 1. Intermarket "Wall Street" Modülü 🏦
Alice, karar vermeden önce şu dış verileri kontrol eder:
* **US10Y (10 Yıllık Tahvil Faizleri):** Faizler artıyorsa Teknoloji hisseleri (Nasdaq) baskılanır. Alice bunu görür.
* **DXY (Dolar Endeksi):** Doların güçlenmesi riskli varlıklar için negatiftir.
* **VIX (Korku Endeksi):** Volatilite artışlarını hesaba katar.
* **XLK (Teknoloji Sektör Fonu):** Sektörün genel sağlığını kontrol eder.

### 2. Puanlama Motoru (Scoring Engine) 💯
Sistem, her mum kapanışında 0 ile 100+ arasında bir **"Conviction Score" (İnanç Puanı)** üretir. Bir sinyalin oluşması için sadece bir indikatör yetmez, birden fazla faktörün (Confluence) bir araya gelmesi gerekir:
* **Trend:** Zero Lag Trend (ZLT) ve EMA 8/200 kombinasyonları.
* **Momentum:** MACD ve Volumatic VIDYA.
* **Yapı (Structure):** SMC (Smart Money Concepts) ile BOS, CHoCH ve Order Block yapıları.
* **Volatilite:** QQE Mod ve Bollinger Bantları.

### 3. Dinamik Risk Yönetimi 🛡️
* **Otomatik TP/SL:** Sinyal geldiğinde, geçmiş destek/direnç bölgelerine ve Order Block'lara göre otomatik *Take Profit* ve *Stop Loss* seviyeleri çizer.
* **R:R Filtresi:** Eğer potansiyel Kazanç/Risk oranı (Reward:Risk) kullanıcının belirlediği eşiğin (Örn: 1.5) altındaysa sinyali iptal eder.

---

## 📊 Ekran Görüntüleri

### 1. Dashboard ve Makro Analiz
> *Alice, sol alttaki panelde ABD Ekonomisinin o anki durumunu (Risk-On / Risk-Off) ve sağ altta stratejinin başarı oranını canlı olarak gösterir.*
`!https://github.com/Lomion9/TradingView-Karar-Destek-Indikatorleri/blob/main/dashboard.png?raw=true`

### 2. "Sniper" Giriş Sinyali
> *Yüksek puanlı bir AL sinyali. Otomatik çizilen TP/SL çizgilerine ve ZLT Trendinin (renkli şerit) uyumuna dikkat edin.*
`!https://github.com/Lomion9/TradingView-Karar-Destek-Indikatorleri/blob/main/guclu-al-sinyali.png?raw=true`
`!https://github.com/Lomion9/TradingView-Karar-Destek-Indikatorleri/blob/main/guclu-sat-sinyali.png?raw=true`

### 3. SMC Yapıları (Order Blocks & FVG)
> *Fiyatın kurumsal "Order Block" bölgelerinden (kutucuklar) nasıl tepki aldığını gösteren piyasa yapısı analizi.*
`!https://github.com/Lomion9/TradingView-Karar-Destek-Indikatorleri/blob/main/smc-yapisi.png?raw=true`

---

## ⚙️ Teknik Özellikler

* **Platform:** TradingView (Pine Script v5)
* **Optimize Edilen Varlık:** Nasdaq (NQ / NDX)
* **Zaman Dilimleri:** 15dk, 1S, 4S (Scalping ve Swing uyumlu)
* **Kullanılan Kütüphaneler:** `ta.macd`, `ta.rsi`, `request.security`, `box.new`, `line.new`

## ⚠️ Yasal Uyarı (Disclaimer)

Bu kod deposu, algoritmik trading stratejilerinin kodlanması üzerine bir **AR-GE ve Eğitim** çalışmasıdır. Kesinlikle **Yatırım Tavsiyesi Değildir (NFA).** Finansal piyasalar yüksek risk içerir. Geçmiş performans, gelecekteki sonuçların garantisi değildir.
