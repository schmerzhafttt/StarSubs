# ASS Translator - GladionStar 🚀

## 📖 Tanıtım

**ASS Translator - GladionStar**, `.ass` (Advanced SubStation Alpha) formatındaki altyazı dosyalarını bir dilden diğerine çevirmek için tasarlanmış, kullanıcı dostu bir masaüstü uygulamasıdır. Bu yazılım, **DeepL API**'sinin gücünü kullanarak yüksek kaliteli çeviriler sunmayı hedefler.

> **ÖNEMLİ:** Bu yazılım **kapalı kaynaklıdır** ve ticari bir üründür. Kullanımı için geçerli bir lisans anahtarı gereklidir.

---

## ✨ Temel Özellikler

### 🛡️ 1. Lisanslama ve Güvenlik
*   **Donanım Kimliği (Hardware ID) Tabanlı Koruma:** Yazılım, her kullanıcının bilgisayarına özgü bir donanım kimliği oluşturarak lisansın yetkisiz kullanımını engeller.
*   **Çevrimiçi ve Çevrimdışı Lisans Doğrulama:** Lisans anahtarları hem internet bağlantısı olduğunda sunucu üzerinden hem de internet olmadığında yerel önbellek üzerinden doğrulanabilir.
*   **Güvenli Lisans Saklama:** Lisans bilgileri (lisans anahtarı, kullanıcı adı, donanım ID) yerel bir yapılandırma dosyasında (`C:/GladionSubs/config.json`) ve SQLite tabanlı bir önbellekte (`user_cache.db`) güvenli bir şekilde saklanır.
*   **Kullanıcı Bilgileri Paneli:** Arayüz üzerinden Discord kullanıcı adınızı ve lisansınızın kalan süresini (gün, saat, dakika olarak) bir ilerleme çubuğuyla birlikte görüntüleyebilirsiniz.

### 📄 2. `.ASS` Dosya İşlemleri
*   **Dosya Yükleme ve Ayrıştırma:** `.ass` dosyalarını yükleyebilir ve içerisindeki diyalog satırlarını (zamanlamaları ve orijinal metinleri) alabilirsiniz. Çeviri kalitesini artırmak için metin içindeki `{}` formatındaki stil etiketleri temizlenir.
*   **Altyazı Tablosu:** Yüklenen altyazılar, satır numarası, zaman damgası, orijinal metin ve çevrilmiş metin sütunlarını içeren etkileşimli bir tabloda görüntülenir.
*   **Çevrilmiş Dosyayı Kaydetme:** Çevrilen metinler, orijinal `.ass` dosyasının formatını koruyarak yeni bir dosyaya kaydedilir. Sadece diyalog metinleri güncellenir, zamanlama ve diğer bilgiler korunur.

### 🌐 3. Çeviri Yetenekleri
*   **DeepL API Entegrasyonu:** Güçlü ve doğal çeviriler için **DeepL API**'sini kullanır.
*   **Çoklu Dil Desteği:** Desteklenen diller arasında Türkçe, İngilizce, İspanyolca, Fransızca ve Almanca bulunmaktadır. Hedef dil arayüzden seçilebilir.
*   **API Anahtarı Yönetimi:** Kullanıcılar kendi DeepL API anahtarlarını girip, geçerliliğini uygulama içinden kontrol edebilirler.
*   **Asenkron Çeviri:** Çeviri işlemi arayüzü kilitlemeden arka planda çalışır. İlerleme durumu (yüzde, mevcut çevrilen satır) ayrı bir pencerede gösterilir ve işlem istenildiği zaman iptal edilebilir.

### 🖥️ 4. Gelişmiş Kullanıcı Arayüzü
*   **Modern ve Özelleştirilmiş Tasarım:** **PyQt5** kütüphanesi ile geliştirilmiş, koyu tema ve modern bileşenlere sahip bir arayüze sahiptir.
*   **Çerçevesiz ve Sürdürülebilir Pencere:** Ana pencere, özel başlık çubuğu sayesinde sürüklenebilir, simge durumuna küçültülebilir, kapatılabilir ve yeniden boyutlandırılabilir.
*   **Özel Dialog Pencereleri:** Giriş yapma, kullanıcı bilgileri, API anahtarı kontrolü, çeviri ilerlemesi, hata/bilgi mesajları ve çevrilmiş satırları düzenleme için ayrı, stilize edilmiş dialog pencereleri mevcuttur.
*   **Etkileşimli Altyazı Yönetimi:**
    *   Çevrilmiş bir satırı doğrudan tablo üzerinden veya özel bir düzenleme penceresi aracılığıyla manuel olarak düzenleyebilirsiniz.
    *   Tüm çevirileri tek bir tıklamayla temizleyebilirsiniz.

---

## 🛠️ Kullanılan Teknolojiler

| Kategori           | Teknoloji/Kütüphane                                                                  |
|--------------------|--------------------------------------------------------------------------------------|
| Programlama Dili   | Python                                                                               |
| Grafik Arayüz (GUI)| **PyQt5**                                                                              |
| Çeviri Servisi     | **DeepL API**                                                                        |
| Yerel Veritabanı   | SQLite (kullanıcı ve lisans önbelleği için)                                          |
| Diğer Kütüphaneler | `requests`, `json`, `re`, `hashlib`, `uuid`, `datetime`, `pathlib`, `os`, `sys`, `time` |

---

## ⚙️ Sistem Gereksinimleri
*   **İşletim Sistemi:** **Windows** (Önerilen)
*   **İnternet Bağlantısı:** Lisansın ilk aktivasyonu, periyodik çevrimiçi kontrolü ve DeepL API üzerinden çeviri yapabilmek için gereklidir. Çevrimdışı lisans doğrulama, daha önce çevrimiçi doğrulama yapılmış ve önbelleğe alınmış anahtarlar için sınırlı bir süre geçerlidir.
*   **Geçerli Bir Lisans Anahtarı:** Yazılımı kullanabilmek için bir lisans anahtarı satın almanız gerekmektedir.
*   **DeepL API Anahtarı:** Çeviri özelliğini kullanabilmek için geçerli bir DeepL API (Free veya Pro) anahtarına sahip olmanız ve bunu uygulamaya girmeniz gerekmektedir.

---

## 🚀 Kurulum ve İlk Kullanım
1.  Yazılımın yürütülebilir dosyasını (`.exe`) edinin.
2.  Uygulamayı çalıştırdığınızda bir giriş ekranı ile karşılaşacaksınız.
3.  Size verilen **Lisans Anahtarını** girerek "**Giriş Yap**" butonuna tıklayın.
    *   Lisansınız ilk kez doğrulanıyorsa veya periyodik kontrol gerekiyorsa internet bağlantısı zorunludur.
    *   Doğrulama başarılı olursa, anahtarınız donanım kimliğinizle eşleştirilir ve yerel olarak kaydedilir.
4.  Ana arayüz açıldığında, sol paneldeki "**Çeviri Ayarları**" bölümüne kendi **DeepL API Anahtarınızı** girin ve "**Kontrol Et**" butonu ile geçerliliğini doğrulayın.
5.  "**Dosya İşlemleri**" bölümünden çevirmek istediğiniz `.ass` dosyasını "**Giriş Dosyası**" olarak seçin.
6.  Çevrilmiş dosyanın kaydedileceği yeri ve adını "**Çıkış Dosyası**" olarak belirleyin.
7.  "**Dosyayı Yükle**" butonuna tıklayarak altyazıları tabloya yükleyin.
8.  "**Hedef Dil**" seçiminizi yapın.
9.  "**Çeviriyi Başlat**" butonuna tıklayarak çeviri işlemini başlatın. İlerleme penceresinden süreci takip edebilirsiniz.
10. Çeviri tamamlandıktan sonra, gerekirse tablo üzerinden veya "**Seçili Satırı Düzenle**" butonu ile düzenlemeler yapın.
11. Son olarak, "**Dosyayı Kaydet**" butonu ile çevrilmiş altyazı dosyasını kaydedin.

---

## 📜 Lisans Bilgileri
> Bu yazılım, **GladionStar** tarafından geliştirilmiş **kapalı kaynaklı ve ticari bir üründür**. Kaynak kodları dağıtılmamaktadır ve yazılımın izinsiz kopyalanması, dağıtılması veya üzerinde değişiklik yapılması yasaktır. Yazılımı kullanmak için resmi kanallardan geçerli bir lisans anahtarı edinmeniz gerekmektedir.

---

## 📞 Destek ve İletişim
Yazılımla ilgili soru, sorun veya geri bildirimleriniz için lütfen **https://gladiatorstech.net.tr/** üzerinden bizimle iletişime geçin. 
