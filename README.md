Fine-mapping transcriptome-wide association studies
===================================================

The repository contains the main results for the fine-mapping of transcriptome-wide association studies (TWAS) reported in

*Probabilistic fine-mapping of transcriptome-wide association studies*
Nicholas Mancuso, Malika K. Freund, Ruth Johnson, Huwenbo Shi, Gleb Kichaev, Alexander Gusev, Bogdan Pasaniuc.
bioRxiv 2018.

Results
-------
`LIPIDS.FUSION.tsv` contains the lipids (HDL, LDL, TG, total chol) TWAS association statistics.

Trait   Expression.Reference    Gene    Chr Tx.Start    Tx.End  Expression.h2g  Best.GWAS.SNP  
Best.GWAS.SNP.Z.score   Top.eQTL.SNP    Top.eQTL.R2 Top.eQTL.Z  Top.eQTL.GWAS.Z N.SNPs  Non.zero.weights
Best.fit.model  Model.5CV.R2    Model.5CV.P TWAS.Z  TWAS.

| Column | Description |
|--------|-------------|
| `Trait` | The lipids trait investigated |
| `Expression.Reference` | Short description of the gene expression reference panel |
| `Gene` | Canonical gene name |
| `Chr` | Chromosome |
| `Tx.Start` | Transcription start site |
| `Tx.End` | Transcription end site |
| `Expression.h2g` | SNP-hertiability explained by cis-SNPs in reference panel |
| `Best.GWAS.SNP` | SNP ID of the best GWAS SNP in the prediction model (i.e. smallest p-value) |
| `Best.GWAS.SNP.Z.score` | Z-score of the best GWAS SNP |
| `Top.eQTL.SNP` | SNP ID of the  best cis-eQTL SNP in the reference panel |
| `Top.eQTL.R2` | Variance-explained in measured gene expression by best cis-eQTL SNP |
| `Top.eQTL.Z` | Z-score of the best cis-eQTL SNP |
| `Top.eQTL.GWAS.Z` | GWAS Z-score of the best cis-eQTL SNP |
| `N.SNPs` | Number of SNPs in the model |
| `Non.zero.weights` | Number of SNPs with non-zero weights in the model |
| `Best.fit.model` | Model with the best prediction accuracy |
| `Model.5CV.R2` | Adjusted estimate of variance-explained in measured gene expression using 5-fold CV |
| `Model.5CV.P` | P-value of cross-validation R2 estimate |
| `TWAS.Z` | Z-score for TWAS test of association |
| `TWAS.P` | P-value for TWAS test |


`LIPIDS.FOCUS.XX.tsv` contains the secondary gene-based fine-mapping analysis over TWAS associations using prior variance of XX = {40, 80}.

| Column | Description |
|--------|-------------|
| `Expression.Reference` | Short description of the gene expression reference panel |
| `Gene` | Canonical gene name |
| `Chr` | Chromosome |
| `Tx.Start` | Transcription start site |
| `Tx.End` | Transcription end site |
| `Region` | Identifier for a risk region |
| `TWAS.Z` | Z-score for TWAS test of association |
| `TWAS.P` | P-value for TWAS test |
| `Resid.Z` | Residual Z-score after accounting for average signal at region |
| `PIP` | Marginal posterior probability for explaining observed association signal at BLOCK |
| `In.Cred.Set` | Boolean indicating whether the gene-model is in the 90% credible gene set |

Software and support
--------------------
For performing fine-mapping of TWAS associations please see [FOCUS](http://github.com/bogdanlab/focus).

For performing TWAS using summary-data, computing expression weights using custom expression panels,
and additional post-TWAS analyses please see [FUSION](http://github.com/gusevlab/fusion_twas).

If you have any questions or comments please contact nmancuso@mednet.ucla.edu
