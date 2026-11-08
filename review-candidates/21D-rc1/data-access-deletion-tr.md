> SUPERSEDED AUDIENCE NOTE (8 November 2026): This 21D-rc1 candidate predates the owner's later confirmation that MiniVerse Road Puzzle is intended for a general family audience including children, teens and adults. Do not use its prior 13+ or earlier audience wording as the current product decision. See `LEGAL-REVIEW-TR-EN.md` Section 10. The candidate remains a draft and is not publication-approved.

> SADECE İNCELEME ADAYI — Yayımlanmamıştır; yayıncı veya hukukçu onayı verilmiş değildir. İnceleme sürümü: **21D-rc1**, tarih: **2026-11-07**. Önerilen yürürlük kuralı: bütün açık alanlar tamamlanıp malikin ayrıca onayladığı yayın gününde veya açıkça seçtiği daha sonraki tarihte yürürlük; bugün yürürlükte değildir. Kesin tarih: [OWNER_APPROVED_EFFECTIVE_DATE].

Veri sorumlusu/hizmet sağlayıcı: **Barışcan DEDEOĞLU**. Marka: **DEVZASOFT**. Bireysel geliştirici. İletişim: **devzasoft@gmail.com**. Uygulama: **MiniVerse Road Puzzle**, paket: **com.devzasoft.miniverseroadpuzzle**. Konut adresi bu adayda yayımlanmaz. Gerekli resmi başvuru/tebligat kanalının hukuka uygun, konut adresini ifşa etmeyen çözümü yayın öncesi incelenmelidir; e-posta tek başına her şartı karşılıyor sayılmaz.

# Veri Saklama ve Silme Politikası

## Teknik olarak mevcut olanlar
Yerel oyun dosyaları için otomatik gün bazlı genel silme görülmedi. Progress, energy, achievements, preferences, first-launch ve eski age dosyası farklı amaçlarla saklanır. Bazı depolar tmp/bak/corrupt/invalid kopyaları tutar. RewardReceipts içinde makbuz/used/backup kayıtları kalır; süreli makbuz temizliği saptanmadı. Event trace yaklaşık 262144 bayt eşiğiyle bir previous kopyasına döner ve 96 bellek olayı tutar. Callback trace 131072 bayt aşıldığında yeni satır eklemeyi durdurur. Bu ölçüler gün/ay saklama taahhüdü değildir.

## Kullanıcının seçenekleri
Ayarları Sıfırla müzik, efekt, parlaklık, öğretici ve ipucu tercihlerini varsayılan yapar. Bölüm/yıldız/yakıt, dil/ilk açılış, eski yaş, makbuz, SDK veya OS verilerinin tümünü silmez. Önce hangi veriyi silmek istediğinizi belirleyin. Android Ayarlar üzerinden uygulama verisini temizleme yerel ilerlemeyi kaybettirebilir; bunun bir geri alma garantisi yoktur. Bu doküman aşamasında hiçbir veri silinmedi.

Uygulamayı kaldırma uygulamaya ait dosyaların kaldırılmasına yol açabilir; OS/OEM yedekleri, dış posta ve sağlayıcı kayıtları ayrı kalabilir veya yeniden kurulurken geri gelebilir. Mevcut oyun verisine zarar vermeden gerçek backup/restore testi henüz yapılmamıştır. Yedekleri yönetmek için cihaz/OS sağlayıcısının araçları gerekir; geliştiricinin bütün yedekleri uzaktan silebildiği söylenmez.

## Sağlayıcı ve destek kayıtları
UMP reset bir Development test aracıdır; kullanıcının bütün verisini/sunucu kaydını silmez ve gerçek rızayı otomatik değiştirmek için kullanılmaz. Google reklam kimliği OS kontrolü de App Set ID/diğer kayıtların tamamını silme değildir. Google genel retention açıklaması bu uygulamanın her GMA/UMP kaydı için kesin süre sağlamaz. [Google saklama bilgisi](https://policies.google.com/technologies/retention).

Destek posta kutusu [SUPPORT_RETENTION], hak başvuru kayıtları [RIGHTS_REQUEST_RETENTION], sağlayıcı kayıtları [PROVIDER_RETENTION_REGISTER], yerel bozuk/yedek/makbuzların hedef süre ve imha yöntemi [LOCAL_RETENTION_SCHEDULE] olarak tamamlanmalıdır. Gerçekte olmayan otomatik silme planı yayımlanmayacaktır.

## Silme başvurusu
devzasoft@gmail.com ilk iletişim; resmi kanal [FORMAL_REQUEST_CHANNEL]. Talebin kapsamı ve gerçekten erişilen kopyalar belirlenir. Gerekli meşru saklama istisnası varsa somut dayanağı ve sınırı açıklanmalıdır; sınırsız saklama varsayılmaz. Sağlayıcıya yönlendirme, yerel adımlar ve tamamlanan işlemler ayrı bildirilir. Uzaktan erişilmeyen yerel kaydın sunucudan silindiği söylenmez. Kanuni yanıt süreleri, veri saklama süresi değildir.

# Gizlilik Hakları ve İletişim Prosedürü

## Kullanıcı için
İlk iletişim devzasoft@gmail.com. Konuya “MiniVerse — gizlilik talebi” yazabilirsiniz. İstediğiniz işlemi (bilgi/düzeltme/silme/itiraz vb.), ilgili veri türünü ve size yanıt verilebilecek kanalı belirtin. Varsa uygulama sürümü ve sorunun genel açıklaması yardımcı olabilir. Varsayılan olarak reklam kimliği, izin tokenı, parola veya kimlik fotoğrafı göndermeyin. Resmi KVKK başvuru yöntemi/kanuni alanlar [FORMAL_REQUEST_CHANNEL] altında kesinleştirilmelidir; genel destek adresinin otomatik resmi kanal olduğu varsayılmaz.

## Yayıncının uygulayacağı iş akışı
1. [PRIVACY_REQUEST_OWNER] talebi kaydeder; gereksiz ekleri istemez. Kayıt erişimi yetkili kişiyle sınırlanır; gerçek prosedür yayın öncesi onaylanmalıdır.
2. Yerel oyun dosyası, destek postası, Google/UMP veya OS yedeği gibi kapsamı ayırır. Kullanıcıyla ilişkilendirilemeyen veriyi varmış gibi eşleştirmez.
3. Gerekli ve orantılı kimlik/yetki teyidi [REQUEST_VERIFICATION_METHOD] uygulanır; resmi usulün zorunlu alanları güvenli kanalla alınır. Kimlik belgesi toplama varsayılan değildir.
4. Uygulanabilir hukuk, hak/istisna, gerçek erişim ve alıcı rolleri değerlendirilir. Destek kayıtları için erişilebilen işlemler yapılır; OS/Google kontrolündeki kopyalar için uygun yönlendirme bildirilir. Yerel progress'in uzaktan silindiği iddia edilmez.
5. Sonuç ve gerekçe, yapılan işlemler/erişilemeyen kopyalar ve şikâyet yolu kullanıcıya açıklanır. İşlem ispatı [RIGHTS_REQUEST_RETENTION] süresine tabi tutulur; süresiz saklama varsayılmaz.

## Haklar ve süreler
KVKK m.11 hakları ayrı aydınlatmada belirtilmiştir; usulüne uygun talepler en kısa sürede, en geç 30 gün içinde sonuçlandırılmalıdır. GDPR uygulanıyorsa bilgi/erişim/düzeltme/silme/kısıtlama/taşınabilirlik/itiraz ve ilgili rıza geri alma hakları koşullarına göre değerlendirilir; kural olarak en geç bir ay içinde yanıt gerekir. Kanuni uzatma/istisnalar somut gerekçeyle uygulanmalıdır; bu süreler veri saklama planı değildir. Yetkili makama şikâyet hakkı saklıdır. Çocuk/temsilci taleplerinde yetki/menfaat ayrıca incelenir; tüm gençler yetişkin sayılmaz.

## Hesap silme ve izin ayrımı
Oyunda kullanıcı hesabı yoktur; olmayan hesap için silme ekranı vaat edilmez. Yerel veri temizleme ilerlemeyi kaybettirebilir; ayar sıfırlama toplu silme değildir. UMP tercihini değiştirme, şart kabulünü geri alma, cihaz reklam kimliği kontrolü ve veri silme birbirinden farklıdır. Privacy Options gerekli/uygun olduğunda mevcut Settings yoludur; gerçek form kanıtı aşağıda belirtilen Development teşhis testiyle sınırlıdır.

[KVKK başvuru](https://www.kvkk.gov.tr/Icerik/2062/Basvuru-Hakki), [süreler](https://www.kvkk.gov.tr/Icerik/5358/Kamuoyu-Duyurusu), [AB taleplere yanıt](https://commission.europa.eu/law/law-topic/data-protection/information-business-and-organisations/dealing-requests-individuals_en). Yayın öncesi resmi kanal ve operasyon sorumlusu tamamlanmalıdır.
## Teknik doğrulama kapsamı — yayın iddiası değildir
7 Kasım 2026 tarihli Stage21B.3 testinde Android 15 üzerindeki Development-only, reklamları engelleyen teşhis yolunda gerçek UMP 4.0.0 EEA debug formu, kapanış callback'i, Privacy Options, kullanıcının tercih değişikliği ve yeniden başlatma sonrası SDK durumunun korunması gözlendi. Güncel cihaz hash'i yalnız yerel test dosyasındadır. ABD eyaleti ve Other debug denemeleri form gerekmediği sonucunu verdi; her ülkenin hukuki uygunluğu doğrulanmış değildir. Çevrimdışı güncelleme hata kodu 2 ile sonuçlandı; reklamlar açılmadı. Bu, yayımlanmış Production akışının veya tam ağ/veri davranışının doğrulanması değildir. UMP sıfırlama, veri silme veya Terms kabulü yapılmadı. Gizlilik formu tercihi bütün sağlayıcı verilerinin silinmesi değildir.

Son incelenen Development APK'da AD_ID ve AdServices izinleri ile MobileAdsInitProvider bulunmadı; SDK kütüphaneleri yine paketteydi. Kesin son Release manifesti, veri içerikleri, alternatif tanımlayıcılar ve Backup/Restore kapsamı ayrıca doğrulanmalıdır. Formdaki genel sağlayıcı/konum açıklaması, oyunun GPS izni istediğinin kanıtı değildir. Güncel izin kapıları eksikliği aşmak için kaldırılmaz.
