# 🎮 SteamID64 to GUID Converter

**A tactical identity conversion toolkit for DayZ & Arma
administrators.**

Convert SteamID64 into native engine identifiers, generate BattlEye ban
entries and inspect public Steam account reputation.

[🇬🇧 English](#english) · [🇦🇷 Español](#español) · [🇫🇷
Français](#français) · [🇮🇹 Italiano](#italiano) · [🇩🇪 Deutsch](#deutsch)
· [🇨🇿 Čeština](#čeština) · [🇷🇺 Русский](#русский) · [🇵🇱 Polski](#polski)
· [🇧🇷 Português](#português-brasil) · [🇨🇳 简体中文](#简体中文) · [🇹🇼
繁體中文](#繁體中文) · [🇯🇵 日本語](#日本語)

[![Stars](https://img.shields.io/github/stars/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github)](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/stargazers)
[![Forks](https://img.shields.io/github/forks/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github)](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/network/members)
[![License](https://img.shields.io/github/license/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge)](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/blob/main/LICENSE)
[![Last
Commit](https://img.shields.io/github/last-commit/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github)](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/commits/main)

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Client
Side](https://img.shields.io/badge/Architecture-Client--Side-24292f?style=flat-square)
![DayZ](https://img.shields.io/badge/DayZ-Supported-8aab42?style=flat-square)
![Arma](https://img.shields.io/badge/Arma-Supported-8aab42?style=flat-square)
![No
Backend](https://img.shields.io/badge/Backend-Not%20Required-24292f?style=flat-square)

------------------------------------------------------------------------

## 📑 Contents

-   [🇬🇧 English](#english)
    -   [Overview](#overview)
    -   [Features](#features)
    -   [Conversion formats](#conversion-formats)
    -   [Quick start](#quick-start)
    -   [Deployment](#deployment)
    -   [Privacy](#privacy)
    -   [Contributing](#contributing)
-   [🇦🇷 Español](#español)
-   [🇫🇷 Français](#français)
-   [🇮🇹 Italiano](#italiano)
-   [🇩🇪 Deutsch](#deutsch)
-   [🇨🇿 Čeština](#čeština)
-   [🇷🇺 Русский](#русский)
-   [🇵🇱 Polski](#polski)
-   [🇧🇷 Português (Brasil)](#português-brasil)
-   [🇨🇳 简体中文](#简体中文)
-   [🇹🇼 繁體中文](#繁體中文)
-   [🇯🇵 日本語](#日本語)
-   [📜 License](#license)

------------------------------------------------------------------------

# 🇬🇧 English

`<a id="overview">`{=html}`</a>`{=html}

## Overview

**SteamID64 to GUID Converter** is a 100% client-side HTML/JavaScript
toolkit for DayZ and Arma server administrators and developers. It
converts SteamID64 into native hash formats used by the Enfusion/Real
Virtuality engines and checks public account information through
SteamRep.

No installation, application backend or database is required.

## ✨ Features

  -----------------------------------------------------------------------
  🔧 Feature                          Description
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Generates URL-safe Base64 from the
                                      plain-text SHA-256 digest, used in
                                      `.rpt` files and DayZ Standalone
                                      profiles.

  🛡️ **BattlEye / Classic Arma**      Generates hexadecimal MD5 from
                                      Little Endian bytes, used in
                                      classic GUIDs and bans.

  📄 **Ban formatting**               Automatically generates the line
                                      for the BattlEye `bans.txt` file.

  👤 **SteamRep Checker**             Retrieves public profile
                                      information, avatar, username, VAC
                                      and Trade Ban status, and
                                      reputation indicators through a
                                      public proxy.

  📋 **One-click copy**               Click a result to copy its value to
                                      the clipboard.

  ⚡ **Client-side processing**       Cryptographic processing runs
                                      locally in the browser. No
                                      application backend or database is
                                      needed.
  -----------------------------------------------------------------------

`<a id="conversion-formats">`{=html}`</a>`{=html}

## 🧬 Conversion formats

  -----------------------------------------------------------------------
  Format            Algorithm         Output            Intended use
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 →         Encoded digest    DayZ `.rpt` files
  ID**              URL-safe Base64                     and Standalone
                                                        profiles

  **BattlEye /      MD5 + Little      Hexadecimal       Classic Arma
  Classic GUID**    Endian bytes                        GUIDs and bans

  **BattlEye ban    GUID formatting   `bans.txt` line   Server ban
  entry**                                               management
  -----------------------------------------------------------------------

These formats serve different purposes and are not interchangeable. Use
the identifier expected by the target game or server system.

## 🖥️ Workflow preview

``` text
┌──────────────────────────────────────────────────────┐
│             STEAMID64 → GUID CONVERTER               │
├──────────────────────────────────────────────────────┤
│  INPUT                                               │
│  ┌────────────────────────────────────────────────┐  │
│  │ 76561198000000000                              │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  CONVERSION RESULTS                                  │
│  ┌────────────────────────────────────────────────┐  │
│  │ DAYZ HASHED ID                         [COPY]  │  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE GUID                         [COPY]   │  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE BAN ENTRY                    [COPY]   │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  STEAMREP ACCOUNT CHECK                              │
│  ┌────────────────────────────────────────────────┐  │
│  │ Profile · VAC · Trade Bans · Reputation        │  │
│  └────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────┘
```

*Conceptual workflow illustration, not an application screenshot.*

`<a id="quick-start">`{=html}`</a>`{=html}

## 🚀 Quick start

1.  Download or clone this repository.
2.  Open `index.html` in a modern browser.
3.  Paste a SteamID64 (for example, `76561198000000000`) or a Steam
    profile URL.
4.  Click any result box to copy its value.

[Open the
repository](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool)

## ☁️ Deployment

The project has no application backend or external dependencies, so it
can be served as a static website or opened locally.

  -------------------------------------------------------------------------
  Hosting option       Difficulty              Cost         Setup
  --------------- -------------------- -------------------- ---------------
  **GitHub              🟢 Easy                Free         Enable Pages
  Pages**                                                   for the
                                                            repository

  **Cloudflare          🟢 Easy             Free tier       Connect the Git
  Pages**                                                   repository

  **Local**           🟢 Very easy             Free         Open
                                                            `index.html`

  **Custom web         🟡 Medium             Depends        Serve the
  server**                                                  static files
  -------------------------------------------------------------------------

**Offline note:** Cryptographic conversion runs locally. SteamRep
profile lookups require an internet connection.

`<a id="privacy">`{=html}`</a>`{=html}

## 🔒 Privacy

-   Cryptographic calculations run locally in the browser.
-   The application does not require its own backend or database.
-   SteamRep lookups use a public proxy and therefore require network
    access.
-   Do not interpret client-side processing as meaning that every
    feature is offline.

## 🧰 Technology

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Steam](https://img.shields.io/badge/Steam-000000?style=flat-square&logo=steam&logoColor=white)

  Component      Role
  -------------- ------------------------------------------------
  HTML           Application structure
  JavaScript     Conversion logic and interface functionality
  Browser APIs   Local processing and clipboard operations
  SteamRep       External public account reputation information

## 🤝 Contributing

Contributions, suggestions and bug reports are welcome.

1.  Fork the repository.
2.  Create a branch for your change.
3.  Make and test your changes locally.
4.  Submit a Pull Request describing what you changed.

[Report a bug or suggest an
improvement](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇦🇷 Español

## Descripción

**SteamID64 to GUID Converter** es una herramienta táctica 100%
client-side (HTML/JS) para administradores y desarrolladores de
servidores DayZ y Arma. Convierte SteamID64 a los formatos de hash
nativos de los motores Enfusion/Real Virtuality y verifica información
pública de cuentas mediante SteamRep.

No requiere instalación, backend ni base de datos.

## ✨ Características

  -----------------------------------------------------------------------
  Función                             Descripción
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Genera el Base64 (URL-Safe) del
                                      SHA-256 en texto plano, utilizado
                                      en archivos `.rpt` y perfiles de
                                      DayZ Standalone.

  🛡️ **BattlEye / Arma clásico**      Genera el MD5 hexadecimal de los
                                      bytes en Little Endian, utilizado
                                      en GUID clásicos y bans.

  📄 **Formateo automático**          Genera automáticamente la línea
                                      para el archivo `bans.txt` de
                                      BattlEye.

  👤 **SteamRep Checker**             Obtiene foto de perfil, nombre de
                                      usuario y verifica el estado de
                                      VAC, Trade Bans y reputación
                                      general mediante un proxy público.

  📋 **Copiado rápido**               Permite copiar cualquier resultado
                                      al portapapeles con un clic.

  ⚡ **Procesamiento local**          Todo el procesamiento criptográfico
                                      se ejecuta en el navegador. No
                                      requiere backend ni base de datos.
  -----------------------------------------------------------------------

## 🧬 Formatos de conversión

  -----------------------------------------------------------------------
  Formato           Algoritmo         Resultado         Uso
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Hash codificado   Archivos `.rpt` y
  ID**              URL-Safe                            perfiles DayZ

  **BattlEye / GUID MD5 + bytes       Hexadecimal       GUID clásicos y
  clásico**         Little Endian                       bans

  **BattlEye Ban    Formateo de GUID  Línea `bans.txt`  Administración de
  Entry**                                               bans
  -----------------------------------------------------------------------

Los formatos tienen funciones distintas y no son intercambiables.
Utilizá el identificador que requiera el juego o sistema de servidor
correspondiente.

## 🚀 Uso rápido

1.  Descargá o cloná este repositorio.
2.  Abrí `index.html` en un navegador moderno.
3.  Pegá un SteamID64 (por ejemplo, `76561198000000000`) o la URL
    completa de un perfil de Steam.
4.  Hacé clic sobre cualquier resultado para copiarlo al portapapeles.

[Ver
repositorio](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool)

## ☁️ Hosting y despliegue

  -------------------------------------------------------------------------
  Plataforma           Dificultad             Costo         Configuración
  --------------- -------------------- -------------------- ---------------
  **GitHub              🟢 Fácil              Gratis        Activar Pages
  Pages**                                                   en el
                                                            repositorio

  **Cloudflare          🟢 Fácil          Plan gratuito     Conectar el
  Pages**                                                   repositorio

  **Local**           🟢 Muy fácil            Gratis        Abrir
                                                            `index.html`

  **Servidor            🟡 Media             Variable       Servir los
  propio**                                                  archivos
                                                            estáticos
  -------------------------------------------------------------------------

**Uso offline:** Las conversiones criptográficas funcionan localmente.
Las consultas a SteamRep requieren conexión a internet.

## 🔒 Privacidad

-   Los cálculos criptográficos se realizan localmente en el navegador.
-   La aplicación no necesita backend ni base de datos propios.
-   Las consultas a SteamRep utilizan un proxy público y requieren
    conexión.

## 🤝 Contribuciones

1.  Hacé un Fork del repositorio.
2.  Creá una rama para tu modificación.
3.  Implementá y probá los cambios localmente.
4.  Enviá un Pull Request describiendo las modificaciones.

[Reportar un error o sugerir una
mejora](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇫🇷 Français

## Description

**SteamID64 to GUID Converter** est un outil tactique 100 % côté client
(HTML/JS) destiné aux administrateurs et développeurs de serveurs DayZ
et Arma. Il convertit les SteamID64 aux formats de hachage natifs des
moteurs Enfusion/Real Virtuality et vérifie les informations publiques
des comptes via SteamRep.

Aucune installation, aucun backend ni aucune base de données ne sont
nécessaires.

## ✨ Fonctionnalités

  -----------------------------------------------------------------------
  Fonctionnalité                      Description
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Génère le Base64 (URL-Safe) du
                                      SHA-256 en texte brut, utilisé dans
                                      les fichiers `.rpt` et les profils
                                      DayZ Standalone.

  🛡️ **BattlEye / Arma classique**    Génère le MD5 hexadécimal des
                                      octets Little Endian, utilisé pour
                                      les GUID classiques et les
                                      bannissements.

  📄 **Formatage automatique**        Génère automatiquement la ligne
                                      pour le fichier `bans.txt` de
                                      BattlEye.

  👤 **SteamRep Checker**             Récupère l'avatar, le nom
                                      d'utilisateur et vérifie les
                                      bannissements VAC, Trade Bans et la
                                      réputation via un proxy public.

  📋 **Copie rapide**                 Copie les résultats dans le
                                      presse-papiers en un clic.

  ⚡ **Traitement local**             Les opérations cryptographiques
                                      sont exécutées dans le navigateur.
                                      Aucun backend ni base de données
                                      n'est requis.
  -----------------------------------------------------------------------

## 🧬 Formats de conversion

  -----------------------------------------------------------------------
  Format            Algorithme        Résultat          Utilisation
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Hash encodé       Fichiers `.rpt`
  ID**              URL-Safe                            et profils DayZ

  **BattlEye / GUID MD5 + octets      Hexadécimal       GUID classiques
  classique**       Little Endian                       et bannissements

  **BattlEye Ban    Formatage du GUID Ligne `bans.txt`  Gestion des
  Entry**                                               bannissements
  -----------------------------------------------------------------------

Ces formats ont des usages différents et ne sont pas interchangeables.

## 🚀 Utilisation rapide

1.  Téléchargez ou clonez ce dépôt.
2.  Ouvrez `index.html` dans un navigateur moderne.
3.  Collez un SteamID64 (ex. : `76561198000000000`) ou l'URL d'un profil
    Steam.
4.  Cliquez sur un résultat pour copier sa valeur.

## ☁️ Hébergement

  --------------------------------------------------------------------------
  Plateforme            Difficulté              Coût         Configuration
  ---------------- -------------------- -------------------- ---------------
  **GitHub Pages**      🟢 Facile             Gratuit        Activer Pages
                                                             dans le dépôt

  **Cloudflare          🟢 Facile          Offre gratuite    Connecter le
  Pages**                                                    dépôt

  **Local**           🟢 Très facile          Gratuit        Ouvrir
                                                             `index.html`

  **Serveur             🟡 Moyenne            Variable       Servir les
  personnalisé**                                             fichiers
                                                             statiques
  --------------------------------------------------------------------------

Les conversions fonctionnent hors ligne. Les recherches SteamRep
nécessitent Internet.

## 🤝 Contributions

1.  Forkez le dépôt.
2.  Créez une branche pour votre modification.
3.  Effectuez et testez vos changements.
4.  Soumettez une Pull Request décrivant vos modifications.

[Signaler un problème ou proposer une
amélioration](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇮🇹 Italiano

## Descrizione

**SteamID64 to GUID Converter** è uno strumento tattico 100% lato client
(HTML/JS) per amministratori e sviluppatori di server DayZ e Arma.
Converte SteamID64 nei formati hash nativi dei motori Enfusion/Real
Virtuality e verifica le informazioni pubbliche degli account tramite
SteamRep.

Non richiede installazione, backend o database.

## ✨ Caratteristiche

  -----------------------------------------------------------------------
  Funzione                            Descrizione
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Genera il Base64 (URL-Safe) dello
                                      SHA-256 in testo normale,
                                      utilizzato nei file `.rpt` e nei
                                      profili DayZ Standalone.

  🛡️ **BattlEye / Arma classico**     Genera l'MD5 esadecimale dai byte
                                      Little Endian, utilizzato nei GUID
                                      classici e nei ban.

  📄 **Formattazione automatica**     Genera automaticamente la riga per
                                      il file `bans.txt` di BattlEye.

  👤 **SteamRep Checker**             Recupera avatar e nome utente e
                                      verifica lo stato dei ban VAC,
                                      Trade Ban e reputazione tramite un
                                      proxy pubblico.

  📋 **Copia rapida**                 Copia i risultati negli appunti con
                                      un clic.

  ⚡ **Elaborazione locale**          Le operazioni crittografiche
                                      vengono eseguite nel browser. Non
                                      servono backend o database.
  -----------------------------------------------------------------------

## 🧬 Formati di conversione

  -----------------------------------------------------------------------
  Formato           Algoritmo         Risultato         Utilizzo
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Hash codificato   File `.rpt` e
  ID**              URL-Safe                            profili DayZ

  **BattlEye / GUID MD5 + byte Little Esadecimale       GUID classici e
  classico**        Endian                              ban

  **BattlEye Ban    Formattazione     Riga `bans.txt`   Gestione dei ban
  Entry**           GUID                                
  -----------------------------------------------------------------------

I formati hanno scopi diversi e non sono intercambiabili.

## 🚀 Utilizzo rapido

1.  Scarica o clona questo repository.
2.  Apri `index.html` in un browser moderno.
3.  Incolla uno SteamID64 (es.: `76561198000000000`) o il link del
    profilo Steam.
4.  Fai clic su un risultato per copiarne il valore.

## ☁️ Hosting

  -----------------------------------------------------------------------------
  Piattaforma             Difficoltà             Costo         Configurazione
  ------------------ -------------------- -------------------- ----------------
  **GitHub Pages**        🟢 Facile              Gratis        Attivare Pages
                                                               nel repository

  **Cloudflare            🟢 Facile          Piano gratuito    Collegare il
  Pages**                                                      repository

  **Locale**           🟢 Molto facile           Gratis        Aprire
                                                               `index.html`

  **Server                 🟡 Media            Variabile       Servire i file
  personalizzato**                                             statici
  -----------------------------------------------------------------------------

Le conversioni funzionano offline. Le ricerche SteamRep richiedono
Internet.

## 🤝 Contributi

1.  Crea un Fork del repository.
2.  Crea un branch per la modifica.
3.  Apporta e testa le modifiche.
4.  Invia una Pull Request descrivendo il lavoro.

[Segnala un problema o proponi un
miglioramento](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇩🇪 Deutsch

## Beschreibung

**SteamID64 to GUID Converter** ist ein zu 100 % clientseitiges
(HTML/JS) Tool für Administratoren und Entwickler von DayZ- und
Arma-Servern. Es konvertiert SteamID64 in die nativen Hash-Formate der
Enfusion/Real-Virtuality-Engines und überprüft öffentliche
Kontoinformationen über SteamRep.

Keine Installation, kein Backend und keine Datenbank erforderlich.

## ✨ Funktionen

  -----------------------------------------------------------------------
  Funktion                            Beschreibung
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Erzeugt Base64 (URL-Safe) aus dem
                                      SHA-256-Klartext-Hash, der in
                                      `.rpt`-Dateien und
                                      DayZ-Standalone-Profilen verwendet
                                      wird.

  🛡️ **BattlEye / Klassisches Arma**  Erzeugt MD5 im Hexadezimalformat
                                      aus Little-Endian-Bytes, verwendet
                                      für klassische GUIDs und Banns.

  📄 **Automatische Formatierung**    Erstellt automatisch die Zeile für
                                      die BattlEye-Datei `bans.txt`.

  👤 **SteamRep Checker**             Ruft Profilbild und Benutzernamen
                                      ab und überprüft VAC-Banns, Trade
                                      Bans und den allgemeinen Ruf über
                                      einen öffentlichen Proxy.

  📋 **Schnelles Kopieren**           Kopiert Ergebnisse mit einem Klick
                                      in die Zwischenablage.

  ⚡ **Lokale Verarbeitung**          Kryptografische Verarbeitung
                                      erfolgt direkt im Browser. Kein
                                      Backend oder Datenbank
                                      erforderlich.
  -----------------------------------------------------------------------

## 🧬 Konvertierungsformate

  ----------------------------------------------------------------------------
  Format            Algorithmus           Ausgabe            Verwendung
  ----------------- --------------------- ------------------ -----------------
  **DayZ Hashed     SHA-256 → Base64      Kodierter Hash     `.rpt`-Dateien
  ID**              URL-Safe                                 und DayZ-Profile

  **BattlEye /      MD5 +                 Hexadezimal        Klassische GUIDs
  Klassische GUID** Little-Endian-Bytes                      und Banns

  **BattlEye Ban    GUID-Formatierung     `bans.txt`-Zeile   Bannverwaltung
  Entry**                                                    
  ----------------------------------------------------------------------------

Die Formate haben unterschiedliche Zwecke und sind nicht austauschbar.

## 🚀 Schnellstart

1.  Repository herunterladen oder klonen.
2.  `index.html` in einem modernen Browser öffnen.
3.  Eine SteamID64 (z. B. `76561198000000000`) oder eine
    Steam-Profil-URL einfügen.
4.  Auf ein Ergebnis klicken, um den Wert zu kopieren.

## ☁️ Hosting

  -------------------------------------------------------------------------
  Plattform          Schwierigkeit            Kosten        Einrichtung
  --------------- -------------------- -------------------- ---------------
  **GitHub             🟢 Einfach           Kostenlos       Pages im
  Pages**                                                   Repository
                                                            aktivieren

  **Cloudflare         🟢 Einfach       Kostenloser Tarif   Repository
  Pages**                                                   verbinden

  **Lokal**         🟢 Sehr einfach         Kostenlos       `index.html`
                                                            öffnen

  **Eigener            🟡 Mittel             Variabel       Statische
  Server**                                                  Dateien
                                                            bereitstellen
  -------------------------------------------------------------------------

Die Konvertierungen funktionieren offline. SteamRep-Abfragen benötigen
eine Internetverbindung.

## 🤝 Mitwirken

1.  Repository forken.
2.  Einen Branch für die Änderung erstellen.
3.  Änderungen durchführen und lokal testen.
4.  Einen Pull Request mit Beschreibung einreichen.

[Fehler melden oder Verbesserung
vorschlagen](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇨🇿 Čeština

## Popis

**SteamID64 to GUID Converter** je 100% klientský (HTML/JS) taktický
nástroj pro správce a vývojáře serverů DayZ a Arma. Převádí SteamID64 na
nativní hashovací formáty enginů Enfusion/Real Virtuality a ověřuje
veřejné informace o účtu prostřednictvím SteamRep.

Není nutná instalace, backend ani databáze.

## ✨ Funkce

  -----------------------------------------------------------------------
  Funkce                              Popis
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Generuje Base64 (URL-Safe) z
                                      prostého SHA-256, používaného v
                                      souborech `.rpt` a profilech DayZ
                                      Standalone.

  🛡️ **BattlEye / Klasická Arma**     Generuje hexadecimální MD5 z bajtů
                                      Little Endian, používaný pro
                                      klasická GUID a bany.

  📄 **Automatické formátování**      Automaticky generuje řádek pro
                                      soubor BattlEye `bans.txt`.

  👤 **SteamRep Checker**             Získává profilový obrázek a
                                      uživatelské jméno a ověřuje VAC
                                      bany, Trade Bans a celkovou
                                      reputaci prostřednictvím veřejného
                                      proxy serveru.

  📋 **Rychlé kopírování**            Kliknutím zkopíruje výsledek do
                                      schránky.

  ⚡ **Lokální zpracování**           Kryptografické operace probíhají v
                                      prohlížeči. Není potřeba backend
                                      ani databáze.
  -----------------------------------------------------------------------

## 🧬 Formáty převodu

  -----------------------------------------------------------------------
  Formát            Algoritmus        Výstup            Použití
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Kódovaný hash     Soubory `.rpt` a
  ID**              URL-Safe                            profily DayZ

  **BattlEye /      MD5 + bajty       Hexadecimální     Klasická GUID a
  klasické GUID**   Little Endian                       bany

  **BattlEye Ban    Formátování GUID  Řádek `bans.txt`  Správa banů
  Entry**                                               
  -----------------------------------------------------------------------

Jednotlivé formáty mají odlišné použití a nelze je zaměňovat.

## 🚀 Rychlé použití

1.  Stáhněte nebo naklonujte tento repozitář.
2.  Otevřete `index.html` v moderním prohlížeči.
3.  Vložte SteamID64 (např. `76561198000000000`) nebo URL profilu Steam.
4.  Kliknutím na výsledek zkopírujete jeho hodnotu.

## ☁️ Hosting

  -------------------------------------------------------------------------
  Platforma            Obtížnost               Cena         Nastavení
  --------------- -------------------- -------------------- ---------------
  **GitHub             🟢 Snadné              Zdarma        Aktivovat Pages
  Pages**                                                   v repozitáři

  **Cloudflare         🟢 Snadné         Bezplatný tarif    Připojit
  Pages**                                                   repozitář

  **Lokálně**       🟢 Velmi snadné           Zdarma        Otevřít
                                                            `index.html`

  **Vlastní            🟡 Střední          Podle služby     Zpřístupnit
  server**                                                  statické
                                                            soubory
  -------------------------------------------------------------------------

Převody fungují offline. Dotazy SteamRep vyžadují připojení k internetu.

## 🤝 Přispívání

1.  Vytvořte Fork repozitáře.
2.  Vytvořte větev pro svou změnu.
3.  Proveďte a lokálně otestujte úpravy.
4.  Odešlete Pull Request s popisem změn.

[Nahlásit chybu nebo navrhnout
vylepšení](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇷🇺 Русский

## Описание

**SteamID64 to GUID Converter** --- это тактический инструмент на
HTML/JavaScript, полностью работающий на стороне клиента, для
администраторов и разработчиков серверов DayZ и Arma. Он преобразует
SteamID64 в нативные форматы хешей движков Enfusion/Real Virtuality и
проверяет общедоступную информацию об аккаунте через SteamRep.

Установка, backend и база данных не требуются.

## ✨ Возможности

  -----------------------------------------------------------------------
  Возможность                         Описание
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Создаёт Base64 (URL-Safe) из
                                      обычного SHA-256, используемого в
                                      файлах `.rpt` и профилях DayZ
                                      Standalone.

  🛡️ **BattlEye / классическая Arma** Создаёт шестнадцатеричный MD5 из
                                      байтов Little Endian для
                                      классических GUID и банов.

  📄 **Автоматическое                 Автоматически формирует строку для
  форматирование**                    файла BattlEye `bans.txt`.

  👤 **SteamRep Checker**             Получает аватар и имя пользователя,
                                      проверяет VAC-баны, Trade Bans и
                                      общую репутацию через публичный
                                      прокси.

  📋 **Быстрое копирование**          Копирует результат в буфер обмена
                                      одним нажатием.

  ⚡ **Локальная обработка**          Криптографические операции
                                      выполняются в браузере. Backend и
                                      база данных не нужны.
  -----------------------------------------------------------------------

## 🧬 Форматы преобразования

  -------------------------------------------------------------------------
  Формат            Алгоритм          Результат           Назначение
  ----------------- ----------------- ------------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Закодированный хеш  Файлы `.rpt` и
  ID**              URL-Safe                              профили DayZ

  **BattlEye /      MD5 + байты       Шестнадцатеричный   Классические GUID
  классический      Little Endian     формат              и баны
  GUID**                                                  

  **BattlEye Ban    Форматирование    Строка `bans.txt`   Управление банами
  Entry**           GUID                                  
  -------------------------------------------------------------------------

Форматы предназначены для разных задач и не взаимозаменяемы.

## 🚀 Быстрый старт

1.  Скачайте или клонируйте репозиторий.
2.  Откройте `index.html` в современном браузере.
3.  Вставьте SteamID64 (например, `76561198000000000`) или ссылку на
    профиль Steam.
4.  Нажмите на результат, чтобы скопировать его.

## ☁️ Размещение

  -------------------------------------------------------------------------
  Платформа            Сложность            Стоимость       Настройка
  --------------- -------------------- -------------------- ---------------
  **GitHub              🟢 Легко            Бесплатно       Включить Pages
  Pages**                                                   в репозитории

  **Cloudflare          🟢 Легко         Бесплатный тариф   Подключить
  Pages**                                                   репозиторий

  **Локально**       🟢 Очень легко         Бесплатно       Открыть
                                                            `index.html`

  **Собственный        🟡 Средне        Зависит от сервиса  Разместить
  сервер**                                                  статические
                                                            файлы
  -------------------------------------------------------------------------

Конвертация работает офлайн. Запросы SteamRep требуют подключения к
интернету.

## 🤝 Участие в проекте

1.  Сделайте Fork репозитория.
2.  Создайте ветку для изменений.
3.  Внесите и проверьте изменения локально.
4.  Отправьте Pull Request с описанием изменений.

[Сообщить об ошибке или предложить
улучшение](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇵🇱 Polski

## Opis

**SteamID64 to GUID Converter** to w 100% klienckie narzędzie taktyczne
HTML/JavaScript dla administratorów i programistów serwerów DayZ i Arma.
Konwertuje SteamID64 do natywnych formatów hash silników Enfusion/Real
Virtuality i sprawdza publiczne informacje o koncie za pomocą SteamRep.

Nie wymaga instalacji, backendu ani bazy danych.

## ✨ Funkcje

  -----------------------------------------------------------------------
  Funkcja                             Opis
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Generuje Base64 (URL-Safe) z
                                      tekstowego SHA-256, używanego w
                                      plikach `.rpt` i profilach DayZ
                                      Standalone.

  🛡️ **BattlEye / klasyczna Arma**    Generuje szesnastkowy MD5 z bajtów
                                      Little Endian, używany w
                                      klasycznych GUID i banach.

  📄 **Automatyczne formatowanie**    Automatycznie generuje wpis do
                                      pliku BattlEye `bans.txt`.

  👤 **SteamRep Checker**             Pobiera awatar i nazwę użytkownika
                                      oraz sprawdza bany VAC, Trade Bans
                                      i ogólną reputację za pośrednictwem
                                      publicznego proxy.

  📋 **Szybkie kopiowanie**           Kopiuje wynik do schowka jednym
                                      kliknięciem.

  ⚡ **Przetwarzanie lokalne**        Operacje kryptograficzne wykonywane
                                      są w przeglądarce. Backend i baza
                                      danych nie są wymagane.
  -----------------------------------------------------------------------

## 🧬 Formaty konwersji

  -----------------------------------------------------------------------
  Format            Algorytm          Wynik             Zastosowanie
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Zakodowany hash   Pliki `.rpt` i
  ID**              URL-Safe                            profile DayZ

  **BattlEye /      MD5 + bajty       Zapis             Klasyczne GUID i
  klasyczny GUID**  Little Endian     szesnastkowy      bany

  **BattlEye Ban    Formatowanie GUID Wpis `bans.txt`   Zarządzanie
  Entry**                                               banami
  -----------------------------------------------------------------------

Formaty mają różne zastosowania i nie są zamienne.

## 🚀 Szybki start

1.  Pobierz lub sklonuj repozytorium.
2.  Otwórz `index.html` w nowoczesnej przeglądarce.
3.  Wklej SteamID64 (np. `76561198000000000`) lub adres profilu Steam.
4.  Kliknij wynik, aby skopiować jego wartość.

## ☁️ Hosting

  -------------------------------------------------------------------------
  Platforma             Trudność              Koszt         Konfiguracja
  --------------- -------------------- -------------------- ---------------
  **GitHub              🟢 Łatwa            Bezpłatnie      Włącz Pages w
  Pages**                                                   repozytorium

  **Cloudflare          🟢 Łatwa           Darmowy plan     Połącz
  Pages**                                                   repozytorium

  **Lokalnie**      🟢 Bardzo łatwa         Bezpłatnie      Otwórz
                                                            `index.html`

  **Własny             🟡 Średnia       Zależnie od usługi  Udostępnij
  serwer**                                                  pliki statyczne
  -------------------------------------------------------------------------

Konwersja działa offline. Zapytania SteamRep wymagają połączenia z
internetem.

## 🤝 Współtworzenie

1.  Zrób Fork repozytorium.
2.  Utwórz gałąź dla zmian.
3.  Wprowadź i przetestuj zmiany lokalnie.
4.  Wyślij Pull Request z opisem zmian.

[Zgłoś błąd lub zaproponuj
ulepszenie](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇧🇷 Português (Brasil)

## Descrição

**SteamID64 to GUID Converter** é uma ferramenta tática 100% client-side
(HTML/JS) para administradores e desenvolvedores de servidores DayZ e
Arma. Converte SteamID64 para os formatos de hash nativos das engines
Enfusion/Real Virtuality e verifica informações públicas de contas
através do SteamRep.

Não requer instalação, backend ou banco de dados.

## ✨ Recursos

  -----------------------------------------------------------------------
  Recurso                             Descrição
  ----------------------------------- -----------------------------------
  🔐 **DayZ Hashed ID**               Gera o Base64 (URL-Safe) do SHA-256
                                      em texto puro, utilizado em
                                      arquivos `.rpt` e perfis do DayZ
                                      Standalone.

  🛡️ **BattlEye / Arma clássico**     Gera o MD5 hexadecimal dos bytes
                                      Little Endian, utilizado em GUIDs
                                      clássicos e bans.

  📄 **Formatação automática**        Gera automaticamente a linha para o
                                      arquivo `bans.txt` do BattlEye.

  👤 **SteamRep Checker**             Obtém avatar e nome de usuário e
                                      verifica o status de VAC, Trade
                                      Bans e reputação geral através de
                                      um proxy público.

  📋 **Cópia rápida**                 Copia qualquer resultado para a
                                      área de transferência com um
                                      clique.

  ⚡ **Processamento local**          O processamento criptográfico
                                      acontece no navegador. Não é
                                      necessário backend ou banco de
                                      dados.
  -----------------------------------------------------------------------

## 🧬 Formatos de conversão

  -----------------------------------------------------------------------
  Formato           Algoritmo         Resultado         Uso
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  Hash codificado   Arquivos `.rpt` e
  ID**              URL-Safe                            perfis DayZ

  **BattlEye / GUID MD5 + bytes       Hexadecimal       GUIDs clássicos e
  clássico**        Little Endian                       bans

  **BattlEye Ban    Formatação de     Linha `bans.txt`  Gerenciamento de
  Entry**           GUID                                bans
  -----------------------------------------------------------------------

Os formatos têm finalidades diferentes e não são intercambiáveis.

## 🚀 Início rápido

1.  Baixe ou clone este repositório.
2.  Abra `index.html` em um navegador moderno.
3.  Cole um SteamID64 (ex.: `76561198000000000`) ou o link de um perfil
    Steam.
4.  Clique em qualquer resultado para copiar o valor.

## ☁️ Hospedagem

  -------------------------------------------------------------------------
  Plataforma          Dificuldade             Custo         Configuração
  --------------- -------------------- -------------------- ---------------
  **GitHub              🟢 Fácil              Grátis        Ativar Pages no
  Pages**                                                   repositório

  **Cloudflare          🟢 Fácil          Plano gratuito    Conectar o
  Pages**                                                   repositório

  **Local**          🟢 Muito fácil           Grátis        Abrir
                                                            `index.html`

  **Servidor            🟡 Média             Variável       Servir os
  próprio**                                                 arquivos
                                                            estáticos
  -------------------------------------------------------------------------

As conversões funcionam offline. As consultas ao SteamRep exigem conexão
com a internet.

## 🤝 Contribuições

1.  Faça um Fork do repositório.
2.  Crie uma branch para sua alteração.
3.  Implemente e teste as mudanças localmente.
4.  Envie um Pull Request descrevendo as alterações.

[Reportar um problema ou sugerir uma
melhoria](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

------------------------------------------------------------------------

# 🇨🇳 简体中文

## 简介

**SteamID64 to GUID Converter** 是一款面向 DayZ 和 Arma
服务器管理员及开发者的 100% 客户端 HTML/JavaScript 工具。它可将
SteamID64 转换为 Enfusion/Real Virtuality 引擎使用的原生哈希格式，并通过
SteamRep 检查公开帐户信息。

无需安装、后端或数据库。

## ✨ 功能

  ----------------------------------------------------------------------------------------
  功能                                说明
  ----------------------------------- ----------------------------------------------------
  🔐 **DayZ Hashed ID**               生成纯文本 SHA-256 的 Base64（URL-Safe），用于
                                      `.rpt` 文件和 DayZ Standalone 配置文件。

  🛡️ **BattlEye / 经典 Arma**         从 Little Endian 字节生成十六进制 MD5，用于经典 GUID
                                      和封禁。

  📄 **自动格式化**                   自动生成 BattlEye `bans.txt` 文件所需的封禁行。

  👤 **SteamRep Checker**             通过公共代理获取头像、用户名，并检查 VAC
                                      封禁、交易封禁和总体声誉。

  📋 **快速复制**                     点击结果即可复制到剪贴板。

  ⚡ **本地处理**                     所有加密处理均在浏览器本地运行，无需后端或数据库。
  ----------------------------------------------------------------------------------------

## 🧬 转换格式

  -----------------------------------------------------------------------
  格式              算法              输出              用途
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  编码哈希          `.rpt` 文件和
  ID**              URL-Safe                            DayZ 配置文件

  **BattlEye / 经典 MD5 + Little      十六进制          经典 GUID 和封禁
  GUID**            Endian 字节                         

  **BattlEye Ban    GUID 格式化       `bans.txt` 行     服务器封禁管理
  Entry**                                               
  -----------------------------------------------------------------------

这些格式用途不同，不能互换。

## 🚀 快速开始

1.  下载或克隆此仓库。
2.  使用现代浏览器打开 `index.html`。
3.  粘贴 SteamID64（例如 `76561198000000000`）或完整 Steam
    个人资料链接。
4.  点击任意结果框即可复制对应值。

## ☁️ 部署托管

  平台                       难度          费用     配置
  ---------------------- ------------- ------------ --------------------
  **GitHub Pages**          🟢 简单        免费     在仓库中启用 Pages
  **Cloudflare Pages**      🟢 简单      免费套餐   连接 Git 仓库
  **本地运行**            🟢 非常简单      免费     打开 `index.html`
  **自建服务器**            🟡 中等     视服务而定  部署静态文件

加密转换可离线运行。SteamRep 查询需要互联网连接。

## 🤝 参与贡献

1.  Fork 此仓库。
2.  为修改创建分支。
3.  完成修改并在本地测试。
4.  提交 Pull Request 并说明修改内容。

[报告问题或提出改进建议](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues)。

------------------------------------------------------------------------

# 🇹🇼 繁體中文

## 簡介

**SteamID64 to GUID Converter** 是一款面向 DayZ 和 Arma
伺服器管理員及開發者的 100% 客戶端 HTML/JavaScript 工具。它可將
SteamID64 轉換為 Enfusion/Real Virtuality 引擎使用的原生雜湊格式，並透過
SteamRep 檢查公開帳戶資訊。

無需安裝、後端或資料庫。

## ✨ 功能

  ----------------------------------------------------------------------------------------
  功能                                說明
  ----------------------------------- ----------------------------------------------------
  🔐 **DayZ Hashed ID**               生成純文字 SHA-256 的 Base64（URL-Safe），用於
                                      `.rpt` 檔案和 DayZ Standalone 設定檔。

  🛡️ **BattlEye / 經典 Arma**         從 Little Endian 位元組生成十六進位 MD5，用於經典
                                      GUID 和封鎖。

  📄 **自動格式化**                   自動生成 BattlEye `bans.txt` 檔案所需的封鎖行。

  👤 **SteamRep Checker**             透過公共代理取得頭像、使用者名稱，並檢查 VAC
                                      封鎖、交易封鎖和整體聲譽。

  📋 **快速複製**                     點擊結果即可複製到剪貼簿。

  ⚡ **本機處理**                     所有加密處理都在瀏覽器本機執行，無需後端或資料庫。
  ----------------------------------------------------------------------------------------

## 🧬 轉換格式

  -----------------------------------------------------------------------
  格式              演算法            輸出              用途
  ----------------- ----------------- ----------------- -----------------
  **DayZ Hashed     SHA-256 → Base64  編碼雜湊          `.rpt` 檔案和
  ID**              URL-Safe                            DayZ 設定檔

  **BattlEye / 經典 MD5 + Little      十六進位          經典 GUID 和封鎖
  GUID**            Endian 位元組                       

  **BattlEye Ban    GUID 格式化       `bans.txt` 行     伺服器封鎖管理
  Entry**                                               
  -----------------------------------------------------------------------

這些格式用途不同，不能互換。

## 🚀 快速開始

1.  下載或複製此儲存庫。
2.  使用現代瀏覽器開啟 `index.html`。
3.  貼上 SteamID64（例如 `76561198000000000`）或完整 Steam
    個人資料連結。
4.  點擊任何結果框即可複製對應值。

## ☁️ 部署託管

  平台                       難度          費用     設定
  ---------------------- ------------- ------------ ----------------------
  **GitHub Pages**          🟢 簡單        免費     在儲存庫中啟用 Pages
  **Cloudflare Pages**      🟢 簡單      免費方案   連結 Git 儲存庫
  **本機執行**            🟢 非常簡單      免費     開啟 `index.html`
  **自架伺服器**            🟡 中等     視服務而定  部署靜態檔案

加密轉換可離線執行。SteamRep 查詢需要網際網路連線。

## 🤝 參與貢獻

1.  Fork 此儲存庫。
2.  為修改建立分支。
3.  完成修改並在本機測試。
4.  提交 Pull Request 並說明修改內容。

[回報問題或提出改進建議](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues)。

------------------------------------------------------------------------

# 🇯🇵 日本語

## 概要

**SteamID64 to GUID Converter** は、DayZ および Arma
サーバーの管理者や開発者向けの 100% クライアントサイド HTML/JavaScript
ツールです。SteamID64 を Enfusion/Real Virtuality
エンジンのネイティブハッシュ形式に変換し、SteamRep
を通じて公開アカウント情報を確認できます。

インストール、バックエンド、データベースは不要です。

## ✨ 機能

  ----------------------------------------------------------------------------------------------------------------
  機能                                説明
  ----------------------------------- ----------------------------------------------------------------------------
  🔐 **DayZ Hashed ID**               `.rpt` ファイルや DayZ Standalone プロファイルで使用される、プレーンテキスト
                                      SHA-256 の Base64（URL-Safe）を生成します。

  🛡️ **BattlEye / クラシック Arma**   Little Endian バイトから 16 進数 MD5 を生成し、クラシック GUID や BAN
                                      に使用します。

  📄 **自動フォーマット**             BattlEye の `bans.txt` ファイル用の行を自動生成します。

  👤 **SteamRep Checker**             公開プロキシ経由でプロフィール画像、ユーザー名を取得し、VAC BAN、Trade
                                      BAN、全体的な評価を確認します。

  📋 **ワンクリックコピー**           結果をクリックしてクリップボードにコピーできます。

  ⚡ **ローカル処理**                 暗号処理はブラウザ内で実行されます。バックエンドやデータベースは不要です。
  ----------------------------------------------------------------------------------------------------------------

## 🧬 変換形式

  ------------------------------------------------------------------------------
  形式              アルゴリズム      出力                     用途
  ----------------- ----------------- ------------------------ -----------------
  **DayZ Hashed     SHA-256 → Base64  エンコード済みハッシュ   `.rpt` ファイルと
  ID**              URL-Safe                                   DayZ プロファイル

  **BattlEye /      MD5 + Little      16 進数                  クラシック GUID
  クラシック GUID** Endian バイト                              と BAN

  **BattlEye Ban    GUID              `bans.txt` の行          サーバーの BAN
  Entry**           のフォーマット                             管理
  ------------------------------------------------------------------------------

各形式は用途が異なり、相互に置き換えることはできません。

## 🚀 クイックスタート

1.  このリポジトリをダウンロードまたはクローンします。
2.  最新のブラウザで `index.html` を開きます。
3.  SteamID64（例：`76561198000000000`）または Steam プロフィール URL
    を貼り付けます。
4.  結果欄をクリックして値をコピーします。

## ☁️ ホスティング

  プラットフォーム           難易度            費用       設定
  ---------------------- --------------- ---------------- -----------------------------
  **GitHub Pages**           🟢 簡単           無料       リポジトリで Pages を有効化
  **Cloudflare Pages**       🟢 簡単        無料プラン    Git リポジトリを接続
  **ローカル**            🟢 とても簡単        無料       `index.html` を開く
  **独自サーバー**          🟡 中程度     サービスによる  静的ファイルを配信

暗号変換はオフラインで動作します。SteamRep
の照会にはインターネット接続が必要です。

## 🤝 コントリビューション

1.  リポジトリを Fork します。
2.  変更用のブランチを作成します。
3.  変更を実装し、ローカルでテストします。
4.  変更内容を説明して Pull Request を送信します。

[バグ報告または改善提案](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues)。

------------------------------------------------------------------------

## 📜 License

Developed and maintained by
[IgnacioChemes](https://github.com/ignaciochemes).

Distributed under the [MIT
License](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/blob/main/LICENSE).
You are free to use, modify and distribute the code according to its
terms.

::: {align="center"}
**⚙️ Built for server administrators. Designed for practical use.**

If this tool helps you manage your DayZ or Arma server, consider giving
the repository a ⭐.

[![Star this
repository](https://img.shields.io/badge/⭐_Star_this_repository-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool)
:::
