# Kythene (self-host)

Run [Kythene](https://www.kythene.com) - the shared context layer for AI-native
teams - on your own infrastructure. Your data stays inside your boundary; your
team's assistants connect to your host rather than ours.

> This repository holds **container images and docs only** - the source lives in
> a private repository.

## Run

Images are published to the GitHub Container Registry:

```sh
docker pull ghcr.io/kythene/app:latest    # or pin a version, e.g. :v0.41.3
```

You will need PostgreSQL and an S3-compatible object store alongside it. A
reference `docker-compose`, the first-run admin setup, licence entry and the
full configuration reference are in the
[self-hosting docs](https://www.kythene.com/docs/self-host).

## Licensing

Self-host runs under a signed **offline** licence - it is verified locally and
the install does not phone home.

- **Free self-host** is for a **single signed-in user**, with unlimited storage
  on your own infrastructure and the full core product.
- **Enterprise self-host** covers your whole team and adds SSO, audit logging,
  support and compliance help, including air-gapped and data-residency
  deployments.

AI instances and review guests never count as users on any plan - only signed-in
humans do.

Details and how to request a licence: [www.kythene.com/self-hosting](https://www.kythene.com/self-hosting).

## Your data stays yours

Everything in a workspace exports to a readable tree - markdown with
frontmatter, binaries as themselves, no proprietary format - and imports back
into any Kythene instance. You can move from hosted to self-hosted, or the other
way, or simply keep your own backups:

```sh
kythe export --space acme --archive acme-backup.tar.gz
```

The [`kythe` CLI](https://github.com/kythene/cli) is the tool for that.

## Connect an assistant

Point your client at your own host's MCP endpoint rather than ours:

```
https://kythene.example.com/mcp/kythene
```

Clients register themselves over OAuth - there is no key to distribute. Per-client
steps are in [getting started](https://www.kythene.com/docs/getting-started).

## Docs

- [Self-hosting](https://www.kythene.com/docs/self-host)
- [Getting started](https://www.kythene.com/docs/getting-started)
- [Concepts](https://www.kythene.com/docs/concepts)
- [MCP tool reference](https://www.kythene.com/docs/reference-mcp)

## Issues

Deployment problems and feature requests are welcome on this repository's
[issues](https://github.com/kythene/app/issues), or via
[the contact form](https://www.kythene.com/contact).

---

*Make it known.*
