## Determining cement porewater pH from total alkalinity titration
Accurate measurement of the pH of cement porewater solutions is difficult without highly specialized pH probes and where carbonation on contact with the atmosphere cannot be prevented. Alkalinity titration provides a crude measure of pH, however, when combined with speciation modelling is able to provide an accurate measure, since hydroxide complexes and carbonation products are accounted for. 

Total alkalinity in these solutions is primarily due to hydroxide ions with contributions from hydroxide complexes and carbonates. Ion pairs, such as KOH, NaOH, and CaOH<sup>+</sup>, provide the main additional contribution. Mineral hydroxides that can protonate, such as silicates, aluminates, ferric hydroxides, are present in much lower concentrations. Carbonate is present in negligible concentrations prior to porewater extraction since it is controlled by CaCO<sub>3</sub> solubility.

During and following extraction from cement, the expressed porewater comes into contact with atmospheric CO<sub>2</sub> unless specialized procedures that shroud the sample in an inert gas are used. The high pH of the porewater solution drives rapid absorption of CO<sub>2</sub> which reacts with hydroxide to form carbonate. 

CO<sub>2</sub> + 2OH<sup>-</sup> --> CO<sub>3</sub><sup>2-</sup> + H<sub>2</sub>O

This process does not change the total alkalinity since the formed carbonate reacts with the same amount of acid that the neutralized hydroxide would have.

Speciation modelling of the porewater, in a package such as Phreeqc, is undertaken using the elemental analyses (typically ICP-OES) and an estimated pH value (from the total alkalinity titration). The pH value is adjusted in an iterative manner until the modelled value for total alkalinity equals the measured value. This slow and tedious procedure can be automated by undertaking virtual titrations of the solution using a python wrapper for IPhreeqc called Phreeqpython (Vitens) in combination with an optimization algorithm (SciPy) where the pH value is optimized to minimise the difference between the modelled and measured total alkalinity.