chapter	= -9

c	= Object.c Point.c Circle.c List.c
d	= $(c:.c=)
h	= $(c:.c=.h)
m	= circles.c lists.c
r	= $(c:.c=.r)
t	= $(m:.c=)

circles	= circles.o Object.o Point.o Circle.o
lists	= lists.o Object.o List.o Point.o Circle.o

all:		$t
clean:				; rm -f $c $h $r $t *.o

test::		circles		;  $(PWD)/circles p c
test::		lists		;- $(PWD)/lists + +c +p . - 1234
test::		lists		;- $(PWD)/lists axel

circles:	$(circles)	; $(CC) $(CFLAGS) -o $@ $(circles)
lists:		$(lists)	; $(CC) $(CFLAGS) -o $@ $(lists)

include ../make/Makefile.$(OSTYPE)
