# sched_other_policy
handling many processes in pseudo-parallel way may have many advantages, but it also comes with a cost.
The kernel must keep track of the relevant data for many processes, and context switching itself is an operation that consumes some resources. 
Thus, it makes sense to let important, short, CPU-bound processes run without
interruption and avoid unnecessary context switches to the l/O bound processes .
In this project, I've added a new scheduling policy to the Linux kernel. The new policy, called SCHEDULE SHORT, is designed to support important short CPU bound processes and will schedule some of the processes running in the system according to a different scheduling algorithm that you will implement and which favors scheduling SCHEDULE SHORT policies almost uninterrupted by context
