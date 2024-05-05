# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:

## C Program to print process ID and parent Process ID using Linux API system calls

```


#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{	//variable to store calling function's process id
	pid_t process_id;
	//variable to store parent function's process id
	pid_t p_process_id;
	//getpid() - will return process id of calling function
	process_id = getpid();
	//getppid() - will return process id of parent function
	p_process_id = getppid();
	//printing the process ids

//printing the process ids
	printf("The process id: %d\n",process_id);
	printf("The process id of parent function: %d\n",p_process_id);
	return 0; }



```
## OUTPUT
![318005559-15c28aa0-5670-494a-b712-b36aa2dbf1d5](https://github.com/Goutham2306/Linux-Process-API-fork-wait-exec/assets/138971154/5a6092b4-04f7-4132-bf0e-9a281943a418)



## C Program to create new process using Linux API system calls fork() and exit()
```
//C Program to create new process using Linux API system calls fork() and exit()
#include <stdlib.h>
#include <sys/wait.h>
#include<stdio.h>
#include<unistd.h>
#include <sys/types.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}

```
## OUTPUT
![318005539-9134c939-35d8-4ea7-aa05-ede6f1bd49fe](https://github.com/Goutham2306/Linux-Process-API-fork-wait-exec/assets/138971154/aecebe0f-0bf9-4170-933a-eb3968582a62)

 
## C Program to execute Linux system commands using Linux API system calls exec() family
```
//C Program to create new process using Linux API system calls fork() and exit()
#include <stdlib.h>
#include <sys/wait.h>
#include<stdio.h>
#include<unistd.h>
#include <sys/types.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}

```

## OUTPUT
![318005585-662799cb-b088-4a2a-894d-4cbba685d1e2](https://github.com/Goutham2306/Linux-Process-API-fork-wait-exec/assets/138971154/8a69b592-b5da-4a3a-98ed-a805ccdfb889)

## RESULT:
The programs are executed successfully.























