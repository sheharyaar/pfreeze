# Pfreeze

> [!WARNING]
> This project is not to be used in production environments. It is intended for educational purposes only. It is my personal project to implement process migration like CRIU on Linux x86\_64 systems.

> This project will **not** be build using any LLMs. Only the Makefile and some parts of the README.md could be generated from them. I _do not hate_ LLMs but I don't prefer to use them for my learning projects. I like to make my own mistakes and fix them.

An independent, experimental and personal implementation of Process Freeze/Unfreeze/Migration inspired by [CRIU](https://github.com/checkpoint-restore/criu) (Checkpoint/Restore in Userspace).

### TODO

- Use CRIU (and if unit tests available) to see commands and effects and try to implement them.
- Investigate the entire process creation flow in the kernel.
- Investigate use of mmap to create memory regions for a new process.
- Dump register values (ptrace ?)
- Dump memory mappings (ptrace ?)
- Handling library changes and how does CRIU handle that ?
  - What if the library is different now and the RIP points to a code in the library mapping ?
- Move to multithreaded process and dump threads and thread states ?
- Dump socket states ?