---
trigger: glob
globs: "*.gd, *.tscn"
---

# Godot rules
- Godot 4 syntax only (e.g. @export, @onready, signal.connect(callable))
- Use typed GDScript: var speed: float = 200.0
- Don't hand-edit .tscn files; describe the editor steps instead
