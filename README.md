# Forma Studio
Independent React/Vite portfolio; no SDK or key is installed. Includes optional consent controls that do nothing until the monitoring script is installed. Uses hash navigation and same-origin JSON fetches, plus deliberate missing resource and JavaScript error for testing.

## Local
Node.js 22: `npm install`, `npm run dev`, then `npm run build` and `npm run preview`. Commit the generated package-lock.json after successful installation.

## GitHub Pages
Use an empty public repository named `YOUR-USERNAME.github.io` for a dedicated user site (do not overwrite an existing site). The current security platform verifies domain roots, so a repository subpath alone is insufficient. Alternatively use a dedicated custom domain. Push this project's contents including `.github/workflows/pages.yml` to main. In Settings > Pages > Build and deployment > Source choose GitHub Actions. Run the workflow if necessary. Use the actual deployed URL.

## Ownership and integration
Register site in AI Security Platform as Source Code / Browser Runtime. Put exact public verification text into `public/.well-known/ai-security-verification.txt`, commit and deploy. Verify the expected root URL returns the text, then check ownership in the platform. Generate public browser identifier. Run Connector on this repo root, select Browser Runtime and manual consent, preview and apply. Commit/push and redeploy. Never include private telemetry key. Open the deployed site, click Enable optional monitoring, visit Home/Work/About, click Fetch project data twice, Request missing resource, Test JavaScript error. Wait for the 15-second SDK flush and UI refresh. Compare Browser metrics (page visits, requests, errors). Disable optional monitoring to stop collection. Consent is per page load. CPU/RAM/Disk and direct server traffic are not available through Browser SDK.
