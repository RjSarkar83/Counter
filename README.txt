ArtViSiON - Display Counter   (final, 01-Oct-2026)
==============================================================

FILES  (all in ONE flat folder: no sub-folders anywhere)
  index.html     The design pack: Counter 3D, Screen UI, Build sheet.  Open this one.
  kiosk.html     The touch-screen catalog, full-screen, for the counter's 32" display.
  ArtViSiON_Counter_Drawing_A3.pdf         A3, 2 sheets: front / section A-A / plan at 1:15, then BOM and notes
  ArtViSiON_Counter_Sheet1_Drawing_A3.svg  the same drawing as SVG (open in CorelDRAW)
  ArtViSiON_Counter_Sheet2_BOM_A3.svg      bill-of-materials sheet as SVG
  ArtViSiON_Counter_BOQ.xlsx               BOQ with blank rate cells, bay schedule, ACP take-off, assumptions
  .nojekyll      empty file: tells GitHub Pages to publish the files exactly as they are
  README.txt     this file

PUT IT ON GITHUB PAGES   (https://rjsarkar83.github.io/Counter/)
  1. github.com/rjsarkar83/Counter  ->  Add file  ->  Upload files.
  2. Drag in everything from this zip: the files themselves, not the zip, and not inside any folder.
     If GitHub says index.html / kiosk.html already exist, let it replace them.  ->  Commit changes.
  3. First time only: Settings -> Pages -> Source "Deploy from a branch" -> branch main, folder / (root) -> Save.
  4. Wait 1-2 minutes, open the link and press Ctrl+F5 (browsers keep the old copy for about 10 minutes).
  Counter screen online:  https://rjsarkar83.github.io/Counter/kiosk.html
  Open it through the github.io link. The github.com page of a file only shows its code, it does not run it.

IF IT FEELS SLOW
  Phones and weaker laptops start in light mode on their own (lite glass, lower resolution, shadows drawn once).
  To force it:  https://rjsarkar83.github.io/Counter/?q=low       (?q=high forces full quality)
  The page needs WebGL 2 for the 3D tab. Without it the Screen UI and the Build sheet still work.

KIOSK ON THE COUNTER PC (Chrome kiosk mode)
  chrome.exe --kiosk --app=file:///C:/kiosk/kiosk.html          (copy kiosk.html to C:\kiosk\ first, works offline)
  or, if the PC is online:  chrome.exe --kiosk --app=https://rjsarkar83.github.io/Counter/kiosk.html
  Keys: 1-5 = bays A-E (wire the five counter buttons to these), L = language, H = home, Esc = back.

SIZE   2400 W x 650 D x 1000 H mm, tower to 2000 mm. Bays A-E = 440 / 440 / 520 / 440 / 440 mm.
Everything is an assumption until you confirm it: see "Assumptions to confirm" in the Build sheet.
