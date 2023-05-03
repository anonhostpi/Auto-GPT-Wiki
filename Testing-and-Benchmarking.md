# Testing VS Benchmarking what are the differences?

## Testing
Testing is about testing deterministic functionality of the app. This is broken into two pieces: Unit and integration tests.
Unit tests focus on extremely small, but discrete parts of the application, normally single functions of an app. Integration tests test the interaction between multiple pieces of functionality. 

You can find the code for all of the tests in the tests folder: https://github.com/Significant-Gravitas/Auto-GPT/tree/master/tests
And you can run them locally with the pytest command. They also are run automatically in CI.

Check out the :test_tube: Testing Channel on discord!

## Benchmarking
Benchmarking and challenges are fundamentally different. They do not test deterministic code, but rather capabilities of the agent in specific ways that the agent may or may not be currently capable of. One example of this is the memory challenges that are currently tracked in integrations in the main repo [here](https://github.com/Significant-Gravitas/Auto-GPT/tree/master/tests/integration/challenges).

Another example can be found in the benchmarking repo [here](https://github.com/Significant-Gravitas/Auto-GPT-Benchmarks). This repo runs OpenAI evals against the AutoGPT Agent. This saves an OpenAI prompt to a file in the Agents workspace, the agent must read the file, come up with a good answer and then save the answer to a specific file which we then let OpenAI evals evaluate for us. 

Currently, on stable we see about a 60% success rate for this task. But we are working on integrating this into an optional GitHub workflow so we can benchmark relevant PRs in CI.

Check us out in the :bar_chart: Benchmarking Channel on Discord.
Also, check out the project for tracking benchmarking efforts [here](https://github.com/orgs/Significant-Gravitas/projects/3)

We also are working on figuring out the best ways to measure agent performance which is an ongoing research effort and is supported by our reading group. The discord channel for that will be coming shortly.

# Long Term Plan and Vision for Benchmarks

The dev velocity for this project is absurd. We have had great success with defining memory metrics and then letting the community optimize for those.

The goal for the benchmarking project is to build on that success and to find specific challenges and benchmarks with which the agent currently fails and to get folks to consistently beat them.

We would like to build a full testing pipeline for recursive code self improvement and other definitions of "AGI" so we can quickly move towards autonomous agents that provide value in a deterministically measurable way even if the agents themselves are stochastic.