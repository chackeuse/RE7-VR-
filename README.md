<div align="center">

<img src="docs/images/icon.png" alt="RE7 VR" width="140" />

# RE7 VR

**Play Resident Evil 7 in virtual reality on PC — in one click.**<br/>
**Jouez à Resident Evil 7 en réalité virtuelle sur PC, en un clic.**

![Version](https://img.shields.io/badge/version-0.1.0-F0A040?style=for-the-badge)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-2A1D12?style=for-the-badge&logo=windows)
![OpenXR](https://img.shields.io/badge/VR-OpenXR%20%2F%20SteamVR-A8321E?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-5A3F25?style=for-the-badge)

**[🇬🇧 English](#-english) · [🇫🇷 Français](#-français)**

<img src="docs/images/app-home.png" alt="RE7 VR — application" width="820" />

*Dev by Chackeuse*

</div>

---

## 🇬🇧 English

### What is it?

**RE7 VR** is an unofficial, free tool that turns the PC version of *Resident Evil 7: Biohazard* into a
**virtual reality** experience. No manual file copying, no tinkering: a Windows installer, an application
with three big buttons — **INSTALL**, **UNINSTALL**, **LAUNCH GAME IN VR** — and you are in the Baker house,
headset on.

Under the hood, VR rendering, head tracking and motion controls come from
[**REFramework**](https://github.com/praydog/REFramework) by **praydog**, compiled from source by this project.
RE7 VR wraps it in a safe, reversible, bilingual experience.

### ✨ Features

| | |
|---|---|
| 🎮 **One-click VR** | Detects your Steam copy of RE7, installs the VR module, launches the game in VR. |
| 🛡️ **Safe & reversible** | Every replaced file is backed up first; **UNINSTALL** restores the game exactly as it was. Interrupted installs are rolled back automatically. |
| ✅ **Version check** | Recognises your game build by its fingerprint and warns you if it has not been validated. |
| 🎯 **Comfortable defaults** | View pitch driven by your head only (no tilted rooms), camera shake and artificial head bob disabled. |
| 🔧 **Repair & diagnostics** | Verify and repair module files, export an anonymised diagnostic report in one click. |
| 🌍 **English & French** | Switch language instantly, in the app and in the installer. |
| 🎨 **Original design** | Dark sepia theme with animated light, dust and film grain — no Capcom artwork. |
| 🔒 **Private** | No telemetry, nothing sent over the Internet, no administrator rights needed. |

<div align="center">
<img src="docs/images/app-settings.png" alt="VR settings" width="720" />
</div>

### 📋 Requirements

| | |
|---|---|
| **System** | Windows 10 or 11, 64-bit |
| **Game** | *Resident Evil 7: Biohazard* on **Steam** (default version, DirectX 12) — a legitimate copy is required |
| **VR** | **SteamVR** with an OpenXR-compatible headset |
| **Tested headset** | **Meta Quest 3** via **Steam Link** |

Validated game build: Steam `22773795` (`re7.exe` 1.0.0.7). Other headsets supported by SteamVR should work
but have not been tested yet — feedback welcome!

### 🚀 Installation

1. Download **`ResidentEvil7VR-Setup.exe`** from the [**Releases**](../../releases/latest) page.
2. Run it. The installer is not code-signed yet, so Windows SmartScreen may warn you:
   click **More info → Run anyway**.
3. In the RE7 VR app, click **INSTALL**.
4. Put on your headset, start **SteamVR** (Steam Link for Quest), then click **LAUNCH GAME IN VR**.
   Look straight ahead while the game loads.

To remove everything, click **UNINSTALL** in the app: your game goes back to its original state.

### 🕹️ Tips

- **Don't open the SteamVR or Meta menu while playing** — controllers stop reaching the game while it is open.
- Press **Insert** on your keyboard for the REFramework menu: **VR → Recenter View** if your view is off.
- Menus and cutscenes are shown on a virtual screen in front of you — that's expected.

### ❓ FAQ

<details>
<summary><b>Is this official?</b></summary>
No. RE7 VR is a fan project, not affiliated with or endorsed by Capcom. The official VR mode of RE7 was
PlayStation VR only.
</details>

<details>
<summary><b>Will it break my game or my saves?</b></summary>
No. The module only adds files next to the game; anything it would replace is backed up first, and your
save files are never touched. Uninstalling restores the original state. If something ever goes wrong,
Steam's <i>Verify integrity of game files</i> also restores the game.
</details>

<details>
<summary><b>The room looks tilted / my view is off.</b></summary>
Look straight ahead, press <b>Insert</b>, then <b>VR → Recenter View</b>. RE7 VR already enables
<i>Decoupled Camera Pitch</i> by default to avoid this.
</details>

<details>
<summary><b>My controllers do nothing.</b></summary>
Make sure no SteamVR or Meta overlay menu is open, and that the game window has focus on your PC.
</details>

<details>
<summary><b>The app says my game version is not validated.</b></summary>
Your game was probably updated. You can enable <i>Developer mode</i> in <b>VR settings</b> to try anyway,
at your own risk — and please open an issue so the new build can be validated.
</details>

### 🐞 Reporting a bug

Open an [issue](../../issues) and attach the archive from **Diagnostics → Export diagnostics** plus the
`re2_framework_log.txt` file from your game folder. The report contains no game files and no personal data.

### 🛠️ Building from source

Requirements: .NET 9 SDK, Visual Studio 2022/2026 (or Build Tools) with *Desktop development with C++*, Git.

```
git clone --recurse-submodules <this-repository-url>
powershell -ExecutionPolicy Bypass -File scripts\build-installer.ps1
```

The installer and its SHA-256 checksum land in `dist\`. Run the tests with `dotnet test`.
Technical documentation lives in [`docs/`](docs/).

### 🙏 Credits

- **Chackeuse** — development of RE7 VR.
- **[praydog](https://github.com/praydog)** — [REFramework](https://github.com/praydog/REFramework), which makes VR in RE Engine games possible.
- The Khronos Group (OpenXR), and all open-source libraries listed in `THIRD-PARTY-NOTICES.txt`.

### ⚖️ License & disclaimer

RE7 VR is released under the [MIT license](LICENSE). Third-party components keep their own licenses.
*Resident Evil* is a trademark of Capcom Co., Ltd. This project is not affiliated with, sponsored or endorsed
by Capcom, Meta or Valve, and ships no game files or Capcom artwork.

---

## 🇫🇷 Français

### C'est quoi ?

**RE7 VR** est un outil gratuit et non officiel qui transforme la version PC de *Resident Evil 7: Biohazard*
en expérience de **réalité virtuelle**. Pas de fichiers à copier à la main, pas de bidouille : un installateur
Windows, une application avec trois gros boutons — **INSTALLER**, **DÉSINSTALLER**, **LANCER LE JEU EN VR** —
et vous voilà chez les Baker, casque sur la tête.

Sous le capot, le rendu VR, le suivi de la tête et les manettes viennent de
[**REFramework**](https://github.com/praydog/REFramework) par **praydog**, compilé depuis les sources par ce projet.
RE7 VR l'emballe dans une expérience sûre, réversible et bilingue.

### ✨ Fonctionnalités

| | |
|---|---|
| 🎮 **La VR en un clic** | Détecte votre RE7 sur Steam, installe le module VR, lance le jeu en VR. |
| 🛡️ **Sûr et réversible** | Chaque fichier remplacé est sauvegardé avant ; **DÉSINSTALLER** remet le jeu exactement comme avant. Une installation interrompue est annulée automatiquement. |
| ✅ **Contrôle de version** | Reconnaît la version de votre jeu à son empreinte et prévient si elle n'a pas été validée. |
| 🎯 **Réglages confortables** | Inclinaison de la vue pilotée uniquement par la tête (fini la pièce penchée), secousses de caméra et balancement de tête désactivés. |
| 🔧 **Réparation et diagnostic** | Vérification et réparation des fichiers du module, export d'un rapport de diagnostic anonymisé en un clic. |
| 🌍 **Français et anglais** | Changement de langue instantané, dans l'application comme dans l'installateur. |
| 🎨 **Design original** | Thème sépia sombre avec lumière, poussière et grain animés — aucune image de Capcom. |
| 🔒 **Respect de la vie privée** | Aucune télémétrie, rien n'est envoyé sur Internet, aucun droit administrateur requis. |

### 📋 Configuration requise

| | |
|---|---|
| **Système** | Windows 10 ou 11, 64 bits |
| **Jeu** | *Resident Evil 7: Biohazard* sur **Steam** (version par défaut, DirectX 12) — copie légitime obligatoire |
| **VR** | **SteamVR** avec un casque compatible OpenXR |
| **Casque testé** | **Meta Quest 3** via **Steam Link** |

Version du jeu validée : build Steam `22773795` (`re7.exe` 1.0.0.7). Les autres casques pris en charge par
SteamVR devraient fonctionner mais n'ont pas encore été testés — vos retours sont les bienvenus !

### 🚀 Installation

1. Téléchargez **`ResidentEvil7VR-Setup.exe`** depuis la page [**Releases**](../../releases/latest).
2. Lancez-le. L'installateur n'est pas encore signé : Windows SmartScreen peut afficher un avertissement,
   cliquez sur **Informations complémentaires → Exécuter quand même**.
3. Dans l'application RE7 VR, cliquez sur **INSTALLER**.
4. Mettez votre casque, démarrez **SteamVR** (Steam Link pour le Quest), puis cliquez sur
   **LANCER LE JEU EN VR**. Regardez droit devant vous pendant le chargement.

Pour tout retirer, cliquez sur **DÉSINSTALLER** dans l'application : le jeu revient à son état d'origine.

### 🕹️ Conseils

- **N'ouvrez pas le menu SteamVR ni le menu Meta pendant le jeu** : les manettes ne sont plus transmises au jeu tant qu'il est ouvert.
- Touche **Inser** du clavier : menu REFramework, **VR → Recenter View** si la vue est décalée.
- Les menus et cinématiques s'affichent sur un écran virtuel devant vous : c'est normal.

### ❓ FAQ

<details>
<summary><b>C'est officiel ?</b></summary>
Non. RE7 VR est un projet de fan, sans lien avec Capcom et non approuvé par Capcom. Le mode VR officiel de
RE7 était réservé au PlayStation VR.
</details>

<details>
<summary><b>Est-ce que ça peut abîmer mon jeu ou mes sauvegardes ?</b></summary>
Non. Le module ajoute seulement des fichiers à côté du jeu ; tout fichier qu'il remplacerait est sauvegardé
avant, et vos sauvegardes de partie ne sont jamais touchées. La désinstallation restaure l'état d'origine.
En dernier recours, <i>Vérifier l'intégrité des fichiers du jeu</i> dans Steam remet aussi le jeu d'aplomb.
</details>

<details>
<summary><b>La pièce est penchée / ma vue est décalée.</b></summary>
Regardez droit devant vous, appuyez sur <b>Inser</b>, puis <b>VR → Recenter View</b>. RE7 VR active déjà
<i>Decoupled Camera Pitch</i> par défaut pour éviter ce problème.
</details>

<details>
<summary><b>Mes manettes ne font rien.</b></summary>
Vérifiez qu'aucun menu SteamVR ou Meta n'est ouvert par-dessus le jeu, et que la fenêtre du jeu est au premier
plan sur le PC.
</details>

<details>
<summary><b>L'application dit que ma version du jeu n'est pas validée.</b></summary>
Le jeu a probablement été mis à jour. Vous pouvez activer le <i>mode développeur</i> dans
<b>Paramètres VR</b> pour essayer quand même, à vos risques — et ouvrez une issue pour que la nouvelle version
puisse être validée.
</details>

### 🐞 Signaler un problème

Ouvrez une [issue](../../issues) en joignant l'archive générée par **Diagnostic → Exporter le diagnostic** et le
fichier `re2_framework_log.txt` du dossier du jeu. Le rapport ne contient ni fichiers du jeu ni données personnelles.

### 🛠️ Compiler depuis les sources

Prérequis : SDK .NET 9, Visual Studio 2022/2026 (ou Build Tools) avec *Développement Desktop en C++*, Git.

```
git clone --recurse-submodules <url-de-ce-dépôt>
powershell -ExecutionPolicy Bypass -File scripts\build-installer.ps1
```

L'installateur et sa somme de contrôle SHA-256 sont générés dans `dist\`. Tests : `dotnet test`.
Documentation technique : [`docs/`](docs/).

### 🙏 Crédits

- **Chackeuse** — développement de RE7 VR.
- **[praydog](https://github.com/praydog)** — [REFramework](https://github.com/praydog/REFramework), qui rend la VR possible dans les jeux RE Engine.
- Le Khronos Group (OpenXR) et toutes les bibliothèques open source listées dans `THIRD-PARTY-NOTICES.txt`.

### ⚖️ Licence et avertissement

RE7 VR est distribué sous [licence MIT](LICENSE). Les composants tiers conservent leurs propres licences.
*Resident Evil* est une marque de Capcom Co., Ltd. Ce projet n'est ni affilié, ni sponsorisé, ni approuvé par
Capcom, Meta ou Valve, et ne contient aucun fichier du jeu ni image de Capcom.

<div align="center">

*Dev by Chackeuse*

</div>
