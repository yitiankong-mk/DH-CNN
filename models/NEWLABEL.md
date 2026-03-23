1. Prepare your dataset.
Provide molecular structures in a format such as SMILES, together with the corresponding spectra. Each spectrum should be linked to the correct molecular structure so that labels can be generated automatically.
2. Define functional-group labels using SMARTS.
Use the SMARTS definition to specify the functional groups of interest. These SMARTS patterns can be matched against each molecule and generate multilabel annotations automatically.
3. Modify the label set if needed.
If you want to change the functional-group labels, you can:
-remove labels that are not needed,
-add new labels by introducing additional SMARTS patterns, or
-discard the current label set entirely and rebuild the annotations from scratch using a completely new label set.
4. Train the model on the revised dataset.
Use the same preprocessing and training pipeline. This may include preparing the spectra in the expected format, aligning them with the regenerated labels, and training the model with the updated label dimension.
5. Evaluate performance.
After training, evaluate the model using multilabel metrics such as macro-F1, micro-F1, per-class scores, and exact-match ratio. This step is especially important when the label set has changed, since some newly added labels may be much rarer than others.
