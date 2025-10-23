1. Konuya giriş: Anten ne işe yarar?

Bir anten, elektriksel sinyalleri elektromanyetik dalgaya çeviren (veya tam tersi işi yapan) bir cihazdır.
Yani:

Vericide: Elektrik akımını → Radyo dalgasına çevirir 📡

Alıcıda: Radyo dalgasını → Elektrik akımına çevirir 🎧

Kısaca anten, cihazla hava arasındaki köprüdür. (Wi-Fi sinyalinin “ruhu” gibi düşünebilirsin 😂)

🌊 2. Propagasyon (yayılım) nedir?

“Propagasyon”, elektromanyetik dalgaların havada, uzayda veya diğer ortamlarda nasıl yayıldığını inceleyen konudur.
Bir sinyal, kaynaktan çıktıktan sonra boşlukta "hop" diye gitmez; yol boyunca bir sürü şey olur:

Yayılım türleri:

Yansıma (Reflection): Dalga duvara, dağa, binaya çarpar ve geri döner.

Kırılma (Refraction): Ortam değişirse (örneğin hava → su), yön değiştirir.

Saçılma (Scattering): Küçük nesneler (yağmur, toz vs.) dalgayı dağıtır.

Difraksiyon (Bükülme): Dalga engelin arkasına “kıvrılarak” geçebilir.

Bu olaylar yüzünden sinyal bazen zayıflar, gecikir veya parazitlenir. Yani “çekmiyor yaa” dediğin olay tamamen propagasyonun eseri 😅

📏 3. Temel kavramlar
📶 Frekans (f)

Dalganın saniyede kaç titreşim yaptığı.
Yüksek frekans → kısa dalga boyu → daha yüksek veri aktarımı ama kısa menzil.
Düşük frekans → uzun dalga boyu → daha geniş kapsama ama düşük hız.

🌐 Dalga boyu (λ)

Formül:

λ = c / f
(c = ışık hızı ≈ 3×10⁸ m/s)

📡 Kazanç (Gain)

Anteni “yönlü” hale getirir.
Bazı antenler her yöne yayın yapar (omnidirectional), bazıları sadece belirli bir yöne (directional).
Kazanç arttıkça menzil uzar ama kapsama alanı daralır.

🧩 4. Anten çeşitleri
Anten tipi	Görünüşü / Kullanımı	Özellik
Dipol	En temel anten türü	Teorik temel, her şey bunun üzerinden anlatılır
Yagi-Uda	TV anteni gibi	Yönlü, yüksek kazançlı
Parabolik (çanak)	Uydu anteni	Çok yüksek yönlülük
Monopole	Araç üzerindeki çubuk anten	Pratik, düşük frekanslarda iyi
Patch (mikroşerit)	Telefonlarda, Wi-Fi'da	Küçük boyutlu, yüksek frekanslı
Helix (spiral)	Uzay haberleşmesi	Dairesel polarizasyon sağlar
📡 5. Propagasyon türleri (detaylı)
Tür	Nerede görülür	Açıklama
Uzay dalgası	Uydular, radarlar	Havadaki direkt yol
Yeryüzü dalgası (ground wave)	AM radyo	Dünya yüzeyini takip eder
Gökyüzü dalgası (sky wave)	Kısa dalga radyo	İyonosferden yansıyıp uzun mesafe kat eder
⚙️ 6. Gerçek dünyada uygulamalar

📱 Telefon sinyalleri

🛰️ GPS ve uydular

📶 Wi-Fi / Bluetooth

📻 Radyo-TV yayınları

🚗 Araç radar sistemleri

⚔️ Askerî haberleşme sistemleri

Hepsi “anten” + “propagasyon” fiziğine dayanır.

🧠 Kısa özet (ezberlik mini tablo)
Kavram	Açıklama
Anten	Elektrik ↔ EM dalga dönüşümü
Propagasyon	Dalgaların yayılması
Kazanç	Antenin yönlü gücü
Polarizasyon	Dalganın titreşim yönü
Yansıma / Kırılma	Dalganın ortamla etkileşimi
⚙️ 1. Anten Kazancı (Gain)

Kazanç, antenin enerjiyi belirli bir yöne yoğunlaştırma yeteneğini ölçer.
Yani “aynı gücü her yöne saçmak yerine belli bir yöne basmak” olayı.

Formül:

G = (4π × Aₑ) / λ²

G → kazanç (boyutsuz veya dBi cinsinden)

Aₑ → efektif alan

λ → dalga boyu

Ama genelde kazanç dB cinsinden verilir:

G(dB) = 10 × log₁₀(G)

📏 2. dB (desibel) sistemi – Kısaca nasıl düşünmelisin

dB, güç farklarını logaritmik olarak ifade eder.
Çünkü elektromanyetik sistemlerde güç farkları genelde çok büyük olur.

Durum	Anlamı
+3 dB	Güç 2 katına çıktı
+10 dB	Güç 10 katına çıktı
-3 dB	Güç yarıya düştü
-10 dB	Güç 1/10’una düştü

Örnek:
Bir antenin kazancı 6 dB → 4 kat güç yoğunluğu demek.
(Çünkü 3 dB ≈ 2x, 6 dB ≈ 4x)

🎯 3. Yönlülük (Directivity, D)

Antenin enerjiyi ne kadar dar bir alana yönlendirdiğini gösterir.
Yönlülük sadece geometrik bir özelliktir, kayıpları hesaba katmaz.

Formül:

D = 4π / Ω

Ω → Radyasyon açısı (steradyan cinsinden)

Kazançla arasındaki fark:

G = η × D

Burada η (eta) → anten verimliliği (% değer)
Yani verimsizlik varsa kazanç, yönlülükten düşük olur.

🔋 4. Anten Verimliliği (Efficiency, η)

Gerçek hayatta antenin bir kısmı ısınıp kaybolur (özellikle metal kayıpları, direnç, bağlantı zayıflıkları).

η = (Radyasyon gücü) / (Toplam giriş gücü)

Yani %100 verim → sıfır kayıp, tam mükemmel anten (hayal dünyası 😅)

🌐 5. Radyasyon Diyagramı (Radiation Pattern)

Bu, antenin hangi yöne ne kadar enerji yaydığını gösteren bir grafiktir.

Genelde iki şekilde çizilir:

Polar (daire biçiminde) → yönelimi gösterir

3D diyagram → tam uzaysal dağılım

Kavramlar:

Ana lob (Main lobe): En güçlü sinyal yönü

Yan loblar (Side lobes): İstenmeyen küçük yönlerdeki yayılım

Arka lob (Back lobe): Tam ters yöndeki sızıntı

Basitçe:

Omnidirectional anten → her yöne eşit (Wi-Fi çubukları gibi)

Directional anten → tek yönde güçlü (Yagi, çanak vs.)

💫 6. Anten Polarizasyonu

Polarizasyon, elektrik alan vektörünün yönüdür.

Tür	Açıklama
Dikey (Vertical)	E alanı dikey, çoğu radyo anteni böyle
Yatay (Horizontal)	TV antenleri genelde böyle
Dairesel (Circular)	Uydu ve GPS sistemleri (dönerek gider, yön bağımsızdır)

Polarizasyonlar uyuşmazsa sinyal ciddi zayıflar.
Yani bir dikey anten, yatay anteni iyi duyamaz — tıpkı “frekans uyuşmazlığı” gibi 🎧

🚀 7. Friis İletim Denklemi (çok klasik ama önemli)

Bu formül, verici-anteni-alıcı arasındaki güç ilişkisini anlatır:

Pᵣ = Pₜ × Gₜ × Gᵣ × (λ / (4πR))²

Pᵣ → alıcıda alınan güç

Pₜ → vericide gönderilen güç

Gₜ, Gᵣ → anten kazançları

R → iki anten arası mesafe

λ → dalga boyu

Bu formül, sinyalin mesafeyle karesel olarak zayıfladığını gösterir.
Yani “2 kat uzaklaşınca sinyal 4 kat azalır.”

🛰️ 8. Propagasyonun zorlayıcı etkileri
Etki	Sonuç	Örnek
Fading (Sönümleme)	Sinyal dalgalanır	Telefonun bazen çekip bazen kesilmesi
Multipath	Aynı sinyal farklı yollardan gelir	Eko veya parazit oluşur
Path loss	Uzaklığa bağlı zayıflama	Uydudan gelen sinyalin çok düşük olması
📚 Mini Özet:
Terim	Anlamı
G (Kazanç)	Yönlülük + verimlilik
D (Yönlülük)	Enerji yoğunluğu, kayıpsız hali
η (Verimlilik)	Enerji kayıplarını gösterir
Polarizasyon	Dalga titreşim yönü
Radiation Pattern	Antenin enerji haritası
🎓 Eğer sen yazılım mühendisliği okuyorsan:

"Antenler ve Propagasyon" dersi doğrudan senin alanının ana gövdesi değil.
Amaaa... bazı özel alanlarda inanılmaz işine yarayabilir:

Alan	Neden önemli?
📡 Gömülü sistemler / IoT (Internet of Things)	Cihazların kablosuz haberleşmesi anten fiziğine dayanır. (Wi-Fi, Bluetooth, Zigbee, LoRa, vs.)
🚗 Otonom sistemler / sensör teknolojisi	Radar, lidar, ultrasonik sistemler hep dalga yayılımıyla ilgilidir.
🛰️ Uydu haberleşmesi	Uzay teknolojileri, savunma sistemleri, GPS sinyalleri = propagasyon fiziği
📶 Telekom / 5G / Ağ mühendisliği	Frekans, sinyal zayıflaması, anten kazancı… hepsi burada öğreniliyor.
🧠 Yapay zeka + Haberleşme birleşimi	“Smart antenna systems”, “beamforming” gibi kavramlar sinyal işleme + AI birleşimi.

Yani eğer senin hedefin:

“Ben sadece web & app geliştiricem, backend & frontend”
diyorsan bu ders çok da kritik değil, ama genel kültür olarak bilmen fena olmaz.

Ama diyorsan ki:

“Ben sensörler, görüntü işleme, radar, savunma teknolojisi, IoT, drone’lar gibi işlerle uğraşacağım,”
o zaman bu ders temel taşı gibi.

🧩 Kısacası:
Hedef	Gereklilik
Web / mobil / klasik yazılım	⚪ Temel bilmek yeter
IoT, sinyal işleme, sensör sistemleri	🟡 Orta seviye şart
Savunma, haberleşme, radar sistemleri	🔴 Derinlemesine bilmen lazım
👀 Benim tavsiyem:

Bu dersi tamamen ezber olarak değil de,
“sinyallerin havada nasıl hareket ettiğini” anlamak için öğren.
Çünkü o mantığı bir kez kaptığında, ileride gördüğün:

Wi-Fi anteni

GPS modülü

Bluetooth sensörü

hatta radar veri seti

hepsi "hah işte propagasyon!" diye gözünün önüne gelir.
📡 Antenler ve Propagasyon Dersi – Kapsamlı Özet Not
🧠 1. Giriş: Anten Nedir?

Bir anten, elektriksel sinyalleri elektromanyetik dalgalara dönüştüren (veya tam tersini yapan) bir sistemdir.
Yani, elektronik devre ile “hava” arasında köprü görevi görür.

Verici anten: Elektrik akımını elektromanyetik dalgaya dönüştürür.

Alıcı anten: Elektromanyetik dalgayı tekrar elektrik sinyaline çevirir.

Örnek:

Wi-Fi anteni → modemin sinyalini havaya yollar.

Radyo anteni → yayını yakalayıp sese çevirir.

🌊 2. Propagasyon (Yayılım) Nedir?

Propagasyon, elektromanyetik dalgaların ortamda nasıl yayıldığını inceleyen bilim dalıdır.

🔄 Temel Yayılım Türleri:
Tür	Açıklama	Örnek
Yansıma (Reflection)	Dalga bir yüzeye çarpar ve geri döner.	Bina, dağ, deniz yüzeyi
Kırılma (Refraction)	Dalga farklı yoğunlukta ortama geçerken yön değiştirir.	Hava ↔ Su geçişi
Saçılma (Scattering)	Küçük parçacıklara çarpıp dağılır.	Yağmur, sis, toz
Difraksiyon (Bükülme)	Dalga engelin arkasına kıvrılarak geçer.	Köşe arkasından sinyal almak
⚙️ 3. Temel Kavramlar
🔢 Frekans (f)

Bir dalganın saniyedeki titreşim sayısıdır.
Birim: Hertz (Hz)

Yüksek frekans = kısa dalga boyu = yüksek hız, kısa menzil

📏 Dalga Boyu (λ)

Dalga boyu, bir dalganın iki tepe noktası arasındaki mesafedir.
Formül:

λ = c / f
(c = ışık hızı ≈ 3×10⁸ m/s)

📡 Kazanç (Gain, G)

Antenin enerjiyi belirli bir yöne yoğunlaştırma gücüdür.

G = (4π × Aₑ) / λ²
veya
G(dB) = 10 × log₁₀(G)

Yüksek kazanç = güçlü yönlendirme, ama dar kapsama alanı.

🎯 Yönlülük (Directivity, D)

Anteni sadece “şekil olarak” düşünür — yani kayıpsız durumda enerjiyi ne kadar dar bir alana yoğunlaştırabiliyor.

D = 4π / Ω
(Ω → antenin toplam radyasyon açısı)

Kazançla ilişkisi:

G = η × D
Burada η → anten verimliliği

🔋 Verimlilik (Efficiency, η)

Antenin aldığı gücün ne kadarını yayabildiğini gösterir.

η = (Radyasyon Gücü) / (Toplam Giriş Gücü)

Kaynakta 100 W varsa, 80 W yayılıyorsa verimlilik %80’dir.

📊 4. Radyasyon Diyagramı (Radiation Pattern)

Antenin enerjiyi hangi yöne ve ne kadar yaydığını gösteren grafiktir.
2D (polar) veya 3D olarak çizilir.

🧭 Terimler:
Terim	Açıklama
Ana lob (Main lobe)	En güçlü sinyal yönü
Yan loblar (Side lobes)	İstenmeyen yayılım alanları
Arka lob (Back lobe)	Tam ters yöndeki enerji sızıntısı

Yönlü anten: Enerjiyi belirli yöne toplar.
Yönsüz anten: Her yöne eşit yayar.

🧲 5. Polarizasyon

Polarizasyon, dalganın elektrik alan vektörünün yönüdür.

Tür	Açıklama	Kullanım
Dikey (Vertical)	E alanı dikey	Mobil antenler, telsiz
Yatay (Horizontal)	E alanı yatay	TV yayınları
Dairesel (Circular)	E alanı döner	Uydu haberleşmesi, GPS

Uyarı:
Polarizasyonlar farklıysa sinyal ciddi zayıflar. (Dikey anten yatay anteni iyi duymaz.)

🛰️ 6. Yayılım (Propagasyon) Türleri
Tür	Açıklama	Kullanım Alanı
Yeryüzü dalgası (Ground wave)	Dünya yüzeyini takip eder.	AM radyo
Uzay dalgası (Space wave)	Doğrudan veya yansımayla iletilir.	FM, TV, Mikrodalga
Gökyüzü dalgası (Sky wave)	İyonosferden yansıyarak uzun mesafeye gider.	Kısa dalga radyo
🔭 7. Friis İletim Denklemi

Verici ile alıcı arasındaki güç ilişkisini açıklar:

Pᵣ = Pₜ × Gₜ × Gᵣ × (λ / (4πR))²

Sembol	Açıklama
Pᵣ	Alıcıdaki güç
Pₜ	Vericideki güç
Gₜ	Verici anten kazancı
Gᵣ	Alıcı anten kazancı
R	Mesafe
λ	Dalga boyu

Sonuç:
Uzaklık iki katına çıkarsa sinyal gücü 4 kat azalır.

(Inverse Square Law)

💥 8. Propagasyonda Karşılaşılan Sorunlar
Etki	Açıklama	Sonuç
Fading (Sönümleme)	Sinyalin zayıflayıp güçlenmesi	Bağlantı kopmaları
Multipath	Aynı sinyalin farklı yollardan ulaşması	Gecikme, eko, parazit
Path Loss	Uzaklığa bağlı sinyal azalması	Düşük güçte alım
Shadowing	Engeller nedeniyle gölgelenme	Sinyal çekmemesi
📡 9. Anten Türleri
Anten Tipi	Görünüm / Kullanım	Özellik
Dipol	En temel anten	Teorik model, dengeli yapı
Monopole	Yarım dipol, toprak düzlemi üzerinde	Araç antenleri
Yagi-Uda	TV anteni gibi	Yönlü, yüksek kazanç
Parabolik (Çanak)	Uydu anteni	Çok yüksek yönlülük
Patch (Mikroşerit)	Telefon, Wi-Fi	Küçük boyutlu, düz yapı
Helix (Helisel)	Uzay iletişimi	Dairesel polarizasyon sağlar
🔢 10. dB Hesaplamaları (Kısa Rehber)
Artış/Azalış	Güç Oranı	Açıklama
+3 dB	2x	Güç iki katı
+10 dB	10x	Güç on katı
-3 dB	0.5x	Güç yarısı
-10 dB	0.1x	Güç onda biri

Formül:

dB = 10 × log₁₀(P₂ / P₁)

🧩 11. Özet Tablo
Kavram	Sembol	Açıklama
Kazanç	G	Yönlülük + verimlilik
Yönlülük	D	Antenin enerjiyi yönlendirme gücü
Verimlilik	η	Enerji kaybı oranı
Polarizasyon	-	Dalga yönü
Dalga Boyu	λ	c / f
Radyasyon Diyagramı	-	Antenin enerji dağılım haritası
Friis Denklemi	-	Güç yayılım ilişkisi
🎓 12. Gerçek Hayattaki Uygulamalar

📶 Wi-Fi ve Bluetooth sistemleri

📡 GSM baz istasyonları

🛰️ Uydu haberleşmesi

🚗 Araç radarları

🔐 Savunma sistemleri (Radar, Jammer, vs.)

🤖 IoT (Nesnelerin İnterneti) cihazları

💡 13. Dersin Önemi
Alan	Bu Dersin Önemi
Web / Mobil Yazılım	⚪ Genel kültür seviyesinde bilmek yeter
IoT, Gömülü Sistemler	🟡 Anten ve sinyal mantığını anlamak gerekli
Savunma, Haberleşme, Uydu	🔴 Derinlemesine öğrenmek şart
AI + Donanım (Akıllı sistemler)	🟡 Temel düzeyde bilinmeli
🧠 14. Kapanış: Akılda Kalıcı Cümleler

Anten, “cihazın sesi”dir.

Propagasyon, “sinyalin yolu”dur.

Kazanç yönlülükle gelir, verimlilikle yaşar.

Polarizasyon uymazsa, sinyal küser. 😄
📘 Antenler ve Propagasyon – Çizimler + Formüllerle Notlar
🧩 1. Temel Anten Modeli: Dipol Anten
🎯 Tanım:

Dipol anten, en temel anten yapısıdır.
İki iletken çubuktan oluşur, genelde yarım dalga boyu (λ/2) uzunluğundadır.

     |<---- λ/4 ---->|<---- λ/4 ---->|
     -----------------|-----------------
                     |
                   Besleme noktası

Özellikleri:

Simetrik yapıya sahiptir.

En çok 3 boyutlu olarak “donut” (simite benzer) şeklinde enerji yayar.

Polarizasyonu, antenin eksenine paraleldir (genelde dikey).

Temel Formül:

L = λ / 2
(L = anten boyu, λ = dalga boyu)

🚗 2. Monopole (Yarım Dipol) Anten
🎯 Tanım:

Dipol antenin yarısı, iletken bir yüzey (toprak) üzerine yerleştirilirse monopole anten oluşur.

        |
        |
       / \
      /   \
     -------
     Toprak düzlemi

Özellikleri:

Gerçek boyu: λ/4

Yere monte edilir (araç antenleri gibi).

Dipole göre yarı yükseklikte ama aynı kazanca sahiptir.

📡 3. Yagi–Uda Anteni
🎯 Tanım:

Yönlü, yüksek kazançlı anten türüdür.
Bir sürü paralel metal çubuktan oluşur.

| Reflector | Driven | Director | Director | Director |
|------------|--------|-----------|-----------|-----------|

Yapısı:

1 adet Reflektör (yansıtıcı)

1 adet Driven Element (aktif anten)

1+ adet Director (yönlendirici çubuklar)

Özellikleri:

TV antenleri buna örnektir.

Yönlülük ve kazanç çok yüksektir.

Dar açılı radyasyon diyagramına sahiptir.

☄️ 4. Parabolik (Çanak) Anten
🎯 Tanım:

Bir parabol yüzey ve odak noktasında bir anten elemanından oluşur.
Yansıtıcı yüzey, sinyalleri tek noktaya odaklar.

        /\
       /  \
      /    )----> Odak noktası (feed)
     /____/

Özellikleri:

Yüksek kazanç: 30–50 dB

Çok yönlü değil, tek bir doğrultuda yayın yapar.

Uydu haberleşmesi, radar, mikrodalga linklerinde kullanılır.

Formül:

G ≈ (πD / λ)² × η

Sembol	Anlam
D	Çap (metre)
λ	Dalga boyu
η	Verimlilik (0.5–0.7 arası genelde)
📱 5. Patch (Mikroşerit) Anten
🎯 Tanım:

İnce bir metal plaka (patch) ile toprak düzlemi arasına yerleştirilmiş, küçük ve düz anten yapısıdır.

 -----------------   ← Patch (İletken)
 |   Dielectric   |  ← Yalıtkan tabaka
 -----------------   ← Ground Plane

Özellikleri:

Küçük boyut → cep telefonu, Wi-Fi, drone gibi cihazlarda yaygın.

Genellikle mikrodalga frekanslarında (2–10 GHz) çalışır.

Üretimi kolay ve ucuzdur.

🌀 6. Helisel (Helix) Anten
🎯 Tanım:

Spiral şeklinde sarılmış tel yapısı.
Genellikle dairesel polarizasyon elde etmek için kullanılır.

       /\
      /  \
     /    \
    /      \
   /________\

Özellikleri:

Polarizasyonu daireseldir.

Uzay haberleşmesi ve GPS sistemlerinde tercih edilir.

Yüksek kazanç sağlar.

⚙️ 7. Radyasyon Diyagramı (Radiation Pattern)
🎯 Tanım:

Antenin enerjiyi hangi yönde ne kadar yaydığını gösteren grafik.

1) Polar (2D) Görünüm:

          ↑ Ana Lob
        .-' '.
     .-'       '-.
    (    Anten     )
     '-.       .-'
        '-._.-'


Main lobe: En güçlü yön

Side lobes: İstenmeyen küçük yayılımlar

Back lobe: Ters yöndeki sızıntı

2) 3D Görünüm:
Bir simit (donut) şeklinde enerji dağılımı (dipol anten için klasik görünüm).

📈 8. Friis İletim Denklemi

Amaç: Verici ile alıcı arasındaki güç ilişkisini hesaplamak.

Pᵣ = Pₜ × Gₜ × Gᵣ × (λ / (4πR))²

Sembol	Anlam
Pᵣ	Alıcı gücü (W)
Pₜ	Verici gücü (W)
Gₜ	Verici anten kazancı
Gᵣ	Alıcı anten kazancı
λ	Dalga boyu
R	Mesafe (m)

dB formunda:

Pᵣ(dB) = Pₜ(dB) + Gₜ(dB) + Gᵣ(dB) - 20log₁₀(4πR/λ)

⚡ 9. Yönlülük (Directivity) Formülü

D = 4π / Ω

Sembol	Anlam
D	Yönlülük
Ω	Radyasyon açısı (steradyan)
🔋 10. Verimlilik (Efficiency)

η = Pᵣadiated / Pinput

η = 1 (veya %100) → kayıpsız anten

Gerçekte %70–90 arasıdır.

🧮 11. Anten Kazancı (Gain)

G = η × D
veya
G(dB) = 10 × log₁₀(G)

📶 12. dB Hesap Örnekleri
Güç Oranı	dB	Anlam
2x	+3 dB	Güç iki katına çıktı
10x	+10 dB	Güç on katına çıktı
0.5x	-3 dB	Güç yarıya düştü
0.1x	-10 dB	Güç onda birine indi
💡 13. Polarizasyon Türleri (Görsel)
1️⃣ Dikey (Vertical)    → | | | |
2️⃣ Yatay (Horizontal)  → ------
3️⃣ Dairesel (Circular) → 🔄 spiral

🧭 14. Özet: Anten Tipleri Karşılaştırma Tablosu
Anten Türü	Frekans Aralığı	Polarizasyon	Kazanç	Kullanım Alanı
Dipol	30 MHz – 3 GHz	Dikey / Yatay	Orta	Radyo, TV
Monopole	< 1 GHz	Dikey	Orta	Araç, baz istasyonu
Yagi-Uda	30–300 MHz	Yatay	Yüksek	TV, telsiz
Parabolik	1–100 GHz	Dairesel	Çok Yüksek	Uydu, radar
Patch	1–10 GHz	Dikey / Yatay	Orta	Wi-Fi, telefon
Helisel	1–10 GHz	Dairesel	Yüksek	GPS, uzay iletişimi
🧠 15. Ezberlik Kısa Özet
Kavram	Formül / Tanım
Dalga Boyu	λ = c / f
Friis Denklemi	Pᵣ = Pₜ × Gₜ × Gᵣ × (λ / (4πR))²
Kazanç	G = η × D
Yönlülük	D = 4π / Ω
Verimlilik	η = Pᵣadiated / Pinput
Polarizasyon	Dalgadaki E alan yönü
💬 16. Kapanış Cümlesi

Anten, cihazın “ağzıdır”; propagasyon, “sözünün gittiği yoldur.”
Kazançla bağırır, yönlülükle hedef alır, verimlilikle etkili konuşur. 😎📡
⚡ Antenler ve Propagasyon — Dersin Mantığı
🎯 Temel fikir:

Bu dersin olayı şudur:

“Elektrik sinyalini havaya nasıl göndeririz ve o sinyal havada nasıl davranır?”

Yani elektriksel enerjiyi elektromanyetik dalga hâline getirip uzaya yaymak, sonra da onu başka bir yerde geri yakalamak.

🧩 1. Anten ne yapar?

Bir anten:

Vericide: Elektrik akımını → Elektromanyetik dalgaya dönüştürür

Alıcıda: Elektromanyetik dalgayı → Elektrik akımına dönüştürür

Yani anten, cihazla uzay arasında köprü gibidir.

Basit örnek:
Wi-Fi sinyalin modemden çıkıyor → havada dolaşıyor → laptop anteni onu yakalıyor.
Bu iki cihazın “konuştuğu dil” elektromanyetik dalgalardır.

🌊 2. Propagasyon ne yapar?

“Propagasyon” = yayılım demek.
Dalga bir kez havaya salındıktan sonra, o dalganın:

Nasıl hareket ettiğini,

Nereye kadar ulaştığını,

Ne kadar zayıfladığını
inceleyen kısım.

Dalga yayılırken başına neler gelir?

Yansıma (Reflection) – duvara, dağa, binaya çarpar ve geri döner

Kırılma (Refraction) – farklı yoğunluktaki ortama girince yön değiştirir

Saçılma (Scattering) – yağmur, toz gibi küçük parçacıklar sinyali dağıtır

Difraksiyon (Bükülme) – engelin arkasına kıvrılarak geçer

Bu olaylar yüzünden sinyal bazen zayıflar, kayar ya da gecikir.

📐 3. Dalganın doğası

Elektromanyetik dalga iki bileşenden oluşur:

Elektrik alan (E)

Manyetik alan (H)

Bu iki alan birbirine dik olarak titreşir,
ve dalga ışık hızıyla (c ≈ 3×10⁸ m/s) yayılır.

Dalga boyu (λ) – Frekans (f) ilişkisi:

λ = c / f

Frekans yükseldikçe dalga boyu kısalır.

Dalga boyu kısaldıkça anten boyutu da küçülür.

Örnek:

FM radyo (100 MHz) → uzun dalga boyu → büyük anten

Wi-Fi (2.4 GHz) → kısa dalga boyu → küçük anten

📡 4. Antenlerin yönü ve kazancı

Bir anten her yöne eşit yayın yapmaz.
Bazıları belirli bir yöne odaklanır (örneğin radar antenleri).

Bu odaklanma “anten kazancı (gain)” ile ölçülür.
Bir nevi ses yükseltici gibi düşün:
Aynı gücü tek yöne odaklarsan, o yönde sinyal çok daha güçlü olur.

🔁 5. Propagasyon türleri

Sinyalin gittiği ortam ve mesafeye göre farklı yayılım yolları vardır:

Tür	Açıklama	Nerede kullanılır
Yeryüzü dalgası (Ground Wave)	Dünya yüzeyini takip eder	AM radyo
Uzay dalgası (Space Wave)	Doğrudan hat üzerinde gider	TV, Wi-Fi, radar
Gökyüzü dalgası (Sky Wave)	İyonosferden yansır	Kısa dalga yayınları, uzun mesafe iletişim
📉 6. Sinyal zayıflaması (attenuation)

Dalga yayılırken gücü azalır.
Sebep: mesafe, ortam kaybı, yansıma, nem, yağmur vs.
Formül genelde şu mantıkla gider:

Güç ∝ 1 / (mesafe²)

Yani uzaklaştıkça sinyal karesel oranda zayıflar.

🧠 7. Dersin altındaki mantık

Bütün bu konuların altında şu fikir yatar:

“Bilgi, enerjiye yüklenir; enerji dalgaya dönüşür; dalga havada yayılır.”

Sen o dalganın:

Nasıl üretildiğini,

Nasıl yayıldığını,

Nasıl alındığını
anladığında, kablosuz iletişimin tüm prensibini çözmüş oluyorsun.

🚀 8. Gerçek dünyaya bağlantı
Alan	Nerede karşına çıkar
📱 Mobil haberleşme	GSM, 4G, 5G baz istasyonları
🛰️ Uydu sistemleri	GPS, uzay iletişimi
🏠 IoT cihazları	Akıllı ev sensörleri
🚗 Otonom sistemler	Radar, lidar sensörleri
⚙️ Savunma sanayi	Jamming, radar, telsiz sistemleri
🧩 9. Özet Mantık Şeması
Elektrik sinyali ──► Anten ──► Elektromanyetik dalga
                         │
                         ▼
                (Hava, uzay, ortam)
                         │
                         ▼
                     Alıcı anten ──► Elektrik sinyali

🎯 Sonuç

Bu dersin amacı sana şunu öğretmek:

“Bir sinyalin kaynaktan çıkıp hedefe ulaşana kadar başına neler geldiğini fiziksel olarak anlayabilmek.”

Eğer bu mantığı kavrarsan, o zaman:

IoT cihaz tasarlarken neden anteni oraya koyduğunu,

Wi-Fi neden duvarın arkasında zayıfladığını,

Radar neden bazı açılarda nesneyi görmediğini
kendin çözebilirsin.
📐 Antenler ve Propagasyon — Matematiksel Mantığı
⚡ 1. Sinyal gücü nasıl hesaplanır?

Bir anten bir sinyal gönderdiğinde, sinyal uzaklaştıkça zayıflar.
Çünkü enerji geniş bir alana yayılır.
Bu zayıflamayı hesaplamak için kullandığımız en temel formül:

➤ Friis Yayılım Denklemi
𝑃
𝑟
=
𝑃
𝑡
+
𝐺
𝑡
+
𝐺
𝑟
−
𝐿
𝑝
P
r
	​

=P
t
	​

+G
t
	​

+G
r
	​

−L
p
	​


veya logaritmik olmayan haliyle:

𝑃
𝑟
=
𝑃
𝑡
×
𝐺
𝑡
×
𝐺
𝑟
×
(
𝜆
4
𝜋
𝑑
)
2
P
r
	​

=P
t
	​

×G
t
	​

×G
r
	​

×(
4πd
λ
	​

)
2
Ne ifade ediyor bunlar?
Sembol	Açıklama

𝑃
𝑡
P
t
	​

	Verici antenin gönderdiği güç (Watt)

𝐺
𝑡
G
t
	​

	Verici anten kazancı

𝐺
𝑟
G
r
	​

	Alıcı anten kazancı

𝜆
λ	Dalga boyu (c / f)

𝑑
d	Antenler arası mesafe

𝐿
𝑝
L
p
	​

	Yayılım kaybı (path loss, dB)

𝑃
𝑟
P
r
	​

	Alıcı antenin aldığı güç
🎯 2. Path Loss (Yayılım Kaybı)

Dalga uzaklaştıkça sinyalin enerjisi “yayıldığı alan” kadar zayıflar.
Mantık şu:

Enerji sabit ama kapsadığı yüzey büyüyor → Yoğunluk düşüyor.

Bu kayıp genelde logaritmik (dB) ölçülür.

Formül:
𝐿
𝑝
(
𝑑
𝐵
)
=
20
log
⁡
10
(
𝑑
)
+
20
log
⁡
10
(
𝑓
)
−
147.55
L
p
	​

(dB)=20log
10
	​

(d)+20log
10
	​

(f)−147.55

(Burada 
𝑑
d metre, 
𝑓
f Hz cinsinden)

Örnek:

Wi-Fi frekansı = 2.4 GHz
Mesafe = 10 m

𝐿
𝑝
=
20
log
⁡
10
(
10
)
+
20
log
⁡
10
(
2.4
×
10
9
)
−
147.55
L
p
	​

=20log
10
	​

(10)+20log
10
	​

(2.4×10
9
)−147.55
𝐿
𝑝
≈
20
+
187.6
−
147.55
≈
60
 dB
L
p
	​

≈20+187.6−147.55≈60 dB

Yani 10 metrede 60 dB kadar sinyal kaybı olur.
(dB cinsinden her 3 dB = yaklaşık %50 güç kaybı demektir.)

📡 3. Anten kazancı (Gain)

Anten kazancı, antenin enerjiyi belirli bir yöne ne kadar iyi odaklayabildiğini gösterir.
Tıpkı el fenerini dar açıya getirince ışığın daha uzağa gitmesi gibi.

Formül:
𝐺
=
4
𝜋
𝐴
𝑒
𝜆
2
G=
λ
2
4πA
e
	​

	​

Sembol	Anlamı

𝐺
G	Anten kazancı

𝐴
𝑒
A
e
	​

	Antenin etkin alanı (m²)

𝜆
λ	Dalga boyu

Kazanç genelde dB cinsinden yazılır:

𝐺
(
𝑑
𝐵
)
=
10
log
⁡
10
(
𝐺
)
G(dB)=10log
10
	​

(G)

Yani:
Kazanç ne kadar büyükse → sinyal o yönde o kadar güçlü.
Ama aynı zamanda kapsama alanı daralır.

🧩 4. Dalga boyu (λ) ve Frekans (f)

Bunlar birbirinin ters orantılısıdır:

𝜆
=
𝑐
𝑓
λ=
f
c
	​

Frekans	Dalga boyu	Kullanım
100 MHz	3 metre	FM Radyo
2.4 GHz	12.5 cm	Wi-Fi
5 GHz	6 cm	Modern Wi-Fi
24 GHz	1.25 cm	Radar

Kısacası:
Frekans artarsa → dalga boyu kısalır → anten küçülür ama menzil düşer.

📉 5. Desibel (dB) mantığı

Sinyal gücünü ölçerken dB (desibel) kullanırız çünkü:

Güç farkları çok büyük olabilir (örneğin 10 W ile 0.000001 W arası)

Logaritmik ölçmek kolaylaştırır.

Formüller:
G
u
¨
c
¸
 kazancı (dB)
=
10
log
⁡
10
(
𝑃
2
𝑃
1
)
G
u
¨
c
¸
	​

 kazancı (dB)=10log
10
	​

(
P
1
	​

P
2
	​

	​

)
Gerilim kazancı (dB)
=
20
log
⁡
10
(
𝑉
2
𝑉
1
)
Gerilim kazancı (dB)=20log
10
	​

(
V
1
	​

V
2
	​

	​

)

Örnek:
Bir sinyalin gücü 10 kat artarsa:

10
log
⁡
10
(
10
)
=
10
 dB
10log
10
	​

(10)=10 dB

100 kat artarsa → 20 dB
Yani 10 dB = 10x güç artışı
-10 dB = 10x güç kaybı

🌀 6. Polarizasyon

Dalganın elektrik alanının titreşim yönüdür.

Dikey → Vertical polarization

Yatay → Horizontal polarization

Dairesel → Circular polarization (örnek: uydu antenleri)

Eğer iki antenin polarizasyonu uyumlu değilse, sinyal kaybı yaşanır.
(Yani biri dikey, biri yatay olursa “çakışmazlar”.)

🧠 7. Radyasyon Diyagramı (Radiation Pattern)

Bu diyagram antenin hangi yöne ne kadar güç yaydığını gösterir.
Genelde polar grafikte çizilir.

Geniş halka = Her yöne eşit (omnidirectional anten)

İnce ok şeklinde = Belirli yöne yoğun (directional anten)

Yani grafik ne kadar “odaklı”ysa, kazanç o kadar yüksektir.

🧭 8. Özetle Mantık
Konu	Ne işe yarar	Formül / Mantık
Sinyal zayıflaması	Mesafe arttıkça güç azalır	
1
/
𝑑
2
1/d
2
 veya 
20
log
⁡
10
(
𝑑
)
20log
10
	​

(d)
Anten kazancı	Belirli yönde güç artışı	
𝐺
=
4
𝜋
𝐴
𝑒
/
𝜆
2
G=4πA
e
	​

/λ
2

Dalga boyu	Frekansla ters orantılı	
𝜆
=
𝑐
/
𝑓
λ=c/f
Path loss	Toplam kayıp (dB)	
20
log
⁡
10
(
𝑑
)
+
20
log
⁡
10
(
𝑓
)
20log
10
	​

(d)+20log
10
	​

(f)
Radyasyon deseni	Yayılım yönü	Polar grafikte gösterilir
💡 Sonuç

Bu formüller ezber değil, aslında hep aynı mantığın farklı yansımaları:

“Enerji yayılır → uzaklaştıkça yoğunluğu azalır → antenin yönü bunu değiştirir → frekans dalga boyunu belirler.”

Hepsi bir enerji dengesi oyunudur ⚖️
⚙️ Antenler ve Propagasyon — Uygulamalı Mantık ve Örnekler
📶 1. Wi-Fi sinyal zayıflaması örneği
Durum:

Bir Wi-Fi cihazı 2.4 GHz frekansta yayın yapıyor.
Antenler arası mesafe = 10 metre.

Soru: Bu sinyal 10 metrede kaç dB zayıflar?

Kullanacağımız formül:
𝐿
𝑝
(
𝑑
𝐵
)
=
20
log
⁡
10
(
𝑑
)
+
20
log
⁡
10
(
𝑓
)
−
147.55
L
p
	​

(dB)=20log
10
	​

(d)+20log
10
	​

(f)−147.55

Yerine koyalım:

𝐿
𝑝
=
20
log
⁡
10
(
10
)
+
20
log
⁡
10
(
2.4
×
10
9
)
−
147.55
L
p
	​

=20log
10
	​

(10)+20log
10
	​

(2.4×10
9
)−147.55
𝐿
𝑝
=
20
+
187.6
−
147.55
=
60.05
 
𝑑
𝐵
L
p
	​

=20+187.6−147.55=60.05dB
🔍 Yorum:

10 metrede yaklaşık 60 dB kayıp oluyor.
Yani sinyal gücü, her 3 dB’de yarıya düşüyorsa:
→ 
60
/
3
=
20
60/3=20 defa yarıya inmiş.
Yani 
2
20
≈
1
,
000
,
000
2
20
≈1,000,000 kat zayıflamış 😱

Ama yine de cihazlar bunu tolere ediyor çünkü Wi-Fi sinyali zaten “modülasyon” sayesinde çok düşük seviyede bile okunabiliyor.

📡 2. Aynı anteni 5 GHz’te çalıştıralım
Durum:

Antenler yine 10 m uzakta, ama bu kez frekans 5 GHz.

𝐿
𝑝
=
20
log
⁡
10
(
10
)
+
20
log
⁡
10
(
5
×
10
9
)
−
147.55
L
p
	​

=20log
10
	​

(10)+20log
10
	​

(5×10
9
)−147.55
𝐿
𝑝
=
20
+
193.98
−
147.55
=
66.43
 
𝑑
𝐵
L
p
	​

=20+193.98−147.55=66.43dB
🔍 Yorum:

Yani 2.4 GHz’te 60 dB kayıp varken,
5 GHz’te 66 dB kayıp oluyor → 6 dB fazla.

🔸 Sonuç: Frekans artarsa dalga boyu kısalır → yayılım azalır → menzil düşer.

O yüzden 5 GHz Wi-Fi hızlı ama kısa menzilli,
2.4 GHz Wi-Fi yavaş ama uzak mesafeye gider.

📏 3. Anten boyutu örneği
Dalga boyu formülü:
𝜆
=
𝑐
𝑓
λ=
f
c
	​


1️⃣ 2.4 GHz için:

𝜆
=
3
×
10
8
2.4
×
10
9
=
0.125
 
𝑚
=
12.5
 
𝑐
𝑚
λ=
2.4×10
9
3×10
8
	​

=0.125m=12.5cm

2️⃣ 5 GHz için:

𝜆
=
3
×
10
8
5
×
10
9
=
0.06
 
𝑚
=
6
 
𝑐
𝑚
λ=
5×10
9
3×10
8
	​

=0.06m=6cm
🔍 Yorum:

5 GHz anteni 2 kat daha küçük boyutlu olur ama daha kısa menzilli.
Bu yüzden telefonların içindeki antenler yüksek frekansta, küçük ve hassastır.

💪 4. Anten kazancı örneği
Diyelim ki:

Antenin etkin alanı 
𝐴
𝑒
=
0.01
 
𝑚
2
A
e
	​

=0.01m
2

Frekans = 2.4 GHz → 
𝜆
=
0.125
 
𝑚
λ=0.125m

Formül:

𝐺
=
4
𝜋
𝐴
𝑒
𝜆
2
G=
λ
2
4πA
e
	​

	​

𝐺
=
4
𝜋
(
0.01
)
(
0.125
)
2
=
8.04
G=
(0.125)
2
4π(0.01)
	​

=8.04
𝐺
(
𝑑
𝐵
)
=
10
log
⁡
10
(
8.04
)
=
9.05
 
𝑑
𝐵
G(dB)=10log
10
	​

(8.04)=9.05dB
🔍 Yorum:

Bu anten yaklaşık 9 dB kazançlı.
Yani aynı gücü yönlü olarak verirsen, o yönde 8 kat daha güçlü sinyal elde edersin.

Omnidirectional anten yerine directional (yönlü) kullanmanın olayı tam olarak bu!

🔄 5. Toplam sinyal hesabı (örnek senaryo)
Değer	Açıklama
Verici gücü	
𝑃
𝑡
=
20
 
𝑑
𝐵
𝑚
P
t
	​

=20dBm (yaklaşık 100 mW)
Verici kazancı	
𝐺
𝑡
=
9
 
𝑑
𝐵
G
t
	​

=9dB
Alıcı kazancı	
𝐺
𝑟
=
9
 
𝑑
𝐵
G
r
	​

=9dB
Yayılım kaybı	
𝐿
𝑝
=
60
 
𝑑
𝐵
L
p
	​

=60dB
𝑃
𝑟
=
𝑃
𝑡
+
𝐺
𝑡
+
𝐺
𝑟
−
𝐿
𝑝
P
r
	​

=P
t
	​

+G
t
	​

+G
r
	​

−L
p
	​

𝑃
𝑟
=
20
+
9
+
9
−
60
=
−
22
 
𝑑
𝐵
𝑚
P
r
	​

=20+9+9−60=−22dBm
🔍 Yorum:

Alıcı antene ulaşan sinyal -22 dBm (yaklaşık 6 μW).
Yani çok zayıf ama hala okunabilir.
Zaten Wi-Fi alıcıları genelde -80 dBm’e kadar sinyali okuyabilir.
Demek ki bu durumda iletişim gayet sağlıklı olurdu ✅

🧠 6. Tüm bu hesapların ardındaki mantık

Aslında her şey şu mantığa dayanıyor:

🔹 Enerji yayılırken geniş bir alana dağılır (zayıflar).
🔹 Anten bu enerjiyi toplar veya odaklar (kazanç sağlar).
🔹 Frekans arttıkça dalga boyu küçülür, menzil azalır.
🔹 Tüm güç hesapları logaritmik sistemle yapılır (dB).

Bu yüzden haberleşmede daima şu denge aranır:

Küçük anten + yüksek frekans + kısa mesafe
Büyük anten + düşük frekans + uzun mesafe

🔭 7. Gerçek hayattan küçük örnekler
Sistem	Frekans	Dalga boyu	Anten boyutu	Menzil	Not
AM Radyo	~1 MHz	300 m	Devasa	Çok uzun	Düşük hız
Wi-Fi (2.4 GHz)	2.4 GHz	12.5 cm	Küçük	Orta	Orta hız
Wi-Fi (5 GHz)	5 GHz	6 cm	Çok küçük	Kısa	Yüksek hız
Radar	24 GHz	1.25 cm	Mini	Kısa	Hassas ölçüm
🧩 8. Büyük resmi hatırla

Antenler ve propagasyon dersi sana şunu öğretir:

“Bir sinyal gönderdiğinde, o sinyalin havada nasıl hareket ettiğini, ne kadar kaybolduğunu ve antenin bunu nasıl etkilediğini anlamak.”

Yani bu dersin özü:
Matematikle fiziği birleştirip iletişimi anlamak.
⚙️ 3️⃣ Anten Türleri ve Temel Özellikleri

Anten çeşitleri çok fazla ama ana mantık hep aynı:
👉 Elektrik enerjisini elektromanyetik dalgaya çevirir ya da tam tersini yapar.

🧩 1. Dipol Anten

En temel ve en klasik antendir.

Genelde bir telin ortasından beslendiği, iki ucundan da dalga yayan yapıdadır.

Radyo ve TV vericilerinde sıkça kullanılır.
📏 Uzunluğu genelde dalga boyunun yarısı kadardır (λ/2).

Örnek: 100 MHz (radyo dalgası) için λ ≈ 3 metre → dipol uzunluğu ≈ 1.5 m olur.

📡 2. Yönlü (Directional) Anten

Enerjiyi belirli bir yöne odaklar.

Uzak mesafelere sinyal göndermek için idealdir.

Türleri:

Yagi-Uda Anten: TV antenleri (klasik çubuklu olanlar)

Parabolik Anten: Uydu anteni gibi, sinyali bir noktaya odaklar.

Horn (Boynuz) Anten: Radar sistemlerinde yaygın.

📈 Avantajı: Yüksek kazanç (gain) → sinyali uzağa taşır.
📉 Dezavantajı: Kapsama alanı dar olur.

🔄 3. Omnidirectional (Çok Yönlü) Anten

Her yöne eşit şekilde yayın yapar (360°).

Wi-Fi modemlerin antenleri genelde böyledir.

Kapsama geniş ama menzil kısa olur.

📡 Örnek: Telefon baz istasyonları genelde bu türdendir.

🪶 4. Patch (Mikroşerit) Anten

İnce, düz ve baskı devre kartına basılabilir yapıdadır.

Dronelarda, GPS modüllerinde ve IoT cihazlarında çok kullanılır.

Hafif, küçük ama düşük kazançlıdır.

💬 Özet:
Anten Türü	Yayılım Yönü	Kullanım Alanı
Dipol	İki yönlü	Radyo, TV
Yönlü (Parabolik, Yagi)	Tek yönlü	Uydu, radar
Omnidirectional	360°	Wi-Fi, GSM
Patch	Küçük, yüzey tipi	IoT, drone, GPS
🌍 4️⃣ Propagasyon (Yayılım) Türleri

Tamam, şimdi enerjiyi gönderdik diyelim.
Peki bu elektromanyetik dalga havada nasıl yayılıyor? İşte propagasyon bunu anlatır.

1. Doğrudan (Line-of-Sight, LOS) Yayılım

Antenler birbirini görürse sinyal doğrudan gider.

Yüksek frekanslı dalgalar (mikrodalga, Wi-Fi, radar) bu şekilde çalışır.

Araya bina, dağ girerse sinyal kesilir.

📶 Örnek:
Wi-Fi sinyali neden duvar arkasında zayıflıyor?
Çünkü line-of-sight bozuluyor!

2. Yansıma (Reflection)

Dalgalar yüzeylere çarparak geri döner.

Özellikle radarlarda hedef tespiti buna dayanır.

Çok fazla yansıma olursa sinyal karışır (çok yollu yayılım / multipath).

📡 Örnek:
Telefonla konuşurken yankı gelmesi — işte bu reflection olayı.

3. Kırılma (Refraction)

Dalga farklı yoğunlukta ortama geçince yön değiştirir.

Atmosfer tabakaları nedeniyle radyo dalgaları bazen bükülür ve menzil uzar.

📻 Örnek:
FM radyoların bazen uzak şehirlerden de çekmesi, atmosfer kırılması yüzünden.

4. Saçılma (Scattering)

Dalga küçük parçacıklara (yağmur damlası, toz) çarpınca farklı yönlere dağılır.

Özellikle yüksek frekanslarda etkilidir (5G, radar vs.)

5. Yer Dalgası (Ground Wave)

Dalgalar yer yüzeyini takip eder.

Düşük frekanslı iletişimde kullanılır (örneğin askeri haberleşme, denizaltı sistemleri).

🔎 Kısa Özet Tablosu:
Yayılım Türü	Özellik	Örnek
Line-of-Sight	Doğrudan	Wi-Fi, radar
Reflection	Yansıma	Yankı, radar
Refraction	Kırılma	FM radyo menzili
Scattering	Saçılma	5G, yağmur etkisi
Ground Wave	Yer boyunca	Denizaltı, uzun dalga radyo

Buraya kadar olan kısım:
"Anten nasıl çalışır, türleri neler, sinyaller havada nasıl yayılır" sorularının tamamını kapsıyor.
Yani dersi %70 anladık diyebiliriz 🔥