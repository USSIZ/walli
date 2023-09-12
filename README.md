While learning how to code with Golang, I wanted to understand how computers works at a lower level.

So, I decided to learn the basics of ASM and make a program with those new learnings.

***

## **Necessary tools**

For a `Windows` with `x86-64` architecture, those tools were recommended:

| Tool            | Name       | Source                     |
|:----------------|:-----------|:---------------------------|
| **Assembler**   | `NASM`     | https://www.nasm.us        |
| **Linker**      | `Golink`   | https://www.godevtool.com  |

> **Note**: Because Windows keeps control on syscalls, we also have to use the Windows API

***

## **Running the commands**

To use the assembler, run this command:

`nasm.exe -f win64 <file>.asm -o <file>.obj`

Then, to use the linker, run this command:

`golink.exe <file>.obj /entry main /console kernel32.dll`

> **Note**: Executables must be in the root folder of the project to execute the commands correctly