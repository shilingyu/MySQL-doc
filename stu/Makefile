CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi loginstu.cgi logintea.cgi addscore.cgi addcourse.cgi selcourse.cgi check_sc.cgi score_sel.cgi scoreall.cgi realdel.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi
install:
	cp *.cgi /usr/lib/cgi-bin/sx
	cp head.html footer.html logintea.html loginstu.html /usr/lib/cgi-bin/sx
