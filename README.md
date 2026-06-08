# key-panel

Static website publishing is configured via GitHub Pages.

## Shareable Link

After you push changes to `main`, GitHub Pages can publish the site at:

`https://pushkar4888.github.io/key-panel/`

Use that URL to share the website with customers once the workflow completes successfully.

## Deployment

The repository includes a GitHub Actions workflow at `.github/workflows/pages.yml` that publishes the site from the `main` branch.

## DDoS Protection

This site is a static HTML site, so the best way to add DDoS protection is to use a CDN / security proxy in front of GitHub Pages.

Recommended setup:

1. Use Cloudflare as a proxy for your GitHub Pages domain.
2. Point your custom domain to GitHub Pages using Cloudflare DNS.
3. Enable Cloudflare security features:
   - "Under Attack Mode" while you suspect a DDoS event
   - Firewall rules to block suspicious traffic
   - Rate limiting for repeated requests
   - Bot management and high security level
4. Use Cloudflare caching to reduce origin load and improve availability.

> Note: A static site itself cannot stop network-layer DDoS attacks. A fronting service like Cloudflare provides effective protection.

## Notes

- After pushing to `main`, GitHub Pages will deploy the site automatically.
- If you want a custom domain, add a `CNAME` file and configure the domain in both GitHub Pages and Cloudflare.

