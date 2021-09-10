

app = main
lib = libcat.so libdog.so

CFLAGS = -Wall -ansi -pedantic
LDFLAGS = -ldl

all: $(lib)
	$(CC) main.c  $(CFLAGS) $(LDFLAGS) -o main

lib%.so: %.c
	$(CC) -shared -fPIC $(CFLAGS) -o $@ $<

clean:
	$(RM) $(app) $(lib)

run: all
	./$(app) cat
	./$(app) dog
	-./$(app) bear

$(lib): animal.h
