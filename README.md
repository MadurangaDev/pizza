# 🍕 Pizza

> "**Pizza**: The Secret Recipe for Clean, Tasty Code!" 🍕  
> Write once in Pizza's simple syntax → transpile to Python, C++, and more.

**Pizza** is a developer-first transpiler and CLI toolchain that introduces a clean, JavaScript-inspired syntax which compiles into your favorite backend languages — starting with Python. It’s designed to improve readability, reduce boilerplate, and provide a hot-reload-ready dev workflow. Powered by Rust, Pizza runs fast and scales well for future enhancements.

---

## 📦 Features

- 🍝 JS-like syntax with optional braces and semicolons
- ⚙️ Built-in CLI (`pizza cook`, `pizza bake`, `pizza serve`, etc.)
- 🧠 Plugin system & macro support (e.g. `repeat`, `until`)
- 🔁 Hot-reload-ready (planned)
- 🧰 Dev server support (e.g. Flask, FastAPI, etc.)
- 📚 File-based modules with auto import
- 🎨 Themes & starter templates (CLI, FastAPI, Flask)
- 🚀 Fast performance via native Rust binary
- ✅ No need to install Rust — comes as a standalone binary
- 💻 VS Code extension (coming soon)

---

## 📁 Folder Structure

```
pizza-project/
├── src/                   # .pza source files
│   └── main.pza
├── out/                   # Transpiled output (e.g., Python)
│   └── main.py
├── plugins/               # Custom macro/syntax plugins
│   └── repeat.rs
├── templates/             # Starter templates (e.g., CLI, API)
│   └── fastapi.pza
├── dist/                  # Production-ready build
├── recipe.json            # Project config (replaces pizza.json)
├── README.md
```

---

## ✨ Example

### `main.pza`

```pizza
if(5 > 2){
  print("Five is greater than two!");
}

repeat(3){
  print("Hello!");
}
```

### Compiles To (Python)

```python
if 5 > 2:
    print("Five is greater than two!")

for _ in range(3):
    print("Hello!")
```

---

## ⚙️ How It Works

- Parses `.pza` into AST
- Transforms AST via macros/plugins
- Transpiles to target language (initially Python)
- Outputs result to `out/` or `dist/` folder

All written in high-performance Rust, compiled to a native binary (`pizza.exe` or `pizza`).

---

## 🧪 CLI Commands

| Command         | Description                                     |
|-----------------|-------------------------------------------------|
| `pizza prep`    | Initialize a new Pizza project                  |
| `pizza cook`    | Transpile + run dev build (hot reload in future)|
| `pizza bake`    | Transpile production build only                 |
| `pizza serve`   | Transpile + run production build                |

---

## 🔧 `recipe.json` Configuration

```json
{
  "source": "src",
  "output": "out",
  "dist": "dist",
  "language": "python",
  "sourcemaps": true,
  "plugins": ["repeat", "until"],
  "runner": "fastapi",
  "theme": "default",
  "templates": ["fastapi", "cli"]
}
```

---

## 🔌 Plugin System

Create plugins in the `plugins/` folder to transform macro syntax.

### Example: `repeat.rs`

```rust
// Example Rust-based plugin logic
// Converts `repeat(n){...}` to `for _ in range(n): ...` in Python

fn transform_repeat(node: &ASTNode) -> TranspiledCode {
    // Plugin logic here
}
```

---

## 🎨 Templates

Pizza provides reusable starter templates:

- `fastapi` → REST API
- `flask` → Web App
- `cli` → Command-line App

---

## 💻 VS Code Extension (Coming Soon)

- Syntax highlighting
- Auto transpile on save
- Macro autocomplete
- Source map error tracing

---

## 📦 Distribution

Pizza ships as a single **compiled `.exe` or binary**, so you don't need to install Rust, Python, or any build tools. Just install `pizza.exe` and run:

```bash
pizza cook
```

Pizza takes care of everything under the hood.

---

## 📅 Roadmap

- [x] Parser, AST builder
- [x] Transpiler engine
- [x] Plugin system
- [x] CLI tool (Rust)
- [ ] Hot Reloading
- [ ] VS Code extension
- [ ] Playground (Web)
- [ ] Multi-language output (C++, JS, etc.)
- [ ] Template/plugin registry
- [ ] Native GUI (Pizza Studio)

---

## 🤝 Contributing

1. Fork the repo  
2. Create a feature branch  
3. Push your changes  
4. Open a PR

Read `CONTRIBUTING.md` for details.

---

## 📄 License

MIT License. See [`LICENSE`](./LICENSE).

---

## 👨‍🍳 Author

**Maduranga Jayasena**  
Crafting clean code with a crispy crust.

GitHub: [@MadurangaDev](https://github.com/MadurangaDev)
