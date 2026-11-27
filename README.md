# algolotl-content

Algolotl'un öğrenme yolu, üniteleri, dersleri ve soruları. Algolotl, Python öğreten oyunlaştırılmış bir kodlama uygulaması.

İlk sürüm Python öğretir ve 3-4 üniteden oluşur. Yeni bir dil, ünite, ders veya soru eklemek yalnızca bu repoya dosya eklemekle olur, uygulama ve API kodu değişmez.

## Klasör yapısı

```text
python/
  yol.json          dil adı, renklendirme dili, ünite sırası
  unite-01/
    unite.json      ünite başlığı ve ders sırası
    ders-01.json    dersin soruları
```

## Soru örneği

```json
{
  "id": "py-u1-l2-q3",
  "type": "fill_blank",
  "prompt": "Ekrana yazı yazdıran komutu tamamla.",
  "code": "____(\"Merhaba\")",
  "options": ["print", "input", "len"],
  "answer": ["print"],
  "explanation": "print, verilen değeri ekrana yazar."
}
```

Soru tipleri: `multiple_choice` (test), `fill_blank` (boşluk doldurma), `matching` (eşleştirme).

Bu örnek yol göstermek içindir. Dosyaların kesin biçimini API reposundaki [`content.schema.json`](https://github.com/Hasmolam/algolotl-api) belirler. Burada elle ayrı bir şema yazılmaz, böylece iki kopya birbirinden ayrılmaz.

## Yol haritası

İşler yukarıdan aşağıya sırayla ilerler. Her işin ayrıntısı, ne zaman bitmiş sayılacağı ve hangi işe bağlı olduğu kendi issue'sunda yazar. Güncel durumu [Issues](https://github.com/Hasmolam/algolotl-content/issues) ve [Milestones](https://github.com/Hasmolam/algolotl-content/milestones) sayfalarından takip edin.

### 1 · Plan

Müfredat ve yazım kuralları.

- [#1 Python müfredat planı](https://github.com/Hasmolam/algolotl-content/issues/1)
- [#2 Ders yazım kılavuzu](https://github.com/Hasmolam/algolotl-content/issues/2)

### 2 · Altyapı

Otomatik kontrol ve uçtan uca deneme.

- [#3 Dosya biçiminin otomatik kontrolü](https://github.com/Hasmolam/algolotl-content/issues/3)
- [#4 Pilot ders ile uçtan uca deneme](https://github.com/Hasmolam/algolotl-content/issues/4)

### 3 · Üniteler

MVP içeriğinin yazılması.

- [#5 Ünite 1 dersleri](https://github.com/Hasmolam/algolotl-content/issues/5)
- [#6 Ünite 2 dersleri](https://github.com/Hasmolam/algolotl-content/issues/6)
- [#7 Ünite 3 dersleri](https://github.com/Hasmolam/algolotl-content/issues/7)
- [#8 Ünite 4 dersleri (zaman kalırsa)](https://github.com/Hasmolam/algolotl-content/issues/8)

### 4 · Son kontrol

Mekanizma kontrolü ve son gözden geçirme.

- [#9 Yeni dil ekleme mekanizmasının kontrolü](https://github.com/Hasmolam/algolotl-content/issues/9)
- [#10 Telefonda son gözden geçirme turu](https://github.com/Hasmolam/algolotl-content/issues/10)

## İçerik kuralları

- Ders ve soru kimlikleri bir kez verilir, sonra değiştirilmez. Kullanıcı ilerlemesi bu kimliklere bağlıdır.
- Yayındaki bir ders veya soru silinmez. Kaldırılması gerekiyorsa API onu kullanımdan kalktı olarak işaretler.
- Sıra dosya adlarından değil, `yol.json` ve `unite.json` içindeki listeden okunur.
- Bir ders 5-8 sorudan oluşur ve 3-5 dakikada biter.
- Her sorunun kısa bir açıklaması olur.

## Yayın akışı

1. İçerik sorumlusu dersi yazar ve pull request açar.
2. Başka bir ekip üyesi teknik doğruluğunu kontrol eder.
3. Otomatik kontrol dosya biçimini ve cevapları doğrular.
4. Ders test ortamında telefonda denenir, sonra birleştirilir.

## Çalışma kuralları

- `main` dalına doğrudan push yapılamaz. Her değişiklik pull request ile gelir.
- Her pull request en az bir onay almadan birleşmez. Onaydan sonra yeni commit gelirse onay yenilenir.
- Açık kalan yorumlar çözülmeden birleştirme yapılmaz.
- Dal adları `ders/kisa-aciklama`, `feature/kisa-aciklama` veya `fix/kisa-aciklama` biçimindedir.
- Pull request küçük tutulur ve tek bir işi yapar. Bir ders, bir pull request.
- Birleştirme yalnızca "Squash and merge" ile yapılır, dal birleşince otomatik silinir.

## Lisans

Tüm hakları saklıdır. Bu repo yalnızca görüntülenebilir, izinsiz kullanılamaz. Ayrıntılar [LICENSE](LICENSE) dosyasında.
