# key-panel

Static website publishing is configured via GitHub Pages.

## Shareable Link

Your site is available right now via HTML preview:

`https://htmlpreview.github.io/?https://github.com/pushkar4888/key-panel/blob/main/index.html`

This URL renders the live `index.html` from your repository and can be shared with customers immediately.

## GitHub Pages Deployment

Official GitHub Pages publishing can use:

`https://pushkar4888.github.io/key-panel/`

However, this repository still needs Pages enabled in GitHub settings. The current workflow is set to manual dispatch only, because automatic enablement requires a personal GitHub token and repository settings access.

To enable GitHub Pages:

1. Open the repository on GitHub.
2. Go to `Settings` > `Pages`.
3. Choose `main` branch and `/ (root)`.
4. Save and wait a few minutes.

After that, run the workflow manually from the Actions tab or push another change.

## Deployment

The repository includes a GitHub Actions workflow at `.github/workflows/pages.yml` that can publish the site once GitHub Pages is enabled.

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

