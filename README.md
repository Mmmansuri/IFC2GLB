# IFC2GLB# Structural Model Viewer

A modern, interactive 3D structural model viewer built with Three.js. View and analyze your structural models directly in the browser with an elegant, feature-rich interface.

## 🌟 Live Demo

You can see the live viewer at: `https://mmmansuri.github.io/IFC2GLB/`

## ✨ Features

- **Interactive 3D Viewing**: Rotate, pan, and zoom through your structural models
- **Smart Element Coloring**: Automatically color-codes structural elements (beams, columns, walls, slabs, etc.)
- **Vertex Color Support**: Preserves and displays vertex colors from your GLB files
- **Dark/Light Canvas**: Toggle between light and dark canvas backgrounds
- **Fullscreen Mode**: Immersive fullscreen viewing experience
- **Keyboard Navigation**: Use WASD or arrow keys to navigate through the model
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Professional UI**: Modern gradient backgrounds with animated starfield effects
- **No Installation Required**: Runs entirely in the browser

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- An IFC file of your structural model

### Step 1: Convert IFC to GLB

Before using this viewer, you need to convert your IFC file to GLB format:

1. Visit [Convert3D](https://convert3d.org/app)
2. Upload your `.ifc` file
3. Select GLB as the output format
4. Download the converted `model.glb` file

### Step 2: Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git
   cd YOUR-REPOSITORY-NAME
   ```

2. Place your converted `model.glb` file in the root directory (same location as the HTML file)

3. Open `index.html` in your web browser, or serve it using a local web server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

4. Navigate to `http://localhost:8000` in your browser

## 🎮 Controls

### Mouse Controls
- **Left Click + Drag**: Rotate the model
- **Right Click + Drag**: Pan the camera
- **Mouse Wheel**: Zoom in/out

### Keyboard Controls
- **W / ↑**: Move forward
- **S / ↓**: Move backward
- **A / ←**: Move left
- **D / →**: Move right

### UI Controls
- **Canvas BG Toggle**: Switch between light and dark canvas backgrounds
- **Fullscreen Toggle**: Enter/exit fullscreen mode



## 📁 File Structure

```
.
├── index.html          # Main viewer application
├── model.glb          # Your 3D structural model (you provide this)
└── README.md          # This file
```

## 🔧 Customization

### Changing the Model Path

By default, the viewer looks for `model.glb` in the same directory. To load a different file, modify line 567 in `index.html`:

```javascript
loadGLBModel('model.glb');  // Change to your file path
```

### Adjusting Camera Settings

Modify the camera initialization in the `init()` function (around line 537):

```javascript
camera.position.set(5, 5, 10);  // Adjust X, Y, Z positions
```
