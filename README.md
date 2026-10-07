# The Witcher 3 VR — Alternative Edition (Based on v0.9.5)

> **A fork focused on consistent performance and a 100% natural, head-unlocked UI experience anchored in 3D space.**

This project is a community-driven fork built upon **v0.9.5 of [tig3rmast3r/witcher3-vr](https://github.com/tig3rmast3r/witcher3-vr)**.

Official upstream development has continued exploring ambitious and experimental frontiers in its later releases (such as asymmetric projection, DLSS 5 Neural Rendering integration, and OptiScaler). 

This fork was created to pursue **a different path**: taking **v0.9.5** as our foundation—widely regarded as a sweet spot for balanced performance and hardware accessibility—and focusing primarily on resolving one of the biggest comfort barriers in VR: **how the player interacts with user interfaces and text.**

---

### 🌟 The Core Pillar: Farewell to Head-Locking & Natural Reading

In VR, having text and menus rigidly glued to your face (*head-locked*) feels unnatural and causes severe eye strain: whenever you try to glance at a corner, the entire interface drags along with your view, forcing you to strain your eyeballs instead of moving your neck naturally.

In this edition, that behavior has been completely addressed:

* **Complete freedom of gaze & effortless reading:**  
  Every single menu—world map, inventory, character skill tree, pause menu, sign selection radial wheel, and tutorial popups—is **solidly anchored in 3D space**.
* **Natural head movement:**  
  You can now **naturally turn your head and move your neck to read item descriptions, inspect map markers, or browse quest logs**, exactly as if you were looking at a large virtual screen or a holographic board in real life. Your eyes can relax, eliminating reading fatigue.
* **Decoupled, comfortable HUD:**  
  The in-game HUD (health, stamina, minimap) no longer rigidly tracks your facial movements. Its proportions have been adjusted into a comfortable peripheral arc: the information is immediately visible when you look for it, yet completely unobtrusive while fighting or taking in the scenery.

---

### 🛠️ Key Improvements in this Edition

* **Comfortable Cinema 3D cutscenes with balanced eye divergence:**  
  Story cutscenes and pre-rendered videos play in a floating 3D theater screen with corrected ocular divergence, eliminating the cross-eyed fatigue and eye strain often present in close-up cinematic scenes.
* **Consistent, hardware-friendly performance:**  
  By staying on the clean symmetric foundation of v0.9.5 without heavy CPU-side geometry patches or experimental injection wrappers, frametimes remain predictable and stable across a broader range of mid-range hardware.
* **Expanded resolution options:**  
  While automatic headset resolution detection is preserved, additional manual resolution presets have been curated to properly support setups that do not target ultra-high profiles.
* **Intuitive one-touch recentering:**  
  No need to blindly fumble on your keyboard for `F9` while wearing your headset: simply pausing the game automatically aligns and recenters the interface towards wherever you are naturally looking.

---

### 📌 Practical Tips & Known Workarounds

* **Left-eye resolution after loading screens:**  
  Due to how the native game engine handles texture memory transitions when exiting video loading screens, the left eye may occasionally boot into live gameplay at a lower internal resolution.  
  👉 **Quick fix:** Simply **press Pause and immediately unpause the game** (a quick one-second toggle). This refreshes the render pipeline and instantly restores full native resolution to both eyes.
* **Quick recentering on the fly:**  
  If you shifted posture in your seat, tapping Pause and resuming will effortlessly realign the display to your current position.

---

### 🤝 Acknowledgments & Credits

We would like to express our deepest gratitude and respect to **[tig3rmast3r](https://github.com/tig3rmast3r/witcher3-vr)**. His pioneering engineering in reverse-engineering The Witcher 3's engine and architecting the OpenXR/DX12 foundation from scratch is what made playing this masterpiece in VR possible in the first place. This edition simply offers an alternative branch for players seeking this specific gameplay and ergonomics profile.
