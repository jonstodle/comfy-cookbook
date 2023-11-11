+++
title = "Window Sizing"
+++

To set the size of the window, use the `set_inner_size` method:

```rust
pub fn setup(c: &mut GameContext) {
    c.engine.renderer.window.set_inner_size(LogicalSize::new(1920, 1080));
}
```

You can either use `PhysicalSize` or `LogicalSize`. The difference is that `PhysicalSize` is in physical pixels on the screen, while `LogicalSize` is in "displayed" pixels.

Operating systems allows the user to scale up the size of the UI on their screens. A small screen with a high pixel density might scale everything by 200%. This means a button that's 100px wide will be 200px wide on the screen. The physical size of the button is 100px, but the logical size is 200px.

If you want to respect the user's scaling settings, use `LogicalSize`. If you want to ignore the user's scaling settings, use `PhysicalSize`.

More details can be read in the [winit documentation](https://docs.rs/comfy/latest/comfy/winit/dpi/index.html).
