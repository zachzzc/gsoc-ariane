--- 
layout: splash
title: "Microarchitectural Enhancement Of Ariane"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/home_background.jpg
  actions:
    - label: "Original"
      url: "https://github.com/pulp-platform/ariane"
    - label: " Forked "
      url: "https://github.com/zachzzc/ariane"
excerpt: >
  The site for updating the progress of Google Summer of Code 2019 project. <br />
---

## Synopsis
The RISC-V is an open-source and free ISA (instruction set architecture) developed at the University of California Berkeley. It becomes increasingly popular nowadays, both in industry and academia, because it allows to use the ISA without any royalties and it perfectly fits the implementation of small and low-power hardware such as IoT devices. [Ariane](https://github.com/pulp-platform/ariane) is a 6-stage, linux-capable, open-source processor implementing RISC-V ISA (RV64GC), developed at ETH Zurich. It is highly configurable and well-tested and successfully booting Linux. Currently, the processor is single-issue, meaning that the processor can only issue one instruction per clock cycle. That is a huge performance bottleneck since most functional units in the processor will stay idle when it does not have any instructions to proceed. In this project, I will implement super-scalar issue logic which allows Ariane to issue two (or more) instructions in the same clock cycle so that the overall performance will be greatly improved

## Deliverables

| Task          | Details       | Status        |
| ------------- | ------------- | ------------- |
| Wider fetch width | Generalize the instruction realigner in Ariane to support wider fetch width, i.e., 64 bit per fetch | :hourglass: |
| Proper branch prediction modifications for the widend fetch interface | The instruction frontend and branch prediction will encounter problems when we fetch two instruction from the memory since it is likely that the incoming instruction data is compressed and unaligned (e.g. wrapping a natural 32 bit fetch-boundary). And we also consider to add a gshare global history predictor to increase the performance | :hourglass: |
| Enable multi-issue in Ariane | This is the main deliverable of this project which will allow Ariane to issue two (or more) instructions in the same clock cycle | :computer: |
| Another ALU (arithmetic logic unit) | If the processor is able to issue two instruction at the same time, it is beneficial to have more functional units to process the incoming instructions at the same time. A new ALU is considered to be added to the execution stage | :clock1: |

:clock1: Not start yet &emsp; :computer: Developing &emsp; :hourglass: Wait for review &emsp; :pushpin: Code pushed