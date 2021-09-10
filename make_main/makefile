# http://www.gnu.org/software/make/manual/html_node/Automatic-Variables.html
# $@：current target
# $^: all the prerequisites (dependencies)
# $<：current prerequisite
# $?：rebuild-required prerequisite

CC = gcc
CFLAGS = -Wall -pedantic -O2 -std=c99 
exe = main
obj = main.o add.o sub.o

all: $(obj) 
	$(CC) -o $(exe) $(obj)  

%.o: %.c
	${CC} -c $^ -o $@

.PHONY: clean
clean:
	rm -rf $(obj) $(exe)