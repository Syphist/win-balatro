# Balatro Cards for Windows XP Card Games
This mod is for the card games that shipped with Windows XP. The games Solitaire, Spider Solitaire, Hearts, and Free Cell all use the same bitmap format for card data and 3 of the 4 load this data in from cards.dll. These cards are made from the assets within Balatro and super imposed on the bitmaps the OS originally shipped with. The exes expect certain pixels at certain parts of the bitmap so they aren't the exact same look as the cards from Balatro, but it is as close as I could get without editing the executed code in the binaries. Due to this being a modded binary you will need to apply patches to a few of them to allow the mod to fully work.

# Applying the patches
To apply the patches, follow these steps:
1. Clone or download the repo to have the 3 .bps files
2. Use a bps capable ROM Patcher like RomPatcher.js: https://www.marcrobledo.com/RomPatcher.js/
3. Upload the original file with the corresponding patch and apply the patch on the website

## Patched Files

### cards.dll
- Original CRC32 Hash: bb0c1bd6
- Original MD5 Hash: 989974032e6c873a17c9e92d4b339571
- Original SHA-1 Hash:0a19ac47361a87029a3df157d23204a4461f4874
- Patch File: cards_dll.bps
- What it changes: All the Cards in Solitaire, Hearts, and Free Cell. This mod is mandatory to work on all 3 of those games.

### Free Cell.exe
- Original CRC32: 734807d1
- Original MD5: 4d9b5e540158bf8e9b1bcac1aedd8c60
- Original SHA-1: 428ff15fb6583dd5518c5be0297bd8be14fcf5c5
- Patch File: Free Cell.bps
- What it changes: The 3 bitmaps for the king looking left and right and smiling. It is changed with a Yellow and Black Joker from Balatro. Not strictly necessary but makes Free Cell have fully modified graphics.

### Spider Solitaire.exe
- Original CRC32: 00bb470d
- Original MD5: 8d1492dbe9a856ee306edc5a103e0bf2
- Original SHA-1: 42892a52e965bf4684f7375aec47997fffd971ea
- Patch File: Spider Solitaire.bps
- What it changes: All the graphics in Spider Solitaire. This one doesn't load them from cards.dll, but a majority of the source graphics are applied here with a different custom card backing to make it fully seamless.

# How to apply the source images yourself
In this repository the source images I used are supplied. They are saved as .bmp files with the same encoding as the ones embedded in the original binaries. If you are to modify them, I highly recommend loading them in a copy of Windows XP's mspaint.exe and pasting your edits on top of it to save it. This will ensure it can be embedded properly. The program used to then modify the bitmaps in the binaries is Angus Johnson's Resource Hacker found here: https://www.angusj.com/resourcehacker/

To apply the modified bitmap to the corresponding card you will use the action to replace .bmp or use the hotkey Ctrl + R and select the file you want to replace it with.
