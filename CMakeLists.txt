cmake_minimum_required(VERSION 3.3)
project(xv6)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
    include/fcntl.h
    include/fs.h
    include/param.h
    include/stat.h
    include/syscall.h
    include/traps.h
    include/types.h
    include/x86.h
    kernel/asm.h
    kernel/bio.c
    kernel/bootasm.S
    kernel/bootmain.c
    kernel/bootother.S
    kernel/buf.h
    kernel/console.c
    kernel/data.S
    kernel/defs.h
    kernel/elf.h
    kernel/exec.c
    kernel/file.c
    kernel/file.h
    kernel/fs.c
    kernel/ide.c
    kernel/initcode.S
    kernel/ioapic.c
    kernel/kalloc.c
    kernel/kbd.c
    kernel/kbd.h
    kernel/lapic.c
    kernel/main.c
    kernel/makefile.mk
    kernel/mmu.h
    kernel/mp.c
    kernel/mp.h
    kernel/multiboot.S
    kernel/picirq.c
    kernel/pipe.c
    kernel/proc.c
    kernel/proc.h
    kernel/sign.pl
    kernel/spinlock.c
    kernel/spinlock.h
    kernel/string.c
    kernel/swtch.S
    kernel/syscall.c
    kernel/sysfile.c
    kernel/sysfunc.h
    kernel/sysproc.c
    kernel/timer.c
    kernel/trap.c
    kernel/trapasm.S
    kernel/uart.c
    kernel/vectors.pl
    kernel/vm.c
    tools/dot-bochsrc
    tools/dot-gdbinit
    tools/gdbutil
    tools/makefile.mk
    tools/mkfs.c
    user/cat.c
    user/echo.c
    user/forktest.c
    user/grep.c
    user/init.c
    user/kill.c
    user/ln.c
    user/ls.c
    user/makefile.mk
    user/mkdir.c
    user/printf.c
    user/ps.d
    user/rm.c
    user/sh.c
    user/spin.d
    user/stressfs.c
    user/tester.c
    user/ulib.c
    user/umalloc.c
    user/usage.d
    user/user.h
    user/usertests.c
    user/usys.S
    user/wc.c
    user/zombie.c
    FILES
    Makefile
    README
    version)

add_executable(xv6 ${SOURCE_FILES})