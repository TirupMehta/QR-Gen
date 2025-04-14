# QR Gen with Python

A professional, minimal, and customizable QR code generator built using Python. This script allows you to generate high-quality QR codes for any text or URL.

## Features

- Generate QR codes from any text or URL
- High error correction level (H) for enhanced durability
- Customizable size, border, and color scheme
- Output saved as a `.png` image
- Easy to extend for additional functionality (like logo overlays)

## Requirements

- Python 3.x
- `qrcode` library
- `pillow` library

Install the dependencies with:

```bash
pip install qrcode pillow
```

## Usage Guide

1. Clone or download this repository.
2. Open the script and edit the `data` variable with your desired content.
3. Run the script:
   ```bash
   python qr_gen.py
   ```
4. The QR code will be saved as `qr.png` in the current directory.

## Code Snippet

```python
import qrcode

data = "https://example.com"  # Replace this with your URL or text
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=4,
)
qr.add_data(data)
qr.make(fit=True)
img = qr.make_image(fill_color="black", back_color="white")
img.save("qr.png")
```

## Output Preview

A file named `qr.png` will be created in your project directory. Open it to view the generated QR code.

## Customization Tips

- **Change Colors:**
  ```python
  img = qr.make_image(fill_color="black", back_color="white")
  ```
- **Adjust Size or Border:**
  Modify the `box_size` and `border` parameters for your desired resolution.
- **Logo Support:**
  Thanks to high error correction, you can overlay a logo at the center without affecting scanability.

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

Made with ❤️ by **Tirup Mehta**

