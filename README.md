# 100Hires Portfolio Project

A hands-on portfolio piece proving I can pick up new tools fast — built while setting up an AI-assisted coding workflow (Cursor + Claude Code + Codex) from zero prior experience, on a Chromebook, which added its own layer of constraints.

## Tools Installed
- Cursor IDE (via Linux/Crostini on Chromebook)
- GitHub Codespaces (cloud fallback environment)
- Node.js and npm
- Claude Code (installed; login blocked by subscription requirement)
- Codex (installed and successfully logged in)

## Steps Completed

1. Set up the Linux development environment (Crostini) on my Chromebook.
2. Installed Cursor IDE via the Linux `.deb` package.
3. Created this public GitHub repository and cloned it into Cursor via terminal.
4. Searched Cursor's Extensions/Plugins marketplace for "Claude Code" and "Codex" — neither was listed, since Cursor's newer interface distributes third-party AI tools differently than the classic VS Code Extensions model.
5. Installed Node.js and attempted to install Claude Code and Codex via npm in the terminal instead.
6. Hit local storage limitations on the Chromebook (Crostini's disk allocation ran low, ~500MB free), which broke the standard `apt install nodejs` approach.
7. Worked around it by installing Node.js as a direct binary (avoids pulling in large compiler dependencies).
8. Hit the storage wall again shortly after — switched to **GitHub Codespaces** as a cloud-based environment to remove the local storage constraint entirely.
9. Installed Claude Code successfully via npm inside Codespaces.
10. Attempted Claude Code login — presented with three options (subscription account, Console/API account, or third-party platform). Selected the subscription option, but the flow returned "Claude Max or Pro is required to connect to Claude Code" since I only have a free account.
11. Installed Codex successfully via npm inside Codespaces.
12. Logged into Codex successfully using a free ChatGPT account — no subscription required.

## Issues I Ran Into (and how I solved them)

- **Crostini launch failure** ("CONTAINER_CREATE_FAILED_SIGNAL") — resolved by restarting the Chromebook.
- **Cursor blank/black screen on launch** — resolved by launching with `--no-sandbox --disable-gpu` flags to work around a GPU rendering conflict inside the Linux container.
- **ChromeOS/Linux file separation** — Chrome downloads and the Linux filesystem are isolated by default; resolved using ChromeOS's built-in "Install with Linux" option for the `.deb` file.
- **Local disk space exhaustion** — `apt install nodejs` pulls in large compiler toolchains (gcc, cpp) that exceeded available Crostini storage; resolved short-term with a direct Node.js binary install, then permanently by moving the whole workflow to GitHub Codespaces.
- **Claude Code subscription requirement** — CLI login via the standard account option requires Claude Pro or Max. I identified a possible workaround (Anthropic Console API key) but chose not to pursue it further, since it isn't guaranteed to be free and I wanted to complete this task without any cost. This is documented here transparently rather than worked around artificially.
- **Codex succeeded where Claude Code didn't** — logging in with a free ChatGPT account worked immediately, showing that account requirements differ meaningfully between the two tools even though they serve a similar purpose.

## What I Learned

**Troubleshooting is a transferable skill, not a technical one.** Almost every failure in this process was solvable by reading the exact error message closely and researching it specifically, rather than guessing. That instinct — read carefully, search precisely, try the smallest fix first — is the same instinct I'd bring to debugging a broken campaign, a confusing analytics report, or an underperforming funnel.

**Knowing when to pivot is as valuable as knowing how to push through.** When my Chromebook's storage kept blocking progress, the right move wasn't to keep forcing the same approach — it was to recognize the constraint and switch to a completely different environment (Codespaces). I think that kind of judgment — knowing when a workaround is worth it versus when to change the whole approach — matters a lot in growth marketing, where you're constantly testing channels and need to know when to cut losses versus dig deeper.

**Honest documentation of limitations is more valuable than a falsified success.** I could have hidden the Claude Code login issue or found a workaround requiring payment, but I chose to document the real constraint (subscription requirement) and explain the reasoning behind not paying for it. I think being transparent about what worked, what didn't, and why it builds more trust than a report where everything mysteriously went perfectly.