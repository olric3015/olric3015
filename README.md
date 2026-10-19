<p align="center">
  <img src="assets/banner.svg" alt="olric3015: Open-source contributor to Hermes Agent. web3 is my life." width="100%">
</p>

<p align="center">
  <a href="https://github.com/NousResearch/hermes-agent/commits/main?author=olric3015"><img src="https://img.shields.io/badge/Hermes_Agent-35_commits_on_main-C8243A?style=flat-square&labelColor=141312" alt="Hermes Agent: 35 commits on main"></a>
  <a href="https://hermes-agent.nousresearch.com/docs/plugins/by/olric3015"><img src="https://img.shields.io/badge/Plugin_catalog-10_plugins-B9BD8A?style=flat-square&labelColor=141312" alt="Plugin catalog: 10 plugins"></a>
  <a href="https://github.com/olric3015/hermes-plugins"><img src="https://img.shields.io/badge/hermes--plugins-MIT-C9B8A3?style=flat-square&labelColor=141312" alt="hermes-plugins: MIT"></a>
</p>

I build small, local plugins for [Hermes Agent](https://github.com/NousResearch/hermes-agent), the open-source agent from Nous Research. Each one hooks into a single point in the agent, keeps a short local ledger, and answers one question with one slash command: which models are slow, which calls fail, how long the agent waits on you, which files it touched. No network, no subprocesses, no credentials; nothing leaves your machine.

<p align="center">
  <img src="assets/stats.svg" alt="10 plugins in the Hermes catalog, 35 commits on Hermes Agent main, 26 pull requests merged, 0 network calls in the plugins" width="100%">
</p>

## Plugins

All ten live in one repo, [olric3015/hermes-plugins](https://github.com/olric3015/hermes-plugins), and install by name from the Hermes catalog:

```
hermes plugins install <name> --enable
```

| Plugin | Command | What it tells you |
|---|---|---|
| [**aux-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/aux-ledger) | `/aux` | Every auxiliary LLM call (titles, compression, vision, approvals) by task, model and provider |
| [**stream-speed**](https://hermes-agent.nousresearch.com/docs/plugins/stream-speed) | `/speed` | Time to first text and characters per second for each model |
| [**error-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/error-ledger) | `/errors` | Failed provider requests by model, provider and failure reason |
| [**approval-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/approval-ledger) | `/approval-log` | Approval prompts by rule, with how often each was approved, denied or left unanswered |
| [**command-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/command-ledger) | `/command-log` | Which slash commands you actually use, on which surfaces |
| [**wait-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/wait-ledger) | `/waits` | How long the agent sat waiting on you: approvals, questions, password prompts |
| [**stop-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/stop-ledger) | `/stop-log` | Turns cut short by `/stop` or `/new`, per platform |
| [**voice-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/voice-ledger) | `/voice-log` | Voice recordings sent to speech-to-text, by provider, model and language |
| [**interim-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/interim-ledger) | `/interim-log` | Progress messages the agent sends mid-turn, even where the display hides them |
| [**edit-ledger**](https://hermes-agent.nousresearch.com/docs/plugins/edit-ledger) | `/edit-log` | Files the agent changed per turn, by file type |

Every plugin is tested on Linux, macOS and Windows, and end to end against both the oldest supported Hermes release and current `main` in CI.

<table>
  <tr>
    <td width="50%"><a href="https://hermes-agent.nousresearch.com/docs/plugins/stream-speed"><img src="https://raw.githubusercontent.com/olric3015/hermes-plugins/d7b48bbe90d18bfdf26ccbf7bd4da6616e7645d6/docs/stream-speed-card.png" alt="stream-speed: /speed output" width="100%"></a></td>
    <td width="50%"><a href="https://hermes-agent.nousresearch.com/docs/plugins/error-ledger"><img src="https://raw.githubusercontent.com/olric3015/hermes-plugins/dd646070c662ebf1978e5623bf30d2d1f55f7bef/docs/error-ledger-card.png" alt="error-ledger: /errors output" width="100%"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://hermes-agent.nousresearch.com/docs/plugins/wait-ledger"><img src="https://raw.githubusercontent.com/olric3015/hermes-plugins/c44b60aa6a6621147ce5b3168b7841bf1f8ac006/docs/wait-ledger-card.png" alt="wait-ledger: /waits output" width="100%"></a></td>
    <td width="50%"><a href="https://hermes-agent.nousresearch.com/docs/plugins/edit-ledger"><img src="https://raw.githubusercontent.com/olric3015/hermes-plugins/c0a93cb23627ac1856cb29db163e2cbfff77251d/docs/edit-ledger-card.png" alt="edit-ledger: /edit-log output" width="100%"></a></td>
  </tr>
</table>

## Toolbox

<p>
  <img src="https://img.shields.io/badge/Python-141312?style=for-the-badge&logo=python&logoColor=C9B8A3" alt="Python">
  <img src="https://img.shields.io/badge/pytest-141312?style=for-the-badge&logo=pytest&logoColor=C9B8A3" alt="pytest">
  <img src="https://img.shields.io/badge/GitHub_Actions-141312?style=for-the-badge&logo=githubactions&logoColor=C9B8A3" alt="GitHub Actions">
</p>
