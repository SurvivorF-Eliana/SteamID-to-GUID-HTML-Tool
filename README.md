# 🎮 SteamID64 to GUID Converter

\<p align="center">
&#x20; \<strong>A tactical identity conversion toolkit for DayZ & Arma administrators.\</strong>
&#x20; \<br />
&#x20; Convert SteamID64 into native engine identifiers, generate BattlEye bans and inspect Steam account reputation.
\</p>

\<p align="center">   \<a href="#english">🇬🇧 English\</a> ·   \<a href="#español">🇦🇷 Español\</a> \</p>

\<p align="center">   \<a href="[https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool)">     \<img src="[https://img.shields.io/github/stars/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github&label=Stars](https://img.shields.io/github/stars/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge\&logo=github\&label=Stars)" alt="GitHub Stars" />   \</a>   \<a href="[https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/network/members](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/network/members)">     \<img src="[https://img.shields.io/github/forks/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github&label=Forks](https://img.shields.io/github/forks/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge\&logo=github\&label=Forks)" alt="GitHub Forks" />   \</a>   \<a href="[https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/blob/main/LICENSE](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/blob/main/LICENSE)">     \<img src="[https://img.shields.io/github/license/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&color=blue](https://img.shields.io/github/license/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge\&color=blue)" alt="License" />   \</a>   \<a href="[https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/commits/main](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/commits/main)">     \<img src="[https://img.shields.io/github/last-commit/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge&logo=github&label=Last%20commit](https://img.shields.io/github/last-commit/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool?style=for-the-badge\&logo=github\&label=Last%20commit)" alt="Last Commit" />   \</a> \</p>

\<p align="center">   \<img src="[https://img.shields.io/badge/Platform-Web%20%2F%20Desktop-18181b?style=flat-square](https://img.shields.io/badge/Platform-Web%20%2F%20Desktop-18181b?style=flat-square)" />   \<img src="[https://img.shields.io/badge/Architecture-Client--Side-18181b?style=flat-square](https://img.shields.io/badge/Architecture-Client--Side-18181b?style=flat-square)" />   \<img src="[https://img.shields.io/badge/Backend-Not%20Required-18181b?style=flat-square](https://img.shields.io/badge/Backend-Not%20Required-18181b?style=flat-square)" />   \<img src="[https://img.shields.io/badge/DayZ-Supported-8aab42?style=flat-square](https://img.shields.io/badge/DayZ-Supported-8aab42?style=flat-square)" />   \<img src="[https://img.shields.io/badge/Arma-Supported-8aab42?style=flat-square](https://img.shields.io/badge/Arma-Supported-8aab42?style=flat-square)" />   \<img src="[https://img.shields.io/badge/Dependencies-None-18181b?style=flat-square](https://img.shields.io/badge/Dependencies-None-18181b?style=flat-square)" /> \</p>

---

## 📑 Navigation

- [🇬🇧 English](#english)
  - [Overview](#overview)
  - [Features](#features)
  - [Conversion formats](#conversion-formats)
  - [Interface preview](#interface-preview)
  - [Quick start](#quick-start)
  - [Deployment](#deployment)
  - [Technology stack](#technology-stack)
  - [Contributing](#contributing)
- [🇦🇷 Español](#español)
  - [Descripción](#descripción)
  - [Características](#características)
  - [Formatos de conversión](#formatos-de-conversión)
  - [Instalación](#instalación)
  - [Despliegue](#despliegue)
  - [Contribuciones](#contribuciones)
- [📜 License](#license)

---

# 🇬🇧 English

\<a id="overview">\</a>

## Overview

**SteamID64 to GUID Converter** is a 100% client-side HTML/JavaScript toolkit designed for DayZ and Arma server administrators, developers and community managers.

It converts SteamID64 identifiers into native engine-compatible hash formats and provides additional utilities for BattlEye ban management and Steam account reputation checks.

No installation, backend, database or external dependencies are required.

### ✨ Features

\<table>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🔐 Identity Conversion\</h3>
&#x20;     Convert SteamID64 into DayZ Hashed IDs and classic BattlEye GUIDs.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🛡️ BattlEye Integration\</h3>
&#x20;     Generate formatted ban entries compatible with \<code>bans.txt\</code>.
&#x20;   \</td>
&#x20; \</tr>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>👤 SteamRep Checker\</h3>
&#x20;     Retrieve public profile information, avatars, usernames and reputation indicators.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>📋 One-Click Copy\</h3>
&#x20;     Copy generated identifiers and formatted results directly to your clipboard.
&#x20;   \</td>
&#x20; \</tr>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>⚡ Local Processing\</h3>
&#x20;     Cryptographic calculations run directly inside your browser.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🌐 Serverless Architecture\</h3>
&#x20;     No application server or database required.
&#x20;   \</td>
&#x20; \</tr>
\</table>

\<a id="conversion-formats">\</a>

### 🧬 Conversion formats

The tool supports different identification formats depending on the target engine and use case.

| Format                 | Algorithm                 | Output          | Intended use                          |
| :--------------------- | :------------------------ | :-------------- | :------------------------------------ |
| **DayZ Hashed ID**     | SHA-256 → Base64 URL-Safe | Encoded hash    | DayZ `.rpt` files and player profiles |
| **BattlEye GUID**      | MD5 + Little Endian bytes | Hexadecimal     | Classic Arma GUIDs and BattlEye bans  |
| **BattlEye Ban Entry** | GUID formatting           | `bans.txt` line | Server ban management                 |

**Why different formats?**

- **SHA-256:** Generates a 256-bit digest from the SteamID64 text representation, subsequently encoded using URL-safe Base64.
- **MD5:** Processes the identifier's Little Endian byte representation to generate the hexadecimal GUID format.
- **BattlEye entry:** Formats the resulting GUID into a ready-to-use ban entry.

These formats are not interchangeable. Always use the identifier expected by the target game or server system.

### 🖥️ Interface preview

Conceptual workflow:

```text
┌──────────────────────────────────────────────────────┐
│           STEAMID64 → GUID CONVERTER                  │
├──────────────────────────────────────────────────────┤
│                                                      │
│  INPUT                                               │
│  ┌────────────────────────────────────────────────┐  │
│  │ 76561198000000000                              │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  CONVERSION RESULTS                                  │
│  ┌────────────────────────────────────────────────┐  │
│  │ DAYZ HASHED ID                         [COPY]  │  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE GUID                         [COPY]  │  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE BAN ENTRY                    [COPY]  │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  STEAMREP ACCOUNT CHECK                              │
│  ┌────────────────────────────────────────────────┐  │
│  │ Profile information · VAC · Trade bans         │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
└──────────────────────────────────────────────────────┘
```

*Illustrative workflow, not an exact screenshot of the application.*

\<a id="quick-start">\</a>

### 🚀 Quick start

**Option 1 — Run locally**

1. Clone or download the repository.
2. Extract the files.
3. Open `index.html` in your browser.
4. Paste a SteamID64 or Steam profile URL.
5. Click any result to copy its value.

**Option 2 — Use the hosted version**

Visit the project's deployed web application when GitHub Pages or another hosting deployment is configured.

### ☁️ Deployment

The application has no backend requirements, making it suitable for static hosting.

| Hosting               |  Difficulty  |    Cost   | Setup                               |
| :-------------------- | :----------: | :-------: | :---------------------------------- |
| **GitHub Pages**      |    🟢 Easy   |    Free   | Connect repository and enable Pages |
| **Cloudflare Pages**  |    🟢 Easy   | Free tier | Connect Git repository              |
| **Local hosting**     | 🟢 Very easy |    Free   | Open `index.html`                   |
| **Custom web server** |   🟡 Medium  |  Depends  | Upload static files                 |

**Offline compatibility:** Cryptographic conversion features can run locally. SteamRep profile lookups require an internet connection.

\<a id="technology-stack">\</a>

### 🧰 Technology stack

\<p>   \<img src="[https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge\&logo=html5\&logoColor=white)" />   \<img src="[https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge\&logo=javascript\&logoColor=black)" />   \<img src="[https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github\&logoColor=white)" />   \<img src="[https://img.shields.io/badge/Steam-000000?style=for-the-badge&logo=steam&logoColor=white](https://img.shields.io/badge/Steam-000000?style=for-the-badge\&logo=steam\&logoColor=white)" /> \</p>

| Component    | Purpose                                                 |
| :----------- | :------------------------------------------------------ |
| HTML         | Application structure                                   |
| JavaScript   | Conversion logic and application functionality          |
| Browser APIs | Local cryptographic processing and clipboard operations |
| SteamRep     | External account reputation information                 |

### 🔒 Privacy and architecture

- Cryptographic calculations are performed locally in the browser.
- No application backend or database is needed.
- SteamRep lookups rely on a public proxy.
- No private API keys are embedded in the application.

**Important:** External profile lookups still involve third-party services. Client-side processing does not mean every network request remains local.

\<a id="contributing">\</a>

### 🤝 Contributing

Contributions, suggestions and bug reports are welcome.

1. Fork this repository.
2. Create a feature branch.
3. Make your changes.
4. Test the application locally.
5. Submit a Pull Request describing your changes.

For bugs or suggestions, open a [GitHub Issue](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

---

# 🇦🇷 Español

\<a id="descripción">\</a>

## Descripción

**SteamID64 to GUID Converter** es una herramienta táctica desarrollada en HTML y JavaScript para administradores, desarrolladores y gestores de comunidades de servidores DayZ y Arma.

Permite convertir identificadores SteamID64 a formatos hash compatibles con los motores de los juegos, generar entradas de bans para BattlEye y consultar información pública de reputación de cuentas de Steam.

Funciona completamente del lado del cliente, sin instalación, backend ni bases de datos.

\<a id="características">\</a>

### ✨ Características

\<table>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🔐 Conversión de identificadores\</h3>
&#x20;     Generación de DayZ Hashed ID y GUID clásicos de BattlEye.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🛡️ Integración BattlEye\</h3>
&#x20;     Generación automática de entradas compatibles con \<code>bans.txt\</code>.
&#x20;   \</td>
&#x20; \</tr>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>👤 SteamRep Checker\</h3>
&#x20;     Consulta de perfiles públicos, avatares, nombres y reputación.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>📋 Copiado rápido\</h3>
&#x20;     Copia de identificadores y resultados directamente al portapapeles.
&#x20;   \</td>
&#x20; \</tr>
&#x20; \<tr>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>⚡ Procesamiento local\</h3>
&#x20;     Los cálculos criptográficos se ejecutan en el navegador.
&#x20;   \</td>
&#x20;   \<td width="50%" valign="top">
&#x20;     \<h3>🌐 Arquitectura serverless\</h3>
&#x20;     No necesita servidor de aplicación ni base de datos.
&#x20;   \</td>
&#x20; \</tr>
\</table>

\<a id="formatos-de-conversión">\</a>

### 🧬 Formatos de conversión

| Formato                | Algoritmo                 | Resultado        | Aplicación                      |
| :--------------------- | :------------------------ | :--------------- | :------------------------------ |
| **DayZ Hashed ID**     | SHA-256 → Base64 URL-Safe | Hash codificado  | Archivos `.rpt` y perfiles DayZ |
| **BattlEye GUID**      | MD5 + bytes Little Endian | Hexadecimal      | GUID clásicos y bans            |
| **BattlEye Ban Entry** | Formateo de GUID          | Línea `bans.txt` | Administración de bans          |

**¿Por qué existen diferentes formatos?**

- **SHA-256:** Genera un hash de 256 bits a partir del SteamID64 en texto plano, posteriormente codificado en Base64 URL-Safe.
- **MD5:** Procesa la representación de bytes Little Endian para generar el GUID hexadecimal.
- **BattlEye:** Formatea el GUID para generar una entrada lista para utilizar en `bans.txt`.

Cada formato tiene una aplicación específica. No son intercambiables.

### 🖥️ Flujo de uso

```text
┌──────────────────────────────────────────────────────┐
│              STEAMID64 → GUID CONVERTER               │
├──────────────────────────────────────────────────────┤
│                                                      │
│  IDENTIFICADOR DE ENTRADA                            │
│  ┌────────────────────────────────────────────────┐  │
│  │ 76561198000000000                              │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  RESULTADOS                                          │
│  ┌────────────────────────────────────────────────┐  │
│  │ DAYZ HASHED ID                         [COPIAR]│  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE GUID                         [COPIAR]│  │
│  ├────────────────────────────────────────────────┤  │
│  │ BATTLEYE BAN ENTRY                    [COPIAR]│  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
│  CONSULTA DE CUENTA STEAM                            │
│  ┌────────────────────────────────────────────────┐  │
│  │ Perfil · VAC · Trade Bans                      │  │
│  └────────────────────────────────────────────────┘  │
│                                                      │
└──────────────────────────────────────────────────────┘
```

*Diagrama ilustrativo del flujo de trabajo, no una captura exacta de la interfaz.*

\<a id="instalación">\</a>

### 🚀 Uso rápido

**Ejecución local**

1. Cloná o descargá el repositorio.
2. Extraé los archivos.
3. Abrí `index.html` en tu navegador.
4. Pegá un SteamID64 o la URL de un perfil de Steam.
5. Hacé clic en cualquier resultado para copiarlo.

\<a id="despliegue">\</a>

### ☁️ Hosting y despliegue

| Plataforma           |  Dificultad  |     Costo     | Configuración                   |
| :------------------- | :----------: | :-----------: | :------------------------------ |
| **GitHub Pages**     |   🟢 Fácil   |     Gratis    | Activar Pages en el repositorio |
| **Cloudflare Pages** |   🟢 Fácil   | Plan gratuito | Conectar repositorio            |
| **Local**            | 🟢 Muy fácil |     Gratis    | Abrir `index.html`              |
| **Servidor propio**  |   🟡 Media   |    Variable   | Subir archivos estáticos        |

Las conversiones criptográficas funcionan localmente. Las consultas de perfiles requieren conexión a internet.

\<a id="contribuciones">\</a>

### 🤝 Contribuciones

Las mejoras, sugerencias y reportes de errores son bienvenidos.

1. Hacé un Fork del repositorio.
2. Creá una rama para tu modificación.
3. Implementá los cambios.
4. Probá la aplicación localmente.
5. Enviá un Pull Request explicando qué modificaste.

También podés reportar errores o proponer mejoras desde [GitHub Issues](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool/issues).

---

\<a id="license">\</a>

## 📜 License

This project is distributed under the **MIT License**.

You are free to use, modify and distribute the source code according to the license terms.

Developed and maintained by [IgnacioChemes](https://github.com/ignaciochemes).

---

\<p align="center">   \<strong>⚙️ Built for server administrators. Designed for practical use.\</strong>   \<br />\<br />   If this project helps you manage your DayZ or Arma server,   \<br />   consider giving it a ⭐ on GitHub.   \<br />\<br />   \<a href="[https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool](https://github.com/SurvivorF-Eliana/SteamID-to-GUID-HTML-Tool)">     \<img src="[https://img.shields.io/badge/⭐\_Star_this_repository-GitHub-181717?style=for-the-badge&logo=github](https://img.shields.io/badge/⭐_Star_this_repository-GitHub-181717?style=for-the-badge\&logo=github)" alt="Star this repository" />   \</a> \</p>
