CPP			= g++
CPPFLAGS		= -Wall -c -I. -O2 -flto -std=c++11 -g
LD			= g++
LDFLAGS			= -lamqpcpp -lev -lreactcpp
RESULT			= a.out
SOURCES			= $(wildcard *.cpp)
OBJECTS			= $(SOURCES:%.cpp=%.o)

all:	${OBJECTS} ${RESULT}

${RESULT}: ${OBJECTS}
	${LD} -o $@ ${OBJECTS} ${LDFLAGS}

clean:
	${RM} *.obj *~* ${OBJECTS} ${RESULT}

${OBJECTS}:
	${CPP} ${CPPFLAGS} -o $@ ${@:%.o=%.cpp}

