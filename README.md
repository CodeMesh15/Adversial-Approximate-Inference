# Adversial-Approximate-Inference
Adversarial Approximate Inference for Speech to Electroglottograph Conversion A deep generative model that learns to infer Electroglottograph (EGG) signals directly from speech using variational inference and adversarial training — removing the need for specialized hardware in glottal signal analysis.

## 📌 Project Summary

- **Goal**: Predict EGG signals from raw speech using deep generative modeling.
- **Method**: Leverage adversarial approximate inference with a variational autoencoder and informative prior learning.
- **Outcome**: Accurate estimation of EGG signals, enabling applications in speech analysis, speaker diagnostics, and voice pathology detection.

---

## 🧠 Core Ideas

- **Latent Variable Modeling**: The speech-to-EGG mapping is modeled as a conditional latent variable model.
- **Informative Prior**: A neural autoencoder trained on EGG signals acts as a prior to guide the inference.
- **Adversarial Training**: A discriminator network ensures that the latent distributions of speech and EGG representations match.
- **KL-Divergence Minimization**: The Evidence Lower Bound (ELBO) is optimized by aligning approximate and true posterior distributions.

---

## 🛠️ Architecture Overview
Speech → Encoder → Latent z  
            ↓  
 +-------- Adversarial Alignment --------+  
 ↓                      ↓  
Decoder            → Reconstructed EGG

- **Encoder**: Converts speech into a latent representation.
- **Decoder**: Generates EGG from the latent code.
- **Discriminator**: Aligns latent codes of speech and EGG via adversarial loss.

---

## 📦 Installation

```bash
git clone https://github.com/<your-username>/adversarial-approximate-inference.git
cd adversarial-approximate-inference
pip install -r requirements.txt
