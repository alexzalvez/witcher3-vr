### UX Contribution / v0.9.5 Fork: Clean cold-boot head-unlocked UI, natural menu/map anchoring, and cinematic parallax comfort

Hi @tig3rmast3r,

First of all, I want to thank you and congratulate you on the monumental work you have done with The Witcher 3 VR. Getting such a complex game engine to run under OpenXR and DirectX 12 is an incredible technical achievement that the entire VR community deeply appreciates.

I'm reaching out because I have been working on an alternative community fork built on top of your **v0.9.5** milestone:  
🔗 **Release:** https://github.com/alexzalvez/witcher3-vr/releases/tag/v0.9.5-clean-ux  
🔗 **Source Code:** https://github.com/alexzalvez/witcher3-vr  

The reason for staying on v0.9.5 and maintaining this branch is that, for hardware configurations aiming for CPU frametime stability, that release offers a fantastic foundation. However, regarding the user interface and overall UX ergonomics, I ran into several behaviors that you clearly tried to address, but which remained somewhat quirky by design:

1. **The cold-boot Head-Locked lifecycle:**  
   On a cold boot, the main menu was invariably glued to the player's face (*head-locked*). Interestingly, if the user loaded a savegame and then quit back to the main menu, the head-locking was gone, but the screen acquired an unnatural drifting/floating movement whenever the head was turned. That same unnatural motion carried over to the world map, video playback, and other 2D screens.
2. **Exaggerated parallax in 3D Cinematics:**  
   Cinema 3D mode was the one element properly detached as an independent floating screen, but the ocular separation (parallax) was quite aggressive. In close-up shots, it caused noticeable eye strain and made reading subtitles uncomfortable over extended sessions.

---

### What I implemented in this fork (and you are warmly invited to reuse):

* **Two Watchdogs for clean spatial anchoring from Frame 1:**  
  I implemented two control mechanisms (*watchdogs*) that eliminate the dependency on broken transition/loading states. Thanks to this, the game launches from the very first cold-boot frame with the UI properly anchored in 3D space, completely avoiding the *head-locked* state and without requiring any "load game and quit to menu" workarounds.
* **Natural, stable anchoring for menus and the map:**  
  The spatial tracking calculations were revised. Now the map, inventory, tutorial popups, and the radial sign selection feel solid, stable, and natural in 3D space: you can freely turn your neck and read interface text as if looking at a crisp virtual panel, with zero artificial sway or awkward drifting.
* **Balanced ocular divergence in Cinema Mode:**  
  The stereo disparity in cinema mode was softened to preserve stereoscopic 3D depth while ensuring subtitles and dialogue text are relaxed and comfortable to read without visual fatigue.
* **Intuitive one-touch recentering on pause:**  
  Pausing the game automatically handles orientation recentering, avoiding the need to blindly search for `F9` on your keyboard while wearing the headset.

---

**The source code is completely open for you to use.** If at any point you would like to incorporate any of these ergonomic fixes into your main branch (or adapt them to your latest version), please feel free to take whatever you need.

*(Note: You will find many code comments written in Spanish, but if you use tools like Claude Code or any modern AI assistant, they will parse and translate them seamlessly).*

I understand that your recent focus on 0.9.8+ has been on pushing advanced technical frontiers like asymmetric projection, OptiScaler, and DLSS-NR, but I believe these ergonomics and UX refinements significantly improve day-to-day comfort for players.

Thanks again for everything you have built, and best regards!
