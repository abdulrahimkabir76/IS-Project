# EduLight-64 — Educational Lightweight Block Cipher

EduLight-64 is an educational implementation and Gradio demo of a small custom block cipher.

**Warning:** This project is for learning and experimentation only. Do NOT use this cipher to protect real or sensitive data.

- **Block size:** 64 bits (8 bytes)
- **Key size:** 128 bits (16 bytes)
- **Structure:** Substitution–Permutation Network (SPN)
- **Mode:** CTR (stream-like encryption)
- **Default rounds:** 16 (configurable in UI)

## Contents

- `23f-0688_23f0848_23f-0864_23f-0800.ipynb` — Jupyter notebook containing the cipher implementation, tests, and a Gradio UI demo.
- `README.md` — (this file)

## Requirements

- Python 3.8+
- Install Python dependencies before running the demo:

```
pip install gradio
```

The notebook contains internal self-tests (avalanche and CTR roundtrips) that run when cells are executed.

## Quick usage

1. Open the notebook in Jupyter or VS Code and run the cells in order.
2. In the Gradio "EduLight-64" demo tab you can:
   - Encrypt plaintext (auto-derive key/nonce from plaintext when left blank).
   - Decrypt hex ciphertext (provide the same key/nonce used for encryption).
   - Run avalanche strength tests (configurable rounds).

Alternatively, if you prefer a script runner, extract the relevant functions from the notebook into a `.py` file and call `demo.launch()` from there.

## Tests

The notebook includes quick self-tests:
- Block cipher roundtrip tests for multiple round counts.
- CTR mode roundtrip tests.
- Avalanche tests (plaintext/key bit-flip statistics).

Run the corresponding cells to execute these checks.

## License & Attribution

This code is provided for educational purposes only. No warranty is provided. Reuse and modification are allowed for learning and research; include attribution when sharing derived work.


