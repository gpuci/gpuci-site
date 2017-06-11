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

### Architecture

Gpuci is separated into four individual components:
  1. Event aggregator
  2. Job Orchestrator
  3. Results aggregator
  4. Results display

Each component should be (mostly) independent of each other. The goal is to be
able to start with a crude implementation for each one. Then slowly refine them
where the effort would have the most impact on the user experience.

#### Event Aggregator

The Event Aggregator is tasked with providing the [Job
Orchestrator](#job-orchestrator) with

#### Job Orchestrator

TODO

#### Results Aggregator

TODO

#### Results Display

TODO
