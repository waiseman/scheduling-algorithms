# scheduling-algorithms
CPU Process Scheduling algorithms in C++


#First Come First Serve Algorithm

Step 1: Start the process
Step 2: Accept the number of processes in the ready Queue
Step 3: For each process in the ready Q, assign the process name and the burst time Step
Step 4: Set the waiting of the first process as =0‘and its burst time as its turnaround time Step
Step 5: for each process in the Ready Q calculate
	a). Waiting time (n) = waiting time (n-1) + Burst time (n-1) 
	b).Turnaround time (n)= waiting time(n)+Burst time(n) 
Step 6: Calculate
	a) Average waiting time = Total waiting Time / Number of process 
	b) Average Turnaround time = Total Turnaround Time / Number of process                                     
Step 7: Stop the process 


Round Robin Scheduling


Get the number of process and their burst time.
 Initialize the array for Round Robin circular queue as ‘0’.
The burst time of each process is divided and the quotients are stored on the round Robin array.
 According to the array value the waiting time for each process and the average time are calculated as line the other scheduling.
The waiting time for each process and average times are displayed.
 Stop the program.
 
 
 Setps:
 
 1- Create an array rem_bt[] to keep track of remaining
   burst time of processes. This array is initially a 
   copy of bt[] (burst times array)
2- Create another array wt[] to store waiting times
   of processes. Initialize this array as 0.
3- Initialize time : t = 0
4- Keep traversing the all processes while all processes
   are not done. Do following for i'th process if it is
   not done yet.
    a- If rem_bt[i] > quantum
       (i)  t = t + quantum
       (ii) bt_rem[i] -= quantum;
    c- Else // Last cycle for this process
       (i)  t = t + bt_rem[i];
       (ii) wt[i] = t - bt[i]
       (ii) bt_rem[i] = 0; // This process is over

 
