#	Makefile corresponding to BAM2HINTS
#	
# 	NOTE:
#	a) "-g" option allows for debugging
#	b) libbamtools.a and lz library are used during the linking process
#
# 	Created: 14-December-2011
#	Last modified: 14-December-2011

# Variable definition
# on greifweb1
BAMTOOLS = /home/sebastian/pezmaster31-bamtools-466bc50
INCLUDES = $(BAMTOOLS)/include
LIBS = $(BAMTOOLS)/lib/libbamtools.a -lz
SOURCES = bam2hints.cc 
OBJECTS = $(SOURCES:.cc=.o)
CFLAGS = -Wall -g

LINK.cc = g++

# Recipe(s)
# $@: full target name of current target. 
# $<: .c file of target. 
bam2hints : $(OBJECTS) 
	$(LINK.cc) $(CFLAGS) -o $@ $(OBJECTS) $(LIBS) 

all:$(OBJECTS) # Compiles each foo.cc into foo.o

bam2hints.o : $(SOURCES)
	$(LINK.cc) $(CFLAGS) -c $< -o $@ -I$(INCLUDES) 

clean: 
	rm -f $(OBJECTS)