SDST-FJSSP <br />

This is the new library of instances for the Flexible Job Shop Scheduling Problem (FJSSP) with Sequence-Dependent Setup Time (SDST). This library is based on the classical FJSSP [1] [2] [3] [4] [5] [6], and consists of 342 instances divided into 6 groups according to the author. We have from 2 jobs and 2 machines up to 30 jobs and 18 machines. These instances have been modified by including the SDSTs in compliance with the triangular inequality theorem [7], with a uniform distribution from zero to the average time of the processing times of each instance. All details can be found in [8].<br />


[1] P. Brandimarte. Routing and Scheduling in a Flexible Job Shop by Tabu Search. Annals of Operations Research, 41(3):157–183, 1993. https://doi.org/10.1007/BF02023073<br />
[2] J. Hurink, B. Jurisch, and M. Thole. Tabu Search for the Job-Shop Scheduling Problem with Multi-Purpose Machines. OR Spektrum, 15(4):205–215, 1994. https://doi.org/10.1007/BF01719451<br />
[3] S. Dauzère-Pérès and J. Paulli. An Integrated Approach for Modeling and Solving the General Multiprocessor Job-Shop Scheduling Problem Using Tabu Search. Annals of Operations Research, 70:281–306, 1997. https://doi.org/10.1023/a:1018930406487<br />
[4] I. Kacem, S. Hammadi, and P. Borne. Pareto-Optimality Approach for Flexible Job-Shop Scheduling Problems: Hybridization of Evolutionary Algorithms and Fuzzy Logic. Mathematics and Computers in Simulation, 60(3-5):245–276, 2002. https://doi.org/10.1016/S0378-4754(02)00019-8<br />
[5] J. B. Chambers and J. W. Barnes. Flexible Job Shop Scheduling by Tabu Search. The University of Texas, Austin, TX, Technical Report Series ORP96-09, Grad- uate Program in Operations Research and Industrial Engineering, 1996. <br />
[6] P. Fattahi, M. S. Mehrabad, and F. Jolai. Mathematical Modeling and Heuristic Approaches to Flexible Job Shop Scheduling Problems. Journal of Intelligent Manufacturing, 18(3):331–342, 2007. https://doi.or/g10.1007/s10845-007-0026-8<br />
[7] Christian Artigues and Dominique Feillet. A branch and bound method for the job-shop problem with sequence-dependent setup times. Annals of Operations Research, 159(1):135–159, 2008. ISSN 02545330. doi: https://doi.or/10.1007/s10479-007-0283-0.<br />
[8] Working paper.<br />

The new instances follow the following format:<br />

-in the first line there are 3 numbers: the first is the number of jobs , the second the number of machines, and the 3rd number, it is the average number of machines per operation.<br />

-Every row represents one job: the first number is the number of operations of that job, the second number (let's say k>=1) is the number of machines that can process the first operation; then according to k, there are k pairs of numbers (machine,processing time) that specify which are the machines and the processing times; then the data for the second operation and so on.<br />

-After the job information continue the matrices per machine of size jobs x jobs. Each matrix indicates the setup time from job j(row) to job x(column) on machine i(matrix).<br />


Example: Fattahi11<br />

5 6 2.2<br />
3 3 1 147 2 123 3 145 2 4 140 2 130 2 4 150 5 160<br />
3 2 1 214 3 150 2 3 87 2 66 2 5 178 6 95<br />
3 2 1 87 2 62 2 3 180 4 105 3 4 190 5 100 6 153<br />
3 2 1 87 2 65 1 5 173 2 4 145 6 136<br />
3 3 2 123 3 145 1 128 3 3 86 4 65 5 47 2 5 110 6 85<br />
0  77  75  82  46  <br />
71  0  79  55  85  <br />
101  107  0  50  40  <br />
72  104  62  0  94  <br />
88  81  95  80  0  <br />

first row = 5 jobs and 6 machines 2.2 machine per operation<br />
second row = job 1 has 3 operations, the first operation can be processed by 3 machines that is machine 1,2 y 3 with processing times of 147,123 y 145 correspondingly.<br />
sixth row = matrix of the setup times of machine 1, with 6 rows and 6 columns, representing the jobs.  For each machine there is a matrix of setup times.<br />

--<br />
Jhoan Arley Duque Otabo<br />
M.Sc. Student<br />
Pontificia Universidad Javeriana Cali, Colombia<br />
jhoanduque1@javerianacali.edu.co <br />