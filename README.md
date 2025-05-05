
# 🧼 Periodic Noise Removal from Images using Notch Filtering

## 📌 Problem Statement

Design and implement a frequency-domain image denoising technique that can effectively suppress periodic noise using notch reject filters. Evaluate the effectiveness of the denoising process using PSNR and SSIM metrics.

---

## 🔗 GitHub Repository

[GitHub Repository Link](https://github.com/Image_Removal_Restoration)

---

## 👨‍💻 Team Members

- **Pranaam** - 4SO22CD034  
- **Rishal D** - 4SO22CD041  
- **Preethesh** - 4SO22CD036

---

## 🎯 Objective

- Simulate periodic noise in grayscale images.
- Remove this noise using frequency-domain notch filtering.
- Measure the quality of denoising using PSNR and SSIM.

---

## 🛠️ Tools & Libraries Used

- Python (Google Colab)
- OpenCV
- NumPy
- Matplotlib
- scikit-image (PSNR and SSIM calculation)

---

## 🧪 Detailed Description / Program Flow

### 1. **Image Upload & Preprocessing**
- Read the grayscale image using OpenCV.
- Convert image into NumPy array.

### 2. **Simulating Periodic Noise**
- Generate a sinusoidal noise pattern using a defined frequency and amplitude.
- Add it to the original image to simulate interference.

### 3. **Transform to Frequency Domain**
- Perform 2D FFT using `np.fft.fft2()` and shift the zero-frequency component to the center using `np.fft.fftshift()`.

### 4. **Create Notch Reject Filter**
- Build a binary mask that zeros out the specific frequency components causing noise.
- Target both positive and negative frequency spikes.

### 5. **Filter & Inverse Transform**
- Apply the notch mask to the frequency domain image.
- Perform inverse FFT to bring it back to the spatial domain and get the filtered image.

### 6. **Evaluate with PSNR and SSIM**
- PSNR (Peak Signal-to-Noise Ratio) is computed to evaluate pixel-level noise suppression.
- SSIM (Structural Similarity Index) is computed to measure the perceptual quality of the filtered image.

---

## 📊 Results

| Metric | Value |
|--------|-------|
| **PSNR** | ~XX.XX dB |
| **SSIM** | ~0.XXXX |

The results indicate effective noise suppression with structural content preservation.

---

## 📷 Sample Output Images

| Stage            | Image Placeholder |
|------------------|------------------|
| Original Image   | `original_image.jpg` |
| Noisy Image      | `noisy_image.jpg`    |
| Filtered Image   | `filtered_image.jpg` |

---

## 💡 Applications

- **Medical Imaging**: Clean up MRI, X-ray, CT scans affected by periodic hardware noise.
- **Satellite & Aerial Images**: Remove scanning line artifacts in satellite imagery.
- **Digital Document Restoration**: Recover clean visuals from scanned historical documents.
- **Industrial Automation**: Remove electrical interference in visual inspections.

---

## 🚀 Future Work

- Support for color images by filtering RGB channels.
- Auto-detection of noise frequencies.
- Integration with a web UI using Streamlit for demo purposes.

---

## 📁 Project Structure

```
├── image_denoising.ipynb         # Google Colab Notebook
├── original_image.jpg            # Input grayscale image
├── noisy_image.jpg               # Image with added periodic noise
├── filtered_image.jpg            # Output image after noise filtering
└── README.md                     # Project documentation
```

---

## 📬 Contact

For queries or collaboration, reach out via GitHub or college contact details.
