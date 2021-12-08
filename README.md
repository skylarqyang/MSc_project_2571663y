# MSc_project_2571663y

This project addresses the question of whether the use of clustering techniques can improve the performance of random pilot assignment (RPA) schemes in the Cell-free Massive MIMO system. And the project is conducted and developed on the basis of the RPA implementation (original file see Full.m) provided by Abdulrahman AI Ayidh (PGR) from the School of Engineering, University of Glasgow.

The project uses MATLAB_R2021b with Statistics and Machine Learning Toolbox to simulate the calculations. And all files are based on the small simulative data sample, specifically, with the number of access points being 40, the number of users being 8 and 5 available mutual orthogonal pilot sequences.

In this work, hierarchical clustering and K-means clustering are performed on access points (APs) to gain the AP clusters; and the prototype of user grouping is realized by random number generation, and then final user grouping is finished by weights calculation on potential pilot contamination (which is based on the result of AP clusters). Finally, the pilot assignment based on the previous results can be done. 

As shown in section 3.4 in the dissertation, this work also discusses the impact of random user assignment sequence and random pilot assignment sequence on the RPA combined with clustering techniques under different combinations:

A.	For RPA combining Hierarchical and RPA combining K-means, ONLY the random user assignment sequence RU is identical. 

B.	For RPA combining Hierarchical and RPA combining K-means, BOTH the random user assignment sequence RU and the random pilot assignment sequence RP are identical. 
C.	For RPA combining Hierarchical and RPA combining K-means, both the random user assignment sequence RU and the random pilot assignment sequence RP differs.

The comparison of the three schemes (RPA, RPA combined with hierarchical clustering, and RPA combined with K-means clustering) for each of the above three cases can be seen in the following files, namely, assumptionA.m, assumptionB.m and assumptionC.m.

Moreover, this work discusses the relationship between per-user net throughput and the number of APs/ pilots under three assumptions, and the detailed code can be seen in changeM.m and changetau.m. In both files, we used iterations to increase the values of the dependent variable. Specifically, we set five iterations for both, with an initial value of 40 for the number of APs, increasing by 40 for each iteration, and an initial value of 3 for the available pilot sequence, increasing by one for each iteration.

