# vendor-snapshots

Byte-for-byte copies of third-party files the Witbitz Spaces app builds with, so that every release can be rebuilt —
by us and by Witbitz's build enclave — without depending on the original hosts staying up or unchanged.

Each snapshot is a GitHub release of this repository. Its assets are the files exactly as they were published upstream;
`SHA256SUMS` lists them, and the Spaces build checks every file against the same hashes, pinned in its own source
(`spaces/tools/fetch-moonshine.sh`), whichever copy it reads. Nothing here is modified.

## `moonshine-tiny-2026-11-18` — on-device speech to text

| File | Upstream | Licence |
|---|---|---|
| `encoder_model.onnx`, `decoder_model_merged.onnx` | https://download.moonshine.ai/model/tiny/quantized/ | MIT — Moonshine (`LICENSES/moonshine.LICENSE`) |
| `ort-wasm-simd-threaded.jsep.wasm`, `ort-wasm-simd-threaded.jsep.mjs` | npm `onnxruntime-web@1.22.0` (`dist/`) | MIT — Microsoft Corporation (`LICENSES/onnxruntime-web.LICENSE`; the package declares MIT) |
| `silero_vad_v5.onnx`, `silero_vad_legacy.onnx` | npm `@ricky0123/vad-web@0.0.24` (`dist/`) | MIT — Silero Team (`LICENSES/silero-vad.LICENSE`) |
| `vad.worklet.bundle.min.js` | npm `@ricky0123/vad-web@0.0.24` (`dist/`) | ISC — ricky0123 (`LICENSES/vad-web.LICENSE`) |

Each file was fetched from its upstream on 2026-11-18 and was identical to the copy fetched on 2026-09-02.
