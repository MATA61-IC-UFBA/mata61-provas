install:
	sudo apt-get install -f flex
	sudo apt-get install -f bison

compile:
	bison --defines=token.h p2.y
	flex p2.l
	cc -o complm p2.tab.c lex.yy.c main.c expr.c decl.c stmt.c type.c

test:
	./run_tests.sh

all:
	make install
	make compile
	make test

clean:
	rm lex.yy.c
	rm p2.tab.c
	rm token.h
	rm complm

