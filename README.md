
# Statistical Methods in Structural Bioinformatics

This repository gathers a series of Jupyter notebooks showcasing implementations of computational and statistical techniques for analyzing biomolecular structure. Each lab walks you through the workflow—from raw data processing and quality checks to advanced modeling and visualization.

---

## Lab 1: Structure Quality & Comparison  
Explore how to assess the accuracy of predicted or experimentally determined models.  
- **Data preparation & manual curation**  
  Load pairs of reference vs. test structures, visually inspect alignments to confirm correspondence, and remove any misaligned chains by hand.  
- **Metric computation & visualization**  
  Calculate deviation measures (RMSD, TM-score, GDT and LDDT) using established tools; aggregate results into summary tables.  
- **Clash detection**  
  Scan all interatomic distances to flag steric overlaps, manually review the worst offenders, and illustrate clash hotspots in 3D snapshots.  
- **Summary report**  
  Combine plots and tables into a clear single‐page overview, highlighting models that pass or fail user‐defined quality thresholds.

---

## Lab 2: Bayesian Analysis of Riboswitches  
Apply Bayesian inference to understand how ligand binding shifts RNA folding equilibria.  
- **Model setup & prior selection**  
  Define structural states (apo vs. holo) and choose priors from literature–derived folding energies.  
- **Sampling & convergence checks**  
  Run MCMC chains to sample posterior distributions of state populations; manually examine trace plots to verify convergence.  
- **Posterior analysis**  
  Extract credible intervals for each folding state, compare distributions before/after ligand addition, and visualize with violin and density plots.  
- **Interpretation notes**  
  Annotate cases where the sampler struggled (e.g. multi‐modal posteriors) and describe how manual tuning of proposal widths improved mixing.

---

## Lab 3: Markov Chains & Hidden Markov Models  
Build probabilistic sequence models for annotation and motif discovery.  
- **Transition matrix estimation**  
  From hand-curated alignments, count observed transitions and normalize to obtain initial Markov chain probabilities.  
- **HMM training**  
  Use Baum–Welch on training sets to learn emission/transition parameters; track log-likelihood improvement over iterations, discarding early noisy epochs.  
- **Decoding & motif scanning**  
  Apply Viterbi decoding to new sequences, manually inspect alignments at high-scoring regions, and extract candidate motifs for downstream validation.  
- **Performance evaluation**  
  Compute sensitivity/specificity on held‐out data, present ROC curves, and comment on model limitations where false positives clustered in low-complexity regions.

---

## Lab 4: Statistical Physics of Biomolecular Systems  
Model RNA folding as an ensemble phenomenon using principles from statistical mechanics.  
- **Energy function definition**  
  Assign stacking and loop energies from empirical tables; explain manual adjustments made to offset rare motif biases.  
- **Partition function & free energy**  
  Compute partition sums by exhaustive enumeration (for short sequences) and by Monte Carlo integration (for longer chains).  
- **Landscape visualization**  
  Project free‐energy surfaces along reaction coordinates, hand-select representative minima, and annotate folding pathways.  
- **Ensemble averages**  
  Derive expectation values of observables (e.g. radius of gyration) with both direct summation and importance sampling, noting convergence behavior.

---

## Lab 5: Directional Statistics  
Analyze circular data arising from backbone dihedral angles.  
- **Data extraction & preprocessing**  
  Parse PDB files to collect φ/ψ angles, wrap values to [–π, π], and manually remove outliers from poorly resolved residues.  
- **Distribution fitting**  
  Fit von Mises and wrapped Cauchy models to each angle set using maximum likelihood, compare fits via AIC, and document manual checks on parameter sensibility.  
- **Circular descriptive metrics**  
  Compute mean directions, angular variances, and dispersion measures by hand‐verified formulas.  
- **Visualization**  
  Create rose‐diagram plots and polar density curves; annotate peak regions corresponding to known secondary‐structure basins (α-helix, β-sheet, etc.).

