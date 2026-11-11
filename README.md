## 📥 Téléchargement et Installation Rapide

Téléchargez le dernier paquet d'installation `.deb` depuis la section [Releases](https://github.com/autre-ailleurs/scribe-blabla/releases) :

```bash
# Une fois le fichier scribe-blabla-pkg.deb téléchargé :
sudo apt install ./scribe-blabla-pkg.deb



# 🔊 Scribe BlaBla

**Scribe BlaBla** est une application Linux autonome et interactive d'édition de texte, de synthèse vocale et de conversion audio. Elle permet de lire du texte à voix haute en temps réel avec suivi visuel ou d'exporter vos textes sous forme de fichiers MP3.

---

## 📋 Description fonctionnelle

* **Édition textuelle interactive :** Zone de texte enrichie avec gestion dynamique de la taille de police, annulation des frappes (`Ctrl+Z`) et raccourcis d'insertion de pauses et ponctuation d'une seule pression.
* **Lecture vocale dynamique :** Lecture à partir de la position du curseur avec surlignage visuel synchronisé (jaune) mot par mot / phrase par phrase.
* **Conversion MP3 :** Export des textes complets au format MP3 haute qualité (192 kbps) avec choix du débit et du facteur de vitesse (de 0,5x à 2,0x).
* **Support Voix en Ligne et Locales :**
  * Voix en ligne Google Text-to-Speech (gTTS) multilingues.
  * Moteur de synthèse vocale locale hors-ligne basé sur **Piper TTS** (fichiers modèle `.onnx`).
* **Fenêtre d'options modale intégrée :** Centrée au milieu de l'application principale (optimisée multi-écrans) avec barre personnalisée, sans bouton de réduction gênant.
* **Intégration système :** Détection du fichier courant, ouverture du dossier parent via le gestionnaire de fichiers (`xdg-open`), historique des fichiers récents et intégration propre au menu des applications GNOME / MATE.

---

## 🛠️ Spécifications techniques & Dépendances

### Langage et bibliothèques Python
* **Python 3.6+**
* **`tkinter` / `ttk` :** Interface graphique native.
* **`gtts` :** Moteur de synthèse vocale en ligne.
* **`threading` & `subprocess` :** Exécution asynchrone pour éviter le blocage de l'interface lors de la lecture/conversion.

### Dépendances système (Linux / Ubuntu)
Pour fonctionner correctement, l'application s'appuie sur les outils système suivants :
* **`mpv` :** Lecteur multimédia léger utilisé pour la restitution audio en continu.
* **`ffmpeg` :** Outil de traitement audio pour le réglage de la vitesse (`atempo`) et la concaténation MP3.
* **`piper`** *(Optionnel)* : Exécutable de synthèse vocale locale pour l'utilisation des voix hors-ligne au format `.onnx`.

### Installation des dépendances sous Ubuntu / Debian :
```bash
sudo apt update
sudo apt install python3 python3-tk python3-gtts mpv ffmpeg
# scribe-blabla
# scribe-blabla

🚀 Historique des versions
v4.19 :

Optimisation multi-écrans : la fenêtre d'options est désormais calculée et centrée exactement au milieu de la fenêtre principale.

Ajout d'une sécurité syntaxique sur le cadre de la zone de texte.

v4.18 :

Suppression totale de la barre de titre système et du bouton de réduction (-) sur la fenêtre Options.

Intégration d'une barre de titre sombre personnalisée déplaçable avec bouton de fermeture (✕) dédié.

v4.17 :

Masquage du bouton de réduction via les attributs de dialogue et d'outils (toolwindow).

v4.16 :

Application de l'attribut -type dialog sous X11/GNOME pour restreindre les contrôles de la fenêtre d'options.

v4.15 :

Dactivation du redimensionnement de la fenêtre d'options (resizable(False, False)).

v4.14 :

Modification du libellé de configuration : « Nb fichiers récents (x) : » est devenu « Nb fichiers récents : ».

Versions précédentes (v1.0 à v4.13) :

Déploiement initial de l'interface Tkinter.

Ajout du support de Piper TTS (voix .onnx dans ~/ScribeBlaBla/voix-langues).

Intégration du système d'infobulles intelligentes (anti-troncature aux bords d'écran).

Création de la structure d'empaquetage .deb avec raccourci GNOME et script postinst.

📜 Licence & Transparence
Ce projet est distribué sous licence libre Copyleft (GNU GPL v3). Vous êtes libre de réutiliser, modifier et redistribuer ce logiciel à condition de conserver la même licence libre.

Auteur principal : Thierry LLOPIS

Transparence de développement : Ce logiciel a été conjointement développé et optimisé avec l'assistance de l'IA Gemini.
