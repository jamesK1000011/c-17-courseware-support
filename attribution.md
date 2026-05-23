---
title: Open Source Acknowledgments
description: Credit and license notices for the open-source software bundled with C-17 Courseware.
---

<p align="center">
  <img src="screenshots/app_icon.png" alt="C-17 Courseware app icon" width="48">
</p>

<div class="pdf-title" style="display: none;">
  <h1>C-17 Courseware — Open Source Acknowledgments</h1>
  <p>Credit and license notices for the open-source software bundled with C-17 Courseware.</p>
</div>

C-17 Courseware is built on top of one open-source project that deserves
direct credit: **Ruffle**. The license text below is reproduced verbatim
from the upstream source, and the same notices ship inside every copy of
the app at `Player/WebContent/LICENSE_MIT` and
`Player/WebContent/LICENSE_APACHE`.

---

## Ruffle

[Ruffle](https://ruffle.rs) is an open-source Flash Player emulator
written in Rust and WebAssembly. C-17 Courseware uses it to play
legacy SWF lesson modules natively inside an iOS WebView, with no Adobe
Flash Player or external browser required.

We ship a small custom fork of upstream `ruffle-rs/ruffle` that adds
typed WebAssembly exports for AVM2 method calls, display-tree
inspection, and a Flash-compat drop-target picker. The Ruffle player
core itself is unchanged. Both the upstream project and our fork remain
dual-licensed under the **MIT License** and the **Apache License,
Version 2.0**, at the recipient's choice.

- Upstream project: <https://github.com/ruffle-rs/ruffle>
- License terms: dual-licensed MIT OR Apache-2.0
- Bundled in: `Player/WebContent/ruffle_web_bg.wasm`,
  `Player/WebContent/core.ruffle.js`, `Player/WebContent/ruffle.js`

### MIT License (verbatim)

```
Copyright (c) 2018 Ruffle LLC <ruffle@ruffle.rs> and Ruffle contributors

Permission is hereby granted, free of charge, to any
person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the
Software without restriction, including without
limitation the rights to use, copy, modify, merge,
publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software
is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice
shall be included in all copies or substantial portions
of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF
ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT
SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR
IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
```

### Apache License, Version 2.0

The full Apache-2.0 text is reproduced in the bundled
`Player/WebContent/LICENSE_APACHE` file inside every copy of the app,
and is available verbatim at
<https://www.apache.org/licenses/LICENSE-2.0>. The summary clauses
relevant to this distribution:

- The Ruffle source code remains owned by its contributors.
- This app redistributes the compiled WebAssembly + JavaScript outputs
  with attribution preserved (NOTICE-equivalent text retained in the
  bundle).
- No warranty is provided; the software is distributed on an "AS IS"
  basis without warranties or conditions of any kind.

---

## Apple platform components

The rest of the app is built against Apple's first-party frameworks
(SwiftUI, WebKit, QuickLook, AVFoundation, UniformTypeIdentifiers,
Charts, CryptoKit) under the standard Apple Developer Program license
terms. No third-party Swift packages are linked.

---

## Contact

Questions about licensing or attribution: `<j.l.king.1000011@gmail.com>`.
