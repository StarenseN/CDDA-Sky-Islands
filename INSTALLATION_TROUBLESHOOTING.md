# Zone Stalker Mod Installation Troubleshooting

## 🚨 Mod Not Showing Up in CDDA? Follow This Guide

If the Zone Stalker mod isn't appearing in your CDDA game, here are the most common causes and solutions:

## 📁 Step 1: Check Mod Installation Location

The mod must be placed in the correct CDDA mods directory:

### **Windows:**
```
C:\Users\[YourName]\Documents\my_games\Cataclysm-DDA\mods\ZoneStalker\
```

### **Linux:**
```
~/.local/share/cataclysm-dda/mods/ZoneStalker/
```

### **CDDA Installation Directory (Alternative):**
```
[CDDA_Install_Folder]\data\mods\ZoneStalker\
```

## 📋 Step 2: Verify Mod Structure

Your mod folder should contain these files:
```
ZoneStalker/
├── modinfo.json          ← CRITICAL
├── scenario.json         ← CRITICAL  
├── EOCs.json
├── items.json
├── effects.json
├── dialog_statue.json
├── missions_and_mapgen.json
├── (and other .json files)
└── README.md
```

## 🔧 Step 3: Common Installation Issues

### **Issue 1: Wrong Folder Name**
- ❌ **Problem**: Folder named "CDDA-Sky-Islands" or similar
- ✅ **Solution**: Rename folder to exactly `ZoneStalker` (no spaces, no hyphens)

### **Issue 2: Extra Nested Folder**
- ❌ **Problem**: `mods/ZoneStalker/CDDA-Sky-Islands/modinfo.json`
- ✅ **Solution**: Move files directly to `mods/ZoneStalker/modinfo.json`

### **Issue 3: Missing modinfo.json**
- ❌ **Problem**: The `modinfo.json` file is missing or corrupted
- ✅ **Solution**: Re-download the mod files and ensure `modinfo.json` exists

## 🎮 Step 4: In-Game Detection

### **How to Find the Mod:**
1. Launch CDDA
2. Go to "New Game" → "New Character"
3. **Look for "Zone Stalker" in the scenario list**
4. **DO NOT use "Play Now!" - it won't work with this mod**

### **What You Should See:**
- **Scenario Name**: "Zone Stalker"  
- **Description**: Mentions "Stalker operating from a secret underground laboratory"
- **Start Location**: "Zone Laboratory"

## 🔍 Step 5: Debug Information

If the mod still isn't showing up, check these:

### **Check CDDA Debug Log:**
1. Look in your CDDA folder for `debug.log` or similar
2. Search for errors mentioning "zonestalker" or "Zone Stalker"
3. Common errors:
   - JSON syntax errors (should be fixed in this version)
   - Missing dependencies
   - File permission issues

### **Verify Mod ID:**
The mod should appear with:
- **Internal ID**: `zonestalker`
- **Display Name**: `Zone Stalker`
- **Category**: `total_conversion`

## 🆘 Still Having Issues?

### **Try This Step-by-Step:**
1. **Delete any existing Zone Stalker/Sky Islands mod folders**
2. **Download fresh mod files from GitHub**
3. **Create new folder**: `[CDDA_Mods_Path]/ZoneStalker/`
4. **Extract ALL files directly into that folder**
5. **Verify `modinfo.json` is at**: `ZoneStalker/modinfo.json`
6. **Restart CDDA completely**
7. **Create New Character → Find "Zone Stalker" scenario**

### **Alternative Installation Method:**
If the user mods folder doesn't work, try the installation directory:
1. Navigate to your CDDA installation folder
2. Go to `data/mods/`
3. Create `ZoneStalker` folder there
4. Place all mod files inside

## ✅ Success Indicators

You'll know it's working when:
- ✅ "Zone Stalker" appears in scenario selection
- ✅ Character creation shows "Zone Laboratory" start location  
- ✅ Game starts with STALKER-themed messages
- ✅ You spawn in an underground laboratory setting

---

**If none of these solutions work, the issue might be with your CDDA installation or version compatibility. The mod is designed for CDDA experimental builds from 2025-09-29 and later.**