CC = gcc
CFLAGS = -Iinclude -Wall
LDFLAGS = -L.

TARGET = lab2
LIB = libmylib.a

SRC = src/main.c
LIB_SRC = src/mylib.c

OBJ = $(SRC:.c=.o)
LIB_OBJ = $(LIB_SRC:.c=.o)

all: $(LIB) $(TARGET)

$(LIB): $(LIB_OBJ)
	ar rcs $@ $^

$(TARGET): $(OBJ) $(LIB)
	$(CC) $(CFLAGS) -o $@ $^ $(LDFLAGS)

clean:
	rm -f src/*.o $(LIB) $(TARGET)
