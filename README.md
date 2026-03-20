# VCONIC TADHack 2026 - Hackathon Submissions

This repository contains [vCon](https://datatracker.ietf.org/doc/draft-ietf-vcon-vcon-container/) (Virtual Conversation Container) files for hackathon submissions from the [VCONIC TADHack](https://blog.tadhack.com/2025/12/19/vconic-tadhack/), held March 7-8, 2026.

## About the Hackathon

The VCONIC TADHack challenged developers worldwide to build applications using the [vCon MCP Server](https://www.conserver.io/mcp-server/what-is-the-vcon-mcp-server) — a Model Context Protocol server that lets AI assistants work with structured conversation data. Teams had 48 hours to create solutions that demonstrate how standardized conversation containers can power real-world applications across industries including emergency services, finance, education, compliance, and personal productivity.

The hackathon was organized by [TADHack](https://tadhack.com) and [VCONIC](https://www.conserver.io/), with a $5K prize pot. Training sessions were held in the weeks leading up to the event, covering the vCon MCP Server, consent and lifecycle management, spec-driven development, and the vCon app store.

### Key Technologies

- **[vCon](https://datatracker.ietf.org/doc/draft-ietf-vcon-vcon-container/)** — IETF standard container format for conversation data
- **[vCon MCP Server](https://mcp.conserver.io/)** — Model Context Protocol server for AI-powered conversation access
- **[vCon Lifecycle](https://datatracker.ietf.org/doc/draft-howe-vcon-lifecycle/)** — SCITT-based transparency and lifecycle management
- **[vCon Lawful Basis](https://datatracker.ietf.org/doc/draft-howe-vcon-lawful-basis/)** — Consent and legal basis tracking

## Submissions

| # | Project | Team | Description |
|---|---------|------|-------------|
| 1 | **911 First Response** | Shouvik Sharma, Ankita Bhanushali | AI-assisted workflow that processes 911 emergency calls in real time, converting them into structured dispatch actions for first responders |
| 2 | **Apparitions** | David Sikes, Jared Ashcraft | Museum/cultural experience app using vCon and AI to provide contextual, interactive guided experiences for visitors |
| 3 | **Budget Yangu** | Elvis Ogunga | AI-powered personal finance assistant ("My Budget" in Swahili) providing budgeting advice and financial guidance through conversation |
| 4 | **ConsentMate** | Abdurrahman Umar, Berlu (Team Skyline Coders) | AI-powered GDPR compliance dashboard that tracks customer consent, provides compliance scoring, and delivers daily actionable updates |
| 5 | **ConvoLens** | Josphat Mwangi | Customer conversation intelligence platform built for banking and financial services |
| 6 | **ConvoSense** | Collins Omondi | Conversation analysis tool for small to mid-size businesses to improve customer support operations |
| 7 | **Life Canvas** | Sabrina (Valencia College) | Personal life intelligence system that captures everyday moments and turns them into searchable, structured insights using vCon |
| 8 | **Ollie** | Anna Correa | AI-powered platform to help find and rescue lost animals faster through coordinated conversation tracking |
| 9 | **OnePrice Sales Memory** | Joan Ovalles Rosario (Valencia College) | Sales conversation memory system for auto dealerships, giving sales teams persistent memory of customer interactions |
| 10 | **Patanisha** | Charles Wachira | Unified customer support platform that consolidates phone, SMS, email, and chat conversations into vCon-structured records |
| 11 | **TraceConnect** | Jevans Otieno | vCon-powered real-time visibility and compliance platform for global distribution networks |
| 12 | **vChat** | Ahmadu Suleiman | Community mediation platform that records and structures informal agreements for accountability and conflict resolution |
| 13 | **vCohort** | Ziyad Shuaibu, Abdulalim Ladan, Mubarak Ibrahim | Educational platform supporting bootcamps and cohort-based learning in Nigeria, using vCon to track student progress and mentor interactions |
| 14 | **vCon Example App** | Muntaser Syed | Reference implementation demonstrating core vCon functionality for developers |
| 15 | **vCon Intelligence Platform** | Muntaser Syed | Comprehensive multi-module platform for conversation intelligence and analytics |

## Repository Structure

```
vcon-the-hacks/
├── README.md
├── vcons/                          # vCon files for each submission
│   ├── 911-first-response.vcon.json
│   ├── apparitions.vcon.json
│   ├── budget-yangu.vcon.json
│   ├── consentmate.vcon.json
│   ├── convolens.vcon.json
│   ├── convosense.vcon.json
│   ├── life-canvas.vcon.json
│   ├── ollie.vcon.json
│   ├── oneprice-sales-memory.vcon.json
│   ├── patanisha.vcon.json
│   ├── traceconnect.vcon.json
│   ├── vchat.vcon.json
│   ├── vcohort.vcon.json
│   ├── vcon-example-app.vcon.json
│   └── vcon-intelligence-platform.vcon.json
├── transcripts/                    # Raw Whisper transcription output
├── audio/                          # Extracted audio (not committed)
└── LICENSE
```

## vCon Structure

Each vCon file follows the [draft-ietf-vcon-vcon-container](https://datatracker.ietf.org/doc/draft-ietf-vcon-vcon-container/) specification:

```json
{
  "vcon": "0.0.1",
  "uuid": "unique-identifier",
  "created_at": "2026-03-07T12:00:00Z",
  "subject": "VCONIC TADHack 2026 Submission: Project Name",
  "parties": [
    { "name": "Presenter Name", "meta": { "party_type": "human", "role": "presenter" } }
  ],
  "dialog": [
    { "type": "recording", "mediatype": "video/webm", "url": "https://youtube.com/watch?v=..." }
  ],
  "analysis": [
    { "type": "transcript", "vendor": "mlx-community/whisper-turbo", "body": { "text": "...", "segments": [...] } },
    { "type": "summary", "vendor": "claude-opus-4-6", "body": { "summary": "...", "tags": [...] } }
  ],
  "attachments": [
    { "type": "hackathon_metadata", "body": { "event": "VCONIC TADHack 2026", "project_name": "..." } }
  ]
}
```

Each submission vCon contains:

- **Parties** — Presenter(s) who built and demonstrated the hack
- **Dialog** — Video recording of the presentation (YouTube URL + local file reference)
- **Transcript** — Machine-generated transcription with word-level timestamps (Whisper turbo via MLX)
- **Summary** — AI-generated project description, tags, and technology stack
- **Hackathon metadata** — Event information, project name, and YouTube video ID

## Transcription Notes

Transcriptions were generated using [mlx-whisper](https://github.com/ml-explore/mlx-examples/tree/main/whisper) with the `whisper-turbo` model running locally on Apple Silicon. Some proper nouns (project names, people's names) may have minor inaccuracies. The Life Canvas transcript contains a known Whisper hallucination loop at the end due to silence in the source audio.

## Related Resources

- [vCon MCP Server](https://github.com/vcon-dev/vcon-mcp) — The MCP server used in the hackathon
- [vCon Specification](https://datatracker.ietf.org/doc/draft-ietf-vcon-vcon-container/) — IETF vCon container format
- [VCONIC TADHack Blog Post](https://blog.tadhack.com/2025/12/19/vconic-tadhack/) — Event announcement and training session recordings
- [TADHack](https://tadhack.com) — Telecom Application Developer Hackathon

## License

This repository is licensed under the [MIT License](LICENSE). Video content is hosted on YouTube and remains the property of the respective hackathon participants.
