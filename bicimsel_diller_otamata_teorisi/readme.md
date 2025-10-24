
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

⚙️ 1. Mantık Temeli

Bir NFA aynı anda birden fazla durumda olabilir.
DFA ise tek bir durumda olmalıdır.

O yüzden NFA’nın her “durum kümesi”ni, DFA’da tek bir durum olarak temsil ederiz.

NFA: {q₀, q₁}
DFA: Q₀₁ (yeni bir birleşik durum)

Buna subset construction (küme oluşturma) yöntemi denir.

🧠 2. Adım Adım Örnek

Verilen NFA:

Durum	a	b
q₀	{q₀, q₁}	{q₀}
q₁	{q₂}	∅
q₂	∅	∅

Kabul durumları: {q₂}
Başlangıç durumu: q₀

🔹 Adım 1 — Başlangıç

DFA’da ilk durum, NFA’nın başlangıç durumunun epsilon-closure’ıdır (yani ε geçişleriyle ulaşılabilen tüm durumlar).
Burada ε yok, o yüzden DFA’nın başlangıç durumu {q₀}.

🔹 Adım 2 — “a” ve “b” için yeni kümeler oluştur
DFA Durumu	a	b
{q₀}	{q₀, q₁}	{q₀}
{q₀, q₁}	{q₀, q₁, q₂}	{q₀}
{q₀, q₁, q₂}	{q₀, q₁, q₂}	{q₀}
🔹 Adım 3 — Kabul durumlarını belirle

Eğer NFA kümesi içinde q₂ (kabul durumu) varsa, DFA’daki o küme de kabul durumudur.
Yani:

Kabul durumları = { {q₀, q₁, q₂} }

✅ Sonuç: Yeni DFA
Durum	a	b	Kabul?
{q₀}	{q₀, q₁}	{q₀}	❌
{q₀, q₁}	{q₀, q₁, q₂}	{q₀}	❌
{q₀, q₁, q₂}	{q₀, q₁, q₂}	{q₀}	✅

Yani DFA, NFA’nın davranışını deterministik şekilde taklit eder.
Bu yöntemle her NFA, %100 DFA’ya dönüştürülebilir. 💪

🔁 Regular Expression ↔ Otomata İlişkisi

Regular Expression (Düzenli İfade) ile DFA/NFA aslında aynı şeyi temsil eder.
Fark sadece ifadede mi gösteriyorsun, yoksa makineyle mi?

⚙️ 1. Regex → NFA

Regex aslında otomata kurallarının “dil versiyonu”dur.
Her regex ifadesi, bir NFA’ya dönüştürülebilir.

Regex	Anlam	NFA Yorum
a	sadece “a”	tek geçiş
a*	sıfır veya daha fazla “a”	geri döngü (loop)
`a	b`	“a” veya “b”
ab	“a” ardından “b”	seri geçiş
⚙️ 2. NFA → DFA → Regex Döngüsü

Yani şu dönüşüm mümkündür:

Regex ⇄ NFA ⇄ DFA


💡 Örnek:

Regex: a*b


Bunu bir DFA olarak çizelim:

(start) --a--> (loop a) --b--> (accept)


veya tabloyla:

Durum	a	b	Kabul?
q₀	q₀	q₁	❌
q₁	-	-	✅

Bu DFA, “0 veya daha fazla ‘a’ ardından tek bir ‘b’” desenini tanır.

⚡ 3. Regular Dillerin Özellikleri

Regular diller DFA/NFA ile tanınabilir.

Kapanma Özellikleri:

Birleşim (Union): Eğer L₁ ve L₂ düzenliyse, L₁ ∪ L₂ de düzenlidir.

Kesişim (Intersection): L₁ ∩ L₂ düzenlidir.

Ters (Complement): L düzenliyse, L̅ de düzenlidir.

Zincirleme (Concatenation): L₁L₂ düzenlidir.

Yıldız (Kleene Star): L* düzenlidir.

Yani regex’ler matematiksel olarak kapalı sistemlerdir — bu yüzden derleyici ve metin işleme sistemleri bu dili sever 😄

🎓 Özet
Dönüşüm	Açıklama
NFA → DFA	Subset (küme) yöntemiyle yapılır
Regex → NFA	Thompson inşası yöntemiyle yapılır
DFA → Regex	Durum eleme (state elimination) yöntemiyle yapılır
Regex ↔ DFA/NFA	Eşdeğer güçte temsil biçimleridir
🧠 Sonuç

NFA’lar soyut, DFA’lar kararlı.

Regex’ler ise bu otomatların dil halidir.

Her biri düzenli dillerin farklı bir temsilidir.

Ve tümü, bilgisayar biliminin “mantıksal temelini” oluşturur. 💻