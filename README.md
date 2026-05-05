# A* Pathfinder

An interactive pathfinding visualizer built with vanilla JavaScript and HTML5 Canvas. Draw walls and mazes on a 25×25 grid, then watch the A* algorithm find the shortest path from start to finish.

![Demo](https://user-images.githubusercontent.com/47620000/70857738-54000e80-1ec2-11ea-9f2e-f0ba32d0b1f2.png)

---

## 🔍 How It Works

The grid is a 25×25 array of tiles, each carrying an `(x, y)` position and a state. When **Solve** is clicked, the algorithm runs a best-first search using a **heuristic function** — squared Euclidean distance to the finish tile — to prioritize which node to expand next. As nodes are explored, their states are updated and the canvas re-renders at 100 fps via `setInterval`, giving a live visualization of the search process.

Once the finish is reached, the path is reconstructed by replaying the encoded direction string stored in each visited tile's state (`'l'`, `'r'`, `'u'`, `'d'`), then highlighting each step in bright blue.

---

## 🎨 Node Color Legend

| Color | Meaning |
|---|---|
| 🩷 Pink | Start node (top-left) |
| 🔵 Dark Blue | End node (bottom-right) |
| ⬛ Black | Wall / obstacle |
| 💙 Bright Blue | Shortest path |
| 💚 Green | Nodes explored during search |
| 🩵 Light Blue | Empty / unvisited node |

---

## 🕹️ Controls

- **Left click** on an empty tile → place a wall
- **Left click** on a wall → remove it
- **Click and drag** → draw or erase a line of walls continuously
- **Solve** → run the pathfinder and visualize the result
- **Reset** → clear the grid back to its initial state

---

## 🗂️ File Structure

```
a-star-pathfinder/
├── index.html       # Canvas layout, buttons, and outcome text
├── pathfinder.js    # Grid logic, A* algorithm, mouse event handlers
└── pathfinder.css   # Styling for the grid, canvas, and buttons
```

---

## 🚀 Getting Started

No dependencies or build steps required — just open `index.html` in any modern browser.

```bash
git clone https://github.com/your-username/a-star-pathfinder.git
cd a-star-pathfinder
open index.html
```

---

## 💡 Implementation Notes

- The grid is rendered entirely on an HTML5 `<canvas>` element and redrawn every 10ms.
- Wall drawing uses mouse delta tracking (`boundX`/`boundY`) to prevent a single drag from toggling the same tile repeatedly.
- The path encoding encodes the traversal route as a direction string directly in each tile's state, avoiding a separate parent-pointer map.

---

## 📄 License

See [LICENSE](LICENSE) for details.
