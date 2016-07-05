Thank you to all four reviewers for taking the time to read our
paper. Here is a summary of the comments we received and our response
to each of them

## @rcpaffenroth

* It is hard to see the role python plays in this paper
* Why are the libraries used
* why was python chosen
* lessons learned for other projects
* mathematical presentation is too low level for general audience

  These comments are similar to those from @sarostru.  We addressed
  those with a detailed reply and we also edited the manuscript in
  response.

## @certik

* How is the method better than cubic spline fitting
  - There is a simulation between the model and the data.  We don't
    have x,y data that we can fit a spline to.
* Why constant temperature
  - We have added text that explains and justifies modeling isentropic
    expansion.  The key is that there is not enough time for heat
    conduction.
* Legend in figure 6
  - Done
* Testing
  - Currently broken, will fix before conference

## @sarostru

* What are the contents of the paper
  - Abstract was reworded
* What will the reader learn from reading it
  - Abstract was reworded
* How does the MAP function exclude physically impossible functions
  - Updated description of the model
* How does this compare to standard algorithms
  - See @fraserphysics response
* How does fisher information impact stability
  - See @fraserphysics response
* Why are domain specific models needed
  - See @fraserphysics response
* Why is a complex EOS function needed
  - See @fraserphysics response 
* Why are parameterized cubic spline better than parameter based approaches from introduction
  - See @fraserphysics response
* Should PBX be used
  - See @fraserphysics response
* Where are G and h defined
 - G and h express appropriate constraints.  We do not provide more
   detail in this paper, but we refer to the F_UNCLE code where we
   will provide the details.
    
## @kbarbary

* should p_p(\phi) be in the denominator
  - yes, corrected in paper
* should it be argmax(theta)
  - yes, corrected in paper
* move para 5 to be para 2
* remove reference to HPC
  - See @fraserphysics comments for @sarostru
* rework the SQP discussion to be simplified
  - Our estimate of the Fisher information drops a term in the second
    derivative with the justification that its expected value is
    small.  We believe that it's an important point.
* Say if there is anything novel about the optimization algorithm
  - Added brief discussion of the difference from SQP
* Make the paper less domain specific
  - See @fraserphysics comments to @sarostru,
* Describe why different optimization methods were used i.e. brentq
  - The big optimization searches for the MAP estimate.  Our code for
    that goal is ad hoc and we plan to improve it in future work.  We
    use cvxopt inside our main loop because it provides linearly
    constrained optimization of a quadratic objective.  We use brentq
    to solve for the implicitly defined CJ conditions and don't
    consider that optimization.
  



 
