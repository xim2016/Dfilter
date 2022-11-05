# Dfilter
Dfilter is an R package whose function is to filter geneTF prior matrix based on the gene list that the user provides.

In the R environment, simply type in the following code to load the package
```sh
library(devtools)
install.github('xim201/Dfilter')
```
Once the package has been loaded to the R environment, then call the function filter_geneTF(). 

There are 5 parameters in the function call
```sh
@param geneTF_matrix
       geneTF prior
@param gene_lis
       t gene list user provided
@param TF_upbound (optional)
       the upper bound of percentage of TF targeted genes over all genes. The default is 80\%
@param TF_lowbound (optional)
       the lower bound of number of TF targeted genes. The defalut is 10
@param gene_lowbound (optional)
       the lower bound of number of TFs targeting to the gene

@return geneTF matrix
```
Usage examples:
```sh
filter_geneTF(geneTFmatrix, gene_list)
filter_geneTF(geneTFmatrix, gene_list, gene_lowbound=20)

```
Users can download "geneTFprior.csv" provided in ./data folder as the input of geneTFmatrix in the fileter_geenTF() function. In the "code" folder, we archive the process about how we generated this geneTFprior.csv
