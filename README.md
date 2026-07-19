# locate-website

Public marketing / checkout site for Locate (Netlify).

## Related product docs (in the Locate app repo)

App + API live in [UAO-Aura/Locate](https://github.com/UAO-Aura/Locate):

- Blog stories, manual Drop a pin, profanity masking, blog comment tips — see app feed + `locate-social/PROFANITY.md` and `locate-social/STRIPE-BALO.md`
- Admin moderation panel is served by the API at `/admin` (`locate-social/admin`)
- Tip payouts: platform Stripe Checkout → `author_tip_balances` ledger; admins pay authors manually (not Stripe Connect)

No new website env vars for tips — Checkout uses existing `STRIPE_SECRET_KEY` on the API.
