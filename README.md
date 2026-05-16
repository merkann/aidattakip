# AidatPro - Bina & Site Yönetim Sistemi

Bina, site ve kooperatifler için aidat, gelir-gider takip programı.

## Özellikler

- **Üye / Daire Yönetimi**: Giriş/çıkış takibi, eski kiracı arşivi, kat maliki bilgileri
- **Tahsilat & Borçlandırma**: Nakit/Banka/Havale, üye aidat/yakıt/demirbaş borçlandırma
- **Gider Kayıtları**: Fatura, tedarikçi, belge no takibi
- **Raporlar**: Cari durum, Excel'e aktarma
- **Excel İçe/Dışa Aktarma**: Toplu üye ekleme, banka ekstresi, toplu borçlandırma
- **Veri Depolama**: localStorage (tarayıcı) veya Firebase Firestore (bulut)

## Kurulum & GitHub Pages'e Yayınlama

### 1. Repo Oluşturma
```bash
git init
git add index.html
git commit -m "İlk sürüm"
git remote add origin https://github.com/KULLANICI_ADINIZ/aidatpro.git
git push -u origin main
```

### 2. GitHub Pages Etkinleştirme
- Repo → Settings → Pages
- Source: Deploy from branch → main → / (root)
- Save
- Birkaç dakika sonra `https://KULLANICI.github.io/aidatpro` adresinde yayında!

## Ücretsiz Veri Depolama Seçenekleri

### Seçenek A: localStorage (varsayılan, kurulum gerektirmez)
- Tarayıcı belleğinde saklanır
- Aynı cihazda çalışır
- ⚠️ Tarayıcı geçmişi silinirse veri kaybolur — düzenli Excel yedek alın!

### Seçenek B: Firebase Firestore (önerilen, ücretsiz)
1. [Firebase Console](https://console.firebase.google.com) → Yeni Proje
2. Firestore Database → Create → Production mode
3. Project Settings → Web App ekle → Config kopyala
4. Ayarlar sayfasına API Key ve Project ID gir

### Seçenek C: Supabase (alternatif, ücretsiz 500MB)
- [supabase.com](https://supabase.com) ücretsiz plan

## Excel Şablon Kullanımı

| Şablon | İçerik |
|--------|--------|
| `sablon-uye.xlsx` | Kat malikleri ve kiracılar |
| `sablon-tahsilat.xlsx` | Banka ekstresi / ödemeler |
| `sablon-borc.xlsx` | Toplu aidat/yakıt borçlandırma |
| `sablon-gider.xlsx` | Gider/fatura listesi |

Her şablonu "Excel İçe Aktar" sayfasından indirebilirsiniz.

## Teknoloji

- Saf HTML + React (CDN, kurulum gerektirmez)
- SheetJS (Excel okuma/yazma)
- localStorage (veri saklama)

## Lisans

MIT
