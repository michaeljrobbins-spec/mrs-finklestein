# mrs-finklestein
An assignment completed for ENG6806; a character created for basic interactions. Mrs. Finklestein is your kind fifth grade teacher, designed to provide encouragement and all the basic knowledge you need for the future.

## How it works

`index.html` is a single, self-contained page. It uses [Transformers.js](https://huggingface.co/docs/transformers.js) to download `onnx-community/Qwen2.5-0.5B-Instruct` (4-bit weights, roughly 0.8 GB) once into the browser cache. A picker on the page also offers the bigger `onnx-community/Qwen2.5-1.5B-Instruct` (roughly 1.8 GB) for comparison.
After that the model runs entirely on the visitor's device: WebGPU when it's available, WASM otherwise.

## Deploying on GitHub Pages

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*, then choose branch `main` and folder `/ (root)`, and save.
3. After a minute the site is live at `https://<username>.github.io/mrs-finklestein/`.

No build step is needed. The `.nojekyll` file tells Pages to serve the files as-is.

## Running locally

The page must be served over HTTP (not opened as a file). From the repository folder:

```bash
python3 -m http.server
```

Then open http://localhost:8000.
