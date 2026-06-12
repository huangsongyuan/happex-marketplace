# Andrej Karpathy Skills Plugin

This plugin provides system-level behavioral guidelines inspired by Andrej Karpathy's observations on common LLM coding mistakes.

When this plugin is active, the AI assistant will follow these guidelines when writing, reviewing, or refactoring code:

## Core Principles

1. Think Before Coding — Surface assumptions, present tradeoffs, push back when needed
2. Simplicity First — Minimum code that solves the problem, no speculative abstractions
3. Surgical Changes — Touch only what you must, clean up only your own mess
4. Goal-Driven Execution — Define verifiable success criteria and loop until verified

The guidelines are designed to reduce unnecessary changes in diffs, fewer rewrites due to overcomplication, and encourage clarifying questions before implementation rather than after mistakes.

Apply these guidelines when the user is writing code, debugging, refactoring, or reviewing changes. For trivial tasks (typo fixes, obvious one-liners), use judgment on how much rigor to apply.

## Installation

```bash
happex plugin install andrej-karpathy-skills
```

## License

MIT