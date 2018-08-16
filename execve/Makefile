all: clean execve

execve:
	gcc show_info.c -o show_info
	gcc do_execve.c -o do_execve

clean:
	rm -f *.o *.exe *.out
	rm -f do_execve show_info
