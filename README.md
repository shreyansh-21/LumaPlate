<h1>LumaPlate</h1>
<hr>
<h1>License Plate Recognition and Image Enhancement</h1>
<h2>ZeroDCE - Zero-Reference Deep Curve Estimation for Low-Light Image Enhancement</h2>

<p><strong>ZeroDCE</strong> is a deep learning algorithm designed for low-light image enhancement without the need for reference images. It estimates a set of pixel-wise enhancement curves, allowing the model to enhance images directly and efficiently.</p>

<h2>⭐ Key Features</h2>
<ul>
    <li>Fully self-supervised model — no need for reference images.</li>
    <li>Real-time low-light image enhancement.</li>
    <li>Pixel-wise curve estimation for precise adjustments.</li>
    <li>Uses non-reference loss functions for training.</li>
    <li>Lightweight and efficient — suitable for deployment on edge devices.</li>
</ul>

<h2>📖 How It Works</h2>
<h3>1. Curve Estimation Approach</h3>
<p>The model directly estimates the enhancement curves using a deep CNN. The enhancement operation is represented as:</p>
<pre><code>I_enhanced = I + α * I * (1 - I)</code></pre>
<p>where:</p>
<ul>
    <li><code>I</code> = input low-light image</li>
    <li><code>α</code> = pixel-wise curve parameter estimated by the network</li>
</ul>

<h3>2. Non-Reference Loss Functions</h3>
<ul>
    <li><strong>Color loss:</strong> Ensures the color consistency of the enhanced image.</li>
    <li><strong>Spatial loss:</strong> Preserves spatial structure by minimizing the difference between neighboring pixels.</li>
    <li><strong>Exposure loss:</strong> Adjusts the brightness of the image to the desired range.</li>
    <li><strong>Illumination smoothness loss:</strong> Reduces noise and artifacts in the enhanced image.</li>
</ul>

<h2>💻 Installation</h2>
<p>To install the dependencies, run:</p>
<pre><code>pip install tensorflow opencv-python pytesseract</code></pre>

<h2>🚀 Usage</h2>
<pre><code>import cv2
from ZeroDCE import ZeroDCE

# Load input image
img = cv2.imread('path/to/low_light_image.jpg')

# Enhance image
model = ZeroDCE()
enhanced_img = model.enhance(img)

# Save enhanced image
cv2.imwrite('path/to/enhanced_image.jpg', enhanced_img)
</code></pre>

<h2>📋 Requirements</h2>
<ul>
    <li>Python 3.8+</li>
    <li>TensorFlow 2.x</li>
    <li>OpenCV</li>
    <li>Pytesseract</li>
</ul>

<h2>📚 References</h2>
<ul>
    <li>Guo, Chunle, et al. "Zero-reference deep curve estimation for low-light image enhancement." <em>CVPR 2020</em>.</li>
</ul>
