all: hello dump

hello: hello.o
	ld -m elf_i386 -o hello hello.o

hello.o: hello.asm
	nasm -f elf hello.asm

.PHONY: clean dump

dump: hello
	objdump -d hello
clean:
	rm hello hello.o
