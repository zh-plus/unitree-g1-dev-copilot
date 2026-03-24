# unitree-g1-dev-copilot

`unitree-g1-dev-copilot` is a development skill for Unitree G1 work. It helps an AI coding assistant answer G1 questions using a local bundle of official G1 documentation instead of guessing APIs, service names, ROS2 details, or camera workflows.

这个仓库提供一个面向 Unitree G1 开发的 skill，重点覆盖 G1 SDK、DDS、ROS2、服务接口查询、上层/底层运动开发，以及头部 RealSense D435i 深度相机相关问题。它的目标不是“泛泛聊天”，而是基于本地文档给出更稳、更可执行的开发建议。

## What This Skill Does

- Routes G1 questions to the right local reference documents
- Helps with SDK2, DDS, and ROS2 development flows
- Explains when to use high-level vs low-level motion interfaces
- Grounds camera answers in the bundled G1 docs and official RealSense upstream guidance
- Avoids inventing unsupported topics, services, or integration steps

## Repository Layout

- `SKILL.md`: the skill definition and workflow
- `references/G1_docs/`: local snapshot of G1 developer documentation
- `evals/evals.json`: simple eval prompts for smoke-testing the skill behavior
- `INTRO.md`: short project introduction for sharing or repo summary reuse

## Best Fit

This skill is useful when you need help with:

- Unitree G1 SDK or service-interface lookup
- G1 ROS2 or DDS communication questions
- G1 setup, networking, and debug-mode prerequisites
- RealSense D435i usage on G1
- Choosing between SDK-first and ROS-first camera workflows
- Troubleshooting based on the official G1 docs bundle

## How To Use

1. Put this folder where your coding assistant can load skills.
2. Make sure the skill name stays `unitree-g1-dev-copilot`.
3. Ask concrete G1 development questions such as:
   - "Which G1 docs explain DDS topics and service interfaces?"
   - "Should I use SDK2 or ROS2 for my G1 integration?"
   - "Help me install the RealSense ROS wrapper on a Unitree G1."

## Design Principles

- Prefer the bundled G1 docs over memory
- Mark project-specific workflows clearly instead of presenting them as official defaults
- Use current upstream RealSense docs when exact install commands may change
- Keep safety notes explicit for motion-control tasks

## Notes On Sources

The files under `references/G1_docs/` are organized from Unitree G1 developer documentation pages and preserved here for local reference. Original content, trademarks, and documentation rights belong to their respective owners. If you plan to redistribute or commercialize this bundle, review the original source terms first.

## Why This Repo Exists

General-purpose coding assistants are often too eager to guess robotics APIs. This repo packages a narrower, documentation-grounded copilot so G1 development answers stay closer to the official material and are easier to validate on a real robot or Ubuntu development machine.
