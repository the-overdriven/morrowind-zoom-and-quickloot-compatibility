# Compatibility fork for Zoom and QuickLoot, MWSE mods for Morrowind

Added `isActive` flag to QuickLoot's `interop.lua` and set it to true/false in `main.lua`:  
[commit/ce9ba864d122e13bc7bea2e5c5a116f9f80b5781](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/ce9ba864d122e13bc7bea2e5c5a116f9f80b5781)  
[commit/d1341f55bc524e16ebdc426f11c49026378607ac](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/d1341f55bc524e16ebdc426f11c49026378607ac)  

Consequentially I can check `QuickLoot.isActive` in Zoom's main.lua on `mouseWheel` event callback to prevent zooming on scroll:  
[commit/91526f34031173ac7c0d7b00a406ccbb1b4ac193](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/commit/91526f34031173ac7c0d7b00a406ccbb1b4ac193)  

Effect:  
![scroll](https://github.com/the-overdriven/morrowind-zoom-and-quickloot-compatibility/assets/100090726/99d8bf43-6aa0-4b1d-a889-86d5728ca6ae)
  
### How to have highlighted option in ~~orange~~ pumpkin colour?
Open Morrowind.ini and change color_active from `255,255,255` to `255,117,24`

### Why I prevent zooming out to value smaller than 2.5?
Zoom=1 is the default zoom, but I want to use the Zoom mod not only for zooming in but also for zooming out, further than default camera allows, but also not too much. For this reason, I increase FOV to huge value, so that camera looks "normal" in the middle point. That middle point seems to be at Zoom=~2.5. I set following MGE XE settings: Horz. FOV = 150, 3rd person camera Y offset = -260, Z offset = 80. Thanks to this scrolling in Morrowind.exe imitates the camera scroll from OpenMW.
