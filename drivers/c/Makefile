DEFAULT: all
.PHONY: install

CC ?= /usr/bin/gcc

all: pwmControlFan safecutoffpower

install:
	chmod 755 pwmControlFan safecutoffpower
	cp pwmControlFan safecutoffpower /usr/bin/
	chcon -u system_u -t bin_t /usr/bin/pwmControlFan /usr/bin/safecutoffpower

pwmControlFan:  pwmControlFan.c
	${CC} -o pwmControlFan pwmControlFan.c
safecutoffpower:  safecutoffpower.c 
	${CC} -o safecutoffpower safecutoffpower.c
clean:
	rm -rf safecutoffpower pwmControlFan 
