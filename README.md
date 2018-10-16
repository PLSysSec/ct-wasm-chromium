# CT-Wasm Chromium

Instructions and resources for building chromium with support for CT-Wasm.

Maintaining a fork of Chromium is notoriously difficult due to their use of `depot_tools` for custom management of their multi-repository system. For this reason, we provide a git patch that applies to V8 at a specific Chromium build that enables CT-Wasm in the browser.


### Instructions for building CT-Wasm Chromium

1. Checkout Chromium according to the instructions
[here](https://www.chromium.org/developers/how-tos/get-the-code).

2. Once you have the source. Follow the [instructions
here](https://stackoverflow.com/questions/4481803/how-to-get-code-of-specified-tag-version-of-chromium-from-git)
to checkout version `65.0.3325.125`..

3. Enter the `src/v8` directory and apply the patch like so:
```bash
cd v8
git apply path/to/ct.patch
```

4. Build as usual

### Chromium binary

We also provide a pre-built Linux x64 binary for Chromium [here](https://github.com/PLSysSec/ct-wasm-spec/releases/download/artifact/linux_x86_64_ct-chrome.zip).
