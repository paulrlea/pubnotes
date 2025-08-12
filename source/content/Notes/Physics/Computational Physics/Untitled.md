## 3. Pseudo-random numbers

  

### In-class exercises

  

1. One isotope of thallium ($^{208}Ti$) has a half-life $t_{1/2}$ =3.053 minutes, decaying to $^{208}$Pb. You will write a simple for loop using pseudo-random numbers to track the populations of $^{208}$Tl and $^{208}$Pb in a sample over 1,000 seconds, starting with 1,000 atoms of $^{208}$Tl and 0 atoms of $^{208}$Pb.

  

The probability of decay in a time interval dt is $p=1-e^{-dt/\lambda}$ where $\lambda=t_{1/2}$/log2. Set dt=1, and at each step, evaluate the probability that each $^{208}$Tl atom decays by creating an array of random numbers from 0 to 1 whose length is the number of $^{208}$Tl atoms (use `rng.random`). For each atom, it will decay if the random number generated, $n<p$. You’ll need to have two arrays to store the populations for Tl and Pb atoms at each step. (Use `np.where` as described in the notes.)

At each timestep, sum over the number of atoms that do decay (using `np.sum` on the result of the `np.where` call), and use this number to update the total number of thallium and lead atoms. Make a plot of the number of atoms of each species against time.