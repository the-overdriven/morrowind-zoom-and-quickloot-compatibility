# Compatibility fork for Zoom and QuickLoot, MWSE mods for Morrowind

Added `isActive` flag to QuickLoot's `interop.lua` and set it to true/false in `main.lua`:  
[commit/ce9ba864d122e13bc7bea2e5c5a116f9f80b5781](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/ce9ba864d122e13bc7bea2e5c5a116f9f80b5781)  
[commit/d1341f55bc524e16ebdc426f11c49026378607ac](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/d1341f55bc524e16ebdc426f11c49026378607ac)  

Consequentially I can check `QuickLoot.isActiv`e in Zoom's main.lua on `mouseWheel` event callback to prevent zooming on scroll:  
[commit/91526f34031173ac7c0d7b00a406ccbb1b4ac193](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/91526f34031173ac7c0d7b00a406ccbb1b4ac193)  

Effect:  
![scroll](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/assets/100090726/99d8bf43-6aa0-4b1d-a889-86d5728ca6ae)
  
### How to have highlighted option in ~~orange~~ pumpkin colour?
Open Morrowind.ini and change color_active from `255,255,255` to `255,117,24`

