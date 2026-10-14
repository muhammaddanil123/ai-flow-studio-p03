# Design Tokens — [Nama Aplikasi]

> Dokumen ini adalah sumber kebenaran (single source of truth) untuk sistem visual aplikasi.
> Semua layar (Login, Home, Detail, Form, Sukses) HARUS memakai token di bawah ini.
> Dilarang memakai nilai hex, ukuran font, atau spacing di luar tabel ini.

- Kelompok: [Nama Kelompok]
- Anggota: [Nama 1, Nama 2, ...]
- Figma (view only): [link]
- Versi: 1.0

---

## 1. Color

### 1.1 Primary (7 shade)

| Token | Hex | Penggunaan |
|---|---|---|
| `color-primary-50` | `#EEF2FF` | Background tint, hover ringan |
| `color-primary-100` | `#E0E7FF` | Background item terpilih |
| `color-primary-300` | `#A5B4FC` | Border aktif, ilustrasi |
| `color-primary-500` | `#6366F1` | Aksen, ikon aktif |
| `color-primary-600` | `#4F46E5` | **Tombol utama (default)**, link |
| `color-primary-700` | `#4338CA` | Tombol utama (pressed/hover) |
| `color-primary-900` | `#312E81` | Teks di atas background primary muda |

### 1.2 Semantic

| Token | Hex | Penggunaan |
|---|---|---|
| `color-success` | `#16A34A` | Berhasil, layar Sukses |
| `color-success-bg` | `#DCFCE7` | Background alert sukses |
| `color-warning` | `#F59E0B` | Peringatan |
| `color-warning-bg` | `#FEF3C7` | Background alert peringatan |
| `color-error` | `#DC2626` | Error validasi, aksi destruktif |
| `color-error-bg` | `#FEE2E2` | Background alert error |
| `color-info` | `#0284C7` | Informasi |
| `color-info-bg` | `#E0F2FE` | Background alert info |

### 1.3 Neutral

| Token | Hex | Penggunaan |
|---|---|---|
| `color-neutral-0` | `#FFFFFF` | Surface kartu, background utama |
| `color-neutral-50` | `#F9FAFB` | Background halaman |
| `color-neutral-100` | `#F3F4F6` | Background input disabled |
| `color-neutral-300` | `#D1D5DB` | Border, divider |
| `color-neutral-500` | `#6B7280` | Teks sekunder, placeholder |
| `color-neutral-700` | `#374151` | Teks body |
| `color-neutral-900` | `#111827` | Teks heading |

---

## 2. Typography

Font family: **Inter** (fallback: `system-ui, sans-serif`)

| Level | Token | Size / Line-height | Weight | Penggunaan |
|---|---|---|---|---|
| 1 | `type-h1` | 32 / 40 px | 700 | Judul layar utama |
| 2 | `type-h2` | 24 / 32 px | 700 | Judul section |
| 3 | `type-h3` | 20 / 28 px | 600 | Judul kartu |
| 4 | `type-body-lg` | 16 / 24 px | 400 | Teks isi utama, input |
| 5 | `type-body-sm` | 14 / 20 px | 400 | Teks sekunder, label, tombol |
| 6 | `type-caption` | 12 / 16 px | 500 | Caption, badge, helper text |

---

## 3. Spacing

Skala berbasis 4 px.

| Token | Nilai | Penggunaan umum |
|---|---|---|
| `space-1` | 4 px | Jarak ikon–teks |
| `space-2` | 8 px | Jarak antar elemen kecil |
| `space-3` | 16 px | Padding kartu/input, margin layar |
| `space-4` | 24 px | Jarak antar grup |
| `space-5` | 32 px | Jarak antar section |
| `space-6` | 48 px | Jarak besar, padding atas layar |

## 4. Radius & Elevation

| Token | Nilai | Penggunaan |
|---|---|---|
| `radius-sm` | 4 px | Badge |
| `radius-md` | 8 px | Input, tombol |
| `radius-lg` | 16 px | Kartu, modal |
| `radius-full` | 999 px | Avatar, chip |
| `shadow-sm` | `0 1px 2px rgba(17,24,39,0.08)` | Kartu |
| `shadow-md` | `0 4px 12px rgba(17,24,39,0.12)` | Modal, dropdown |

---

## 5. Components (Figma)

| Komponen | Variants | Token utama |
|---|---|---|
| `Button` | primary / secondary / ghost / disabled | `color-primary-600`, `radius-md`, `type-body-sm`, padding `space-2` × `space-3` |
| `Input` | default / focus / error / disabled | border `color-neutral-300`, error `color-error`, `radius-md`, `type-body-lg` |
| `Card` | default / pressed | `color-neutral-0`, `radius-lg`, `shadow-sm`, padding `space-3` |
| `AppBar` | with-back / with-title | `color-neutral-0`, `type-h3`, padding `space-3` |
| `Badge` | success / warning / error / info | warna semantic, `radius-sm`, `type-caption` |
| `ListItem` | default / selected | `type-body-lg`, divider `color-neutral-300`, padding `space-3` |
| `Alert` | success / warning / error / info | warna `*-bg` semantic, `radius-md`, padding `space-3` |

---

## 6. Pemetaan Layar → Token & Komponen

| Layar | Komponen yang dipakai | Catatan token |
|---|---|---|
| Login | AppBar, Input ×2, Button primary, Alert (error) | Margin layar `space-3`, jarak field `space-3` |
| Home | AppBar, Card (list), Badge, ListItem | Background `color-neutral-50`, jarak kartu `space-3` |
| Detail | AppBar (with-back), Card, Badge, Button primary & secondary | Judul `type-h2`, section `space-5` |
| Form | AppBar (with-back), Input ×n, Button primary, Alert | Label `type-body-sm`, error `color-error` |
| Sukses | Alert/ikon success, Button primary | Ikon `color-success`, padding atas `space-6` |

---

## 7. Design Tokens Export (CSS Variables)

```css
:root {
  /* Primary */
  --color-primary-50: #EEF2FF;
  --color-primary-100: #E0E7FF;
  --color-primary-300: #A5B4FC;
  --color-primary-500: #6366F1;
  --color-primary-600: #4F46E5;
  --color-primary-700: #4338CA;
  --color-primary-900: #312E81;

  /* Semantic */
  --color-success: #16A34A;
  --color-success-bg: #DCFCE7;
  --color-warning: #F59E0B;
  --color-warning-bg: #FEF3C7;
  --color-error: #DC2626;
  --color-error-bg: #FEE2E2;
  --color-info: #0284C7;
  --color-info-bg: #E0F2FE;

  /* Neutral */
  --color-neutral-0: #FFFFFF;
  --color-neutral-50: #F9FAFB;
  --color-neutral-100: #F3F4F6;
  --color-neutral-300: #D1D5DB;
  --color-neutral-500: #6B7280;
  --color-neutral-700: #374151;
  --color-neutral-900: #111827;

  /* Spacing */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 16px;
  --space-4: 24px;
  --space-5: 32px;
  --space-6: 48px;

  /* Radius */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 999px;

  /* Typography */
  --font-family: "Inter", system-ui, sans-serif;
  --type-h1: 700 32px/40px var(--font-family);
  --type-h2: 700 24px/32px var(--font-family);
  --type-h3: 600 20px/28px var(--font-family);
  --type-body-lg: 400 16px/24px var(--font-family);
  --type-body-sm: 400 14px/20px var(--font-family);
  --type-caption: 500 12px/16px var(--font-family);

  /* Elevation */
  --shadow-sm: 0 1px 2px rgba(17, 24, 39, 0.08);
  --shadow-md: 0 4px 12px rgba(17, 24, 39, 0.12);
}
```

## 8. Design Tokens Export (JSON)

```json
{
  "color": {
    "primary": { "50": "#EEF2FF", "100": "#E0E7FF", "300": "#A5B4FC", "500": "#6366F1", "600": "#4F46E5", "700": "#4338CA", "900": "#312E81" },
    "semantic": { "success": "#16A34A", "warning": "#F59E0B", "error": "#DC2626", "info": "#0284C7" },
    "neutral": { "0": "#FFFFFF", "50": "#F9FAFB", "100": "#F3F4F6", "300": "#D1D5DB", "500": "#6B7280", "700": "#374151", "900": "#111827" }
  },
  "typography": {
    "fontFamily": "Inter",
    "h1": { "size": 32, "lineHeight": 40, "weight": 700 },
    "h2": { "size": 24, "lineHeight": 32, "weight": 700 },
    "h3": { "size": 20, "lineHeight": 28, "weight": 600 },
    "bodyLg": { "size": 16, "lineHeight": 24, "weight": 400 },
    "bodySm": { "size": 14, "lineHeight": 20, "weight": 400 },
    "caption": { "size": 12, "lineHeight": 16, "weight": 500 }
  },
  "spacing": { "1": 4, "2": 8, "3": 16, "4": 24, "5": 32, "6": 48 },
  "radius": { "sm": 4, "md": 8, "lg": 16, "full": 999 }
}
```

---

## 9. Aturan Penggunaan untuk AI

1. Gunakan hanya token di dokumen ini; jangan membuat warna, ukuran font, atau spacing baru.
2. Teks heading memakai `color-neutral-900`, teks body `color-neutral-700`, teks sekunder `color-neutral-500`.
3. Satu tombol primary per layar; aksi lain memakai secondary atau ghost.
4. Margin horizontal layar selalu `space-3`; jarak antar section `space-5`.
5. Status selalu memakai warna semantic dan disertai ikon atau teks (jangan hanya warna).
6. Setiap elemen UI harus berupa instance komponen dari Bagian 5.
