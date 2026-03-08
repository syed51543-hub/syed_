# AGENTS.md

## Project Goal
Improve the Siemens S7 STL/AWL motor control logic in this repository from a basic seal-in circuit into a production-grade motor control implementation.

## Engineering Priorities
1. Personnel safety
2. Equipment protection
3. Fail-safe behavior
4. Deterministic PLC scan logic
5. Clear diagnostics
6. Maintainable code

## Required Logic Features
When modifying motor_seal_in_stl.awl always consider:

- Start / Stop pushbuttons
- Seal-in motor latch
- External permissive interlocks
- Motor overload trip
- Run feedback verification
- Start failure timeout
- Feedback lost during running
- Unexpected run detection
- Alarm bits
- Trip bits
- Fault latching
- Manual reset
- Safe power-up state
- Restart inhibit after trip

## Coding Rules
- Use Siemens S7 classic STL/AWL syntax
- Comment every network
- Keep safety logic explicit
- Separate command, trip, and alarm bits
- Document I/O mapping
- Never assume unsafe restart behavior
