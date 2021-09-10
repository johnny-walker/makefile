# https://jasonblog.github.io/note/gunmake/makefilefan_li_jiao_xue.html
#all: add.so sub.so main 有順序問題要先編譯出so檔案在main , 所以main擺最後

CC = gcc
SOFLAGS = -shared -fPIC
LDFLAGS = -lm
CFLAGS = -Wall -pedantic -O2 -std=c99 

all: add.so sub.so main

main:
	${CC}  -o main  main.c -L./ -ladd -L./ -lsub ${CFLAGS} ${LDFLAGS} 

add.so: add.c
	$(CC) ${SOFLAGS} -o libadd.so $? 

sub.so: sub.c
	$(CC) ${SOFLAGS} -o libsub.so $? 

.PHONY: clean
clean:
	rm -f main *.so *.o