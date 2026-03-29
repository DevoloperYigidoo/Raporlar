# 🧠 KERNEL

Kernel, işletim sisteminin en temel parçasıdır.  
**Yazılım ile donanım arasında köprü görevi görür.**

Kullanıcı, terminal (konsol) veya uygulamalar aracılığıyla komut verir →  
bu komut önce **shell**’e gider → shell de bunu **kernel**’a iletir →  
kernel de donanıma bu işi yaptırır.

## 📌 Örnek:
- Dosya oluşturma  
- Dosya kaydetme  
- Program çalıştırma  

👉 **Kısaca:**  
Kernel = Donanımla doğrudan konuşan katman

---

# 🔄 SÜREÇ (PROCESS) – İŞ PARÇACIĞI (THREAD) FARKI

Bir program çalıştığında **process (süreç)** oluşur.

Her process’in içinde işleri yapan daha küçük yapılar vardır:  
➡️ **thread (iş parçacığı)**

## 📌 Örnek:
Google Chrome açtın:
- Bu → 1 process  
- Ama:
  - Arayüz çizimi  
  - İnternet bağlantısı  
  - Sayfa yükleme  

👉 Bunları thread’ler yapar

---

## ⚖️ Farkları

- Process’ler birbirinden **bağımsızdır**  
- Thread’ler aynı process içinde **aynı veriyi paylaşır**

---

## ⚠️ Kritik Nokta: Race Condition

Birden fazla thread aynı veriyi aynı anda değiştirirse:

👉 **Race Condition (yarış durumu)** oluşur

---

# 💾 BELLEK YÖNETİMİ (MEMORY MANAGEMENT)

Kernel, RAM’i verimli kullanmak için yönetir.

## 🧩 Nasıl Yapılır?

### 1. 📦 RAM’i Parçalar (Paging)
Kernel RAM’i tek parça kullanmaz.  
Küçük parçalara böler → bunlara **page (sayfa)** denir.

---

### 2. 📌 Programı Yerleştirir
Bir program açıldığında:

- Ne kadar RAM kullanacağı belirlenir  
- RAM’de boş yer bulunur  
- Programa bu alan verilir  

---

### 3. 🔐 İzolasyon Sağlanır
Her program kendi alanında çalışır:

👉 Programlar birbirinin verisine erişemez

---

### 4. 🧠 Virtual Memory (Sanal Bellek)
RAM dolarsa:

👉 Kernel, bazı verileri diske taşır

- Az kullanılan → disk  
- Çok kullanılan → RAM  

---

### 5. 🔄 Swap İşlemi
Kernel sürekli:

- RAM ↔ Disk arasında veri taşır

---

### 6. 🧹 Temizlik
Program kapanınca:

- RAM boşaltılır  
- Kullanılmayan veriler silinir  

---

# ⚙️ CPU ZAMANLAYICILARI (SCHEDULER)

CPU aynı anda tek işlem yapabilir.  
Ama birden fazla program çalışıyormuş gibi görünür.

👉 Çünkü kernel CPU’yu paylaştırır.

## 🔧 Scheduler Türleri

### ⚡ Long-Term Scheduler
- Sisteme hangi process’ler alınacak?
- Sistemin aşırı yüklenmesini engeller

---

### 🔄 Short-Term Scheduler (En Önemlisi)
- CPU’yu hangi process kullanacak?
- Çok hızlı karar verir (milisaniyeler)

---

### ⏳ Medium-Term Scheduler
- RAM dolarsa bazı process’leri durdurur (suspend)
- Daha sonra tekrar çalıştırır

---

# 🚀 GENEL ÖZET

✔ Kernel → donanım ile yazılımı bağlar  
✔ Process → çalışan program  
✔ Thread → process içindeki iş parçaları  
✔ Memory management → RAM’i düzenler  
✔ Scheduler → CPU’yu paylaştırır  