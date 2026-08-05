# Gianluca Lauro - Curriculum Vitae

Repository containing the source code of my Curriculum Vitae in YAML format, compiled into PDF, HTML, and Markdown using [RenderCV](https://github.com/rendercv/rendercv).

## 🚀 Prerequisites

To build the CV locally, you need **Python 3.10+** and **RenderCV**:

```bash
pip install "rendercv[full]"
```

## 🛠️ Local Build

### Standard build (without photo)
```bash
rendercv render Gianluca_Lauro_CV.yaml
```

### Build with photo via command line
```bash
rendercv render Gianluca_Lauro_CV.yaml --cv.photo "https://your-photo-url.com/photo.jpg"
```

The generated files (PDF, HTML, Typst, and Markdown) will be saved in the `rendercv_output/` folder.

## ⚙️ GitHub Actions CI/CD

This repository includes a GitHub Actions workflow (`.github/workflows/rendercv.yaml`) that runs automatically on every `push` to `main`:
1. Dynamically injects the photo URL from GitHub Variables/Secrets.
2. Compiles the CV into PDF, HTML, and Markdown formats.
3. Publishes an updated release under GitHub Releases.

### Configuring the Photo URL on GitHub:
1. Go to **Settings** > **Secrets and variables** > **Actions**.
2. Add a new Repository Variable (or Secret) named **`PHOTO_URL`**.
3. Set the value to the direct URL of your profile photo.
