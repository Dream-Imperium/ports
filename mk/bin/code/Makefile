.POSIX:
.SUFFIXES:
.SUFFIXES: .c .o

all: dbman install list

dbman: dbman.o
	$(CC) $(LDFLAGS) -o $@ $< -lvanilla
install: install.o
	$(CC) $(LDFLAGS) -o $@ $< -lvanilla
list: list.o
	$(CC) $(LDFLAGS) -o $@ $< -lvanilla

.c.o:
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c $<

bootstrap: all
	mv dbman install list ..
