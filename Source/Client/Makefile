#CC=..\bcc\bin\bcc32
CC=gcc
#OPT=-O2 -5 -d -ff -k- -OS -Q -X
#MODEL=-W -WM
#CFLAGS=-I..\bcc\include -Izlib $(OPT) $(MODEL)
CFLAGS = -O2 -Wall -I/usr/include/SDL2 -D_REENTRANT
#LDFLAGS=-L..\bcc\lib -Llpng -Lzlib -L.\bcc\lib\psdk -W -WM -M
LDFLAGS = -lSDL2 -lpng -lz -lm

OBJS = dd.o engine.o main.o inter.o socket.o sound.o conv.o options.o
TARGET=openMerc-client

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) -o $@ $(OBJS) $(LDFLAGS)

# Pattern rule to compile .c to .o
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)



#merc.exe:       dd.obj engine.obj main.obj inter.obj socket.obj sound.obj conv.obj options.obj makefile merc.res merc.def
#        ..\bcc\bin\ilink32 /aa -L..\bcc\lib -Llpng -Lzlib -L..\bcc\lib\psdk ..\bcc\lib\c0w32.obj dd.obj engine.obj main.obj inter.obj socket.obj sound.obj conv.obj options.obj,merc.exe,,cw32mt.lib import32.lib zlib.lib libpng.lib ddraw.lib dsound.lib,merc.def,merc.res

#merc.res:       merc.rc merc.rh
#        ..\bcc\bin\brcc32 merc.rc

#socket.obj:     socket.c common.h inter.h

#main.obj:       main.c common.h inter.h

#clean:
#        del *.obj
#        del merc.exe

