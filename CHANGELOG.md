# Sürüm Notları

## 1.0 — 2026-09-17

Tek dosyalık, kurulum gerektirmeyen lig takip sayfası. Skor girildiği anda puan durumu güncellenir.

### Puan durumu
- Oynanan, galibiyet, beraberlik, mağlubiyet, atılan, yenilen, averaj ve puan sütunları.
- Sıralama puan, averaj, atılan gol ve isim sırasına göre otomatik yapılır.
- Lider satırı kalın gösterilir, averaj artı/eksi durumuna göre renklenir.

### Fikstür
- İlk Devre ve İkinci Devre bölümleri. Masaüstünde yan yana, mobilde alt alta görünür.
- Her maç için iki skor kutusu. Boş bırakılan maç oynanmamış sayılır.
- Girilen skorlar tarayıcıda saklanır, sayfa kapatılıp açılsa da kalır.

### Tema
- Üst çubuktan seçilebilen beş tema: Mor, Gece, Orman, Kızıl, Açık.
- Seçilen tema hatırlanır.

### Sıfırla
- Girilen skorları siler ve koddaki başlangıç skorlarına döner.
- Sayfa yenilendiğinde de aynı başlangıç durumu gelir.

### Yönetim (kod tarafı)
- Takımlar, bölümler, maç sırası, ev/deplasman tarafı ve başlangıç skorları `index.html` dosyasının üstündeki `CONFIG` bloğundan düzenlenir.
- Skorlar takım adına bağlı saklandığı için maç sırası veya tarafı değişse bile kayıtlı skor kaybolmaz.
- Yeni tema eklemek için bir CSS bloğu ve `THEMES` listesine bir satır yeterlidir.

### Bilinen sınırlamalar
- Skorlar her ziyaretçinin kendi tarayıcısında tutulur, kişiler arasında paylaşılmaz. Herkesin göreceği skorlar `CONFIG` bloğuna yazılıp yayınlanmalıdır.
- Tailwind CDN üzerinden yüklenir, çevrimdışı çalışmaz.
