# Sub2s

`subts-player` provides a React HLS player component with built-in controls, LL-HLS support, and real-time playback stats.

## Preview

![SubTSPlayer preview](https://github.com/giapdeviscool/subts-player/blob/main/public/im1.png)

## Installation

Using npm:

```bash
npm install subts-player
```

Using yarn:

```bash
yarn add subts-player
```

## Usage

```tsx
import React from 'react';
import { SubTSPlayer } from 'subts-player';

export default function App() {
  return (
    <div style={{ width: 800, margin: '0 auto' }}>
      <h1>My Live Stream</h1>
      <SubTSPlayer
        url="https://example.com/playlist.m3u8"
        token="your-access-token"
        isLive={true}
        viewerCount={123}
        viewerMinutes={45.5}
      />
    </div>
  );
}
```

## Props

| Prop | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `url` | `string` | required | HLS playlist URL (`.m3u8`). |
| `token` | `string` | `undefined` | Optional Bearer token sent in the `Authorization` header. |
| `isLive` | `boolean` | `false` | Marks the stream as live and enables live badges/behavior and switch to autoplay. |
| `viewerCount` | `number` | `0` | Current concurrent viewer count shown in the top badge. |
| `viewerMinutes` | `number` | `0` | Total viewed minutes shown in the top badge. |

## Features

- LL-HLS (Low-Latency HLS) and standard HLS playback modes.
- Built-in modern controls: play/pause, volume, fullscreen, settings.
- Real-time stats panel: latency, buffer, resolution, bitrate, bandwidth, ABR status.
- Auto recovery for common network/media playback errors.
- Cross-browser support via `hls.js` with native HLS fallback where available.

## Controls

- Click the video to play/pause.
- Open settings to switch playback mode and inspect ABR/stats logs.
- Click `Connect` to jump back/connect to the latest live edge.

## License

MIT License

Copyright (c) 2026 subts-player

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
