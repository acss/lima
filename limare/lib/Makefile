TOP = ../../

include $(TOP)Makefile.inc

CFLAGS += -I$(TOP)include -fPIC

all: liblimare.so

OBJS = bmp.o fb.o plb.o hfloat.o symbols.o jobs.o dump.o gp.o render_state.o \
	pp.o program.o texture.o limare.o

clean:
	rm -f *.P
	rm -f *.o
	rm -f *.so

liblimare.so: $(OBJS)
	$(CC) -shared -Wall -o $@ $^ -lMali -lrt

install: liblimare.so
	$(INSTALL) liblimare.so $(prefix)/lib/
	$(INSTALL) limare.h $(prefix)/include/

include $(TOP)Makefile.post
