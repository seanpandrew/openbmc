# Copyright 2015-present Facebook. All Rights Reserved.

C_SRCS := $(wildcard *.c)
C_OBJS := ${C_SRCS:.c=.o}

all: peci-util

peci-util: $(C_OBJS)
	$(CC) $(CFLAGS) -pthread -lgpio -lpal --std=c99 -o $@ $^ $(LDFLAGS)
 
.PHONY: clean

clean:
	rm -rf *.o peci-util
