all: myapp

# Which compiler
CC = gcc

# Where are include files kept
INCLUDE = .

# Options for develpoment
CFLAGS = -g -Wall -ansi

# Options for release
# CFLAGS = -O -Wall -ansi

# Local Libraries
MYLIB = mylib.a

myapp: a.o b.o c.o $(MYLIB)
	$(CC) -o myapp a.o b.o c.o $(MYLIB)

$(MYLIB): $(MYLIB)(b.o) $(MYLIB)(c.o)
a.o: a.h b.h c.h a.c
b.o: b.c b.h c.h
c.o: c.c a.h c.h

clean:
	rm -f *.o myapp $(MYLIB)
