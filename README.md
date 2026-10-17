<p align="center">
  <img src="docs/images/icon.png" alt="RE7 VR" width="120" />
</p>

<h1 align="center">RE7 VR</h1>

<p align="center">
  Mod VR non officiel pour Resident Evil 7 sur PC<br/>
  <a href="#français">Français</a> · <a href="#english">English</a>
</p>

<p align="center">
  <img src="docs/images/app-home.png" alt="Application RE7 VR" width="800" />
</p>

---

## Français

### Présentation

RE7 VR permet de jouer à *Resident Evil 7: Biohazard* (version Steam) en réalité virtuelle.

Le projet se compose d'un installateur Windows et d'une application qui s'occupe de tout : elle détecte le jeu,
installe le mod VR, lance le jeu et peut tout désinstaller proprement.

La partie VR (affichage dans le casque, suivi de la tête, manettes) repose sur
[REFramework](https://github.com/praydog/REFramework), développé par praydog.

### Fonctionnalités

- Installation et désinstallation du mod en un clic
- Sauvegarde automatique des fichiers du jeu avant toute modification
- Vérification de la version du jeu
- Réglages VR par défaut adaptés (vue stable, secousses de caméra désactivées)
- Réparation des fichiers et export d'un rapport de diagnostic
- Interface en français et en anglais
- Aucun droit administrateur nécessaire, aucune donnée envoyée sur Internet

### Configuration requise

- Windows 10 ou 11 (64 bits)
- Resident Evil 7: Biohazard sur Steam (version par défaut)
- SteamVR
- Un casque VR compatible SteamVR

Testé avec un Meta Quest 3 connecté via Steam Link, sur la version Steam `22773795` du jeu.

### Installation

1. Téléchargez `ResidentEvil7VR-Setup.exe` dans la section [Releases](../../releases/latest).
2. Lancez l'installateur. Si Windows affiche un avertissement, cliquez sur **Informations complémentaires**
   puis **Exécuter quand même** (l'exécutable n'est pas signé).
3. Ouvrez l'application RE7 VR et cliquez sur **INSTALLER**.

### Utilisation

1. Connectez votre casque et démarrez SteamVR.
2. Dans l'application, cliquez sur **LANCER LE JEU EN VR**.
3. Regardez droit devant vous pendant le chargement.

En jeu, la touche **Inser** ouvre le menu REFramework (onglet **VR** pour les réglages et le recentrage).

### Désinstallation

- Pour retirer le mod du jeu : bouton **DÉSINSTALLER** dans l'application. Le jeu revient à son état d'origine.
- Pour retirer l'application : **Paramètres Windows > Applications > Resident Evil 7 VR**.

### Problèmes fréquents

**La vue est penchée ou décalée**
Regardez droit devant vous, appuyez sur **Inser**, puis **VR > Recenter View**.

**Les manettes ne répondent pas**
Fermez le menu SteamVR ou le menu Meta s'il est ouvert : le jeu ne reçoit pas les manettes tant qu'il est affiché.

**« Version du jeu non validée »**
Le jeu a sans doute été mis à jour. Vous pouvez activer le mode développeur dans **Paramètres VR** pour essayer
quand même, et ouvrir une issue pour signaler la nouvelle version.

**Les menus et cinématiques s'affichent à plat**
C'est normal : ils sont affichés sur un écran virtuel devant vous.

### Signaler un bug

Ouvrez une [issue](../../issues) en joignant :
- le rapport créé avec **Diagnostic > Exporter le diagnostic** dans l'application ;
- le fichier `re2_framework_log.txt` situé dans le dossier du jeu.

### Compiler le projet

Prérequis : SDK .NET 9, Visual Studio 2022 ou 2026 avec « Développement Desktop en C++ », Git.

```
git clone --recurse-submodules <url-du-dépôt>
powershell -ExecutionPolicy Bypass -File scripts\build-installer.ps1
```

L'installateur est généré dans le dossier `dist`. La documentation technique se trouve dans [`docs`](docs/).

### Crédits

- Développement : **Chackeuse**
- Mod VR : [REFramework](https://github.com/praydog/REFramework) par **praydog**
- Les licences des composants tiers sont fournies dans `THIRD-PARTY-NOTICES.txt`.

### Licence

Ce projet est distribué sous [licence MIT](LICENSE).

Projet non officiel, sans lien avec Capcom. *Resident Evil* est une marque de Capcom Co., Ltd.
Aucun fichier du jeu n'est fourni : une copie légitime de Resident Evil 7 est nécessaire.

---

## English

### Overview

RE7 VR lets you play *Resident Evil 7: Biohazard* (Steam version) in virtual reality.

The project includes a Windows installer and an application that handles everything: it detects the game,
installs the VR mod, launches the game and can remove everything cleanly.

The VR part (headset rendering, head tracking, controllers) is based on
[REFramework](https://github.com/praydog/REFramework), developed by praydog.

### Features

- One-click install and uninstall of the mod
- Automatic backup of game files before any change
- Game version check
- Sensible VR defaults (stable view, camera shake disabled)
- File repair and diagnostic report export
- French and English interface
- No administrator rights needed, no data sent over the Internet

### Requirements

- Windows 10 or 11 (64-bit)
- Resident Evil 7: Biohazard on Steam (default version)
- SteamVR
- A SteamVR-compatible VR headset

Tested with a Meta Quest 3 connected through Steam Link, on Steam build `22773795` of the game.

### Installation

1. Download `ResidentEvil7VR-Setup.exe` from the [Releases](../../releases/latest) section.
2. Run the installer. If Windows shows a warning, click **More info** then **Run anyway**
   (the executable is not signed).
3. Open the RE7 VR application and click **INSTALL**.

### Usage

1. Connect your headset and start SteamVR.
2. In the application, click **LAUNCH GAME IN VR**.
3. Look straight ahead while the game loads.

In game, the **Insert** key opens the REFramework menu (**VR** tab for settings and recentering).

### Uninstalling

- To remove the mod from the game: **UNINSTALL** button in the application. The game returns to its original state.
- To remove the application: **Windows Settings > Apps > Resident Evil 7 VR**.

### Common issues

**The view is tilted or off-center**
Look straight ahead, press **Insert**, then **VR > Recenter View**.

**Controllers do not respond**
Close the SteamVR or Meta menu if it is open: the game does not receive controller input while it is shown.

**"Game version not validated"**
The game was probably updated. You can enable developer mode in **VR settings** to try anyway, and open an
issue to report the new version.

**Menus and cutscenes are displayed flat**
This is expected: they are shown on a virtual screen in front of you.

### Reporting a bug

Open an [issue](../../issues) and attach:
- the report created with **Diagnostics > Export diagnostics** in the application;
- the `re2_framework_log.txt` file from the game folder.

### Building

Requirements: .NET 9 SDK, Visual Studio 2022 or 2026 with "Desktop development with C++", Git.

```
git clone --recurse-submodules <repository-url>
powershell -ExecutionPolicy Bypass -File scripts\build-installer.ps1
```

The installer is created in the `dist` folder. Technical documentation is in [`docs`](docs/).

### Credits

- Development: **Chackeuse**
- VR mod: [REFramework](https://github.com/praydog/REFramework) by **praydog**
- Third-party licenses are provided in `THIRD-PARTY-NOTICES.txt`.

### License

This project is released under the [MIT license](LICENSE).

Unofficial project, not affiliated with Capcom. *Resident Evil* is a trademark of Capcom Co., Ltd.
No game files are included: a legitimate copy of Resident Evil 7 is required.

