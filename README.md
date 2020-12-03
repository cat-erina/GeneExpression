# GENE EXPRESSION REGULATION

At the end of our project we decided to find the right amount of genes to target for a therapy based on miRnas and genes’ expression normalization. 
 
The idea was to try and simulate a different normalized expression for some genes and find out how closer to the normal condition of co-expression we could get. 
Since we were not interested in the precise correlation value between two genes we decided to measure the differencebetween co-expressions by comparing the resulting adjacency matrices, i.e.  considering only differences that were big enough to change the relation (edge or no edge) between two genes.

In our trials we decided to only consider the hubs of the differential co-expression network, since they are the more altered genes.

Initially we tried by changing the expression of just one gene, creating a vector with mean equal tothe mean expression of that same gene in a normal condition. 
Then, since the results were not asgood as expected we increased the number of genes to alter at the same time (or rather to targetwith miRna), and looked for the best combination.
We tried out all possible combinations of 2, 3 and 4 genes at a time.

Unfortunately due to the factor of time we could not try all the combination of 5 genes (3 millions and a half), but trying out half a million of them we managed to find the bestresult thus far with genes ERBB3 SDC4, GRB7, COL8A1, MEX3A.
Normalizing their expression allowed us to reduce the difference of the normal adjacency matrix and the cancerous one from 26652 to 26150 (these numbers are the sum of how many differences are present when comparing the two matrices element-wise).

Knowing  that  we  lacked  the  means  to  carry  out  an  exhaustive  research  we  decided  to  look for a trend in the improvements of the results in function of the number of genes.
When we add more then 5 genes the speed of the improvement rate decreases, because the selection of genes will also include less influential ones.
