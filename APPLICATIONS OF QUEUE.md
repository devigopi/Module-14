# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
Given n processes with their burst times, the task is to find average waiting time and average turn around time using FCFS scheduling algorithm. First in, first out (FIFO), also known as first come, first served (FCFS), is the simplest scheduling algorithm. 
Here we are considering that arrival time for all processes is 0. How to compute below times in Round Robin using a program?

---

### ALGORITHM  

1. Start the program.  
2. Initialize variables
   Create array rem_bt[] (remaining burst time) and copy all burst times into it.
   Create arrays:
   wt[] → waiting time
   tat[] → turnaround time
   Set all waiting times = 0 initially.
   Set time = 0 → system clock.
3. Loop until all processes are completed 
4. Compute Turnaround Time for each process
5. Compute Average Times  
6. End the program.

---

### PROGRAM  

```
def findWaitingTime(processes, n,bt, wt):

	# waiting time for
	# first process is 0
	wt[0] = 0

	# calculating waiting time
	for i in range(1, n ):
		wt[i] = bt[i - 1] + wt[i - 1]

# Function to calculate turn
# around time
def findTurnAroundTime(processes, n,bt, wt, tat):

	# calculating turnaround
	# time by adding bt[i] + wt[i]
	for i in range(n):
		tat[i] = bt[i] + wt[i]

# Function to calculate
# average time
def findavgTime( processes, n, bt):

	wt = [0] *n
	tat = [0] *n
	total_wt = 0
	total_tat = 0

	# Function to find waiting
	# time of all processes
	findWaitingTime(processes, n, bt, wt)

	# Function to find turn around
	# time for all processes
	findTurnAroundTime(processes, n,bt,wt,tat)

	# Display processes along
	# with all details
	print( "Processes Burst time " +" Waiting time " +" Turn around time")

	# Calculate total waiting time
	# and total turn around time
	for i in range(n):
	
		total_wt = total_wt + wt[i]
		total_tat = total_tat + tat[i]
		print(" " + str(i + 1) + "   " +str(bt[i]) + "  " +str(wt[i]) + "    " +str(tat[i]))

	print( "Average waiting time = "+str(total_wt / n))
	print("Average turn around time = "+str(total_tat / n))

# Driver code
if __name__ =="__main__":
	
	# process id's
	processes = [ 1, 2, 3]
	n = len(processes)

	# Burst time of all processes
	t0=int(input())
	t1=int(input())
	t2=int(input())
	burst_time = [t0,t1,t2]

	findavgTime(processes,n, burst_time)



```

### OUTPUT
<img width="1213" height="417" alt="image" src="https://github.com/user-attachments/assets/4344ba6b-960a-4144-bc4e-45643cf52ecb" />


### RESULT
   The Round Robin scheduling program successfully computes the waiting time and turnaround time for all processes by repeatedly allocating the fixed time quantum to each process in cyclic order until every process completes, and then calculates the average waiting time and average turnaround time using the final computed values is successfully verified.
   

