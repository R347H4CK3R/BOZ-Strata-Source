# BOZ for Strata

Add this catalog in Strata Sources:

https://raw.githubusercontent.com/R347H4CK3R/BOZ-Strata-Source/main/strata-source.json

Experimental unsigned compatibility build 135.8. Launch and gameplay remain unverified. Game belongs to Activision. This repository contains installation metadata, the icon, and the packaged compatibility build only. Diagnostic reports and build inputs are kept in a separate private repository.

## Integrated input — test build 135.20

[Download the unsigned integrated-input IPA](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/integrated-input-v1/BOZ-Integrated-Input-unsigned.ipa) and read [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/integrated-input-v1/INSTALL.md). This separate test release leaves the stable catalog unchanged. Close the game, remove external BOZControls.dylib, keep BOZFreeShop.dylib, and import the IPA as an update to the existing entry without deleting its data.

The built-in input surface owns floating-stick movement, swipe look and independent manual FIRE/ADS, with reload and weapon swap. Native aim-assist flags are disabled and verified. Existing engine physics and content remain; this is not an original-engine source reconstruction. Native artwork hiding is experimental and OFF initially, so old HUD artwork may remain. Keep hiding OFF for the first test.

ARM64 compilation, input/gesture regressions, native ABI checks and retained-content hashes passed in [CI run 41765802190](https://github.com/R347H4CK3R/BOZ-Modern-iOS/actions/runs/41765802190). Phone movement direction, scale, feel and full-session stability still require testing. [Checksums and verification manifest](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/tag/integrated-input-v1) are attached to the test release.

## Small Free Shop add-on — v2

[Download BOZFreeShop.dylib v2](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/BOZFreeShop.dylib) and follow [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/free-shop-v2/INSTALL.md). Close the game completely and replace the old dylib in its assigned Strata tweak folder. Keep only one enabled copy. No full-game reinstall is needed.

v1 is withdrawn because the native game add/save path could freeze. v2 avoids that call and uses a separate local wallet in Documents/BOZFreeShop/wallet.plist, saved asynchronously. Keep the add-on enabled to restore this wallet on launch. Shop status is included in the existing session diagnostic report. Native compilation and wallet filesystem tests passed; phone UI, spending, freeze and restart-persistence checks remain physical-device tests.

## Combat HUD add-on — v5

[Download BOZControls.dylib v5](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v5/BOZControls.dylib) (112,544 bytes) and read [INSTALL.md](https://github.com/R347H4CK3R/BOZ-Strata-Source/releases/download/controls-v5/INSTALL.md). Close the game, remove the previous BOZControls.dylib and import this replacement into the same assigned Strata tweak folder as Free Shop v2. Keep BOZFreeShop.dylib and only one BOZControls.dylib. Enable Controls > Enable COD-style HUD if needed; start a new round for native Touch mode. No full-game reinstall.

v5 removes offscreen combat-widget movement and forced native enabled-state mutations following reported round-entry crashes. The precise cause remains unconfirmed. Controls > Native button hiding toggles suppression and prompt relocation independently; new ready-frame milestones help diagnose remaining failures.

v4 replaced the stalled yield/import bridge with dispatch after regular engine-thread frame presentation. New status distinguishes frame delivery, input-manager readiness and gameplay. Native controls remain available until replacement input is ready. The actual frame callback passes a regression test with no yield calls. Physical iPhone confirmation is still required.

COD Mobile-inspired transparent, movable combat controls: FIRE, ADS, RELOAD, SWAP, MELEE, GRENADE, CROUCH, TACTICAL and a centered BUY / USE target. Matched native combat buttons are hidden using native visibility only; their enabled state and geometry remain intact. Native movement/swipe aiming, menus, health, ammo and score remain. No target-based auto-fire.

BUY / USE appears when the native game permits an interaction. Native price/interaction text moves below it. It invokes the normal game action; prices, perk requirements and proximity checks remain. Its background is transparent so the scene remains visible.

Controls > Restore native buttons stops add-on input and restores recorded native widgets and prompt positions, including retained control schemes. Native Touch mode/sensitivity can be restored separately through the original game options. Replacement status and events use the existing diagnostic reporter.

ARM64 unsigned build, real native input/POI/position/hit-test checks and code review passed. Physical-device rendering, touch behavior, pause/round transitions and restoration remain experimental and require iPhone testing.
