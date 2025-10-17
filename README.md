# ATML-PA2 — Domain Shift: UDA, DG, and Prompt Learning

Code and experiments for ATML-PA2 (Tasks 1–3):  
**Task 1:** Unsupervised Domain Adaptation (UDA)  
**Task 2:** Domain Generalization (DG) via Invariant & Robust Learning  
**Task 3:** Prompt Learning with CLIP (zero-shot + learned prompts)

> **Repo:** https://github.com/tk1475/ATML-PA2  
> **Authors:** Ahmed Hassan (26100308@lums.edu.pk), Basil Hassan (26100303@lums.edu.pk), Ashhad Ali (26100307@lums.edu.pk)

---

## 0) Environment

- Python ≥ 3.10, PyTorch ≥ 2.0, torchvision ≥ 0.15
- CUDA GPU strongly recommended

```bash
# (Option A) Conda
conda create -n atml-pa2 python=3.10 -y
conda activate atml-pa2
pip install -r requirements.txt

# (Option B) Pip only
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### Task2 Results:

| Method      | Target   | Avg Source | Worst Source | Art   | Cartoon | Photo |
| ----------- | -------- | ---------- | ------------ | ----- | ------- | ----- |
| ERM         | 73.6     | 100.0      | 100.0        | 100.0 | 100.0   | 100.0 |
| IRM (IRMv1) | 77.5     | 96.8       | 95.5         | 95.5  | 95.5    | 99.4  |
| Group DRO   | **80.2** | 98.9       | 97.5         | 99.2  | 97.5    | 99.9  |
| SAM         | 78.9     | 100.0      | 100.0        | 100.0 | 100.0   | 100.0 |
