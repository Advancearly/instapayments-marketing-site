# InstaPayments marketing site

A responsive, dependency-free marketing site for InstaPayments, published with GitHub Pages. Only `site/` is deployed; no backend, build step, API keys, or third-party scripts are required.

## Preview locally

From the repository root:

```sh
python3 -m http.server 8080 --directory site --bind 127.0.0.1
```

Open <http://127.0.0.1:8080>.

## Editing

- `site/index.html`: content, prices, links, and metadata
- `site/styles.css`: responsive layout and styles
- `site/script.js`: mobile navigation and accessible feature tabs
- `site/assets/`: self-hosted brand and product images
- `site/404.html`: missing-page fallback

Relative assets work on the GitHub Pages repository subpath and a custom domain. A future custom-domain change must also update the 404 fallback if the repository name changes.

## Publishing

Repository: <https://github.com/Advancearly/instapayments-marketing-site>

Select **Settings → Pages → Source → GitHub Actions**. A push to `main`, or a manual run of `.github/workflows/pages.yml`, uploads only `site/` and deploys it to Pages. The workflow uses the official GitHub Pages actions and scoped deployment permissions.

Expected default URL: <https://advancearly.github.io/instapayments-marketing-site/>

The workflow does not change the existing instapayments.io domain or its DNS. No `CNAME` is included.

## Content and source notes

Content was reviewed against <https://www.instapayments.io/> on October 22, 2026. The site preserves the existing checkout, portal, and card-update capabilities; three setup steps; customer quotation attributed to Integrate Your Business; and Essential ($29/month), Growth ($75/month), and Premium ($499/month) pricing with the stated 0.5% transaction processing fee.

The logo and favicon come from the supplied InstaPayments brand assets. Product screenshots are copied from the public marketing site and stored locally:

- Checkout: `46b5ac_a8e9090777814218964bf85c59b0c7ac~mv2.png`
- Card update: `46b5ac_72b8684c5e824cf29d967730827b0c78~mv2.png`
- Billing portal: `46b5ac_7a68dffbf80d4bae8a2f5de95d07360e~mv2.png`

Signup buttons preserve the existing `orgs.instapayments.io/register3` URLs, including plan selection. Log in goes to the existing app. The terms link continues to the existing marketing site's terms page.

The Wix contact form is replaced by explicit email and demo-request links to the displayed business address, `sales@instapayments.io`. These open the visitor's email application; the static site does not send or store messages. This corrects the original email link's `info@mysite.com` placeholder. No trial length, card requirement, new customer metrics, or unsupported product claims have been added.

No payment information is collected by this marketing site. Product screenshots are examples from the original website; signup and billing remain in the existing applications.
