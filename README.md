# HUDs for BetterHUD

> **Custom HUDs for [BetterHUD](https://github.com/dovahkiinv/BetterHUD) — CarX Drift Racing Online (KSL / Kino)**

Pobierz i instaluj HUDy jednym kliknięciem bezpośrednio w grze: `BetterHUD → ▶ Custom HUDs → 🔴 Download HUDs` — lub ręcznie wrzuć `.bundle` do folderu.

---

## 📦 Available HUDs

| HUD | File | Preview | Size | Version | Author |
|-----|------|---------|------|---------|--------|
| **FH4** | `FH4HUD` | Forza Horizon 4 style — clean, minimal, kmh/mph, gear, tachometer | 73 KB | 1.0 | Dova (dovahkiinv) |
| **CMRT** | `cmrt` | CMRT style — colored dots, turbo arc, dots rpm | 410 KB | 1.0 | Dova |
| *More coming...* | — | — | — | — | — |

> Chcesz dodać swój HUD? Zobacz [How to contribute](#-how-to-contribute).

Files are raw AssetBundles (no extension or `.bundle`) — BetterHUD loads both.

---

## ⬇️ Installation

### Option A — In-game (recommended)

1. Zainstaluj [BetterHUD](https://github.com/dovahkiinv/BetterHUD) (`Kino/Mods/BetterHUD.dll` + `Kino/Mods/BetterHUD_HUDs/`).
2. Uruchom grę → `KSL → BetterHUD` (KSL v1.0.11).
3. Kliknij `▶ Custom HUDs` — wejdziesz do folderu jak `About` (`◀ Back` wraca).
4. Na dole kliknij `🔴 Download HUDs` (czerwony). Pierwsze wejście automatycznie `Fetching from GitHub...`.
5. Wybierz HUD:
   - `[DOWNLOAD] FH4` — nie pobrane, klik pobiera do `Kino/Mods/BetterHUD_HUDs/`
   - `[INSTALLED] FH4` — już pobrane, przycisk nieaktywny
   - `[UPDATE] FH4 - update awaiting` — na GitHubie jest nowsza wersja (`sha` się zmieniło), klik nadpisuje plik
6. Wróć `◀ Back` → w `Custom HUDs` zobaczysz `[OFF] FH4` — klik `[ON]`, potem `▶ Positioning` aby ustawić `X / Y / Scale`.

Updates are detected via GitHub `sha` (or file size fallback) — if already installed `cannot click unless update`.

### Option B — Manual

1. Pobierz plik z tego repo (`FH4HUD`, `cmrt` — **Raw** → `Save as`).
2. Wrzuć do `CarX Drift Racing Online/Kino/Mods/BetterHUD_HUDs/` (lub `..._Data/BetterHUD_HUDs` — ten który otwiera `Open Folder`, teraz dostępne tylko w starej wersji BetterHUD).
3. W grze `Custom HUDs` odświeży się automatycznie co `1.5s` — zobaczysz nowy HUD na liście.

---

## 🖼️ Previews

> Podmień na swoje screenshoty / gify `preview-fh4.jpg`, `preview-cmrt.jpg`.

```
HUDs-for-BetterHUD/
├─ FH4HUD           (73 KB)
├─ cmrt             (410 KB)
└─ README.md
```

| FH4 | CMRT |
|-----|------|
| ![FH4 preview](https://raw.githubusercontent.com/dovahkiinv/HUDs-for-BetterHUD/main/preview-fh4.jpg) | ![CMRT preview](https://raw.githubusercontent.com/dovahkiinv/HUDs-for-BetterHUD/main/preview-cmrt.jpg) |
| *Forza Horizon 4* | *CMRT* |

---

## 🛠️ How to create a Custom HUD

1. Stwórz Unity AssetBundle z prefabem zawierającym `Move` (RectTransform) + komponenty `Speedo`, `Tacho`, `Gear`, `Turbo` z BetterHUD.
2. Zbuduj bundle jako `<nazwa>` lub `<nazwa>.bundle` (np. `MyHUD`).
3. Przetestuj lokalnie wrzucając do `BetterHUD_HUDs` → `Custom HUDs`.
4. Wrzuć do tego repo via PR / upload — zostanie automatycznie dostępny w `Download HUDs`.

Tip: Bundle must be built with same Unity version as CarX (check `BetterHUD/README.md`).


---

## 📄 License

HUD bundles belong to their authors. BetterHUD is MIT. This repo is for sharing community HUDs — by uploading you agree your HUD can be downloaded in-game.

---

### Links

- BetterHUD: https://github.com/dovahkiinv/BetterHUD
- KSL / Kino: https://github.com/Kino
- Author: **Dova (dovahkiinv, dovahkiin_v)** — `Custom HUDs by Dova`

> You can download custom HUDs from GitHub and paste them into the folder. — but now you don't need to paste — just `Download HUDs`!
