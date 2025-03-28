This repository contains the code and files used in the paper called "Chorus: Optimizing Synchrotron Transfer Coefficients with Weighted Sums"

The code is made in Jupyter Notebook Python, so you will find this code to be in the .ipynb format.

This repository contains:

- The code for our new developed method Chorus
- Symphony† data in the form as comparison for Chorus
- Symphony data in the form as components utilized by Chorus
- A folder containing all the plots used in the paper

Additionally, to get the same results as in this paper, use the correct path to the correct .csv files.
If you want to use other data I would recommend installing Symphony and compute the results you want. The steps to installing Symphony can be found at https://github.com/AFD-Illinois/symphony/tree/master.

One can use Chorus to compute transfer coefficients in two ways:
1. Use Symphony data as thermal components. This repository provides 50 thermal components computed by Symphony from the range of 10^-4 < lambda < 10^0. If a different amount or range is needed, I recommend computing the necessary Symphony thermal components yourself.
2. Use fit functions found by Pandya et al. 2016* as the thermal components. This way does not need Symphony thermal components, but can be more prone to errors(see paper).

HOW TO USE for computing transfer coefficients with your own data:
1. Download the whole github repository, so you have every file needed.
2. In the code change the variable "f_data" to your required data. (currently it only contains computed kappa dist. functions)
3. Change the path for Symphony thermal components if needed.
4. Comment the line plotting Symphony data (recognized by the .plot using the label 'Symphony Data') if this plot is not needed.
5. Use the 'def' by indicating how many components, what range of lambda you want to use and if you want to use Symphony components.

As a last comment, the authors thank Marijke Haverkorn for her comments on the work. Additionally, Chorus is much improved by utilizing the interior solver Clarabel developed by Goulart et al.** 

For questions send an email to david.vanduren@ru.nl


† Marszewski A., Prather B. S., Joshi A. V., Pandya A., Gammie C. F., 2021,
The Astrophysical Journal, 921, 17

* Pandya A., Zhang Z., Chandra M., Gammie C. F., 2016, The Astrophysical
Journal, 822, 34

** Goulart P. J., Chen Y., 2024, arXiv preprint arXiv:2405.12762
