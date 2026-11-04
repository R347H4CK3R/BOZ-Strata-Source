# BOZ for Strata

Add this catalog in Strata Sources:

https://raw.githubusercontent.com/R347H4CK3R/BOZ-Strata-Source/main/strata-source.json

Experimental unsigned compatibility build 135.8. Launch and gameplay remain unverified. Game belongs to Activision. This repository contains installation metadata, the icon, and the packaged compatibility build only. Diagnostic reports and build inputs are kept in a separate private repository.

## Small Free Shop add-on — v2

[Download BOZFreeShop.dylib v2](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/BOZFreeShop.dylib) and follow [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/INSTALL.md). Close the game completely and replace the old dylib in its assigned Strata tweak folder. Keep only one enabled copy. No full-game reinstall is needed.

v1 is withdrawn because the native game add/save path could freeze. v2 avoids that call and uses a separate local wallet in Documents/BOZFreeShop/wallet.plist, saved asynchronously. Keep the add-on enabled to restore this wallet on launch. Shop status is included in the existing session diagnostic report. Native compilation and wallet filesystem tests passed; phone UI, spending, freeze and restart-persistence checks remain physical-device tests.

## Combat HUD add-on — v4

[Download BOZControls.dylib v4](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v4/BOZControls.dylib) (112,320 bytes) and read [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v4/INSTALL.md). Close the game, remove the previous BOZControls.dylib and import this replacement into the same assigned Strata tweak folder as Free Shop v2. Keep BOZFreeShop.dylib and only one BOZControls.dylib. Enable Controls > Enable COD-style HUD if needed; start a new round for native Touch mode. No full-game reinstall.

v4 replaces the stalled yield/import bridge with dispatch after regular engine-thread frame presentation. New status distinguishes frame delivery, input-manager readiness and gameplay. Native controls remain available until replacement input is ready. The actual frame callback passes a regression test with no yield calls. Physical iPhone confirmation is still required.\n\nCOD Mobile-inspired transparent, movable combat controls: FIRE, ADS, RELOAD, SWAP, MELEE, GRENADE, CROUCH, TACTICAL and a centered BUY / USE target. Matched native combat buttons are hidden, disabled and moved offscreen while replacement mode is enabled. Native movement/swipe aiming, menus, health, ammo and score remain. No target-based auto-fire.

BUY / USE appears when the native game permits an interaction. Native price/interaction text moves below it. It invokes the normal game action; prices, perk requirements and proximity checks remain. Its background is transparent so the scene remains visible.

Controls > Restore native buttons stops add-on input and restores recorded native widgets and prompt positions, including retained control schemes. Native Touch mode/sensitivity can be restored separately through the original game options. Replacement status and events use the existing diagnostic reporter.

ARM64 unsigned build, real native input/POI/position/hit-test checks and code review passed. Physical-device rendering, touch behavior, pause/round transitions and restoration remain experimental and require iPhone testing.
