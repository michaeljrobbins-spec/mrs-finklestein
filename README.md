# mrs-finklestein
An assignment completed for ENG6806; a character created for basic interactions. Mrs. Finklestein is your kind fifth grade teacher, designed to provide encouragement and all the basic knowledge you need for the future.

## Running it

Open `index.html` from any static web server (for example `python3 -m http.server`) and click **Download model**.
The page uses Transformers.js to download `onnx-community/Qwen2.5-0.5B-Instruct` (4-bit, roughly 0.5 GB) once into the browser cache.
After that it runs entirely on the visitor's device: WebGPU when it's available, WASM otherwise.
