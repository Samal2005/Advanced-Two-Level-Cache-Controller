# Advanced Two Level Cache Controller

Author: Subhalaxmi Samal

## Introduction

This project implements a two-level cache controller using Verilog HDL. The design consists of an L1 Direct Mapped Cache and an L2 4-Way Set Associative Cache. The main objective of the project is to reduce memory access time by storing frequently used data in cache memory.

## Features

- L1 Direct Mapped Cache
- L2 4-Way Set Associative Cache
- LRU Replacement Policy
- Write Back Policy
- No Write Allocate Policy
- Read and Write Operations
- FPGA Implementation
- Simulation Verification

## Cache Organization

The memory hierarchy used in this project consists of:

- L1 Cache
- L2 Cache
- Main Memory

Whenever a processor request is received, the controller first checks L1 Cache. If the data is not found, L2 Cache is searched. If the data is still unavailable, the request is served from Main Memory.

## Replacement Policy

The L2 Cache uses the Least Recently Used (LRU) replacement policy. When a cache set becomes full, the block that has not been used for the longest time is replaced.

## Write Policies

### Write Back

Modified data is first updated in cache memory and written to higher memory levels only when the block is evicted.

### No Write Allocate

During a write miss, data is updated in higher memory levels but is not loaded into cache memory.

## Project Structure

1. Cache_Controller_Simulation_Project
2. Cache_Controller_FPGA_Implementation_Project

The simulation project contains detailed comments and test cases, while the FPGA project contains modifications required for hardware implementation.

## Tools Used

- Verilog HDL
- Xilinx Vivado
- FPGA Board

## Results

The design was verified using simulation waveforms and FPGA implementation. Cache hits, cache misses, block replacement and memory updates were tested successfully.

## Future Scope

- Variable cache sizes
- Different replacement policies
- Performance analysis module
- Multi-level cache extensions
