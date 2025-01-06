# VHDL Counter Bug

This repository demonstrates a common issue in VHDL: improper handling of signals and variables within processes.  Specifically, this example showcases a counter that might not increment correctly due to issues with signal updates within a process.

## The Bug
The provided VHDL code implements a simple counter.  However, the assignment of the `internal_count` signal within the process might lead to unexpected behavior, especially at higher clock frequencies or under certain timing conditions.  This is because there is no explicit wait statement after the `internal_count` update, leading to potential race conditions and incorrect counting if the clock signal changes too quickly.

## Solution
The solution addresses this issue by ensuring proper signal updates within the process. It employs appropriate signal assignments and process structuring.