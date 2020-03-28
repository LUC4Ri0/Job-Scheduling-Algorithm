# Operating-System-Assingment
C Program for implementing Scheduling Algorithm
PROBLEM IDENTIFICATION:
Sudesh Sharma is a Linux expert who wants to have an online system where he can handle student queries. Since there can be multiple requests at any time he wishes to dedicate a fixed amount of time to every request so that everyone gets a fair share of his time. He will log into the system from 10am to 12am only. He wants to have separate requests queues for students and faculty, where faculty queue is given a higher priority. Implement a strategy for the same. The summary at the end of the session should include the total time he spent on handling queries and average query time.

DESCRIPTION (PURPOSE OF USE):
The given problem is based upon solving queries of persons of different classes i.e. Faculty and Students. Thus, these queries can be compared to different processes in terms of operating system where each process has its demands and needs resources and time for its execution. And this demands of processes are handled by the CPU. In the given scenario, Mr. Sudesh Sharma, Linux expert, can be considered as a CPU, who solves the queries of either Faculty or Student by allocating proper resources to their individual demands and processing them by allocating them time accordingly. Now, Mr. Sharma, wants to provide priority for each query based upon its class, as well as, he wants to dedicate a fixed amount of time to every request. Thus in Operating System, if we divide the requests into two separate queues i.e. Faculty and Student such that the first queue contains faculty queries has higher priority and the second contains student queries which has lower priority, then we can resolve the problem, by allocating them required resources based upon their priorities as done in the scheduling algorithm in operating systems.

EXPLAINATION:
1.	Round Robin is the preemptive process scheduling algorithm.
2.	Each process is provided a fix time to execute, it is called a quantum.
3.	Once a process is executed for a given time period, it is preempted and other process executes for a given time period.
4.	Context switching is used to save states of preempted processes.
Example: Assume there are 5 processes with process ID and burst time given below PID Burst Time P1 6 P2 5 P3 2 P4 3 P5 7 – Time quantum: 2 – Assume that all process arrives at 0. Now, we will calculate average waiting time for these processes to complete. Solution – We can represent execution of above processes using GANTT chart as shown below –
Explanation: – First p1 process is picked from the ready queue and executes for 2 per unit time (time slice = 2). If arrival time is not available, it behaves like FCFS with time slice. – After P2 is executed for 2 per unit time, P3 is picked up from the ready queue. Since P3 burst time is 2 so it will finish the process execution at once. – Like P1 & P2 process execution, P4 and p5 will execute 2 time slices and then again it will start from P1 same as above. Waiting time = Turn Around Time – Burst Time P1 = 19 – 6 = 13 P2 = 20 – 5 = 15 P3 = 6 – 2 = 4 P4 = 15 – 3 = 12 P5 = 23 – 7 = 16 Average waiting time = (13+15+4+12+16) / 5 = 12

ALGORITHM:
1.	Initially create Instruction function for proper functioning 
2.	Create input function to enter total no of queries, quanta for process, and choose 1 for faculty and 2 for student, Enter Job Type (1/2), query id, arrival time, correct time, resolving time.
3.	Create merger function to merge the values of job of the faculty according to the student data.
4.	After that we create roundRobin function, in this we take variable time, mark, cc and rc. Using while loop having condition time! = 120 and cc! = mc and in this we check quanta is greater than m array element then we increment time with quanta. We take start = mark+1 and check till less than mc and also, we increment value of mark if time is greater than m array element.
5.	 Create printer function in this we do printing of Summary for the execution. We print Query id, arrival time, resolving time, completion time, turn around time and waiting time. Also, we print average query time and process execution.
6.	In main we call the instruction function, input (), merger (), roundRobin(), printer() function for function of program.

COMPLEXITY:
• Complexity of initialization of variables is O(1). In input function the complexity if O(N) for taking input. Complexity of merger function is O(N^2). In roundRobin, Complexity is O(N^2) and in printer function complexity is O(N).
