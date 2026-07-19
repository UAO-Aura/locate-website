# locate-website

Public marketing / checkout site for Locate (Netlify).

## Related product docs (in the Locate app repo)

App + API live in [UAO-Aura/Locate](https://github.com/UAO-Aura/Locate):

- Blog stories, manual Drop a pin, profanity masking, blog comment tips — see app feed + `locate-social/PROFANITY.md`, `locate-social/STRIPE-BALO.md`, and **`locate-social/AUTHOR-PAYOUTS.md`**
- Admin moderation panel is served by the API at `/admin` (`locate-social/admin`) — includes **Tips** (direct rails + legacy ledger)
- **Tip payouts:** tips go **straight to the author** via Stripe Connect Express, PayPal, Wise, or Payoneer. Locate does **not** hold new tip money and never collects card/bank numbers in the app. Legacy `author_tip_balances` are historical only.

No new website env vars for tips — Checkout / Connect use existing `STRIPE_SECRET_KEY` on the API (plus optional `PAYPAL_*`).
