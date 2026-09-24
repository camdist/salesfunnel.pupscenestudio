PUPSCENE STUDIO SALES FUNNEL v1

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
