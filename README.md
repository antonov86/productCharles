# Product Charles &mdash; Landing Pages

Static landing pages for ProductCharles.com funnels, served via GitHub Pages on `go.productcharles.com`.

## Structure

```
/                      Root redirect to productcharles.com
/blueprint/            PM Career Blueprint lead magnet landing page
/blueprint/thank-you/  Post-signup confirmation + PDF download
/blueprint/assets/     Page-specific assets (PDF, images, CSS, JS)
/shared/               Assets reused across all landing pages
/404.html              Branded 404 fallback
/CNAME                 Custom domain config (go.productcharles.com)
```

## Adding a new landing page

1. Create a new top-level folder (e.g. `/scorecard/`).
2. Inside it, place `index.html` and any page-specific assets in `assets/`.
3. Reuse anything from `/shared/` you can.
4. Commit + push. GitHub Pages auto-deploys to `go.productcharles.com/<folder>/`.

## Form integration

Forms POST to a GoHighLevel inbound webhook. The webhook URL is hardcoded in each page's submit handler. On successful submission, the user is redirected to that page's `thank-you/` subfolder where the lead magnet is delivered.

## Deploying

GitHub Pages is configured to serve from the `main` branch root. Any push to `main` deploys automatically (typically within 60 seconds).
