<p align="center"><img src="plugins/designcraft/assets/logo.png" width="96" alt="Craft Suite for Antigravity"></p>

<h1 align="center">Suite Craft pour Google Antigravity</h1>

<p align="center">
  <a href="README.md">English</a> · <a href="README.es.md">Español</a> · <a href="README.pt-BR.md">Português</a> · <b>Français</b> · <a href="README.de.md">Deutsch</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

<p align="center">Marketplace natif de plugins Google Antigravity pour les 11 applications open source Craft installées sur votre ordinateur (Windows, macOS, Linux).</p>

---

## Plugins (11 Bundles Natifs)

Chaque plugin regroupe **1 Skill** (`/<plugin>`), **1 Règle Permanente** (`rules/AGENTS.md`), **3 Prompts de Démarrage** et **1 Serveur MCP Local** (`${PLUGIN_ROOT}/dist/bundle.cjs`) exécuté en mode headless sans envoi vers le cloud.

| Plugin et Commande | Ce qu’il fait | Prérequis |
| --- | --- | --- |
| **DesignCraft** (`/designcraft`) | Mise en page, publipostage CSV, IDML InDesign, PDF/X-4 prêt à imprimer, PNG, EPUB et HTML | [DesignCraft](https://github.com/storytold/designcraft) + Node.js ≥ 20 |
| **EffectCraft** (`/effectcraft`) | Motion design, titres animés, effets vidéo VFX, modèles ; MP4, ProRes, WebM, GIF, Lottie | [EffectCraft](https://github.com/storytold/effectcraft) + Node.js ≥ 20 |
| **LightCraft** (`/lightcraft`) | Développement RAW : tonalité auto, 125 curseurs, préréglages, masques, HDR et panoramas ; JPEG, TIFF, WebP, AVIF, DNG | [LightCraft](https://github.com/storytold/lightcraft) + Node.js ≥ 20 |
| **PhotoCraft** (`/photocraft`) | Retouche photo par calques : taille, recadrage, Camera Raw, 123 filtres, détourage, texte ; PSD, PNG, JPEG, WebP | [PhotoCraft](https://github.com/storytold/photocraft) + Node.js ≥ 20 |
| **VectorCraft** (`/vectorcraft`) | Dessin vectoriel : vectorisation Image Trace, formes, texte et graphiques, recoloration ; SVG, PDF, AI, EPS, DXF, PNG | [VectorCraft](https://github.com/storytold/vectorcraft) + Node.js ≥ 20 |
| **PdfCraft** (`/pdfcraft`) | Outils PDF : fusionner, scinder, pages, OCR, formulaires, signatures, caviardage, chiffrement ; vers Word, HTML, images, PDF/A | [PdfCraft](https://github.com/storytold/pdfcraft) + Node.js ≥ 20 |
| **FilmCraft** (`/filmcraft`) | Montage vidéo : découper, rogner, 131 effets, looks Lumetri, titres, transitions ; H.264, ProRes, GIF, FCPXML, OTIO | [FilmCraft](https://github.com/storytold/filmcraft) + Node.js ≥ 20 |
| **WordCraft** (`/wordcraft`) | Traitement de texte : documents structurés, rechercher/remplacer, commentaires, suivi des modifications, publipostage ; DOCX, PDF, ODT, RTF, Markdown, LaTeX | [WordCraft](https://github.com/storytold/wordcraft) + Node.js ≥ 20 |
| **SoundCraft** (`/soundcraft`) | Station audio (DAW) : multipiste audio et synthés/batterie MIDI, 30 plugins, bus, mesure LUFS, stems ; WAV, AIFF, FLAC | [SoundCraft](https://github.com/storytold/soundcraft) + Node.js ≥ 20 |
| **DeckCraft** (`/deckcraft`) | Présentations : diapositives avec puces, images, graphiques, tableaux et notes, thèmes et transitions ; PowerPoint PPTX, supports PDF, PNG | [DeckCraft](https://github.com/storytold/deckcraft) + Node.js ≥ 20 |
| **GridCraft** (`/gridcraft`) | Tableurs : classeurs avec 515 formules Excel vivantes, tableaux, graphiques et tableaux croisés ; XLSX, CSV, ODS, JSON, HTML, PDF | [GridCraft](https://github.com/storytold/gridcraft) + Node.js ≥ 20 |

## Installer dans Google Antigravity Harness

### 1. Installation Directe en Une Commande (`agy` CLI)

Installez n’importe quel plugin directement depuis GitHub sans clonage manuel. Les plugins se synchronisent entre **Antigravity CLI**, **Antigravity App** (*Customizations → Installed*) et **Antigravity IDE** :

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/designcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/effectcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/lightcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/photocraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/vectorcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/pdfcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/filmcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/wordcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/soundcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/deckcraft
```

```bash
agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/gridcraft
```

> Dans une session interactive `agy`, vous pouvez aussi saisir `/plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/<nom-du-plugin>`.

### 2. Installer Toute la Suite de 11 Plugins d’un Coup

**macOS / Linux (Bash / Zsh) :**

```bash
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
for p in craft-marketplace-antigravity/plugins/*; do agy plugin install "$p"; done
```

**Windows (PowerShell) :**

```powershell
git clone https://github.com/jhonsu01/craft-marketplace-antigravity.git
Get-ChildItem .\craft-marketplace-antigravity\plugins -Directory | ForEach-Object { agy plugin install $_.FullName }
```

### 3. Antigravity App et Antigravity IDE (Global ou Workspace)

- **Installation globale** : `agy plugin install` place chaque plugin dans `~/.gemini/config/plugins/<nom>` (`%USERPROFILE%\.gemini\config\plugins\<nom>` sous Windows) et l’affiche dans **Customizations → Installed**.
- **Installation par projet (workspace)** : Copiez `plugins/<nom>` dans `.agents/plugins/<nom>` à la racine du projet, ou ouvrez directement ce dépôt (préconfiguré via `.agents/plugins.json`).

## Prérequis et Configuration Multiplateforme

- **Node.js ≥ 20** dans le `PATH`.
- **L’application Craft correspondante** ([Storytold](https://github.com/storytold)) : Windows (`.msi`/`.zip`), macOS (`.dmg` + binaire `<app>-cli` dans `/usr/local/bin` ou `/opt/homebrew/bin`) ou Linux (`.deb`, `.rpm`, `.tar.gz`).
- **Dossier personnalisé (optionnel)** : Définissez `<APP>_DIR` ou `<APP>_CLI` (par ex. `DESIGNCRAFT_DIR`) comme variable d’environnement système.

## Gérer, Valider et Mettre à Jour

Utilisez `agy plugin` pour lister, activer/désactiver, valider ou mettre à jour vos plugins :

```bash
# List installed plugins & bundled components
agy plugin list

# Enable / disable / uninstall a plugin
agy plugin disable designcraft
agy plugin enable designcraft
agy plugin uninstall designcraft

# Update a plugin to the latest version from GitHub
agy plugin uninstall designcraft && agy plugin install https://github.com/jhonsu01/craft-marketplace-antigravity/tree/main/plugins/designcraft

# Validate every plugin in the marketplace catalog
agy plugin validate --strict https://raw.githubusercontent.com/jhonsu01/craft-marketplace-antigravity/main/.agents/plugins/marketplace.json
```

## Autres Environnements et Marketplaces

- **OpenAI Codex et DeepSeek Harness** : Voir [jhonsu01/craft-marketplace](https://github.com/jhonsu01/craft-marketplace).
- **Claude Desktop et Sunsam Code (bundles `.mcpb`)** :

- **DesignCraft**: [designcraft-mcp-server.mcpb](https://github.com/jhonsu01/designcraft-mcp-server/releases/latest/download/designcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/designcraft-mcp-server)
- **EffectCraft**: [effectcraft-mcp-server.mcpb](https://github.com/jhonsu01/effectcraft-mcp-server/releases/latest/download/effectcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/effectcraft-mcp-server)
- **LightCraft**: [lightcraft-mcp-server.mcpb](https://github.com/jhonsu01/lightcraft-mcp-server/releases/latest/download/lightcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/lightcraft-mcp-server)
- **PhotoCraft**: [photocraft-mcp-server.mcpb](https://github.com/jhonsu01/photocraft-mcp-server/releases/latest/download/photocraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/photocraft-mcp-server)
- **VectorCraft**: [vectorcraft-mcp-server.mcpb](https://github.com/jhonsu01/vectorcraft-mcp-server/releases/latest/download/vectorcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/vectorcraft-mcp-server)
- **PdfCraft**: [pdfcraft-mcp-server.mcpb](https://github.com/jhonsu01/pdfcraft-mcp-server/releases/latest/download/pdfcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/pdfcraft-mcp-server)
- **FilmCraft**: [filmcraft-mcp-server.mcpb](https://github.com/jhonsu01/filmcraft-mcp-server/releases/latest/download/filmcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/filmcraft-mcp-server)
- **WordCraft**: [wordcraft-mcp-server.mcpb](https://github.com/jhonsu01/wordcraft-mcp-server/releases/latest/download/wordcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/wordcraft-mcp-server)
- **SoundCraft**: [soundcraft-mcp-server.mcpb](https://github.com/jhonsu01/soundcraft-mcp-server/releases/latest/download/soundcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/soundcraft-mcp-server)
- **DeckCraft**: [deckcraft-mcp-server.mcpb](https://github.com/jhonsu01/deckcraft-mcp-server/releases/latest/download/deckcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/deckcraft-mcp-server)
- **GridCraft**: [gridcraft-mcp-server.mcpb](https://github.com/jhonsu01/gridcraft-mcp-server/releases/latest/download/gridcraft-mcp-server.mcpb) · [repo](https://github.com/jhonsu01/gridcraft-mcp-server)

## Licence

Apache-2.0. Les applications Craft appartiennent à leurs auteurs ([Storytold](https://github.com/storytold)) ; ces plugins ne sont ni affiliés ni approuvés par eux.
