.PHONY= doc clean

CC=g++
OPTIONS= -g 
DEBUG= #-D DEBUG
LIBDIR=lib
INCLUDEDIR=include
_OBJ= tcalendario.o tvectorcalendario.o tlistacalendario.o 
OBJ = $(patsubst %,$(LIBDIR)/%,$(_OBJ))

#tad:    src/tad.cpp $(OBJ)
#	$(CC) $(OPTIONS) $(DEBUG) -I$(INCLUDEDIR) src/tad.cpp $(OBJ) -o tad

#$(LIBDIR)/%.o : $(LIBDIR)/%.cpp $(INCLUDEDIR)/%.h
#	$(CC) $(OPTIONS) $(DEBUG) -c -I$(INCLUDEDIR) -o $@ $<

main:    src/main.cpp $(OBJ)
	$(CC) $(OPTIONS) $(DEBUG) -I$(INCLUDEDIR) src/main.cpp $(OBJ) -o main

#$(LIBDIR)/%.o : $(LIBDIR)/%.cpp $(INCLUDEDIR)/%.h
#	$(CC) $(OPTIONS) $(DEBUG) -c -I$(INCLUDEDIR) -o $@ $<

lib/tcalendario.o : lib/TCalendario.cpp include/TCalendario.h
	$(CC) $(OPTIONS) $(DEBUG) -c -I$(INCLUDEDIR) -o $@ $<

doc:
	doxygen

clean:
	rm -f $(OBJ) 