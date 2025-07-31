# İş Analizi Blog - GitHub Entegrasyonlu Web Sitesi

Bu proje, GitHub'daki .md dosyalarını otomatik olarak web sitesinde gösterebilen modern bir blog sistemidir.

## 🚀 Özellikler

- **GitHub Entegrasyonu**: .md dosyalarını GitHub'dan otomatik çeker
- **Markdown Desteği**: Tam markdown desteği ile zengin içerik
- **Responsive Tasarım**: Mobil uyumlu modern arayüz
- **İçindekiler Tablosu**: Otomatik oluşturulan navigasyon
- **Syntax Highlighting**: Kod blokları için renklendirme
- **SEO Dostu**: Arama motorları için optimize edilmiş

## 📋 Kurulum

### 1. Dosyaları İndirin
```bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
```

### 2. GitHub Konfigürasyonu
`index.html` dosyasındaki `GITHUB_CONFIG` bölümünü güncelleyin:

```javascript
const GITHUB_CONFIG = {
    username: 'yourusername',        // GitHub kullanıcı adınız
    repository: 'your-repo',         // Repository adınız
    branch: 'main',                  // Branch adınız (main/master)
    filePath: 'is_analistleri_2024_blog_yazisi.md' // .md dosyanızın yolu
};
```

### 3. GitHub Repository Yapısı
Repository'nizde şu yapıyı oluşturun:

```
your-repo/
├── index.html
├── README.md
├── is_analistleri_2024_blog_yazisi.md
└── other-articles/
    ├── article1.md
    └── article2.md
```

### 4. Web Sunucusunda Yayınlayın
- GitHub Pages
- Netlify
- Vercel
- Herhangi bir web sunucusu

## 🔧 Konfigürasyon Detayları

### GitHub Raw URL Formatı
```
https://raw.githubusercontent.com/{username}/{repository}/{branch}/{filepath}
```

### Desteklenen Markdown Özellikleri
- **Başlıklar**: # ## ###
- **Listeler**: - * 1. 2.
- **Vurgular**: **bold** *italic*
- **Kod Blokları**: ``` ``` `inline`
- **Linkler**: [text](url)
- **Resimler**: ![alt](url)
- **Tablolar**: | | |
- **Alıntılar**: > quote

### Özel CSS Sınıfları
```css
.article-content h1 { /* Ana başlıklar */ }
.article-content h2 { /* Alt başlıklar */ }
.article-content h3 { /* Alt-alt başlıklar */ }
.article-content code { /* Satır içi kod */ }
.article-content pre { /* Kod blokları */ }
.article-content blockquote { /* Alıntılar */ }
```

## 📝 Yeni Makale Ekleme

### 1. GitHub'da .md Dosyası Oluşturun
```markdown
# Makale Başlığı

## Giriş
Makale içeriği...

## Ana Bölüm
Daha fazla içerik...

## Sonuç
Özet ve kapanış.
```

### 2. Web Sitesinde Görüntüleme
- Dosyayı GitHub'a push edin
- Web sitesi otomatik olarak güncellenecek

## 🎨 Özelleştirme

### Renk Teması Değiştirme
`index.html` dosyasındaki CSS değişkenlerini güncelleyin:

```css
:root {
    --primary-color: #2c3e50;    /* Ana renk */
    --secondary-color: #3498db;  /* İkincil renk */
    --accent-color: #e74c3c;     /* Vurgu rengi */
    --text-color: #2c3e50;       /* Metin rengi */
    --light-bg: #f8f9fa;         /* Açık arka plan */
}
```

### Font Değiştirme
```css
body {
    font-family: 'Your Font', sans-serif;
}
```

### Logo ve Branding
```html
<a class="navbar-brand" href="#">
    <i class="fas fa-your-icon me-2"></i>
    Your Brand Name
</a>
```

## 🔍 SEO Optimizasyonu

### Meta Etiketleri
```html
<meta name="description" content="İş analizi ve dijital dönüşüm blogu">
<meta name="keywords" content="iş analizi, dijital dönüşüm, kariyer">
<meta name="author" content="Your Name">
```

### Open Graph
```html
<meta property="og:title" content="İş Analistleri: 2024'te Dijital Dönüşümün Öncüleri">
<meta property="og:description" content="İş analizi kariyer rehberi">
<meta property="og:image" content="https://yoursite.com/image.jpg">
```

## 🚀 Deployment

### GitHub Pages
1. Repository'yi public yapın
2. Settings > Pages
3. Source: Deploy from a branch
4. Branch: main
5. Save

### Netlify
1. GitHub repository'nizi bağlayın
2. Build command: boş bırakın
3. Publish directory: ./
4. Deploy

### Vercel
1. GitHub repository'nizi import edin
2. Framework Preset: Other
3. Deploy

## 📊 Analytics

### Google Analytics
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔧 Sorun Giderme

### Makale Yüklenmiyor
1. GitHub konfigürasyonunu kontrol edin
2. Dosya yolunun doğru olduğundan emin olun
3. Repository'nin public olduğunu kontrol edin
4. Browser console'da hata mesajlarını kontrol edin

### CORS Hatası
- GitHub Raw URL'lerini kullanın
- HTTPS protokolünü kullanın
- CDN kullanmayı düşünün

### Markdown Render Sorunu
- Marked.js kütüphanesinin yüklendiğinden emin olun
- Markdown syntax'ını kontrol edin

## 📚 Kaynaklar

- [Marked.js Documentation](https://marked.js.org/)
- [Bootstrap Documentation](https://getbootstrap.com/)
- [Font Awesome Icons](https://fontawesome.com/)
- [Prism.js Syntax Highlighting](https://prismjs.com/)

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit edin (`git commit -m 'Add amazing feature'`)
4. Push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 📞 İletişim

- **Email**: your.email@example.com
- **LinkedIn**: [Your LinkedIn](https://linkedin.com/in/yourprofile)
- **Twitter**: [@yourtwitter](https://twitter.com/yourtwitter)

---

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! 