# Hypixel Stats Bot Mod (v1.3.3)

A tiny Forge 1.8.9 **client-side** bot that listens for `/msg` whispers on Hypixel and answers with live player / guild statistics pulled from the public Hypixel REST API.

---

## 1 · Requirements

| What               | Version / Notes                               |
|--------------------|-----------------------------------------------|
| **Minecraft**      | **1.8.9** (any launcher)                      |
| **Forge**          | 1.8.9-latest (download from files.minecraftforge.net) |
| **Java 8 JRE**     | Minecraft 1.8.9 already ships with it         |
| **Hypixel API key**| Generate once at **<https://developer.hypixel.net/reset>** (see step 3) |

---

## 2 · Installation

1. Download the release **`HypixelStatsBot-1.3.3.jar`**.  
   *You get a single JAR — no other files needed.*
2. Drop the JAR into your local **`<minecraft folder>/mods/`** directory.
3. Launch Minecraft with the **Forge 1.8.9** profile once; the mod will create `config/hypixelstatsbot.cfg`.

---

## 3 · Get your Hypixel API key  ( `/api new` was removed )

1. Log into your Hypixel account in any browser.  
2. Open **<https://developer.hypixel.net/reset>**.  
3. Click **“Generate New API Key”** → copy the 32-character key shown.  

> You can manage / revoke keys at any time from the same page.

---

## 4 · Configure the mod

1. In your **`.minecraft`** folder, open  
   `config/hypixelstatsbot.cfg` with any text editor.
2. Paste the key you copied:

   ```properties
   [api]
   key = 01234567-89ab-cdef-0123-456789abcdef
   requests_per_min = 75      # default: 75 (runs well below Hypixel’s 120 rpm cap)
