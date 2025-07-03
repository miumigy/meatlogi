# Meat Supply-Chain Simulation

A single-file **Three.js** demo that visualises a complete pork supply-chain:

* raising pigs  
* processing at two factories  
* shipping to three stores and one warehouse  
* selling to customers in real-time  

The simulation keeps a detailed cost breakdown for every product and lets you
inspect transactions via an on-screen log.

---

## Demo Controls

| Gesture / Key | Action | Note |
|---------------|--------|------|
| **Tap (single click)** | Toggle the **sales-transaction log** overlay | Disabled while the help screen is open |
| **Double-tap (double click)** | Toggle the **help** overlay | Closes the log if it’s open |
| Resize window | Scene resizes automatically | |

---

## Simulation Highlights

| Category | Setting |
|----------|---------|
| **Season cycle** | 40 s normal &nbsp;/&nbsp; 20 s peak |
| **Pig spawn** | 2000 ms ±10 % (normal) / 1500 ms ±10 % (peak) |
| **Customer spawn** | 3 s ±10 % (normal) / 1 s ±10 % (peak) |
| **Truck capacity** | 32 (normal) / 16 (peak) |
| **FIFO inventory** | Warehouse & store both sell oldest stock first |
| **Cost model** | raw = 10, mfg = 10/12, delivery = 80 – 160 / truck, holding = 0.1/0.2 s |

All parameters are declared near the top of the HTML file—tweak at will.

---

## Getting Started

1. **Clone** the repo or download `index.html`.
2. Open the file in any modern desktop browser (local file:// is fine).
3. That’s it—there is no build step.  
   Mobile Safari / Chrome also work, but a mouse makes navigation easier.

> **Tip:** If you serve the file via a tiny web-server (`python -m http.server`)
> you avoid CORS warnings when loading textures or screenshots.

---

## File Structure

├─ index.html        # self-contained 

All JavaScript, HTML and CSS live in **one** file to keep copy-and-paste
experiments simple.

---

## Roadmap & Ideas

* Performance profiling on mobile (object pooling, instancing)
* Additional animal types / colour schemes
* Keyboard orbit controls for camera
* CSV export of the transaction log
* TS refactor & automated tests

Feel free to open an Issue / PR!

---

## Built With

* [Three.js](https://threejs.org/) r158   –  WebGL rendering
* Plain ES-modules & zero build tools

---

## Licence

[MIT](LICENSE)

(c) 2025 miumigy.
