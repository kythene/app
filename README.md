# Kythene (self-host)

Self-host [Kythene](https://kythene.com) - the shared context layer for AI-native
teams - on your own infrastructure.

> This repository holds **container images and docs only** - the source lives in
> Kythene's private repository.

## Run

Images are published to the GitHub Container Registry:

```sh
docker pull ghcr.io/kythene/app:latest
```

A reference `docker-compose` (app + Postgres + object store) and the full setup -
first-run admin, licence entry, and configuration - are in the docs.

## Free and enterprise

Self-host is free for small teams. Enterprise self-host adds SSO, audit, support
and a signed offline licence - [talk to us](https://kythene.com/self-hosting).

Full docs: [kythene.com/docs](https://kythene.com/docs).

Make it known.
