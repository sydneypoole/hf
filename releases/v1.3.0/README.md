# HongFu Release Package v1.3.0

This release package was generated from private source repository `sydneypoole/hongfu` at commit `f5c825411b088ee823e66b6cff3d66a5b272e0c4`.
It contains deployment artifacts only and does not include application source code.

## Image

```text
ghcr.io/sydneypoole/hf:v1.3.0
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
