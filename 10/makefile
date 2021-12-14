chapter	= -10

c	= Object.c Filter.c Cmd.c Wc.c String.c List.c Sort.c
d	= $(c:.c=)
h	= $(c:.c=.h)
r	= $(c:.c=.r)
t	= cmd wc sort

cmd	= Object.o Filter.o Cmd.o
wc	= Object.o Filter.o Wc.o
sort	= Object.o Filter.o String.o List.o Sort.o

all:		$t
clean:				; rm -f $c $h $r $t *.o

test::		cmd		;  $(PWD)/cmd -fffv10 -- -f filename
test::		wc		;  cat Wc.dc | $(PWD)/wc - Wc.dc none-such
test::		sort		;  cat Sort.d | $(PWD)/sort -r - Sort.d

cmd:		$(cmd)		; $(CC) $(CFLAGS) -o $@ $(cmd)
wc:		$(wc)		; $(CC) $(CFLAGS) -o $@ $(wc)
sort:		$(sort)		; $(CC) $(CFLAGS) -o $@ $(sort)

include ../make/Makefile.$(OSTYPE)
