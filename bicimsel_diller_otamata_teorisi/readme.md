# 📘 **Otomata Teorisi — Temel Kavramlar ve Yapısal Çerçeve**

Otomata teorisi, biçimsel dilleri tanımlamak ve girdi dizileri üzerinde karar verebilen soyut hesaplama modelleri geliştirmek için kullanılan matematiksel bir disiplindir. Bilgisayar biliminde derleyicilerden güvenlik sistemlerine, metin işlemcilerden protokol doğrulamasına kadar geniş bir alanda temel rol oynar.

---

## **1. Otomata Kavramı**

Bir otomaton,
- Sınırlı sayıda **duruma** sahip olan,
- Dışarıdan aldığı her bir **girdi sembolü** ile durum değiştiren,
- Girdi tamamlandığında **kabul veya ret** kararı veren
bir soyut makinedir.

Otomatonun bileşenleri genellikle şu beşli ile ifade edilir:

\[
M = (Q, \Sigma, \delta, q_0, F)
\]

- **Q:** Sonlu durum kümesi  
- **Σ:** Girdi alfabesi  
- **δ:** Geçiş fonksiyonu  
- **q₀:** Başlangıç durumu  
- **F:** Kabul durumlarının kümesi  

---

## **2. DFA (Deterministic Finite Automaton)**

Deterministik sonlu otomaton, her girdi sembolü için **tek bir geçiş** tanımlayan ve herhangi bir anda **tek bir** durumda bulunabilen bir makinedir.

Özellikleri:
- Geçiş fonksiyonu δ tam olarak tanımlıdır.
- Karar mekanizması nettir.
- Her string için benzersiz çalıştırma yolu bulunur.

DFA’lar hızlı, deterministik ve donanım seviyesinde uygulanmaya elverişlidir.

---

## **3. NFA (Nondeterministic Finite Automaton)**

Nondeterministik sonlu otomaton, aynı anda **birden fazla olası durumda** bulunabiliyormuş gibi davranır.  
Bir sembol için:
- Birden fazla duruma geçiş olabilir,
- Hiç geçiş olmayabilir,
- **Epsilon (ε)** geçişi ile sembol tüketmeden durum değiştirilebilir.

Özellikler:
- Daha soyuttur.
- Tanımlaması ve tasarımı DFA’ya göre daha kolaydır.
- Hesaplama gücü DFA ile **eşdeğerdir**.

---

## **4. NFA → DFA Dönüşümü (Subset Construction)**

Her NFA, deterministik hale getirilerek DFA’ya dönüştürülebilir.  
Burada temel fikir:

> “NFA’nın aynı anda olabileceği tüm durum kümeleri, DFA’da tek bir durum haline getirilir.”

Adımlar:
1. Başlangıç durumu = NFA’nın ε-closure(q₀) kümesi  
2. Her sembol için yeni durum kümeleri oluşturulur  
3. Her yeni küme DFA’da yeni bir durumdur  
4. Bir kümede NFA’nın bir kabul durumu varsa, o küme DFA’da kabul durumudur  

Bu yöntem sayesinde nondeterministik yapı deterministik bir forma dönüştürülür.

---

## **5. Düzenli İfadeler (Regular Expressions) ve Otomata**

Düzenli ifadeler, düzenli dillerin **metinsel tanımlarıdır**.  
Her regular expression:
- Bir NFA’ya dönüştürülebilir (Thompson inşası),
- Oradan DFA’ya dönüştürülebilir,
- İstenirse tekrar regex’e çevrilebilir.

Temel operasyonlar:
- **Birleşim**: `a|b`
- **Sıralı bağlama (concatenation)**: `ab`
- **Kleene Yıldızı**: `a*`
- **Artı**: `a+`
- **Seçim ve grup**: `(ab|cd)e`

Regular expression ↔ NFA ↔ DFA tamamen **eşdeğer** yeteneğe sahiptir.

---

## **6. Otomata ve Düzenli Dillerin Kapanma Özellikleri**

Regular diller şu işlemler altında kapalıdır:
- **Birleşim (Union)**  
- **Kesişim (Intersection)**  
- **Tümleyen (Complement)**  
- **Fark (Difference)**  
- **Concatenation (L₁L₂)**  
- **Kleene Star (L*)**

Bu matematiksel kapalı yapı, düzenli dillerin hem analizini hem de inşa edilmesini kolaylaştırır.

---

## **7. Uygulama Alanları**

Otomata teorisi modern bilgisayar sistemlerinin temelinde yer alır:

- Derleyici tasarımı (lexer, tokenization)
- Veri doğrulama sistemleri
- Arama motorları ve pattern matching
- Ağ protokolü doğrulaması
- Güvenlik duvarları
- Metin işleme
- Kriptografik protokol analizleri
- Donanım tasarımı (CPU instruction decoder)

Bu nedenle otomata teorisi, bilgisayar biliminin kavramsal iskeletini oluşturur.

---

## **8. Kısa Özet**

- Otomata: Dilleri tanıyan soyut makineler.  
- DFA: Deterministik, tek durumlu, her sembolde net geçişli.  
- NFA: Nondeterministik, çoklu olası durumlu, ε-geçişli.  
- Regex: Bu makinelerin dilsel ifadesi.  
- Hepsi aynı dil sınıfını temsil eder: **Regular (Düzenli) Diller.**

# 🧠 Biçimsel Diller ve Otomata Teorisi

Bu dersin amacı, bilgisayarların **neleri yapabileceğini** ve **hangi sınırlar içinde çalıştığını** anlamaktır.  
Yani sadece nasıl kod yazıldığını değil, bir bilgisayarın **mantıksal sınırlarını** keşfetmeyi öğretir.  

---

## ⚙️ 1. Biçimsel Dil (Formal Language)

Bir **biçimsel dil**, belirli **kurallara göre oluşturulmuş semboller dizisidir**.

**Örnek:**

Alfabemiz:

Olası kelimeler:  
`a`, `b`, `ab`, `aab`, `abba`, ...

Kural: “Her `a`’nın ardından bir `b` gelmeli.”  
Geçerli kelimeler: `ab`, `aabb`  
Geçersiz kelimeler: `aa`, `aba`

Bu kuralları tanımlayan yapıya **gramer (grammar)** denir.

---

## ⚙️ 2. Otomata (Automata)

“Otomata”, belirli kurallara göre sembol dizilerini okuyan ve **kabul / red** kararı veren soyut makineleri ifade eder.  
Bu makineler, programların mantıksal temelini oluşturur.

---

## ⚙️ 3. Otomata Türleri

### 🟢 1. Deterministik Sonlu Otomat (DFA)

- Belirli sayıda durumu vardır.  
- Her sembol için tek geçiş tanımlıdır.  
- Kabul veya red kararı verir.

**Örnek:**  
“Çift sayıda ‘a’ içeren kelimeleri kabul et.”

---

### 🟡 2. Non-Deterministik Sonlu Otomat (NFA)

- Bir sembol için **birden fazla** geçiş olabilir.  
- Bazı durumlarda sembol okumadan (ε) geçiş yapılabilir.  
- Teorik olarak DFA ile **eşdeğer güçtedir.**

---

### 🔵 3. Yığınlı Otomat (PDA)

- Yığıt (stack) yapısı kullanır.  
- Parantez dengesi gibi iç içe yapıları tanır.  
- Örnek: `(()())` geçerli, `(()` geçersiz.

---

### 🔴 4. Turing Makinesi (TM)

- En güçlü modeldir.  
- Sonsuz bir bant üzerinde okuma-yazma kafasıyla çalışır.  
- Günümüz bilgisayarlarının teorik temelidir.

---

## 📚 4. Chomsky Hiyerarşisi

| Seviye | Dil Türü | Otomat Türü | Örnek |
|--------|-----------|--------------|--------|
| Tip 0 | Turing Dili | Turing Makinesi | Herhangi bir algoritma |
| Tip 1 | Bağlama duyarlı | Linearly bounded automaton | Programlama dilleri |
| Tip 2 | Bağlamdan bağımsız | Yığınlı Otomat | Parantez dengesi, ifadeler |
| Tip 3 | Düzenli | Sonlu Otomat | Regex desenleri |

---

## 🎯 5. Gerçek Hayat Bağlantıları

- **Regex (Regular Expression)** → DFA / NFA tabanlıdır.  
- **Derleyiciler** → PDA ve gramer analizine dayanır.  
- **NLP & Yapay Zekâ** → Biçimsel dil mantığı kullanır.  

---

# 🟢 DFA (Deterministic Finite Automaton)

## 1. Tanım
> Belirli sayıda durumu olan ve her sembolde tek geçiş yapan bir otomat türüdür.

Formel gösterim:

| Sembol | Anlam |
|--------|--------|
| Q | Durum kümesi |
| Σ | Alfabe |
| δ | Geçiş fonksiyonu |
| q₀ | Başlangıç durumu |
| F | Kabul durumları |

---

## 2. Örnek: “a sayısı çift olan kelimeler”

### Alfabe

---

## 3. Girdi Örnekleri

| Girdi | a sayısı | Son Durum | Kabul mü? |
|--------|-----------|------------|-----------|
| ε | 0 | q₀ | ✅ |
| a | 1 | q₁ | ❌ |
| aa | 2 | q₀ | ✅ |
| aba | 2 | q₀ | ✅ |
| abb | 1 | q₁ | ❌ |

---

# 🟡 NFA (Non-Deterministic Finite Automaton)

## 1. Tanım
> NFA, bir sembolde birden fazla geçiş yapabilen, hatta sembol okumadan (ε) da hareket edebilen otomat türüdür.

Formel gösterim:

(*) kabul durumu

---

## 3. NFA vs DFA

| Özellik | DFA | NFA |
|----------|-----|-----|
| Geçiş sayısı | Tek | Birden fazla |
| ε-geçiş | Yok | Var |
| Kararlılık | Belirli | Belirsiz |
| Güç | Eşit | Eşit |
| Tasarım kolaylığı | Zor | Kolay |

---

## 4. NFA → DFA Dönüşümü (Subset Construction)
Her NFA, **DFA’ya dönüştürülebilir.**  
Bunun için:
- NFA’daki tüm olası durum kümeleri, DFA’da **tek bir durum** olarak temsil edilir.  
- Bu yönteme **Subset Construction** veya **Powerset yöntemi** denir.

---

## 5. Gerçek Hayattaki Kullanımı

- **Regex motorları** (örneğin `grep`, `Python re`, `VSCode search`)  
- **Derleyici (lexer) tasarımı**  
- **Oyunlardaki durum makineleri**

---

## 🧩 Özet

| Kavram | DFA | NFA |
|--------|-----|-----|
| Belirleyicilik | ✅ | ❌ |
| Epsilon geçişi | ❌ | ✅ |
| Tasarım kolaylığı | Daha zor | Daha kolay |
| Hesap gücü | Aynı | Aynı |
| Kullanım alanı | Donanım, derleyici | Regex, dil tanıma |

---

## 💬 Sonuç
> “Kod yazmak yürümekse, otomata bilmek koşmaktır.” 🏃‍♂️💨  
Biçimsel diller ve otomata teorisi, bilgisayar biliminin **mantıksal iskeletini** oluşturur.  
Regex’lerden derleyicilere, yapay zekâdan doğal dil işlemeye kadar her şeyin temelinde bu teori yatar.
🧩 NFA → DFA Dönüşümü (Subset Construction Yöntemi)

NFA’lar sezgisel olarak kolay ama kararsızdır.
DFA’lar kararlı ama katıdır.
Bu yüzden NFA’yı DFA’ya çevirerek hem kararlılığı hem de aynı dili koruruz.



Her biri düzenli dillerin farklı bir temsilidir.

Ve tümü, bilgisayar biliminin “mantıksal temelini” oluşturur. 💻
# 🔹 Regex ve Otomata Rehberi

Bu rehberde **Regular Expression (Düzenli İfade)**, **NFA** ve **DFA** arasındaki ilişkiyi, dönüşümleri ve temel mantığı adım adım öğrenebilirsiniz. 💻✨

---

## ⚙️ 1. Mantık Temeli

- **NFA (Nondeterministic Finite Automaton)**: Aynı anda birden fazla durumda olabilir.  
- **DFA (Deterministic Finite Automaton)**: Her an tek bir durumda olmalıdır.  

💡 Bu yüzden NFA’nın her “durum kümesi”ni DFA’da tek bir durum olarak temsil ederiz.  
Bu işleme **Subset Construction (Küme Oluşturma) Yöntemi** denir.

| NFA          | DFA        |
|-------------|------------|
| {q₀, q₁}    | Q₀₁        |

---

## 🧠 2. Adım Adım Örnek

**Verilen NFA:**

| Durum | a        | b      |
|-------|----------|--------|
| q₀    | {q₀,q₁} | {q₀}   |
| q₁    | {q₂}     | ∅      |
| q₂    | ∅        | ∅      |

- Başlangıç durumu: `q₀`  
- Kabul durumu: `{q₂}`

### 🔹 Adım 1 — Başlangıç

DFA’nın ilk durumu, NFA başlangıç durumunun **epsilon-closure**’ıdır.  
Burada ε yok, o yüzden DFA başlangıcı: `{q₀}`

---

### 🔹 Adım 2 — “a” ve “b” için yeni kümeler oluştur

| DFA Durumu   | a          | b        |
|-------------|------------|----------|
| {q₀}        | {q₀,q₁}   | {q₀}    |
| {q₀,q₁}     | {q₀,q₁,q₂}| {q₀}    |
| {q₀,q₁,q₂}  | {q₀,q₁,q₂}| {q₀}    |

---

### 🔹 Adım 3 — Kabul Durumlarını Belirle

Eğer NFA kümesinde `q₂` varsa, DFA’daki o küme kabul durumudur.

**Kabul Durumları:** `{ {q₀,q₁,q₂} }`

---

### ✅ Sonuç: DFA Tablosu

| Durum        | a          | b        | Kabul? |
|-------------|------------|----------|--------|
| {q₀}        | {q₀,q₁}   | {q₀}    | ❌     |
| {q₀,q₁}     | {q₀,q₁,q₂}| {q₀}    | ❌     |
| {q₀,q₁,q₂}  | {q₀,q₁,q₂}| {q₀}    | ✅     |

> DFA, NFA’nın davranışını deterministik şekilde taklit eder.  
> Bu yöntemle her NFA %100 DFA’ya dönüştürülebilir. 💪

---

## 🔁 Regular Expression ↔ Otomata İlişkisi

- **Regex ↔ NFA**: Regex, otomata kurallarının dil versiyonudur.  
- **NFA ↔ DFA**: Subset construction ile dönüşüm yapılır.  
- **DFA ↔ Regex**: State elimination yöntemiyle DFA’dan regex elde edilebilir.

### ⚙️ Örnek: Regex → NFA → DFA

Regex: `a*b` → “0 veya daha fazla ‘a’ ardından tek bir ‘b’”

**DFA ile temsil:**

| Durum | a   | b   | Kabul? |
|-------|-----|-----|--------|
| q₀    | q₀  | q₁  | ❌     |
| q₁    | -   | -   | ✅     |

---

## ⚡ 3. Regular Dillerin Özellikleri

- **Birleşim (Union)**: L₁ ∪ L₂ düzenlidir.  
- **Kesişim (Intersection)**: L₁ ∩ L₂ düzenlidir.  
- **Ters (Complement)**: L̅ düzenlidir.  
- **Zincirleme (Concatenation)**: L₁L₂ düzenlidir.  
- **Kleene Star (Yıldız)**: L* düzenlidir.

> Yani regex’ler matematiksel olarak kapalı sistemlerdir, derleyici ve metin işleme sistemleri bu dili çok sever 😄

---

## 🎓 Özet

| Dönüşüm         | Yöntem / Açıklama                     |
|-----------------|--------------------------------------|
| NFA → DFA       | Subset (Küme) yöntemi                |
| Regex → NFA     | Thompson inşası                       |
| DFA → Regex     | State elimination                     |
| Regex ↔ DFA/NFA | Eşdeğer güçte, sadece temsil farkı   |

**🧠 Sonuç:**  
- NFA: soyut ve esnek  
- DFA: deterministik ve kararlı  
- Regex: NFA/DFA’nın dil halidir  

---

🚀 Artık Regex, NFA ve DFA dünyasında yolun açık! 😎

# 🔹 Regex & Otomata Rehberi — Part 2

Part 1’de temel mantığı, subset construction ve örnek DFA’yı gördük.  
Şimdi daha ileri örnekler, dönüşümler ve optimizasyonları inceleyelim. 💡

---

## 🧩 1. Daha Karmaşık NFA → DFA Örneği

**NFA Örneği:**

| Durum | a          | b      |
|-------|------------|--------|
| q₀    | {q₀,q₁}   | {q₀}   |
| q₁    | {q₂}       | {q₃}   |
| q₂    | ∅          | {q₃}   |
| q₃    | ∅          | ∅      |

- Başlangıç: `q₀`  
- Kabul: `{q₃}`

### 🔹 Adım Adım DFA Oluşturma

| DFA Durumu     | a              | b            | Kabul? |
|----------------|----------------|--------------|--------|
| {q₀}           | {q₀,q₁}       | {q₀}         | ❌     |
| {q₀,q₁}        | {q₀,q₁,q₂}    | {q₀,q₃}      | ❌     |
| {q₀,q₁,q₂}     | {q₀,q₁,q₂}    | {q₀,q₃}      | ❌     |
| {q₀,q₃}        | {q₀,q₁}       | {q₀}         | ✅     |

> Daha karmaşık NFA’lar da bu adım adım yöntemle deterministik hale getirilebilir.  

---

## 🎨 2. DFA Optimizasyonu

DFA oluşturduktan sonra gereksiz durumları **minimize** edebiliriz:

- **Eşdeğer durumları birleştir:** Aynı geçişlere ve kabul durumuna sahip olanlar  
- **Boş veya ulaşılmaz durumları kaldır:** DFA daha küçük ve hızlı olur

> Minimized DFA, özellikle büyük regex ve dil tanımlamalarında hayat kurtarır ⚡

---

## 🔁 3. Regex ↔ NFA ↔ DFA Döngüsü

### 🔹 Regex → NFA
- Thompson Construction yöntemi ile  
- Örnek: `(a|b)*abb`

**Adımlar:**
1. `a|b` → basit seçim NFA’sı  
2. `*` → loop  
3. `abb` → seri geçiş  
4. Tümünü birleştir → tek NFA  

---

### 🔹 NFA → DFA
- Subset construction ile deterministik hale getir  
- Elde edilen DFA ile regex’in tanıdığı tüm stringleri deterministik biçimde tarayabilirsin  

---

### 🔹 DFA → Regex
- State elimination yöntemi:  
  1. Kabul olmayan durumları ve geçişleri sil  
  2. Kalan durumları regex ifadeleri ile ifade et  
- Karmaşık DFA’lar için biraz matematiksel işlem gerekebilir, ama her zaman mümkündür  

---

## ⚡ 4. Regex ve Otomata Arasındaki Güç Dengesi

- **NFA**: Esnek, paralel durum takibi, daha az durum ama non-deterministic  
- **DFA**: Deterministik, hızlı tarama, daha fazla durum  
- **Regex**: İnsan okuyabilir dil, hızlı prototip, NFA/DFA’ya dönüşebilir  

> Özetle: “Regex → NFA → DFA → optimize → regex” döngüsü  
> Modern derleyici ve text engine’lerin temel çalışma prensibi 😎

---

## 📌 5. İleri Konseptler

- **Epsilon geçişleri (ε-transitions)**: Durumlar arasında ücretsiz geçişler  
- **Lazy DFA oluşturma**: Sadece kullanılan durumları oluştur, belleği koru  
- **Regular Language Closure Properties**: Birleşim, kesişim, tamamlayıcı, yıldız, zincirleme → her zaman geçerli  

---

## 🎓 Sonuç

- NFA → DFA: Subset construction  
- DFA optimize: Eşdeğer durumları birleştir  
- Regex ↔ Otomata: Her dil düzenli ise her gösterim eşdeğer  

> Artık regex ve otomataların tüm dönüşümlerini hem teorik hem pratik olarak anlayabiliyorsun! 💪  

---

💡 **İpucu:** GitHub README’inde bu tabloların yanına **ASCII veya Graphviz diagramları** ekleyerek çok daha görsel ve anlaşılır hale getirebilirsin.
