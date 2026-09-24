PUPSCENE STUDIO SALES FUNNEL v1.3

FILES
- index.html ........ Sales funnel + 3-question interactive ad planner
- payment.html ...... Name/email + payment-method selection
- thank-you.html .... Purchase thank-you + QR + install options
- assets/config.js .. Add live merchant payment URLs here
- assets/install-qr.png .. QR to https://www.pupscenestudio.site

LIVE LINKS ALREADY SET
Demo: https://demo.pupscenestudio.site
Product/App: https://www.pupscenestudio.site
Support: support@pupscenestudio.site

PAYMENT SETUP BEFORE PUBLIC SALES
This static package intentionally does NOT collect card numbers or fake payment success.
Edit assets/config.js and add your live hosted checkout/payment URLs.

Recommended Philippine setup:
1) Maya Business Checkout / Payment Link as the primary hosted checkout, with enabled e-wallet / QR Ph / GCash options plus debit/credit card support.
2) Optional PayPal checkout link for international buyers.
3) Optional bank transfer only as a manual fallback.

For a proper paid-product launch, use a backend/payment gateway webhook to verify PAYMENT_SUCCESS before granting access or treating an order as paid. Configure the gateway success redirect to your deployed thank-you.html. Also configure separate failure and cancellation pages/handling before launch.

THANK-YOU TEST
Open thank-you.html?preview=1 to preview the post-purchase experience without representing it as a verified order.


PRICING / LOCALIZATION
- Current plans: Free (1/day), USD 1.00 Creator (5 generations / 30 days), USD 7.99 Unlimited (30 days). Paid plans support one-time access or monthly subscription.
- index.html and payment.html load assets/pricing.js.
- On Cloudflare Pages Functions, functions/api/localize.js uses request.cf.country to select the visitor currency and retrieves a USD FX rate.
- If that endpoint is unavailable, the browser falls back to locale detection and a public FX lookup; if conversion fails, USD remains visible.
- A manual currency selector is provided for travelers, VPN users, or unsupported geolocation.
- Local currency amounts are display estimates; the secure payment gateway should confirm the final amount.
- Third-party AI video generation/credits are not included in either PupScene plan.

v1.4 currency behavior:
- Selected currency is now the primary displayed price.
- Changing the selector fetches the latest available USD-to-selected-currency exchange rate and recalculates both plans immediately.
- The USD base price remains visible as the billing reference.
- The checkout page uses the same conversion state and refreshes interactively.
