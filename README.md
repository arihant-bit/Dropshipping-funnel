# D2C Workshop Landing Page — deploy

Static site. No build step, no dependencies to install.

## Deploy to Vercel

1. Push this folder's contents to a GitHub repo (`index.html` must sit at the repo root).
2. In Vercel: **Add New → Project → Import** that repo.
3. Framework Preset: **Other**. Leave Build Command empty. Output Directory: leave empty (root).
4. Deploy.

## Before you go live — 3 edits

**1. Razorpay redirect.** The CTAs already point at `https://rzp.io/rzp/4AIfdE6I`. In your Razorpay payment-page settings, set the post-payment redirect to `https://your-domain.com/thank-you`.

**2. Seats counter.** Same block, `seatsLeft: this.props.seatsLeft ?? 37`. Appears in the sticky bar and the final CTA.

**3. Countdown target.** Search for `2026-08-28T23:59:00+05:30` and set your real registration close time.

## Also worth checking

- Two bonus prices are marked with a dashed underline (Media Buying SOP ₹2,499, Shopify Leak Audit ₹1,999) — these were read off a clipped screenshot and are unconfirmed. Fix them, update the `₹27,495` total in two places, and delete the orange note under the total bar.
- Footer links (Privacy, Terms, Refunds, Contact) point at `#`.
- The five dashboard screenshots still show client store names in the Shopify header.
- `thank-you.html` says the Zoom link and files are sent to the number and email used at payment. Change that line if you deliver them another way.

## Files

```
index.html          the landing page
thank-you.html      post-payment page (set as the Razorpay redirect)
support.js          runtime — required, keep alongside the pages
assets/             photo, 8 client logos, 5 dashboard screenshots
```

Fonts load from Google Fonts (Archivo). Everything else is local.
