# Train_Scheduling_Problems
Test problems for the non-periodic train scheduling problem.

This library is originally created for the following paper:

Barah, M., Seifi, A., & Ostrowski, J. (2019). Decomposing the Train-Scheduling Problem into Integer-Optimal Polytopes. Transportation Science.

Problem sets are categorized based on the number of stations (S) and the number of trains (TN). For instance directory "S,10,TN,12" contains those problems with 10 stations and 12 trains. Note that all instaces assume a single track connecting two consecutive stations.

Each directory has a file titled "GlobalInputParameters.txt" which contains information about the network infrastructure. The structure of the infrastructure data is as follows:

Line 1: The total number of blocks, including stations and the tracks connecting the stations;

Line 2: The maximum number of stations;

Line 3: The trains' dispatching ticket (in minutes), i.e., the length of the time interval during which the train can begin from its origin;

Line 4: The planning horizon of scheduling (in minutes);

Line 5: The minimum headway time (in minutes) between two consecutive trains that traverse a track in the same direction;

Line 6: The minimum headway time (in minutes) between two consecutive trains that traverse a track in opposite directions.

Each train data is stored in a file titled "T-i.txt," where "i"  denotes the train number. The structure of the train data is as follows:

Line 1: The train's origin (block number);

Line 2: The train's destination (block number);

Line 3: The earliest time at which the train can depart its origin;

Line 4: The latest time at which the train can depart its origin;

Line 5: The maximum profit of a travel arc that is associated with the travel arc representing the earliest possible track traversing time;

Line 6: The incremental penalty for the travel arc other than the earliest travel arc at each track;

Line 7: The penalty of waiting arcs at stations (the weight of waiting arcs at stations). Note that dwell arcs take zero weight;

Line 8: The sequence that denotes trains traverse and dwell times. The numbers at even positions denote the expected track travel times, whereas the numbers at odd positions denote the minimum dwell time at stations. 


Finally, the file titled "TrainCombinations.txt" is the combination of trains (train numbers): Each line of the file denotes a test problem. 

For more information, please refer to the paper. Please cite the library as well as the paper if you want to use the test problems in your research.
