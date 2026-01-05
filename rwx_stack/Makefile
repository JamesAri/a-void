# Makefile

CC = gcc
# make stack executable, set older compiler so gets compiles
CFLAGS = -z execstack -std=gnu89

build: main.o 
	$(CC) $(CFLAGS) -o vuln main.o 

main.o: main.c
	$(CC) $(CFLAGS) -c main.c

clean:
	rm -f *.o vuln

