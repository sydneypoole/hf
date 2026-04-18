# HongFu Release Package v1.0.3-test

This release package was generated from private source repository `sydneypoole/hongfu` at commit `7dc3013782251b09d61196d4a70647ad1374eedc`.
It contains deployment artifacts only and does not include application source code.

## Image

```text
ghcr.io/sydneypoole/hongfu:v1.0.3-test
```

## Included files

- `image.txt` — image reference only
- `image.json` — image metadata, release name, source repo, and commit SHA
- `deploy/docker-compose.ghcr.yml` — compose example for this image
- `deploy/runtime.env.example` — compose variables with `IMAGE_REF` prefilled to this release
- `deploy/app.env.example` — application runtime `.env` template mounted to `/app/.env`

## Quick start

1. Copy `deploy/runtime.env.example` to `deploy/runtime.env`
2. Copy `deploy/app.env.example` to your persistent runtime `.env` path
3. Start with:

```bash
docker compose --env-file deploy/runtime.env -f deploy/docker-compose.ghcr.yml up -d
```

4. Check health:

```bash
curl http://127.0.0.1:<your-port>/health
curl http://127.0.0.1:<your-port>/api/health
```
