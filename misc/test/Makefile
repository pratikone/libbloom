NAME = basic
LIB = bloom
LIBFILE = libbloom.a
ROOT = /projects/libbloom
BUILD = $(ROOT)/build

SRC = $(NAME).c

CC = gcc
CFLAGS = -Wall -Wextra -Werror
RM = /bin/rm -rf


all : dynamic_build
static_build : $(SRC) $(BUILD)/$(LIBFILE)
	$(CC) -I$(ROOT) -L$(BUILD) $(SRC) -o $(NAME) $(BUILD)/$(LIBFILE) -lm	
dynamic_build : $(SRC) $(BUILD)/$(LIBFILE)
	$(CC) -I$(ROOT) -L$(BUILD) -l$(LIB) $(SRC) -o $(NAME) -Wl,-rpath,$(BUILD)

clean:
	$(RM) $(NAME)

#gcc -I../.. -L../../build -o basic basic.c -lbloom -Wl,-rpath,../../build

# number of lines in final executable
# objdump -dr basic | wc -l
# static build  : 714
# dynamic build : 389