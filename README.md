# Priority_sheduling_in_pintos

Analysing scheduling algorithms, deeply studying and implementing  priority scheduling in pintos.Download the pintos.

Follow this steps for running the code compiled-
#A. Compiling Pintos
	1. sudo apt-get install qemu
	2. Download Pintos. Extract it in some directory say $HOME/os-pg/
	3. Open the script ‘pintos-gdb’ (in $HOME/os-pg/pintos/src/utils). Find GDBMACROS and set it to point to ‘$HOME/os-pg/pintos/src/misc/gdb-macros’.
	4. $ cd $HOME/os-pg/pintos/src/utils; $make
	5. Open the file “$HOME/os-pg/pintos/src/threads/Make.vars” and change the last line to: SIMULATOR = –qemu
	6. $ cd $HOME/os-pg/pintos/src/threads/; $ make
	7. In “$HOME/os-pg/pintos/src/utils/pintos” :
		a. Change line no. 103 to “$sim = “qemu” if !defined $sim;” to enforce qemu as simulator
		b. On line no. 257, replace “kernel.bin” to path pointing to kernel.bin file at “$HOME/os-pg/pintos/src/threads/build/kernel.bin”.
	8. Open “$HOME/os-pg/pintos/src/utils/Pintos.pm” and replace “loader.bin” at line no. 362 to “$HOME/os-pg/pintos/src/threads/build/loader.bin”
	9. export PATH=$HOME/os-pg/pintos/src/utils:$PATH
	10.$ cd $HOME/os-pg/pintos/src/utils/; $ pintos run alarm-multiple
	(Note: Replace $HOME by your home directory path in every step)

#B. Hello in Pintos
	1. make clean in $HOME/os-pg/pintos/src/threads/
	2. make
	3. pintos run alarm-hi

#C.Replacing files
Now replace all files in the edited files folder with the corresponding files in pintos.eg-:replace the orignal thread.c file of pintos with the file new thread.c file containg in edited files folder.Similarly replace all the files in edited files folder. 

#D.Running the c codes
Compile C code, based on test cases file(c codes folder contains all the c codes of three scheduling algorithms)
	1. FCFS (no of process, arrival time, burst time)
	2. Preemptive Priority Scheduling (no of process, arrival time, burst time, priority)
	3. SJF (no of process, arrival time, burst time)
		Note the average Turnaround and waitng time for each test case for all three sheduling algorithms and analyse them by plotting graph.

#E. Testing 
Test cases in Pintos(to check if priority sheduling is implemented or not)
	1. pintos run priority-change
	2. pintos run priority-preepmt
	3. pintos run priority-sema 

#There is a project report which briefly explains the project 

