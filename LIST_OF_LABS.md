# List of labs <!-- omit in toc -->

This is a brief overview of the labs we've created for this course. Since our
course is only 2 credits, we can't run all of them, and some semesters you can
get through more than others.

Some labs have pre-labs, but not all of them do. The intent was to encourage
students to read some of the (often voluminous) linked documentation before
class and come at least somewhat prepared to get started. Otherwise students
would often spend 30 minutes to an hour of the beginning of their precious
not-quite-2-hours of lab time just reading background material.

I'm not convinced that all the pre-labs are awesome, and it would probably
be good to have more pre-labs in places.

:bangbang: I've tried having the students read the lab write-ups in Perusall
with mixed results. An awful lot of the actual reading is material we _link_
to, and there's no way for them to comment on that, so they have been (I think
legitimately) grumpy about that. I bet there's a way to make that work, but
I'm not sure I've figured it out.

- [Git, the command line, and shell programming](#git-the-command-line-and-shell-programming)
- [C, memory management, and system calls](#c-memory-management-and-system-calls)
  - [C and memory management](#c-and-memory-management)
  - [C system calls; traversing directories](#c-system-calls-traversing-directories)
- [Client-server architectures, remote procedure calls, and socket programming](#client-server-architectures-remote-procedure-calls-and-socket-programming)
- [Threading and concurrency](#threading-and-concurrency)
- [A little Rust](#a-little-rust)
- [Mapping the Internet!](#mapping-the-internet)
- [Circuit design](#circuit-design)

## Git, the command line, and shell programming

These labs set the course up, making sure that folks understand how to use `git`
and basic command line tools, and do a little bit of shell programming.

- Command line introduction
  - Command line introduction pre-lab
  - Command line introduction lab
- Log processing
  - Log processing pre-lab
  - Lob processing lab

We tend to spread the Log Processing lab across two weeks, and we tend to have
two assignments in Canvas so there's a reasonable waypoint for the students and
they don't put the whole thing off to the second week.

These labs use the `bats` shell testing tool for the tests. `bats` is a nice
framework, but their use of `git` submodules complicates things and interacts
badly with GitHub Classrooms templating system. I should probably make a
completely separate page outlining those issues and how to deal with them.

## C, memory management, and system calls

These use [Google's Cmockery testing library](https://github.com/google/cmockery). 
That's worked fairly well, but can be a little tricky to set up. There also
doesn't appear to have been any commits to that repository since May, 2020, in
case we care. I've never really looked into alternatives.

### C and memory management

The [C and memory management lab](https://github.com/UMM-CSci-Systems/C-Lab-Starter) introduces the use of arrays (and strings) in C, along with the allocation and freeing of memory. It uses [the CMockery test library](https://code.google.com/p/cmockery/) for unit testing, and `valgrind` to identify memory leaks.

### C system calls; traversing directories

The [Traversing Directories lab](https://github.com/UMM-CSci-Systems/Traversing-Directories-starter) introduces making system calls from C, with a focus on calls that allow one to traverse directories and examine the status of files. It (currently) uses shell testing tools and doesn't need any special tools, although `valgrind` can be used to identify memory leaks.

## Client-server architectures, remote procedure calls, and socket programming

## Threading and concurrency

## A little Rust

## Mapping the Internet!

## Circuit design

The [Circuit Design lab](https://github.com/UMM-CSci-Systems/Circuit-design-lab) is a simple, ungraded, "in lab" experience with basic circuit design using the [Logisim program](http://www.cburch.com/logisim/index.html) for the design work.
