# CForge — İndirme

[English](README.md) · **Türkçe**

CForge, C dersi için gereken ortamı bilgisayarına tek işlemde kurar: VS Code,
C derleyicisi, gerekli eklentiler ve çalışmaya hazır bir örnek proje. Yönetici
yetkisi gerekmez.

**[→ İndirme sayfası](https://cforge-indir.mtvrkan.com/)**

Kurulum dosyaları bu depoda değil. CForge dersi veren okulların öğrencilerine
açık: indirme sayfasında adını, soyadını ve **okulunun verdiği e-posta
adresini** yazıyorsun, **her öğrenci haftada bir kez** indirebiliyor. Kod ya da
parola yok.

Bağlantılar verildikten sonra 24 saat geçerli — indirme yarıda kalırsa aynı
bağlantıdan devam edebilirsin, haftalık hakkın gitmez.

Tanıtım sayfası: [cforge.mtvrkan.com](https://cforge.mtvrkan.com)

![CForge — birinci sınıf için C geliştirme ortamı](og-cover.png)

---

## Hangisini indireceğim?

| Sistemin | Dosya |
| --- | --- |
| Windows 10/11 — **önerilen** | `CForge-windows-offline-<sürüm>.exe` |
| Windows, interneti hızlı ve serbest olan | `CForge-windows-online-<sürüm>.exe` |
| Mac (Apple Silicon — M1, M2, M3, M4) | `CForge-macos-arm64-<sürüm>.dmg` |
| Mac (Intel) | `CForge-macos-x64-<sürüm>.dmg` |
| Linux (x64) | `CForge-linux-x64-<sürüm>.tar.gz` |

**Hangi Mac'e sahip olduğunu bilmiyorsan:**  → Bu Mac Hakkında → "Yonga" satırında
*Apple* yazıyorsa arm64, *Intel* yazıyorsa x64.

**online / offline farkı:** offline sürüm VS Code'u ve derleyiciyi kendi içinde
taşır — büyük dosya, ama kurulum sırasında internet gerekmez. online sürüm
küçüktür, karşılığında kurulum sırasında bunları indirir. Kampüs ağı indirmeleri
engellediğinde kurulumun yarıda kalmasının sebebi budur, o yüzden önerilen
offline olan.

## Nasıl çalıştırılır

**Windows** — indirdiğin `.exe`'yi çalıştır, kurulacak bir şey yok.
İlk açılışta birkaç saniye bekleyebilir.
**"Windows kişisel bilgisayarınızı korudu" uyarısı çıkarsa** bu normaldir: CForge
imzalı bir uygulama değil, Windows da tanımadığı her programa aynı uyarıyı verir.
Mavi pencerede **Daha fazla bilgi** → **Yine de çalıştır**.

**macOS** — `.dmg`'yi çift tıkla, açılan pencerede `CForge.app`'i yanındaki
**Applications** klasörüne sürükle. Sonra Applications içinden **sağ tık → Aç**
ile başlat (ilk açılışta çift tıklama macOS tarafından engellenir). Sürükleme adımını
atlayıp uygulamayı İndirilenler'den çalıştırma: macOS karantinadaki bir klasörden
açılan uygulamayı her seferinde rastgele adlı, salt okunur geçici bir kopyadan
başlatır. Applications'a taşımak bunu kapatan şeydir.

**Linux** — arşivi çıkar ve çalıştır:

```bash
tar -xzf CForge-linux-x64-*.tar.gz
./CForge/CForge
```

## İndirdiğin dosya sağlam mı

Her sürümün [release sayfasında](https://github.com/mtvrkan/cforge-releases/releases/latest)
`SHA256SUMS.txt` var. İndirme sayfası da her dosyanın SHA-256 özetini gösteriyor;
ikisi tutuyorsa dosya bozulmadan gelmiştir.

```powershell
Get-FileHash CForge-windows-offline-*.exe -Algorithm SHA256
```

```bash
shasum -a 256 CForge-macos-arm64-*.dmg      # macOS
sha256sum CForge-linux-x64-*.tar.gz          # Linux
```

## Kurulum bittiğinde

VS Code açılır ve `ilkprojem.c` hazır bekler. **F5** programı derler ve
çalıştırır. Kurulum, kendi kurduğu ortamı gerçekten derleyip çalıştırarak
doğrular — yani "tamamlandı" yazıyorsa çalışıyor demektir.

Proje klasörün: `Belgeler/algoritma-1` (macOS ve Linux'ta `Documents`).

## Bir sorun çıkarsa

CForge hata durumunda ne olduğunu düz Türkçe anlatan bir rapor üretir ve
kopyalanabilir hâlde gösterir. O raporu dersin sorumlusuna ilet — antivirüs
silmesi, yarıda kalan kurulum, eksik derleyici ve indirmeyi engelleyen ağ
durumlarını ayrı ayrı tanır.

Yeniden denemek güvenlidir: CForge kaldığı yerden devam eder, kurulu olanı
tekrar kurmaz.

**İndirme sayfası "bu hafta hakkını kullandın" diyorsa** ve elinde çalışan bir
kurulum yoksa dersin sorumlusuna yaz; hak haftalık ve kendiliğinden yenilenir,
sayfa da ne zaman yenileneceğini yazar.

---

Bu depo sürüm notlarını, sağlama toplamlarını ve tanıtım sayfasının görsellerini
barındırır. Kurulum dosyaları indirme sayfasının arkasındadır.
