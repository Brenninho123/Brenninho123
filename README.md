# Brenninho — Developer Portfolio

## About

Brenninho (Breno) is a Brazilian mobile-focused game developer working primarily in the **Friday Night Funkin'** ecosystem — building engines, forks, mobile ports, mods, and standalone tools for the FNF modding community.

- 🎮 Focus: FNF engines, mobile ports, and mod tooling
- 🛠️ Core stack: **Haxe, HaxeFlixel, Lime, OpenFL**
- 🌱 Currently in school, developing alongside studies
- 📫 Discord: `_brenninho880`
- 🇧🇷 Based in Brazil — writes code in English, communicates in Portuguese

---

## Tech Stack

![Haxe](https://img.shields.io/badge/Haxe-EA8220?style=for-the-badge&logo=haxe&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)

**Toolchain:**
- Dependency management: `hmm.json` / `hxpkg`
- Build configuration: `Project.xml` / `Project.hxp`
- CI/CD: GitHub Actions (Android/iOS/Windows/desktop builds)
- Android NDK: r21e (hxcpp 4.3.2) / r25c (newer stacks)
- Code style: no comments, no `trace()` calls, English-only code

**Engine ecosystem experience:** Psych Engine, Kade Engine, Forever Engine, NightmareVision, Banana Engine, P-Slice, V-Slice (Codename Engine)

---

## 🎮 Engines & Forks

### BrenninhoEngine
Brenninho's own FNF engine, built on Psych Engine, package `com.funkin.brenninhoengine` (v0.2.8). Extensive work on Flixel 6.1.2 compatibility, Android/iOS/desktop GitHub Actions workflows, mobile touch systems, shader improvements, and HScript integration.

### FNF-AstroEngine
Source-based Funkin' fork using the `hxp` build system with ASTC texture compression and `hmm.json` dependencies. Rebranded as "Friday Night Funkin' Astro Engine" (desktop) / "FNF: Astro Engine" (mobile), package `me.brenninho.astroengine`.

### FNF-PsychEngine (Mobile Fork)
Extensive CI/CD and mobile toolchain work: converted `Project.xml` to `project.hxp`, resolved a custom `lime` fork's missing platform APIs, built merged Windows/Android CI workflows with Gradle/haxelib caching, fixed multiple build and asset-inclusion bugs, and added a first-launch welcome flow.

### FNF-Lime-Engine-Mobile
Mobile fork of a Brazilian FNF Legacy-style engine (originally by glitch781212master-mist) using Polymod `.hxc` scripting, adapted for mobile devices.

### FNF-Transversal-Engine
A Psych Engine v1.0.4-based FNF engine template with mobile support, based on the Mind Games Mod.

### Kade-Extended-Community
Mobile fork of Kade Engine Community (itself a fork of Kade Engine by TheRealJake12).

### PrismEngine
Custom FNF engine featuring **LexisScript**, a custom `.lx` scripting language with its own Linguist syntax-highlighting registration.

### JackEngine
A Java-based game engine for desktop and Android, built with Swing/AWT and a custom build orchestration system.

### Psych Engine 0.4.2 (Android Port)
Full Android port of Psych Engine 0.4.2: asset extraction, multi-strategy native library scanning, mobile touch/swipe controls, and crash handling.

---

## 🕹️ Mods & Games

### Vs Impostor Legacy (IMPOSTOR-MOBILE)
An FNF V-Slice mod converting Psych Engine Lua scripts to official Haxe/HScript for the V-Slice modding API. Built on the NightmareVision engine base (inky03/MotorFrog), with deep exploration of V-Slice's Module scripting system and `ScriptedStage` base class. Uses `hxpkg` for dependencies. Extensive mobile porting work for Flixel 6.1.2 / Haxe 4.3.7 / Android compatibility.

### Kareshi Project
A Touhou-style bullet hell game built in Haxe, migrated from `project.xml` to the `Build.hx` HXP format, with Android CI fixes.

### Fragile
A 2D horror game in HaxeFlixel featuring dual-camera gameplay with mobile and desktop support, built via `Project.hxp`.

### FNF-BFYoutubers
CI/CD work on a Psych Engine fork (`ek-mobile` branch): pinned GitHub Action versions, corrected build flags, added Android SDK license acceptance, and introduced haxelib caching.

---

## 🌐 Tools & Sites

### Funkin' Coding
An HScript/Lua code generator and tutorials site for FNF engines (renamed from "Code Generator Ultimate"). Features an engine selector (Psych Engine / V-Slice), a Characters JSON generator, a built-in AI assistant, full PWA support, Google Sign-In, a live WebSocket community chat backed by an Express server, English/Portuguese language switching, and a CI pipeline that builds a standalone Windows `.exe`.

### FunkinHelper
An English-language AI chat site that helps with FNF source code across Haxe/HaxeFlixel engines. Backend deployed on Render, frontend on GitHub Pages.

### Funkin-Optimizer
An in-progress automatic optimizer for FNF mods — auto-optimizes PNG+XML sprite atlases (with spritemap/JSON atlas support), auto-generates matching character JSON, and packages results as a downloadable zip. Built as an offline-capable installable app.

### V-Stuff
A PWA that converts Friday Night Funkin' content between **Psych Engine** and **V-Slice** formats — Charts, Characters, and Stages — with a bidirectional Psych ↔ V-Slice switcher and full V-Slice schema handling.

### V-Slice-Modpacks
A modpack collection for Mods V-Slice.

### DWP Generator
Generates DirectWave `.dwp` chromatic instrument presets from an uploaded template `.dwp` plus a single chromatic-scale audio recording. Fully reverse-engineered the undocumented `.dwp` binary format (TLV record structure) and built a client-side splice-and-rebuild pipeline, validated 37/37 zones round-tripped correctly.

### WAV to DWP
A from-scratch `.dwp` generator: converts a single `.wav` recording of one note into a full multi-zone `.dwp` instrument via automatic pitch-shift zone mapping — no template file required. Involved reverse-engineering the `.dwp` preamble and per-zone byte structure independently, including tracking down a subtle file-size-header bug that caused "sample not found" errors in FL Studio.

### FLP-to-FLM-Converter
A client-side tool that parses FL Studio Desktop `.flp` binary projects and reconstructs/exports them as MIDI, JSON, and experimental `.flm` files for FL Studio Mobile — entirely in-browser, no backend.

### Funkin' Codename Asset Converter
An HTML/JS tool converting Psych Engine assets to Codename Engine (V-Slice) format.

---

## 📦 Libraries & Native Extensions

### flixel-3D
A haxelib adding 3D rendering to HaxeFlixel — OpenGL rendering with GLSL Phong shading and a scene graph integrated into `FlxState`.

### android-manager
A native Android extension for Haxe games with JNI bindings for permissions, context, media, and battery management.

### hxjavascript
A Haxe-to-JavaScript interop bridge.

---

## 🧪 Experiments & Interests

Ongoing explorations and long-term background work, including an FNF port to Godot 4, a C++ recreation of Super Mario World, a Love2D mobile project (SansTale), a web-based Linux desktop simulator, an Adobe Animate-style animation tool, and **DScript** — a custom scripting language built in Haxe.

---

## Contact

- **GitHub:** [Brenninho123](https://github.com/Brenninho123)
- **Discord:** `_brenninho880`
