# Usage
# make			# compile all binary
# make clean	# remove ALL binaries and objects

.PHONY = all clean

CC = gcc		# compiler to use

LINKERFLAGS = -lm

SRCS := $(wildcard *.c)		# store all .c files in variable SRCS
BINS := $(SRCS:%.c=%)		# replace 'foo.c bar.c' with 'foo bar'

all: ${BINS}

%: %.o
	@echo "Checking.."
	${CC} ${LINKERFLAGS} $< -o $@

%.o: %.c
	@echo "Creating object.."
	${CC} -c $<

clean:
	@echo "Cleaning up..."
	rm -rvf *.o ${BINS}
