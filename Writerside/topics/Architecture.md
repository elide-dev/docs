# Architecture

This page gives an overview of %product%'s internal architecture. Users of %product% don't necessarily need to know
these details; these docs are mostly for contributors, but everyone is welcome!

## How %product% works

At a high level, %product% is a suite of libraries and applications written for the Java Virtual Machine, or
[JVM](https://docs.oracle.com/en/java/javase/21/vm/java-virtual-machine-technology-overview.html).

The JVM is an incredibly powerful runtime system, offering state-of-the-art just-in-time (JIT) compilation, memory
safety, and a full standard library with plenty of testing and functional coverage (referred to as the
[JDK](https://en.wikipedia.org/wiki/Java_Development_Kit), for Java Development Kit).

<img src="arch-v1.svg" />

> Note: This is already out of date, but it's as close as we have right now to an architectural diagram.
