# VibeNest Template: Gatus

Thin deployment adapter for [Gatus](https://github.com/TwiN/gatus), built for a predictable VibeNest one-click launch.

The adapter keeps the upstream product unchanged and provides only deployment-safe defaults:

- official `twinproduction/gatus` image;
- fixed public compose service `app` on port `8080`;
- repository-owned read-only starter configuration without secrets;
- two harmless example checks that users replace after deployment;
- no database or persistent volume required for the starter recipe.

The public dashboard has no configuration editor. Change checks in `config.yaml` and redeploy the repository.

## Smoke checklist

1. Deploy with build pack `docker-compose`, compose file `/docker-compose.yml`, internal port `8080`.
2. Confirm the application reaches `running`.
3. Open the public URL and verify the Gatus dashboard renders the two starter checks.
4. Confirm the response carries `X-Robots-Tag: noindex, nofollow` for the shared proof instance.

Upstream: https://github.com/TwiN/gatus
