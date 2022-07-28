# Codebase for "Missing value estimation of microarray data using Sim-GAN"

Authors: Jinsung Yoon, James Jordon, Mihaela van der Schaar

Paper: Pati, S.K., Gupta, M.K., Shai, R., Banerjee, A., Ghosh, A. Missing value estimation of microarray data using Sim-GAN. Knowl Inf Syst (2022). https://doi.org/10.1007/s10115-022-01718-0
 
Paper Link: https://link.springer.com/article/10.1007/s10115-022-01718-0

Contact: ab2141@cse.jgec.ac.in

We are using Kent Ridge Biomedical Dataset to validate the Sim-GAN Framework
Link: https://leo.ugr.es/elvira/DBCRepository/

To run the pipeline for training and evaluation on Sim-GAN framwork, simply run 
python3 -m main_cancer.py.

Note that any model architecture can be used as the generator and 
discriminator model such as multi-layer perceptrons or CNNs. 

### Command inputs:

-   data_name: leukemia, Colon, Lung, Prostate, DLBCL
-   miss_rate: probability of missing components
-   batch_size: batch size
-   hint_rate: hint rate
-   alpha: hyperparameter
-   iterations: iterations

### Example command

```shell
$ python3 main_letter_spam.py --data_name leukemia 
--miss_rate: 0.2 --batch_size 128 --hint_rate 0.9 --alpha 100
--iterations 10000
```

### Outputs

-   imputed_data_x: imputed data
-   rmse: Root Mean Squared Error
