# canvas-ffmpeg
Record canvas frames to ffmpeg.wasm and export a video file, all in the browser.

Uses <a href="https://github.com/ffmpegwasm/ffmpeg.wasm/">ffmpeg.wasm</a> for the heavy lifting, huge props to the devs there.

## Usage

```bash
# Install dependencies
yarn

# Run server
yarn start
```
Open http://localhost:5000/ for a demo page that records a 10-second video of a 2048x2048 canvas animation. 

See <a href="blob/main/index.html">index.html</a> for the source. 

### Requirements

As a result of the ffmpeg.wasm dependency, the requirements are the same as well: WebAssembly Threads and SharedArrayBuffers.

Because the SharedArrayBuffer requirement, the page needs to be served with <a href="https://developer.chrome.com/blog/enabling-shared-array-buffer/#cross-origin-isolation">cross-origin isolation</a> headers. The <a href="blob/main/serve.json">serve.json</a> config file adds those here.
