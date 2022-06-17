.PHONY: all clean
CC = g++
CFLAGS = -Wall -Wextra -std=c++11 -g
LDFLAGS = -lpthread
SRC = $(wildcard *.cpp)
OBJ = $(SRC:.cpp=.o)
BIN = $(SRC:.cpp=)

all: $(BIN)
	mkdir -p bin
	-mv $(BIN) bin
	-rm -f $(obj)
$(BIN): %:%.o
	-$(CC) -o $@ $^
$(OBJ): %.o:%.cpp
	$(CC) $(CFLAGS) $(LDFLAGS) -c $^ -o $@

clean:
	rm -f $(BIN) $(OBJ)