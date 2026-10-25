# GGG-AI-ROUTER

**One gateway for AI models, with a sovereign lane and a non-sovereign lane.**

Built by GGG TechLab, Global Purchasing Solutions LLC. Based on the MIT-licensed [OmniRoute](https://github.com/cheaper-inference/OmniRoute) project.

> **Status: in preparation.** This public repository is the open-source base: a fork of OmniRoute release 3.8.53. GGG's own additions are proprietary and are developed in a private repository; they are not published here.

## What GGG-AI-ROUTER will do

- **One address for every app.** A single OpenAI-compatible endpoint that any application can call.
- **Sovereign lane.** Requests marked sovereign go only to models running in a cloud region the operator chooses. If that region is unavailable, the request is refused, not sent somewhere else.
- **Non-sovereign lane.** All other requests go to the best available outside provider: free models first, then paid back-up models within a monthly spending limit.
- **Settings that survive a restart.** Providers and settings are kept in a database, not in memory.
- **Usage you can see.** Every call is recorded with model, lane, tokens, cost and speed.

## Planned build on Google Cloud

| Part | Google Cloud service |
|---|---|
| Gateway | Cloud Run |
| Settings and state | Firestore |
| Provider keys | Secret Manager |
| Sovereign models | Vertex AI regional endpoints, or an open-weight model on the operator's own GPU |
| Usage data | BigQuery |

## Credits and licence

- GGG-AI-ROUTER is based on [OmniRoute](https://github.com/cheaper-inference/OmniRoute) and its contributors. OmniRoute's original copyright notice and MIT licence are kept unchanged in [LICENSE](LICENSE).
- GGG's own additions (including the sovereign lane, the GGG settings store and the GGG usage reporting) are proprietary to Global Purchasing Solutions LLC, all rights reserved. They are kept in a private repository and are not licensed for reuse.
- GGG-AI-ROUTER is an independent product of Global Purchasing Solutions LLC and its divisions GGGPlatforms.com and GGG TechLab. None of them is affiliated with, sponsored by or endorsed by the authors of OmniRoute.

See [NOTICE.md](NOTICE.md) for details.

## Security

- Never commit API keys, passwords or customer data to this repository. Keys belong in a secret manager.
- To report a security issue, e-mail support@gggplatforms.com. Please do not open a public issue for security problems.

## Contact

GGG TechLab · Global Purchasing Solutions LLC · 16192 Coastal Highway, Lewes, Delaware 19958, USA
sales@gggplatforms.com · support@gggplatforms.com · [www.gggplatforms.com](https://www.gggplatforms.com)
