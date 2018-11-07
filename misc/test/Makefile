NAME = basic
LIB = bloom
LIBFILE = libbloom.a
ROOT = /projects/libbloom
BUILD = $(ROOT)/build

SRC = $(NAME).c

CC = gcc
CFLAGS = -Wall -Wextra -Werror
RM = /bin/rm -rf


all : build

build : $(SRC) $(BUILD)/$(LIBFILE)
	$(CC) -I$(ROOT) -L$(BUILD) -l$(LIB) $(SRC) -o $(NAME) -Wl,-rpath,$(BUILD)

clean:
	$(RM) $(NAME)

#gcc -I../.. -L../../build -o basic basic.c -lbloom -Wl,-rpath,../../build