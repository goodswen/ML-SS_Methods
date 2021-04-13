# ML-SS_Methods

Linux pipelines for predicting exportome members using machine learning with secondary structure properties (version 1.0)
=============================================================================
In the paper “**Predicting protein vaccine candidates for bovine babesiosis using secondary structure properties and machine learning**”, we present methods (referred to henceforth as the ML-SS methods) for predicting the probability that a protein belongs to a parasite’s exportome. An exportome comprises those proteins secreted outside the parasite and inserted into or onto the membrane of a red blood cell from a host.
The structural properties used are a protein’s local conformational classification states, backbone torsion angles phi and psi, solvent-accessible surface area (ASA), and half-sphere exposure (HSE).

Five Linux pipelines are provided here that implement the ML-SS methods:

**pipeline_ss** = 3 and 8 class conformational predictions

**pipeline_angles** = psi and phi angles predictions

**pipeline_prop** = ASA and HSE-upper predictions

**pipeline_all** = 3 and 8 classes, psi and phi angles, ASA and HSE-upper (with Spider3 inputs)

**pipeline_TM** = predicts the presence of transmembrane (TM) domains.

Four additional pipelines are also provided to conduct automated 10-fold cross validation (CV) of the ML-SS methods: pipeline_CV_ss, pipeline_CV_angles, pipeline_CV_prop, and pipeline_CV_TM.

## Notes:
1. All pipelines are provided with a ReadMe file with instructions, and test and training data for *Babesia bovis* T2Bo.

2. The input to the ML-SS methods are raw files generated by secondary structure predictor programs These programs are not packaged with the pipelines and need to be downloaded and installed independently.

3. The pipelines use the machine learning algorithms adaptive boosting (AdaBoost) and random forest (RF). These algorithms were implemented via the R functions ada and randomForest respectively, and need to be installed.

4. The machine learning models provided are trained on *Babesia bovis* proteins

5. The pipelines have only been tested on Red Hat Enterprise Linux 7.7, but are expected to work on most Linux distributions

For **HELP**, please e-mail Stephen.Goodswen@uts.edu.au
