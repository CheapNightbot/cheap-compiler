# cheap-compiler

1. Convert `scanner.flex` into `scanner.c`:

```bash
flex -o scanner.c scanner.flex
```

2. Compile both `main.c` and `scanner.c`, but do not link:

```bash
gcc -c -o main.o main.c
gcc -c -o scanner.o scanner.c
```

3. Link `main.o` and `scanner.o` together to make an executable:

```bash
gcc -Xlinker -o scanner main.o scanner.o
# OR
gcc -Xlinker -o scanner.exe main.o scanner.o
```
