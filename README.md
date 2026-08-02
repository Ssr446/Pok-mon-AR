<div align="center">
  <img src="favicon.svg" width="120" alt="Pokéball Logo">
  <h1>Pokémon AR</h1>
  <p><strong>A browser-based Augmented Reality experience. Catch Pokémon with your bare hands.</strong></p>

  <p>
    <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
    <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
    <img src="https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js" />
    <img src="https://img.shields.io/badge/MediaPipe-02569B?style=for-the-badge&logo=google&logoColor=white" alt="MediaPipe" />
  </p>
</div>

## 🌟 Overview

**Pokémon AR** is a fully client-side Augmented Reality web application that allows you to catch Pokémon in the real world using nothing but your webcam and your hands. 

There are no apps to install and no external controllers needed. The game leverages advanced computer vision to map your physical hand movements directly into a 3D physical world.

## ⚙️ AR Technology Stack

This project was built from scratch without heavy AR engines (like 8th Wall or Unity) to ensure it runs entirely natively in the browser:

* **[Google MediaPipe](https://mediapipe.dev/):** Used for the core AR tracking. It runs a lightweight machine learning model directly in the browser to detect 21 3D landmarks on your hands at 30+ FPS. This is what allows the game to know when you are "pinching" the Pokéball or holding up two hands.
* **[Three.js](https://threejs.org/):** Powers the 3D WebGL rendering and physics system. It manages the camera feeds, lighting, particle systems, and the mathematical mapping between MediaPipe's 2D screen coordinates and the physical 3D world space so the ball perfectly follows your palm.

## ✨ Key Features

* **👐 Real-Time Hand Tracking:** Pinch your index and thumb together to physically grab the Pokéball on screen. Move your arm to aim, and release your fingers to throw.
* **🕹️ Two-Handed Interactions:**
  * **Power Charge:** Bring your second hand into the frame while holding the ball to charge a super-throw. Wait for the meter to max out before releasing!
  * **Inspection Mode:** Once a Pokémon is caught, bring both hands up. Spread your hands apart to scale the Pokémon up, and move your primary hand side-to-side to rotate it in 3D space.
* **🧬 Dynamic Spawning & Shiny System:** Encounter 8 distinct Pokémon species, each with custom particle auras. Every spawn has a 1-in-10 chance to be a rare "Shiny" variant.
* **📱 Progressive Pokédex:** Track your catches. The game automatically upgrades your Pokéball (Great Ball, Ultra Ball) as your catch count increases.
* **🎨 Premium UI:** Features a sleek, modern, CSS-only animated landing page with floating 3D elements, particle systems, and live glassmorphism HUDs.

## 🚀 How to Play

1. Visit the live site: [Play Pokémon AR](https://ssr446.github.io/Pok-mon-AR/)
2. Grant camera permissions when prompted.
3. Keep your hand visible in the camera frame.
4. Pinch your fingers to grab the ball, swing your arm, and let go to throw!

## 🛠️ Local Development

To run the project locally, you must serve it over HTTPS or `localhost` (browsers block camera access on `file://` protocols).

```bash
# Clone the repository
git clone https://github.com/Ssr446/Pok-mon-AR.git

# Enter the directory
cd Pok-mon-AR

# Run a local server (using npx)
npx serve
```
Then navigate to `http://localhost:3000` in your browser.

---
*Disclaimer: This is a fan-made educational project. Pokémon and all respective names are trademark & copyright of Nintendo / The Pokémon Company.*
