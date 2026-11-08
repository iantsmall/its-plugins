---
name: find-cars
description: This skill should be used when a session mentions "find me cars", "search listings", "look for a used ... for sale", "what's for sale near...", "find a rust-free...", "pull listings", or asks to refresh a car shortlist. It searches live listings for the hunt's candidate models, looks in low-salt states first when the buyer lives in the salt belt, drops the obvious losers, and writes a ranked shortlist with a quick market read. It uses the CarGurus connector's listing tools when they're available.
---

# Find cars

## Before searching

Read `car-hunt/profile.md` and `car-hunt/<hunt>/needs.md`. If the budget, the candidate models or the travel limit are missing, run `grill-car-needs` first. Ask rather than guess, because a wrong guess wastes the whole search.

## Where to look

- **The CarGurus connector.** If its listing tools are connected (for example `vehicle-listing-search` and `vehicle-listing-detail`), use them first. Filter by model and years, price, mileage, location or radius, and drivetrain. Open the details of anything promising.
- **Otherwise,** search the web across CarGurus, Cars.com, Autotrader, Carfax listings, dealer sites, Facebook Marketplace and Craigslist. Ask the user to paste any listing you can't open.
- **Salt-belt buyers shop low-salt states first.** Carfax counts 27 salt-belt states, Virginia among them. The inland Southeast, Tennessee, Texas and the Southwest are the usual targets. But the lot's address isn't the car's history: about a quarter of the used cars for sale in Georgia were registered in salt-belt states before, most often New York. `read-carfax` settles where a car really lived.
- **Flood markets.** After hurricanes or big floods, treat the Gulf Coast, Florida and the coastal Carolinas as areas that need flood checks.
- **Return windows** suit buyers who can't inspect in person. CarMax gives 10 days (under 1,500 miles) and Carvana gives 7 days (400 miles). Both mostly sell newer cars. Re-check the terms.

## First-pass filter

Don't vet deeply yet. Just drop the obvious losers:

- Rebuilt, salvage or flood titles, unless the buyer wants a project.
- No VIN available, or a seller who won't give one.
- A price about 30% or more below comparable listings, with no explanation. That usually means a scam or a hidden problem.
- Anything outside the needs: years, miles, budget, avoided brands, or a missing must-have. Check the trim and not just the model name, because features change by trim.
- Engines or years known to be bad, as named in the needs or found in research.

For each keeper, record the seller type, location and distance, price, miles, trim, drivetrain, the VIN if shown, days listed or price drops, and the link.

## Write the shortlist

Write `car-hunt/<hunt>/shortlist.md`: a table ranked best first, with one line on why for each car. Mark every row "unverified". Search snippets go stale, so confirm a car is still for sale before anyone travels.

Add a short market read for each model: the price range you saw for similar years and miles. `price-it-out` and `negotiate-car` use it as comparables.

Next: `vet-listing` on the top three to five.
