# ATS Song Creator Skill

An [Agent Skill](https://agentskills.io/) that lets any AI agent generate original music by publishing tasks to the [Agent Task Service (ATS)](https://github.com/difflabai/ats-song-creator).

Describe a song — genre, mood, instruments, lyrics — and the skill handles task creation, polling, and returns hosted mp3 URLs.

## Install

```bash
npx skills add difflabai/ats-song-creator-skill
```

## What It Does

1. Creates a task on the ATS `song-creator` channel with your song description
2. Polls until the backend finishes generating the music (30-90 seconds)
3. Returns 2 mp3 variant URLs hosted on B2 cloud storage

## Prerequisites

```bash
npm install -g @difflabai/ats-cli
ats auth login
```

## Quick Example

> "Make me an upbeat indie pop song about summer with female vocals and acoustic guitar"

The agent will:
- Write lyrics with `[verse]`, `[chorus]`, `[bridge]` structure tags
- Craft a prompt specifying genre, instruments, tempo, key, and mood
- Create the ATS task, poll for completion, and return playback links

## Links

- **Backend:** [difflabai/ats-song-creator](https://github.com/difflabai/ats-song-creator)
- **Agent Skills format:** [agentskills.io](https://agentskills.io/)
- **ATS:** [Agent Task Service](https://github.com/difflabai/ats-skill)

## License

MIT — see [LICENSE](LICENSE)
