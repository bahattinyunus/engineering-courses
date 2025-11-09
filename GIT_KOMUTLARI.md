# 🔧 Git Komutları - Kodları GitHub'a Yükleme

Dosyalar oluşturuldu ancak henüz git'e eklenmedi. Aşağıdaki komutları sırayla çalıştırarak dosyaları GitHub'a yükleyebilirsiniz.

## 📋 Adım Adım Talimatlar

### 1. Terminal/Command Prompt'u açın
Repository klasörüne gidin:
```bash
cd "C:\github repolarım\engineering-courses"
```

### 2. Git durumunu kontrol edin
```bash
git status
```

### 3. Tüm dosyaları ekleyin
```bash
git add .
```

### 4. Commit yapın
```bash
git commit -m "Kod örnekleri eklendi: algoritma, betik_diller, veri_tabanı, fizik, görüntü_isleme"
```

### 5. GitHub'a push edin
```bash
git push origin main
```

Eğer `main` branch yoksa:
```bash
git push origin master
```

## 🆕 İlk kez push ediyorsanız

Eğer remote repository henüz ayarlanmamışsa:

```bash
# Remote ekle (GitHub repository URL'inizi kullanın)
git remote add origin https://github.com/KULLANICI_ADI/engineering-courses.git

# Branch'i main olarak ayarla
git branch -M main

# İlk push
git push -u origin main
```

## ✅ Kontrol

Push işleminden sonra GitHub'da şu klasörler görünmelidir:

- `algoritma/examples/`
- `betik_diller/examples/`
- `veri tabanı/examples/`
- `fizik/examples/`
- `görüntü_isleme/examples/`

## 🔍 Sorun Giderme

### "fatal: not a git repository" hatası alıyorsanız:
```bash
git init
```

### "remote origin already exists" hatası alıyorsanız:
```bash
git remote set-url origin https://github.com/KULLANICI_ADI/engineering-courses.git
```

### Dosyalar görünmüyorsa:
```bash
git add .
git status  # Eklenen dosyaları kontrol edin
```

---

**Not:** Eğer PowerShell'de Türkçe karakter sorunu yaşıyorsanız, Git Bash veya Command Prompt kullanabilirsiniz.

