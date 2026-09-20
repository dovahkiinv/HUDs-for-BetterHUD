# HUDs — External Bundles for MultiHUD

This folder contains **all HUDs** for MultiHUD. The core mod (`MultiHUD.dll`) embeds **no HUD** — every HUD is loaded from disk as a Custom HUD.

- **Source:** Built with Unity 2023.2.22f1, `BuildPipeline.BuildAssetBundles`, scripts in `MultiHUD` namespace (`MultiHUD` assembly).
- **Files:** `FH4HUD` (74 KB), `NFSU2` (198 KB), `cmrt` (411 KB), `NFS2015`, `InitialD66`, `NFSU2Poland`, `Two_Faded`, `WM3`, `granturismo` — each is a `UnityFS` AssetBundle (no extension by default, `.bundle` also accepted).

## How to use

1. Download one or many HUDs:
   - **Via git:** `git clone https://github.com/dovahkiinv/MultiHUD.git` → copy from `HUDs/` 
   - **Via Releases:** download `HUDs.zip` or individual `*.bundle` assets from the latest Release.
2. Copy the files into:
   - `CarX Drift Racing Online/Kino/Mods/MultiHUD_HUDs/` (next to `MultiHUD.dll`, created automatically) — also `..._Data/MultiHUD_HUDs` works (auto-detected).
3. In-game: `Kino → MultiHUD → ▼ Import HUD from Disk` → **Open Folder** → drop files → they appear instantly as **Custom HUDs** (auto-refresh every 1.5s, no restart). Click `[OFF] FH4` → `[ON] FH4`.

## Verification with FH4HUD

`FH4HUD` is the reference external HUD:
- Prefab name inside bundle: `FH4`
- Size: 74 KB, contains `MultiHUD.Speedo`, `Tacho`, `Gear` etc.
- Tested: Drop `FH4HUD` into `MultiHUD_HUDs` → Refresh → Enable `FH4` → works identically to the former embedded version (same code path, just `AssetBundle.LoadFromFile` instead of `LoadFromStream`).

## For authors

To add your own:
```bash
python Add_HUD.py MyHUD
# build bundle as `MyHUD` (no extension) in Unity
cp MyHUD HUDs/MyHUD
git add HUDs/MyHUD
```

Custom HUDs (any filename not matching the built-in enum) appear under **Custom imported** in the Import section and are stored as `CUSTOM_<name>_X/Y/S` in `MultiHUD_config.txt`.
