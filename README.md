# GSA-Dehaze: A Grid-Spatial Attention Framework for Dehazing Remote Sensing Video Frames

GSA-Dehaze is a two-phase attention-based architecture designed for dehazing remote sensing video frames. It integrates Grid Attention and Spatial Attention to effectively restore both global structure and fine-grained details under varying haze conditions.

---

## 🔍 Sample Qualitative Results

The following results demonstrate the performance of GSA-Dehaze and baseline models under the **Moderate Fog** setting. Outputs are organized into subfolders per model:

📁 `/Moderate_set/frames_videos/`
- `Phase_1_Grid_Attention/` – Coarse outputs using only global attention
- `Phase_2_Spatial_Attention/` – Final refined outputs using spatial attention
- `Refusion/`, `4KDehazing/`, `spsr/`, `HazeSpace2M/` – Outputs from SOTA baselines
- `Ground_truth/` – Reference clean frames
- `Hazy/` – Input foggy frames

Each folder contains 4-second video sequences for side-by-side qualitative comparison.

---

## 📊 Quantitative Results

### 📌 Single Image Dehazing (SateHaze1k)

| Model         | PSNR ↑ | SSIM ↑  | LPIPS ↓ |
|---------------|--------|---------|----------|
| DCP           | 13.91  | 0.758   | 0.17     |
| AOD-Net       | 17.28  | 0.820   | 0.14     |
| FCTF-Net      | 20.46  | 0.867   | 0.12     |
| EDED-Net      | 24.31  | 0.907   | 0.08     |
| PGSformer     | 25.25  | 0.904   | 0.090    |
| **GSA-Dehaze**| **27.88** | **0.9148** | **0.0694** |

### 📌 Remote Sensing Video Frame Dehazing (SateHaze1k-Videos)

| Model         | PSNR ↑ | SSIM ↑  | LPIPS ↓ |
|---------------|--------|---------|----------|
| Hazy (input)  | 13.40  | 0.6944  | 0.2407   |
| Uformer       | 18.31  | 0.6858  | 0.2311   |
| Refusion      | 22.71  | 0.8240  | 0.1462   |
| 4KDehazing    | 22.25  | 0.8601  | 0.1673   |
| Grid Attention| 20.25  | 0.8452  | 0.1094   |
| **GSA-Dehaze**| **23.28** | **0.8686** | **0.1057** |

📌 *More results in our paper.*

---

## 🧪 Training, Testing, and Inference

Coming soon!

---

## 📦 Pretrained Models and Outputs

| Component        | Checkpoint Link | Notes |
|------------------|-----------------|-------|
| Grid Attention   | [Coming Soon]   | Trained on non-overlapping patches |
| Spatial Attention| [Coming Soon]   | Trained on overlapping patches from Phase 1 output |
| Full GSA-Dehaze  | [Coming Soon]   | End-to-end evaluation |

---

## 📄 Citation

If you find this repository useful, please consider citing our work:

```bibtex
@article{aboessa2025gsadehaze,
  title={GSA-Dehaze: A Grid-Spatial Attention Framework for Dehazing Remote Sensing Video Frames},
  author={Anas M. AboEssa and Bilel Benjdira and Wadii Boulila and Anis Koubaa},
  journal={Under Review},
  year={2025}
}
