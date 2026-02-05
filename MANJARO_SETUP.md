# Windows to Manjaro Transfer - Devlog

**Date:** February 6, 2026
**User:** TamerAli-0 (Tamer Altaweel)

---

## ✅ What Was Backed Up to GitHub

### Repositories Successfully Pushed:
1. **OmniStream** - https://github.com/TamerAli-0/OmniStream
   - Status: ✅ All changes pushed
   - Branch: master
   - Latest: Updated README with cool formatting

2. **OmniStream-Beta** - https://github.com/TamerAli-0/OmniStream-Beta
   - Status: ✅ All changes pushed
   - Branch: master
   - Latest: Active development version

3. **Portfolio** - https://github.com/TamerAli-0/portfolio
   - Status: ✅ All changes pushed
   - Branch: master
   - Latest: Updated README with enhanced design
   - Live at: https://tamerali-0.github.io/portfolio/

4. **Profile README** - https://github.com/TamerAli-0/TamerAli-0
   - Status: ✅ Pushed
   - Branch: main
   - Cool GitHub profile with stats and badges

### Repositories with Local Changes (Not Pushed):
1. **OmniWatch** - Fork of Kotatsu-Redo/Kotatsu-Redo
   - Status: ⚠️ Committed locally, can't push (no permission to upstream)
   - Branch: devel
   - Changes: 105 files modified, video player feature added
   - **Action Required:** Fork to your GitHub after Manjaro install, then push

---

## 📁 Project Locations (Windows)

```
C:\Users\black\AndroidStudioProjects\
├── OmniStream/           ← Main project (pushed ✅)
├── OmniStream-Beta/      ← Beta version (pushed ✅)
├── OmniWatch/            ← Local changes only ⚠️
├── AIbySea2/            ← Old project (not critical)
├── AIbySeaInbox/         ← Old project (not critical)
├── Kotatsu/              ← Fork (not pushed)
└── kotatsu-parsers/      ← Fork (not pushed)

C:\Users\black\portfolio/  ← Portfolio site (pushed ✅)
```

---

## 🔧 After Manjaro Install - TODO List

### 1. **Install Essential Tools (IN ORDER)**

**Step 1: Update System**
```bash
sudo pacman -Syu
```

**Step 2: Install Base Tools**
```bash
sudo pacman -S git base-devel curl wget
```

**Step 3: Install Claude CLI (IMPORTANT!)**
```bash
# Download and install Claude CLI
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code/main/install.sh | bash

# After install, authenticate
claude auth login

# Test it works
claude --version
```

**Step 4: Install AUR Helper (yay)**
```bash
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
cd ..
rm -rf yay
```

**Step 5: Install Development Tools**
```bash
# Android Studio
yay -S android-studio

# Other tools
sudo pacman -S firefox

# Optional: Steam for games
sudo pacman -S steam
```

### 2. **Clone Your Repositories & Resume Work**
```bash
# Create projects directory
mkdir -p ~/AndroidStudioProjects
cd ~/AndroidStudioProjects

# Clone main projects
git clone https://github.com/TamerAli-0/OmniStream.git
git clone https://github.com/TamerAli-0/OmniStream-Beta.git

# Clone portfolio
cd ~
git clone https://github.com/TamerAli-0/portfolio.git
```

**🔥 Continue Work with Claude CLI (Exactly Where You Left Off):**
```bash
# Open any project directory
cd ~/AndroidStudioProjects/OmniStream

# Start Claude CLI
claude

# Or ask Claude directly
claude "Help me continue working on OmniStream"

# Claude will:
# - Remember your GitHub repos
# - Access your code
# - Help you code, debug, commit, push
# - Build APKs
# - Everything you did on Windows!
```

**Claude CLI = Same as Terminal on Windows**
- Works exactly the same way
- All your GitHub repos accessible
- Same commands, same workflow
- Actually FASTER on Linux!

### 3. **Set Up Git**
```bash
git config --global user.name "Tamer Ali"
git config --global user.email "your-email@example.com"

# Set up GitHub CLI
gh auth login
```

### 4. **Handle OmniWatch**
```bash
# Option 1: Fork Kotatsu-Redo on GitHub first, then:
git clone https://github.com/TamerAli-0/OmniWatch.git
# Then manually copy your changes from Windows backup

# Option 2: Create new repo for your changes
gh repo create OmniWatch --public
cd ~/AndroidStudioProjects
git clone https://github.com/TamerAli-0/OmniWatch.git
# Copy changes manually
```

### 5. **Android Studio Setup**
```bash
# Install Android SDK
# Set up AVD (Android Virtual Device)
# Import projects: OmniStream, OmniStream-Beta

# Sync Gradle (first time will download dependencies)
```

### 6. **Customize Your Manjaro**
- Install KDE themes
- Set up desktop widgets
- Configure Firefox
- Install fonts
- Rice it! (r/unixporn style)

---

## 💾 Important Settings to Remember

### GitHub Account:
- Username: **TamerAli-0**
- Name: **Tamer Ali**
- Bio: **Too idle for this**

### Key Projects:
- **Main:** OmniStream (stable release)
- **Beta:** OmniStream-Beta (active development)
- **Portfolio:** https://tamerali-0.github.io/portfolio/

### GitHub Cleanup Done:
- ✅ Deleted old tags (v1.0.0, v2.0-beta1, v2.1.0-beta, v2.1.0)
- ✅ Kept only: v2.3.1, v2.3.0-beta, v2.2.0
- ✅ Updated READMEs with cool formatting
- ✅ No Claude attribution anywhere

---

## 📋 Files NOT Backed Up (Not Critical):

- Android Studio cache/build folders (deleted during cleanup)
- Windows system files
- Temporary downloads
- Old APK files (cleaned up)
- Browser cache

---

## ⚠️ Critical Reminder:

**BEFORE BOOTING MANJARO USB:**
- [ ] Manjaro ISO downloaded (~3.5GB)
- [ ] Rufus ready
- [ ] This devlog saved somewhere accessible (screenshot or save to USB)
- [ ] All important passwords saved/remembered
- [ ] Ready to wipe Windows completely

---

## 🚀 Post-Install Verification:

After Manjaro install, verify:
1. All repos cloned successfully
2. Android Studio opens and recognizes SDK
3. Git configured with your credentials
4. Claude CLI working
5. Firefox synced (if you use Firefox Sync)
6. OmniStream builds successfully

---

## 📝 Notes:

- Windows laptop had 8GB soldered RAM
- Optimization done: Disabled bloatware, telemetry, visual effects
- Freed ~3-4GB RAM before switching
- Manjaro will use ~500MB-1GB idle (vs Windows 2-3GB)
- Expected free RAM after Manjaro: ~6-7GB available for work

---

**Good luck with the switch! Linux >> Windows for 8GB RAM** 🔥
