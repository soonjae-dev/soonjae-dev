## Lee Soon-jae

Physics undergraduate at Chungbuk National University, working on applied
machine learning — and, more often than I expected, on the question of whether
a result that looks right actually is.

Two of my projects turned out to be built on numbers that were wrong while
reporting success. Finding out why taught me more than the original work did,
so both repositories now document the failure alongside the fix.

### Selected work

**[physics-ml-foundations](https://github.com/soonjae-dev/physics-ml-foundations)**
Numerical methods from a physics curriculum — Fourier and wavelet transforms,
SVD and power iteration, compressed sensing, physics-informed neural networks —
written as runnable code and mapped to where the same mathematics appears in
machine learning. Three of the original scripts produced output without
producing an error:

- An ℓ₁ recovery that minimised `sum(x)` subject to `x ≥ 0` instead of the
  actual ℓ₁ norm. The solver reported success and returned a wrong signal;
  correcting the formulation took the recovery error from 2.8 to 10⁻¹⁴.
- A Navier–Stokes PINN with no boundary term in its loss, which makes any
  zero-derivative field a *global* minimum. The ablation reproduces it: the
  degenerate solution scores a PDE residual **5,700× better** than the correct
  one. Judged on physics loss alone, the useless answer wins.
- A diode fit spanning the resistance-limited tail, returning a saturation
  current of 0.45 A and an ideality factor of 130 — both physically impossible
  — at R² = 0.83.

**[IVF-Pregnancy-Prediction](https://github.com/soonjae-dev/IVF-Pregnancy-Prediction)**
Ensemble pipeline for the LG Aimers hackathon: GAIN imputation, SMOTE, Optuna
tuning, stacking and weighted ensembles over 256,351 records. The reported CV
ROC-AUC of 0.89 was inflated — SMOTE had been applied before the
cross-validation split, so synthetic points interpolated from a sample could
land in a training fold while the sample itself sat in validation. Moving the
resampling inside the fold gives **0.7304 AUC / 0.5068 F1** out-of-fold, a drop
of 0.18. The repository reports the corrected figures and the size of the gap.

**[EV-Price-Prediction](https://github.com/soonjae-dev/EV-Price-Prediction)**
Used electric-vehicle price modelling from battery capacity and specifications.

### Background

I came to this from physics rather than computer science, which shows in both
directions. The mathematics transfers directly — linear algebra and SVD,
Fourier and wavelet analysis, numerical methods for differential equations,
and the habit of quoting a measurement with its uncertainty and its resolution
limit rather than as a bare number. The software engineering I have had to
learn deliberately, and am still filling in.

Experimental work leaves a specific instinct: a clean-looking number is not
evidence of anything until you know what would have made it look different.
That turned out to be the most portable thing I brought.

### Tools

Python · PyTorch · scikit-learn · XGBoost / LightGBM / CatBoost · Optuna ·
NumPy / SciPy · Git

### Contact

naver7737@gmail.com
