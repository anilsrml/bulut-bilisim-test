# Bulut Bilişim Testi

`main/` klasöründe tek sayfalık bir quiz arayüzü (`index.html`) ve soru verisi (`sorular.json`) bulunur.

## GitHub Pages ile canlıya alma

Site adresi genelde şu formdadır: `https://KULLANICI_ADI.github.io/REPO_ADI/`

### 1. Git deposu oluşturma

Projeyi GitHub’da yeni bir depoya yükleyin. Varsayılan dal adı **`main`** olmalı (iş akışı buna göre ayarlıdır).

```bash
cd cloud_Q
git init
git add .
git commit -m "İlk yükleme: quiz ve GitHub Pages"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADI/REPO_ADI.git
git push -u origin main
```

### 2. GitHub Pages kaynağını seçme

1. GitHub’da depoyu açın: **Settings** (Ayarlar).
2. Sol menüden **Pages** seçin.
3. **Build and deployment** bölümünde **Source** olarak **GitHub Actions** seçin (Branch değil).

İlk `push` sonrası `.github/workflows/github-pages.yml` çalışır; **Actions** sekmesinden iş akışının yeşil tamamlandığını kontrol edin.

### 3. Site adresi

Birkaç dakika içinde şu adresten erişebilirsiniz:

`https://KULLANICI_ADI.github.io/REPO_ADI/`

Depo **kullanıcı adı ile aynı** özel site ise (`KULLANICI_ADI.github.io`), kök adres doğrudan `https://KULLANICI_ADI.github.io/` olur; yine de `main/` içeriği bu iş akışıyla köke yayınlanır.

### Notlar

- İş akışı yalnızca `main/` klasörünü yayınlar; `index.html` içindeki `fetch('./sorular.json')` bu yüzden çalışır.
- Dal adınız `master` ise `.github/workflows/github-pages.yml` dosyasında `branches: ["main"]` satırını `["master"]` olarak değiştirin veya dalı `main` olarak yeniden adlandırın.
