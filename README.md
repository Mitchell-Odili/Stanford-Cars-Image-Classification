# Stanford Cars Classification: Transfer Learning & Optimization
### Strategic Model Selection (ResNet-34) under Hardware Constraints

This project implements a Computer Vision pipeline to classify the **Stanford Cars Dataset** (16,185 images / 196 classes). The core challenge of this experiment was balancing model complexity with limited GPU RAM, leading to a strategic pivot from custom architectures to **Transfer Learning**.

---

### 🛠 The Engineering Pivot: Custom vs. Pretrained
Initially, a **ResNet-9 architecture** was developed from scratch. However, evaluating the custom model triggered **GPU RAM exhaustion**, highlighting a critical bottleneck in the training pipeline.

**Technical Resolution:**
I transitioned the strategy to **Transfer Learning**, utilizing a pretrained **ResNet-34** model. This allowed for deeper feature extraction and higher predictive power without the memory overhead of training a complex custom architecture from the ground up.

**Advanced Techniques Implemented:**
* **Normalization & Data Augmentation:** Applied random cropping and flipping to improve generalization across 196 fine-grained car classes.
* **Regularization & Residual Connections:** Leveraged skip-connections to mitigate vanishing gradients.
* **One-Cycle Learning Rate Policy:** Optimized convergence speed to maximize the utility of available compute cycles.

---

### 📊 Performance Metrics
* **Architecture:** Modified ResNet-34 (Transfer Learning)
* **Dataset Complexity:** 196 distinct classes (Fine-grained classification)
* **Accuracy:** **~67.5%** * **Outcome:** Successfully demonstrated the power of pretrained models in resource-constrained environments, significantly improving predictive accuracy over scratch-built iterations.

---

### 🚀 Key Takeaways
* **Resource Optimization:** Identifying hardware bottlenecks (GPU RAM) and pivoting the technical roadmap to maintain project velocity.
* **Applied AI:** Understanding when to "build from scratch" vs. when to "leverage existing SOTA (State-of-the-art) models" for faster time-to-value.
* **Fine-Grained Classification:** Navigating the difficulty of high-cardinality label sets (196 classes) where visual variance is subtle.

---

### 🔗 Credits
Originally developed and optimized on [Jovian](https://jovian.com/mitchell-odili/stanford-cars).
