# Recipient Review

A skill for preparing deliverables for their intended recipients. It checks disclosure boundaries, removes drafting residue, and uses one independent Reader to identify confusion or missing context.

## Workflow

1. The main agent checks the content against the task, approved requirements, and disclosure boundaries.
2. A fresh Reader receives the actual delivery package and background available to the recipient, without the drafting conversation.
3. The main agent evaluates the feedback, makes necessary changes, and checks those changes and their effects before delivery.

The Reader's feedback does not authorize disclosure or override the purpose of the task. Clear content stays unchanged. If independent reading is unavailable, the agent reports that limitation separately from the deliverable.

## Install

Clone into your user skill directory. For the default Codex skill directory:

```sh
git clone https://github.com/billerss11/recipient-review.git "$HOME/.codex/skills/recipient-review"
```

If you use a different skill directory, change the destination. To update an existing clone:

```sh
git -C "$HOME/.codex/skills/recipient-review" pull --ff-only
```

## Use

Invoke this skill explicitly with `$recipient-review`. Automatic invocation is disabled.

```text
Use $recipient-review to finalize this supplier RFQ.
The recipient will receive the email, inquiry table, and attached specification.
```

The host must support creating a fresh subagent context for the independent reading. The skill uses the host's configured model and reasoning defaults and requires no additional packages.

## Scope

Suitable for emails, RFQs, reports, proposals, documents, spreadsheets, presentations, and websites ready for delivery. It checks recipient understanding, disclosure suitability, and drafting residue. It does not certify technical, legal, commercial, or factual correctness.

The executable workflow instructions are in [SKILL.md](SKILL.md). The `agents/openai.yaml` file supplies the display name, short description, and invocation policy.
