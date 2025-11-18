📚 Ziraat Fakültesi Akıllı Ders Programı Modülü
Bu proje, Çanakkale Onsekiz Mart Üniversitesi (ÇOMÜ) Ziraat Fakültesi'ne özel olarak tasarlanmış, ders programlarını dinamik ve kullanıcı dostu bir arayüzle görüntülemeyi ve filtrelemeyi sağlayan basit ve etkili bir web modülüdür.

🌟 Temel Özellikler
Dinamik Ders Görüntüleme: Girilen ders verilerini anında tablo formatında listeler.

Filtreleme Fonksiyonu: Ders adı, öğretim elemanı, gün ve saat aralığı gibi kriterlere göre hızlı ve kolay filtreleme imkanı sunar.

Akıllı Saat Gruplama: Bir dersin birden fazla blok saat sürmesi durumunda, başlangıç ve bitiş saatlerini otomatik olarak hesaplayıp aralık olarak gösterir (örnek: 09:00 - 12:00).

Teknolojik Temel: Modern ve responsive tasarım için Tailwind CSS kullanılmıştır.

Sayfa Geçiş Sistemi: Kullanıcı deneyimini artırmak için sonuç ve giriş sayfaları arasında akıcı geçişler sağlanmıştır.

🛠️ Kullanılan Teknolojiler
HTML5

Vanilla JavaScript (Tüm mantık ve DOM manipülasyonları için)

Tailwind CSS (Tasarım ve stil için)

Font Awesome (İkonlar için)

Inter Font (Modern tipografi için)

🚀 Kurulum ve Kullanım
Proje tek bir HTML dosyasından oluşmaktadır ve harici bir derleme/kurulum gerektirmez.

Bu depoyu klonlayın veya Ders Program Modülü.html dosyasını indirin.

Dosyayı herhangi bir modern web tarayıcısında açın.

Veri Yapısı
Filtreleme ve görüntülemenin düzgün çalışması için, ders verilerinin Dersler dizisi içinde aşağıdaki formatta olması gerekmektedir:

JavaScript

const Dersler = [
    {
        dersAdi: "BİTKİ KORUMA GİRİŞ",
        ogretimElemani: "Prof. Dr. X",
        gun: "Pazartesi",
        saatler: ["09:00", "10:00", "11:00"], // Blok saatler
        derslik: "G-101"
    },
    // ... Diğer dersler
];
⚙️ Koddan Öne Çıkanlar
1. Akıllı Saat Aralık Hesaplama
sonuclariGoster fonksiyonu içindeki bu bölüm, aynı derse ait birden fazla saat bloğu varsa, bunları bir saat aralığına dönüştürür.

JavaScript

// Kodunuzdan bir parça:
const siraliSaatler = ders.saatler.sort((a, b) => {
    // ... saatleri sıralama mantığı
});

const baslangicSaat = siraliSaatler[0];
const bitisSaat = saatBasliklari[saatBasliklari.indexOf(siraliSaatler[siraliSaatler.length - 1]) + 1];
const gosterilenSaat = bitisSaat ? `${baslangicSaat} - ${bitisSaat}` : baslangicSaat;
2. Filtreleme Mantığı
sonuclariGetir fonksiyonu, kullanıcının seçtiği kriterlere göre ana Dersler dizisini filtreler.

🤝 Katkıda Bulunma
Proje tamamen açıktır ve geliştirme önerilerine her zaman açığız. Her türlü hata raporu veya iyileştirme için bir Issue açmaktan ya da Pull Request göndermekten çekinmeyin.

📜 Lisans
Bu proje MIT Lisansı altında lisanslanmıştır.
