# BOZ for Strata

Add this catalog in Strata Sources:

https://raw.githubusercontent.com/R347H4CK3R/BOZ-Strata-Source/main/strata-source.json

Experimental unsigned compatibility build 135.8. Launch and gameplay remain unverified. Game belongs to Activision. This repository contains installation metadata, the icon, and the packaged compatibility build only. Diagnostic reports and build inputs are kept in a separate private repository.

## Small Free Shop add-on — v2

[Download BOZFreeShop.dylib v2](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/BOZFreeShop.dylib) and follow [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/INSTALL.md). Close the game completely and replace the old dylib in its assigned Strata tweak folder. Keep only one enabled copy. No full-game reinstall is needed.

v1 is withdrawn because the native game add/save path could freeze. v2 avoids that call and uses a separate local wallet in Documents/BOZFreeShop/wallet.plist, saved asynchronously. Keep the add-on enabled to restore this wallet on launch. Shop status is included in the existing session diagnostic report. Native compilation and wallet filesystem tests passed; phone UI, spending, freeze and restart-persistence checks remain physical-device tests.

## Small Touch Controls add-on — v1

[Download BOZControls.dylib](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v1/BOZControls.dylib) (93,584 bytes) and read [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v1/INSTALL.md). Close the game and import the add-on into the same assigned Strata tweak folder as Free Shop v2. Keep both dylibs. At the main menu, choose Controls > Enable touch preset, then start a new round. No full-game reinstall is needed.

Adds movable manual FIRE, hold ADS, RELOAD, native swipe aiming and sensitivity presets inspired by Dead Trigger 2. No target-based auto-fire is added. Existing combat, AI and manual gestures remain native. Move buttons through the Controls menu; leave an uncovered region for swipe aim. Hiding combat buttons stops add-on commands but retains the native Touch mode and sensitivity; restore those in the game's original options if desired.

ARM64 unsigned build checks, native input-handler emulation, pause-state vector checks and code review passed. Physical-device multitouch, pause transitions and control feel still require testing. Status is included in the existing diagnostic session report.
