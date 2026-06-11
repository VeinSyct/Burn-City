# Burn City

<img width="1919" height="905" alt="Burn City" src="https://github.com/user-attachments/assets/09f196dc-407b-48a2-9e41-1f26688fea6b" />

> A high-performance web-based virtual experience framework for creating immersive, interactive 3D environments with real-time navigation, advanced physics simulation, and scalable scene management.

## Overview

Burn City is a browser-based virtual experience framework designed for architects, developers, designers, and creators who want to transform 3D environments into fully interactive experiences.

Built on top of Three.js and Cannon.js, Burn City enables users to walk, drive, and interact with large-scale virtual environments directly from a web browser without requiring downloads or installations.

Whether you're showcasing architecture, creating digital twins, building virtual event spaces, or developing interactive city experiences, Burn City provides a performant foundation for publishing immersive content on the web.

---

## Highlights

- Browser-Based Virtual Experiences
- Interactive 3D Environment Exploration
- First-Person Navigation
- Physics-Based Vehicle System
- Real-Time Rendering
- Architectural Visualization
- Digital Twin Experiences
- Event & Exhibition Showcases
- SharedArrayBuffer-Powered Physics
- Multi-Threaded Simulation
- Modular Scene Architecture
- Large Environment Support
- Optimized Asset Loading
- Extensible System Design

---

## Why Burn City?

Traditional architectural viewers and 3D web experiences often struggle when environments become large and interactive.

Burn City addresses these challenges by combining:

- High-performance rendering
- Multi-threaded physics simulation
- Shared memory communication
- Modular scene management
- Browser-first deployment

The result is a smooth and scalable virtual experience capable of handling complex environments while maintaining responsive controls and stable frame rates.

---

## Features

### Exploration

- First-Person Walking
- Free Camera Mode
- Interactive Environment Navigation
- Large Open-World Support
- Smooth Character Movement

### Vehicle Systems

- Drivable Vehicles
- Physics-Based Controls
- Custom Vehicle Framework
- Real-Time Suspension Simulation

### Environment

- Dynamic Lighting
- HDR Environment Support
- Real-Time Shadows
- Atmospheric Effects
- Environment Presets

### Architecture & Real Estate

- Interactive Walkthroughs
- Real Estate Presentations
- Interior Visualization
- Exterior Visualization
- Client Demonstrations

### Interactivity

- Trigger Zones
- Interactive Objects
- Hotspots
- Custom Events
- Scriptable Actions

### Performance

- SharedArrayBuffer Communication
- Web Worker Physics
- Optimized Rendering Pipeline
- Efficient Memory Usage
- Large Scene Management

---

## Physics Architecture

Burn City utilizes **Cannon.js** as its core physics engine and extends it through a custom SharedArrayBuffer-based worker architecture.

Instead of continuously sending physics data between threads using traditional message passing, Burn City shares simulation state directly between the renderer and the physics worker.

### Physics Features

- Rigid Body Simulation
- Collision Detection
- Character Controllers
- Vehicle Dynamics
- Physics-Based Interactions
- Continuous Simulation Updates

### Shared Memory Pipeline

```text
Three.js Renderer
        │
        ▼
 SharedArrayBuffer
        ▲
        │
 Physics Worker
        │
        ▼
     Cannon.js
```

### Benefits

- Near-Zero Serialization Cost
- Reduced Main Thread Load
- Faster Physics Synchronization
- Higher Simulation Throughput
- Improved Frame Stability
- Better Scalability
- Optimized Vehicle Performance

This architecture allows Burn City to maintain smooth interaction even in large environments containing numerous active physics objects.

---

## Use Cases

### Architectural Showcases

Convert architectural models into immersive browser-based walkthrough experiences.

### Real Estate

Allow clients to explore properties remotely through interactive virtual tours.

### Digital Twins

Create real-time virtual representations of physical spaces and infrastructure.

### Event Experiences

Build virtual conferences, exhibitions, product launches, and trade shows.

### Urban Planning

Visualize city developments and infrastructure projects at scale.

### Education

Create immersive learning environments and interactive tours.

### Entertainment

Develop experimental virtual worlds and interactive experiences.

---

## Technology Stack

### Rendering

- Three.js
- WebGL
- GLSL

### Physics

- Cannon.js
- SharedArrayBuffer
- Web Workers

### Assets

- GLTF
- GLB
- HDRI
- KTX2

### Web Technologies

- JavaScript
- HTML5
- CSS3
- ES Modules

---

## Getting Started

### Requirements

- Modern Browser
  - Chrome
  - Edge
  - Firefox
- Visual Studio Code (Optional)
- Live Server Extension (Recommended)

### Clone Repository

```bash
git clone https://github.com/your-username/burn-city.git
```

### Open Project

```bash
cd burn-city
```

Open the project folder in Visual Studio Code.

### Run Using Live Server

1. Install the Live Server extension.
2. Open `burn-city.html`.
3. Right-click anywhere inside the file.
4. Select **Open with Live Server**.

The experience will launch automatically in your browser.

---

## Project Structure

```text
Burn-City/
│
├── assets/
│   ├── models/
│   ├── textures/
│   ├── audio/
│   ├── hdr/
│   └── environments/
│
├── burn-city.html
├── main.js
└── README.md
```

---

## Core Systems

### Scene Manager

Handles environment loading, unloading, and lifecycle management.

### Physics System

Custom Cannon.js implementation running in a dedicated worker using SharedArrayBuffer communication.

### Navigation System

Supports walking, free camera exploration, and customizable movement controllers.

### Vehicle System

Provides realistic vehicle physics and extensible driving mechanics.

### Environment System

Manages lighting, atmosphere, HDR environments, and visual effects.

### Interaction System

Supports triggers, hotspots, and event-driven interactions.

### Asset System

Optimizes asset loading and memory usage for large environments.

---

## Performance Goals

Burn City is built around the following principles:

- Fast Initial Load Times
- Stable Frame Rates
- Large Environment Support
- Efficient Physics Processing
- Low Memory Overhead
- Browser-Native Deployment
- Responsive User Interaction
- Scalable Scene Management

---

## Browser Compatibility

| Browser | Supported |
|----------|-----------|
| Chrome | ✅ |
| Edge | ✅ |
| Firefox | ✅ |
| Brave | ✅ |
| Opera | ✅ |

### SharedArrayBuffer Requirements

To enable the high-performance physics pipeline, the server must provide:

```http
Cross-Origin-Embedder-Policy: require-corp
Cross-Origin-Opener-Policy: same-origin
```

These headers are required for SharedArrayBuffer support in modern browsers.

---

## Roadmap

### Core

- [ ] Scene Streaming
- [ ] Runtime Asset Loading
- [ ] Asset Compression Pipeline

### Physics

- [ ] Soft Body Physics
- [ ] Destruction System
- [ ] Advanced Vehicle Dynamics

### Environment

- [ ] Dynamic Weather
- [ ] Day/Night Cycle
- [ ] Volumetric Clouds

### Multiplayer

- [ ] Multi-User Experiences
- [ ] Voice Chat
- [ ] Shared Sessions

### XR

- [ ] VR Support
- [ ] AR Support
- [ ] WebXR Integration

### Tools

- [ ] Visual Scene Editor
- [ ] Analytics Dashboard
- [ ] Asset Management Tools

---

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push your branch.
5. Open a Pull Request.

---

## License

MIT License

---

## Vision

Burn City aims to become a next-generation framework for creating browser-based virtual experiences by combining immersive rendering, advanced physics simulation, and scalable architecture into a single platform.

From architectural walkthroughs and digital twins to virtual events and interactive worlds, Burn City enables creators to publish rich experiences that anyone can explore instantly from a web browser.

### Build Once. Explore Anywhere.
