# cse6220-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [CSE6220 Assignment 1 Solved](https://www.ankitcodinghub.com/product/cse6220-programming-assignment-1-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;126783&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE6220  Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
1 Problem Statement

Write a parallel program in C/C++ to estimate the value of π using the Monte Carlo method specified below. The program should take n as input, which is the number of points to be used for the estimation. The program should then generate n random points in the unit square [0,1] × [0,1] and count the number of points that lie inside the unit circle.

Let n be a large integer, then estimated value of π is

4 · number of points in the circle

Figure 1: Estimating π using Monte Carlo method

2 Parallel Algorithm

The estimation can be easily parallelized by assigning each processor the responsibility for distinct points. You should use the following MPI functions:

• Have processor with rank 0 read n, and use MPI Bcast to broadcast it to all processors.

• Use MPI Reduce function to sum the number of points in the circle across all processors.

• Use MPI Wtime to time the run-time of the program (measure on processor 0).

For the random number generator, you can use the rand() function in C/C++. However, you should make sure that the random number generator is seeded differently for each processor. You can use the processor rank for this purpose. For example, if the rank of the processor is i, then you can use srand(time(NULL) + i) to seed the random number generator on that processor.

3 Code framework

3.1 Input &amp; Output Format

Your program should take n as the input using command line arguments and output the estimated value of π and the time taken to compute this value (comma-separated). For example, if the estimated value is s and the time taken is t, your output should be “s, t”. (Note: s should be printed up to 12 decimal points). All output is done through processor with rank 0.

3.2 Deliverables

1. Create a Makefile for your program, and make sure the name of your output executable is“pi calc”. If you are not familiar with creating Makefiles, check resources below for help.

2. Write a “README.txt” briefly describing how your program works and the machine you used for generating the results.

3. For n = 106, plot a graph of run-time of the program vs. the number of processors for a few chosen values of p. This run-time should include all computations that contribute to the estimation, including any local computations and global reductions. Include your graph and observation regarding the speedup in a PDF file with name “report.pdf”. Make sure to list names of all your teammates at the very beginning of your report.

4. Submit your a) “code.zip” in “Programming Assignment 1 – Code” on Gradescope. Your zip file should include all the .cpp files, Makefile and README.txt file; b) your report in “Programming Assignment 1 – Report” on Gradescope.

4 Resources

1. What is a Makefile and how does it work?: https://opensource.com/article/18/8/what-howmakefile

2. PACE ICE cluster guide: https://docs.pace.gatech.edu/ice cluster/ice-guide/. Documentation for writing a PBS script: https://docs.pace.gatech.edu/software/PBS script guide/
