# WebGPU resize issue

Code is from the [Surface chapter of the Learn Wgpu Book](https://github.com/sotrh/learn-wgpu/tree/e84fa6a4fb38300b242aa45d3ce47e98be127ffd/code/beginner/tutorial2-surface/src) but the backend has been changed to `BROWSER_WEBGPU`.

```diff
let instance = wgpu::Instance::new(&wgpu::InstanceDescriptor {
    #[cfg(not(target_arch = "wasm32"))]
    backends: wgpu::Backends::PRIMARY,
    #[cfg(target_arch = "wasm32")]
-    backends: wgpu::Backends::GL,
+    backends: wgpu::Backends::BROWSER_WEBGPU,
    ..Default::default()
});
```

