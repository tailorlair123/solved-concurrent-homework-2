Download Link: https://assignmentchef.com/product/solved-concurrent-homework-2
<br>
The purpose of this project is to get you started doing parallel programming on a machine like Beocat.

<strong>Task(s)</strong>

Your first task is to take an existing program and indicate how the performance improves through using using two standard techniques – pthreads and OpenMP – to parallelize this serial code. Your second task is to do a performance evaluation across a range of iterations to see how the various versions match up in terms of run times, CPU efficiency, memory utilization, etc. You’ll want to keep the machines constant, so use the flag for sbatch to confine your jobs to only the ‘elf’ class nodes.

Parallelize the following code using OpenMP parallel and reduction directives. Ensure that your program prints the output and tracks and prints the time expended by the program.

const int NUM_ITER = 100000000;int i;double sum = 0.0, x = 0.0;double st = 1.0/((double) NUM_ITER);for(i = 0; i &lt; NUM_ITER; i++){x = (i + 0.25)*st;sum += 4.0/(x*x+1);}

Plot the CPU time expended by the serial version of the program and by running the program with 2, 4, 8, and 16 threads for both the pthreads and OpenMP versions (feel free to combine these into one graph). Note that the x axis of your plot should be threads used, and the y-axis of your plot should be time expended in seconds. Discuss the results. Are there any race conditions?

<strong>Resources</strong>

Pthreads – <a href="https://computing.llnl.gov/tutorials/pthreads/">https://computing.llnl.gov/tutorials/pthreads/</a>

OpenMP – <a href="https://computing.llnl.gov/tutorials/openMP/">https://computing.llnl.gov/tutorials/openMP/</a>




For help using the Beocat scheduler and its command lines, see the general help page

<a href="https://support.beocat.ksu.edu/BeocatDocs/index.php/Main_Page">https://support.beocat.ksu.edu/BeocatDocs/index.php/Main_Page</a>







Compute node specifications are at

<a href="https://support.beocat.ksu.edu/BeocatDocs/index.php/Compute_Nodes">https://support.beocat.ksu.edu/BeocatDocs/index.php/Compute_Nodes</a>




You will probably need to install a shell program on your Windows machine – I use PuTTY, and program to transfer files back and forth (I use WinSCP, but other options are fine). Linux and Mac OS have terminal and file transfer programs installed by default.