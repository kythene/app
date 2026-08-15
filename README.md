# Kythene, self-hosted

Kythene is where a team and their AI instances work on each other's output: publish any result, review it down to the individual block, approve it, and have the feedback land back in the AI that made it, with the reviewed work accreting into a memory the whole team recalls.

Self-hosting keeps all of that inside your own network - your servers, your data,
including the embeddings behind recall. This repository is how you run Kythene on
your own infrastructure: the published container image, and the guide that goes
with it.

> **Just want it hosted?** Sign up at [kythene.com](https://kythene.com) and skip
> all of this. There is a free tier for one person.

## The image

```
ghcr.io/kythene/app:latest
```

Pin a release for a reproducible deploy, for example
`ghcr.io/kythene/app:v0.83.0`. The image is the same Kythene the hosted
service runs; a self-host instance serves its MCP endpoint on your own domain.

## Run it

You need Docker, a Postgres with the `vector` extension, an S3-compatible object
store, and a reverse proxy terminating TLS in front of the app (the app itself
serves plain HTTP - never expose its port directly). The complete single-node
stack (app plus its own Postgres and MinIO), the annotated environment template
and the step-by-step guide live here:

**[www.kythene.com/self-hosting](https://www.kythene.com/self-hosting)** ·
**[www.kythene.com/docs/self-host](https://www.kythene.com/docs/self-host)**

On boot the app applies its migrations forward (idempotent) and starts serving.
On a fresh instance the first person in becomes the administrator.

## Self-host tiers

- **Free self-host** - Free (one signed-in user)
- **Self-host Team** - $150 per user / year (billed annually · from 5 users)
- **Enterprise self-host** - Contact us

A free self-host instance needs no licence key. A licence lifts the seat cap to
the seats your plan includes and unlocks its entitlements. Licence validation is
offline - only the optional renewal check is a network call - so a paid instance
can run fully air-gapped with that check turned off.

Buy Self-host Team at
[kythene.com/buy?sku=selfhost-team](https://kythene.com/buy?sku=selfhost-team&cycle=annual),
or [talk to us](https://www.kythene.com/self-hosting/request) about Enterprise
self-host.

## Connect an assistant

Kythene is a remote, streamable-HTTP MCP server. Point your client at your
instance's endpoint (`https://<your-domain>/mcp/kythene`) and it registers itself
over OAuth - there is no key to copy.

## Licence

Kythene is proprietary software - see [LICENSE](./LICENSE). This repository is the
public self-host landing page and carries no source.
