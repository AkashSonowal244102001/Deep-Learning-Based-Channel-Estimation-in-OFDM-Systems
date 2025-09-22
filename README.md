
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

</head>
<body>

  <h1>⚡ Deep Learning-Based Channel Estimation for OFDM using CNN 🧠📡</h1>

  <p><em>A deep learning approach to channel estimation in OFDM by modeling the time–frequency response as 2D images and applying CNN-based super-resolution for high accuracy and low complexity.</em></p>

  <div class="section">
    <h2>📌 Project Overview</h2>
    <p>This project applies deep learning techniques, specifically <strong>SRCNN</strong> and <strong>DnCNN</strong>, to improve channel estimation in OFDM wireless systems. The time-frequency channel grid is treated as an image, and neural networks are trained to recover full-resolution channels from limited pilot-based estimates.</p>
  </div>

  <div class="section">
    <h2>🚀 Key Features</h2>
    <ul>
      <li>📶 OFDM Channel Modeled as 2D Grid</li>
      <li>🧠 CNN-based Super-Resolution (SRCNN, DnCNN)</li>
      <li>📉 Low-complexity, high-performance estimation</li>
      <li>🧪 Multiple pilot configurations: 8, 16, 24, 36, 48</li>
      <li>📊 PSNR-based evaluation</li>
    </ul>
  </div>
   <h2>🚀 Block Diagram</h2>
    <ul>
     <img src="Project_Essentials/Block_Diagram (2).png" alt="SRCNN Output">

  <div class="section">
    <h2>📂 Project Structure</h2>
    <pre><code>
├── main_code.py        # All training and evaluation steps
├── models.py           # CNN architectures (SRCNN, DnCNN)
├── utils.py            # PSNR, interpolation, and other helper functions
├── weights/            # Saved model weights
├── data/               # Noisy and perfect .mat channel files
└── index.html          # This page!
    </code></pre>
  </div>

  <div class="section">
    <h2>⚙️ Requirements</h2>
    <p>Install the required packages:</p>
    <pre><code>pip install numpy scipy matplotlib tensorflow</code></pre>
    <p><strong>Note:</strong> Mixed precision is used — run on GPU (Colab or CUDA-enabled local machine).</p>
  </div>

  <div class="section">
    <h2>📥 Data Files</h2>
    <p>Place the following <code>.mat</code> files in the working directory (or Google Drive path):</p>
    <ul>
      <li><code>Perfect_VehA.mat</code></li>
      <li><code>Noisy_VehA_SNR_22.mat</code></li>
    </ul>
    <p>Expected keys inside:</p>
    <ul>
      <li><code>My_perfect_H</code></li>
      <li><code>My_noisy_H</code></li>
    </ul>
  </div>

  <div class="section">
    <h2>🧪 How to Run</h2>
    <p>Run the full script in Google Colab or Jupyter:</p>
    <ol>
      <li>📦 Import libraries</li>
      <li>🔧 Load and preprocess dataset</li>
      <li>🧠 Train <strong>SRCNN</strong> model</li>
      <li>🧠 Train <strong>DnCNN</strong> using SRCNN output</li>
      <li>📈 Evaluate using PSNR</li>
      <li>🎨 Visualize results (images and plots)</li>
    </ol>
  </div>

  <div class="section">
    <h2>📈 Sample Output Visuals</h2>
    <p>Output of Different model:</p>
    <div class="image-grid">
      <img src="Project_Essentials/Final_Output.png" alt="Outout">
        </div>
    <p><strong>Left to Right:</strong> LS → SRCNN → DnCNN → Ground Truth</p>
  </div>
      <img src="Project_Essentials/SRCNN_VAl.png" alt="SRCNN Output">
      <img src="Project_Essentials/DNCNN_Val.png" alt="DnCNN Output">
      <img src="Project_Essentials/Validation_Loss_Curve.png" alt="Ground Truth">
     <img src="Project_Essentials/PNSR_Comparison.png" alt="Ground Truth">

  <div class="section">
    <h2>🏁 Results</h2>
    <p>Final evaluation using PSNR (you can replace these values with real ones):</p>
    <table>
      <thead>
        <tr>
          <th>Model</th>
          <th>PSNR (dB)</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>SRCNN</td>
          <td>52.87</td>
        </tr>
        <tr>
          <td>DnCNN</td>
          <td>40.01</td>
        </tr>
      </tbody>
    </table>
  </div>

