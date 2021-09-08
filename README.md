# Probability-and-stochastic-process(MSA model)
Detailed Analysis of "Multiscale approach predictions for biological outcomes in ion-beam cancer therapy" int context to Probability and stochastic process.
# Reference
 [Multiscale approach predictions for biological outcomes in ion-beam cancer therapy](https://www.nature.com/articles/srep27654)

## How Probability and Stochastic Process is involved?
* Modeling of physical/real-time uncertain Problem, Study of any existing probability based models etc., MSA has an advantage over LQ that it can predict quantitatively survival chances of cells in a tumor theoretically. LQ model took into consideration only dose given whereas MSA includes biological factors like genome size of cell, conversion of SSBs to DSBs, number of base pairs and physical factors as well like energy of the ion beam. The main parameter for calculating the probability of cell survival is damage yield. This yield is derived by calculating the number of lethal lesions in the tumors which follows Poisson distribution.
* Yl = (π/16)σNg(1/Se)d 
  * Yl is number of lethal lesions 
  * Ng is the genome size 
  * Se is the stopping potential 
  * d is the dose
* Finally, a parameter χ , is introduced which is the probability of successful repair of a lesion. The probability of cell survival is certainly not purely exponential and there is a deviation up to certain quantity of dose up to which cell repair is possible, after which the relation follows a purely exponential behavior(Check the refference).
## Eloboration of Code with respect to Probability and Stochastic Process: 
* We showed the decreasing exponential nature of cell survival and also derived the increasing exponential damage that is done as we increase the dose. The cell Survival and Cell Damage are both plotted against dose and both Yield desired Exponential Results as dose is directly proportional to Yield.
* We were given one method to calculate the Survival Curve. We enhanced the Method to derive results for All the 6 Cell Lines that were described in the Paper We Moreover derived the Values of Yield and then iterated to tweak the method and derive more accurate and informative results. We also used other methods to derive parameters that were directly provided to us hence making the code more comprehensive.
* We showed the deviation in the same curve by Changing the LET Values in Accordance with OER Ratio and then we Plotted to show the change from the Normal Curve.
* We used the Poisson PMF to show the cell repair which is given as a formula to show the cell repair and the deviation that is caused by the Hypoxic Conditions and this was illustrated by Poisson PMF Modelling which is Modelling the Uncertainty of Cell Repair in this Case.
* The same set of results have been able to provide Justification for the LQ model that has been a semi empirical model and the results of MSA are pretty much Similar when Shouldered to LQ.
* We have implemented a functionality from the user perspective of a medical professional/doctor where inputs are Cell Line and LET . The output gives a value for dose after which there is no cell repair and also gives the user an idea after what dose there are no chances of repair.

## Innovations derivied using concepts of Probability and Stochastic Process: 
1.  By making the dose time dependent and by increasing the dose in a linear fashion, we observed a significant decrease in relative cell survival. As we have decreased the dose in a pattern 0.96, 0.93, 0.90, 0.88, 0.85(3/(3+i/10) ; i=1,2,3,4,5) as parameters. We assumed a linear relation between dose and time that implies dose is directly proportional to time. Making dose time dependent we also found the exponential nature of survival curves which suffice the inclination of curves towards Linear quadratic equation and multiscale approach. We took a total time interval of 8 minutes and 1 minute is divided into 100 fractions which makes the plot more efficient.
2. We have implemented a small innovation that helps the doctors to estimate the number of Double Strand Breaks caused per cell and also the number of DSBS caused per particle.
3. We have given the doctor the function to input the cell line and the LET to estimate at what dose there will be 0 cell repair. This will help the medical professional in planning dosage for the treatment for optimal efficacy.

## Enumerate the inferences derived from user-centric perspective: 
* MSA takes into consideration key biological factors to calculate survival chances of cells in a tumor. Hence, this approach can be extended to predict radiobiological effects of other cell lines as well. The graph of survival fraction with dose helps the user decide the quantity of the dose to be given, adjust the energy of the ion beam in accordance with the area of tumor. This will also help users to determine the relationship between various biological parameters such as genome size, number of base pairs and physical factors like energy. Researchers can try to study these relationships and build up further theories of MSA.
  1. We can observe that Chi1 (X1) is negatively proportional to Cell Repair Function. Which makes it Negatively Proportional to the Cell Survival. This means that larger the value of CHi1(X1), lesser will be the Cell Repair. This means that the Surviving Fraction will decrease when we increase the value of CHI1(X1).
  2. We also observe that CHI0(X0) is directly proportional to the Cell Repair Function. Which means a larger value of CHI0(X0) will result in a larger cell repair which in turn will increase the surviving fraction of cells.
  3. By making the dose time dependent and by increasing the dose in a linear fashion, we observed a significant decrease in relative cell survival. cell repair which in turn will increase the surviving fraction of cells.
  4.  From Our Small Innovations part we derive that there exists a dose value after which cell repair is 0 which is mentioned as the critical value. So we derive the Critical Value for the input of Se and Cell Line. This Critical Value might be of some help in dose planning as doctor firsthand knows about the value of dose after which there is no chance of cell repair.

#### Note
* Innovation part is with respect to the given Reference
* Data used in code is random please do not drive any inference using it.
