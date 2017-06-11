# Welcome to GpuCI

A small project dedicated to testing the linux opensource gpu driver stack.

## The CI server

You are most likely looking for the [CI server](jenkins/).

## Documentation

### Scope

This is just a small personal project intended to validate my own driver
changes.

It is slowly being built up piece by piece in my free time. So some of the
edges will probably remain pretty rough for an extended period of time.

### Design Brief

Gpuci is a system which designed to provide automatically generated health
report for the linux graphics driver stack.

#### Motivation

*Warning: rambly*

There is a lack of public CI systems for the amdpgu/radeon driver stack. Having
a mechanism to automatically validate the stack as it is being developed helps
improve quality significantly.

I am also curious how far we can push the envelope with a fully open CI
system. Even some of the cool CI projects out there, like the Intel CI
infrastructure, tend to be mostly hidden. This approach usually makes sense in
a corporate environment, since CI systems are a neverending security nightmare.
In combination with how restrictive corporate networks tend to be, it usually
results in some compromise in the design.

I want to throw the security concerns away. Instead of trying to make something
that is unhackable (I don't think I can achieve that), I want to build a system
that sidesteps the issue. Keep everything in an isolated internet connection,
and store the configuration somewhere else. That way there is nothing of real
value in the LAN, and if someone destroys the whole thing for fun, we can just
patch up and re-deploy.

I also mostly want a fun little weekend project that is productive, and if it can
also make my Mon-Fri life a little easier, then that is a big plus.

#### Objectives

This project aims to:

  * Detect regressions on new submissions
  * Validate proposed changes before they are submitted
  * Track performance fluctuations
  * Be fully automated
  * Be publically accesible
  * Be recoverable from failure/compromise of all local hardware

#### The linux graphics driver stack

We will be focused on the amdgpu based graphics stack, which
consists of the following components:

    * Linux kernel
    * Libdrm
    * Mesa
    * LLVM

Gpuci is separated into four individual components:

  1. Event aggregator
  2. Job Orchestrator
  3. Results aggregator
  4. Results display

Each component should be (mostly) independent of each other. The goal is to be
able to start with a crude implementation for each one. Then slowly refine them
where the effort would have the most impact on the user experience.

### Event Aggregator

The Event Aggregator is tasked with providing the [Job
Orchestrator](#job-orchestrator) with

### Job Orchestrator

TODO

### Results Aggregator

TODO

### Results Display

TODO

### FAQs
