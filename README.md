# GoPrep Store Matches

Which supermarket product to buy for each of [GoPrep](https://www.goprep.pro)'s 231 recipe ingredients, at the big German
chains (ALDI, Lidl, REWE, EDEKA, Kaufland, Netto, PENNY and more): product, pack size, price and price per kg.

**Open it:** https://joaquin-duran.github.io/goprep-store-matches/ — ask the GoPrep team for the password.

## Using it

- **Ingredients** lists every ingredient by category. Open one to see the product picked at each chain, why it was
  picked, how its price per kg compares with GoPrep's catalogue, and the other products the search found.
  Mark each pick **OK** or **No**, or add a better product with **Use for …**.
- **All products** searches about 25,700 products by name, brand, category or EAN. Each product shows the ingredients
  it is assigned to, with the model's certainty from 1/5 (least sure, usually a substitute) to 5/5. Filter by chain,
  source or certainty, sort least certain first, and mark each assignment **OK** or **No** right there — or assign
  a product to an ingredient yourself.
- Your decisions are kept in your own browser. When you're done, click **Download my decisions** and send the file to
  the GoPrep team.

## Where the data comes from

- **Receipts:** [Open Prices](https://prices.openfoodfacts.org) by Open Food Facts — crowdsourced receipts and shelf
  photos from German stores, Oct 2024 – Oct 2026. Licensed under the
  [Open Database License 1.0](https://opendatacommons.org/licenses/odbl/1-0/); the ingredient-to-product table derived
  from it is available under the same licence on request.
- **REWE shop listing:** REWE's online assortment of 8–9 Sept 2025, as collected by
  [L480/rewe-price-data](https://github.com/L480/rewe-price-data).
- Products were matched to ingredients by search words plus a language model, and are being reviewed by hand.

## About this repository

The page's data is encrypted (AES-256-GCM, key derived from the password with PBKDF2-SHA256, 600,000 rounds), so the
files here contain no readable product list. The page is generated from GoPrep's private repository; changes made here
are overwritten on the next build.
