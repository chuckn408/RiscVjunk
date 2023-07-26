!clang-12 --target=riscv32 -march=rv32gc -mabi=ilp32d -mno-relax hello.c -c -o hello.o

!ld.lld-12 hello.o -o hello.x

from google.colab import files
files.download('hello.x')

%run -i riscv_ale_load.py hello.x
