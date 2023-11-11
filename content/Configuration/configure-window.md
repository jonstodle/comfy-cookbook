+++
title = "Configure Window"
+++

# Configure Window

To configure the game window, access it through the `EngineContext.renderer.window`:

```rust
pub fn setup(c: &mut GameContext) {
    c.engine.renderer.window.set_resizable(false);
}
```

It is an instance of [`Window`](https://docs.rs/comfy/latest/comfy/winit/window/struct.Window.html).
