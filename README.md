# Sinolife Collagen — landing page

Statik sayt: `index.html` + `img/` papkasi. Hech qanday build kerak emas —
papkani serverga (nginx `root`) yoki GitHub Pages ga yuklash kifoya.

## Sozlash

`index.html` ichida, `<script>` boshidagi `CONFIG` blokini toʻldiring:

- `leadEndpoint` — buyurtma yuboriladigan manzil (masalan `/api/lead` yoki
  `https://api.sizning-domen.uz/api/lead`). Bu server Bitrix24 ga lead yaratadi.
- `phone`, `phoneDisplay`, `telegram`, `instagram`, `workHours` — kontaktlar.
- `pixelId` — Meta Pixel ID (boʻsh qolsa pixel yuklanmaydi).

## Forma nimani yuboradi (POST, JSON)

```json
{
  "name": "Dilnoza",
  "phone": "+998901234567",
  "product": "Sinolife Collagen 10 000 mg",
  "source": "landing",
  "page": "https://…/?utm_source=facebook",
  "referrer": "",
  "sent_at": "2026-09-05T10:00:00.000Z",
  "utm_source": "facebook", "utm_campaign": "…", "fbclid": "…"
}
```

Server `2xx` qaytarsa — sahifada "Buyurtma qabul qilindi" koʻrinadi.
# LandingPage-1
