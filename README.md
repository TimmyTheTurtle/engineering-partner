# Ada — Engineering Partner

Ada is a GitHub Copilot custom agent for collaborative discovery, planning, and design. She helps develop ideas, challenges assumptions constructively, and produces detailed, human-readable implementation handoffs when requested.

This repository is an initial draft. It defines one agent and a small reference library. It does not configure repository-wide instructions, hooks, or other agents.

## Contents

- `agents/ada.agent.md`: Ada's always-on role and collaboration boundaries.
- `skills/engineering-method/SKILL.md`: a manually invoked guide to the references.
- `skills/engineering-method/references/`: focused material for collaboration, design, architecture, and handoffs.

## Use in VS Code with Copilot

1. Clone this repository on the machine where the Copilot harness runs.
2. Copy `agents/ada.agent.md` into `~/.copilot/agents/`.
3. Copy the entire `skills/engineering-method/` directory into `~/.copilot/skills/engineering-method/`.
4. In VS Code's Agents window, select the Copilot harness, open Customizations, and verify that Ada and the `engineering-method` skill are discovered. Start a new session and select Ada from the agent picker.
5. For a detailed methods discussion, explicitly invoke `/engineering-method` or ask Ada to read the appropriate reference file. The skill disables automatic model invocation so other agents do not acquire its instructions automatically.

Paths beginning with `~` refer to the home directory on the machine or remote environment where the Copilot harness runs. Instructions in a project and other applicable user settings still apply. Installing the files does not automatically synchronize them with this repository; pull changes and update your installed copies when desired. A plugin or other distribution mechanism can be considered later.

## Test before relying on it

Check that Ada appears in the Copilot agent picker; ask her to explore a design without edits; invoke the skill and check which reference she reads; and compare a normal Copilot session to ensure the skill is not automatically activated. Test a handoff in a disposable project, including the timestamp and existing project conventions. Behavior and discovery depend on your Copilot/VS Code version and configuration; this draft has not been validated in a live session.

## Sources and scope

The references summarize a collaborative working method, not a complete software engineering methodology. They distinguish stated preferences from examples and hypotheses. Project details belong in each project, and personal or private conversation content should not be added to this public repository without review.

[VS Code custom agents](https://code.visualstudio.com/docs/agent-customization/custom-agents) · [VS Code agent skills](https://code.visualstudio.com/docs/agent-customization/agent-skills)
