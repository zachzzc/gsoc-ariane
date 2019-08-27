--- 
layout: single
title: "Wikis"
permalink: /wikis/
---

## Aug 25, 2019
- Finish about the multi-issue feature
- Re-name is not implemented yet for mult-issue
- Push the code of multi-issue and wait for review [link](https://github.com/pulp-platform/ariane/pull/311)

## Aug 19, 2019
- The misprediction on the same issue cycle can lead to flush other instructions. Modify the scoreboard to catch this.
- Multi-issue is enabled. Tests pass.

## Aug 10, 2019
- Modify the interface of all stages to support multi-issue
- Pass single issue testing 

## Aug 1, 2019
- Modify the interface of instruction queue to support multi-issue
- Pass on single issue testing

## July 20, 2019 
- Push the global predictor improvement and wait for review. [link](https://github.com/pulp-platform/ariane/pull/287)
- Start designing the multi-issue feature
- The user-space program is working. It just takes a while to run.

## July 7, 2019 

- Created github page to track the progress of the project.
- Great template and easy to use. [mmistakes](https://github.com/mmistakes/minimal-mistakes)

## July 5, 2019

- Finished implementing the gshare global history predictor
- Performance improvement compared to the original one with various global history lengths :
- The performance improvement is subtle. Need to debug why and why length = 4 is best.
- The user-space program is broken in Ariane. Wait for the investigation from Florian.

## June 4, 2019

- Finished implementing the generalization of the instruction realigner
- Passed all the tests
- Pushed a PR
- Run the synthesis and timing passes for both 32 and 64 bit. Timing details is here: [link](https://github.com/pulp-platform/ariane/pull/253#pullrequestreview-243921259)

