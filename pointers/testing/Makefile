NAME = learning
VERSION = 0.0.1
PREFIX ?= $(HOME)/.local

CC ?= gcc
CFLAGS = -Wall -Wextra -Werror -pedantic -Wno-unused-parameter

SRC = lib/ds.c src/main.c
OBJ = ds.o main.o
INCLUDE = -Iinclude

all: $(NAME)

$(NAME): $(OBJ)
	$(CC) $(OBJ) -o $(NAME) $(CFLAGS) $(INCLUDE)

ds.o: lib/ds.c
	$(CC) -c $< -o $@ $(CFLAGS) $(INCLUDE)

main.o: src/main.c
	$(CC) -c $< -o $@ $(CFLAGS) $(INCLUDE)

run: $(NAME)
	./$(NAME)

clean:
	rm $(OBJ)
	rm $(NAME)
