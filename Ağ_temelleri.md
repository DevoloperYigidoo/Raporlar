# 🌐 Ağ Temelleri (Network Basics)

Bu doküman, ağ (network) kavramlarının temelini sade bir şekilde anlatmak için hazırlanmıştır.

---

## 📌 IP Nedir?

İnternetteki her cihazın bir **IP adresi** vardır.
Bu adresler, cihazların birbirini tanımasını sağlar.

📍 **Örnek:**
Bir eve mektup göndermek için adres bilmen gerekir.
İşte bu adres = **IP adresi**

---

## 🚪 Port Nedir?

IP adresi bir binanın adresi ise, **port** o binadaki daire numarasıdır.

### 🔢 Yaygın Portlar

| Port | Açıklama                |
| ---- | ----------------------- |
| 80   | HTTP (web)              |
| 443  | HTTPS (güvenli web)     |
| 22   | SSH (sunucu bağlantısı) |
| 5432 | PostgreSQL              |
| 3000 | Local geliştirme        |

📍 **Örnek:**
`127.0.0.1:443` → Aynı cihazda 443 portuna git demektir.

---

## 🌍 DNS Nedir?

DNS (Domain Name System), yazdığımız domain’i IP adresine çevirir.

📍 **Örnek:**

```
google.com → 142.250.xxx.xxx
```

Bilgisayarlar domain değil, **IP adresleri ile iletişim kurar**.

---

## 🔄 TCP ve UDP Nedir?

İkisi de veri iletim protokolüdür.

### 🛡️ TCP (Transmission Control Protocol)

* Güvenilir
* Sıralı
* Daha yavaş

✔ Paketlerin ulaştığını kontrol eder
✔ Ulaşmazsa tekrar gönderir
✔ Handshake mekanizması vardır

📍 Kullanım: Web siteleri, dosya transferleri

---

### ⚡ UDP (User Datagram Protocol)

* Hızlı
* Güvenilir değil
* Sırasız

✔ Paketin ulaşıp ulaşmadığını kontrol etmez
✔ Amaç: **maksimum hız**

📍 Kullanım: Oyunlar, canlı yayınlar

---

## 📦 Paket Yapısı Nasıl Çalışır?

Veriler tek parça halinde gönderilmez.
**Küçük paketlere bölünerek iletilir.**

### 📌 Her pakette bulunan bilgiler:

* Kaynak IP (nereden geldi)
* Hedef IP (nereye gidiyor)
* Sıra numarası
* Veri (payload)

📍 Karşı taraf bu paketleri alır ve birleştirir.

* TCP → Sıralı ve garantili
* UDP → Garantisi yok

---

## 🛠️ Temel Ağ Araçları

### 🟢 Ping

Bir sunucunun çalışıp çalışmadığını kontrol eder.

```
ping google.com
```

---

### 🧭 Traceroute

Verinin hedefe giderken geçtiği yolları gösterir.

```
tracert google.com   (Windows)
traceroute google.com (Linux/Mac)
```

---

### 🔍 Nslookup

Bir domain’in IP adresini öğrenmek için kullanılır.

```
nslookup google.com
```

---

## 🎯 Özet

* IP → Cihazın adresi
* Port → Servisin kapısı
* DNS → Domain → IP çevirir
* TCP → Güvenli ama yavaş
* UDP → Hızlı ama güvensiz
* Paket → Verinin parçalanmış hali

