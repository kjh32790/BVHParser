LINK_TARGET = MotionCapture

OBJS = glad.o MotionCapture.o

REBUILDABLES = $(OBJS) $(LINK_TARGET)

INCLUDES = -I/usr/local/include

all : $(LINK_TARGET)
	echo All successfully linked!

$(LINK_TARGET) : $(OBJS)
	g++ -o $@ $^ -L/usr/local/lib -lglfw.3.2 $(INCLUDES)

MotionCapture.o : MotionCapture.cpp
	g++ -c MotionCapture.cpp $(INCLUDES)

glad.o : glad.c
	g++ -c glad.c $(INCLUDES)

clean :
	rm -f $(REBUILDABLES)
	echo Clean done!

#Header files should not be compiled! (g++ -c (NON HEADER FILES HERE!)). (The header codes are 'included' by preprocessors anyway!!!) However, if header is in a different path, it should be given where it is via the option -I. Linking the library(-lglfw3.2) and library path should be given in the last step when you link together all .o files!
