R Shiny pipeline for analyzing calcium imaging data from prairie vole suprachiasmatic nucleus (SCN) explants, developed to support analysis of calcium dynamics in ex vivo SCN tissue cultured on a 3D-printed bubble perfusion microfluidic chip.
Overview
This pipeline processes raw calcium imaging traces (Calbryte 520 AM fluorescence) acquired during microfluidic perfusion experiments and outputs statistically corrected, photobleach-adjusted signal data ready for figure generation and downstream interpretation.
Pipeline Steps

Data import — Loads raw fluorescence trace data exported from imaging acquisition software (Olympus BX43 / Hamamatsu ORCA-Spark).
Manual artifact exclusion — Interactive frame-level exclusion of frames affected by oxygen bubble artifacts introduced during perfusion switching.
Photobleaching correction — Fits a one-phase exponential decay model to baseline fluorescence and corrects traces accordingly.
Statistical testing — Performs frame-level Wilcoxon rank-sum tests between experimental conditions, with Benjamini-Hochberg false discovery rate (FDR) correction for multiple comparisons.
Output — Generates corrected traces and summary statistics for figure generation.
