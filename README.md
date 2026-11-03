# BOZ for Strata

Add this catalog in Strata Sources:

https://raw.githubusercontent.com/R347H4CK3R/BOZ-Strata-Source/main/strata-source.json

Experimental unsigned compatibility build 135.8. Launch and gameplay remain unverified. Game belongs to Activision. This repository contains installation metadata, the icon, and the packaged compatibility build only. Diagnostic reports and build inputs are kept in a separate private repository.

## Small Free Shop add-on — v2

[Download BOZFreeShop.dylib v2](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/BOZFreeShop.dylib) and follow [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/INSTALL.md). Close the game completely and replace the old dylib in its assigned Strata tweak folder. Keep only one enabled copy. No full-game reinstall is needed.

v1 is withdrawn because the native game add/save path could freeze. v2 avoids that call and uses a separate local wallet in Documents/BOZFreeShop/wallet.plist, saved asynchronously. Keep the add-on enabled to restore this wallet on launch. Shop status is included in the existing session diagnostic report. Native compilation and wallet filesystem tests passed; phone UI, spending, freeze and restart-persistence checks remain physical-device tests.
