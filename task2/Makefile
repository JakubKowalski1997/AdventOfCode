CXX=g++
CXXFLAGS+=-g
CXXFLAGS+=-Wextra
CXXFLAGS+=-pedantic
CXXFLAGS+=-Wall
MAIN=Array
SRC=$(wildcard *.cpp)
OBJ=$(SRC:.cpp=.o)

all: $(MAIN)

$(MAIN): $(OBJ)
		$(CXX) $? -o $@

$(OBJ): $(SRC)
		$(CXX) $(CXXFLAGS) -c $*.cpp -o $@

.PHONY: clean run backup cB

clean:
	rm -f $(MAIN) $(OBJ)

run: $(MAIN)
	./$(MAIN)

backup:
	if [ -d "./backup" ]; then rm -r backup; fi
	mkdir backup
	cp $(SRC) backup
	cp *.h backup

cB:
	rm -r backup
