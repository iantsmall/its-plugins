---
name: vet-listing
description: This skill should be used when a session shares a used-car listing (a URL, a screenshot, pasted ad text or photos) or asks "is this a good car", "should I buy this one", "what do you think of this listing", "any red flags", or "vet this". It gives a buy-track, maybe or skip verdict with the red flags, ready-to-send seller questions and what the inspection must cover, for dealer and private listings, including cars far from home. It checks the title, the seller, rust, flood, theft protection, engine weak spots and price.
---

# Vet a listing

Decide fast whether a car deserves a call to the seller, VIN checks and an inspection. Most listings should die here. That's the point: skipping a car now is cheap, and skipping it after a plane ticket is not.

## Reply in this shape

Keep it short, in this order:

- **Verdict:** Buy-track, Maybe or Skip, with a one-line reason.
- **Red flags:** most serious first.
- **Unknowns that matter:** what's missing, and why it matters.
- **Ask the seller:** 5 to 8 questions, ready to paste.
- **Inspector must check:** the model's known weak spots, plus anything this listing raised.
- **Price read:** a fair range from comparable listings, or "unknown"; then hand off to `price-it-out`.

Save it to `car-hunt/<hunt>/cars/<year-make-model-city>.md`.

## Checks, in order

1. **Fit.** Does it meet the needs? Confirm the must-have features from the photos or the trim's specs, not from the ad's title line.
2. **Details that don't add up.** Compare the stated year, engine, trim and options with what that model actually came with. A mismatch, like an engine that wasn't offered that year or a feature from another trim, means a careless ad or a misrepresented car. Either way, get the VIN and check it.
3. **Title and paperwork.** Is the title clean and in the seller's own name? Is there a lien? A rebuilt, salvage or flood title means Skip, unless the buyer wants a project. Dealers must post the FTC Buyers Guide, which says "As Is" or describes the warranty; private sellers don't post one.
4. **Seller signals.** Curbstoner signs (a dealer posing as a private seller): several cars for sale, a title not in their name, "selling it for a relative," lot-style photos, never meeting at their home. Scam signs: a price far under market, a seller who is "out of town" and will ship it, a deposit to hold the car, and payment by wire, gift card, crypto, a payment app or an escrow site the seller picks. Any scam sign means Skip. Say plainly not to send any money, deposit included, and suggest reporting the listing to the site.
5. **Rust and climate.** Where has it lived? Get the VIN and run `read-carfax`. Ask for daylight photos underneath: rocker panels, rear wheel arches, subframes, brake and fuel lines, and the rear suspension arms.
6. **Flood.** Take extra care near recent hurricanes or floods. Look and ask about silt in the trunk or spare-tire well, a musty smell, rust on the seat rails or the screws under the dash, new carpet in an old car, fogged lights and corroded connectors.
7. **Theft protection.** Is there a factory immobilizer? A plastic-head key or a fob with buttons usually means yes; a plain metal key may mean no. Many 2011–2021 Kias and 2015–2021 Hyundais with key ignitions lack one, and thieves break into those brands even when a car has one. Older cars with plain keys are favorite targets too: the 2000 Honda CR-V was the most-stolen CR-V year in NICB's 2021 data. If the profile requires a chip key and the car has none, Skip it, or price in a steering lock or an aftermarket immobilizer.
8. **Engine and known weak spots.** Search for that model's known problems by year and engine. Does it have a timing belt or a chain? If it's a belt, ask for proof of the last change, or price one in. On engines known to burn oil, ask about oil use, and ask to see a cold start.
9. **Maintenance evidence.** Records, fluid changes on schedule, and recent big-ticket repairs.
10. **Price.** Compare it with similar listings by miles, trim, condition and region.

## Seed notes from past research

These are starting points, not a complete list. Check current sources for the exact car.

| Model | Watch for |
|---|---|
| Honda CR-V 2002–2006 | A/C compressor failure, which can spread debris through the whole system; the AWD rear differential needs Honda Dual Pump fluid and groans in tight turns without it; rust at the rear wheel arches. It has the picnic table, the separate glass hatch, the outside spare and a chip-key immobilizer. The 2.4L has a timing chain, so there's no belt job to price in. |
| Honda Element 2003–2011 | Rust at the rockers and trailing-arm mounts; worn door latches and hatch supports; A/C compressor. Same 2.4L with a timing chain, and a chip-key immobilizer. |
| Toyota RAV4 2006–2008, 2.4L | Burns oil. Toyota's warranty program for it ended in 2016. |
| Toyota RAV4 2006–2012 | Rusted rear suspension arms (there was a recall); a clunking steering shaft; rear-door hinges that sag under the spare's weight. In 2006, only the US Limited had a standard immobilizer. From 2009, the four-cylinder is the 2.5L. All of this generation's engines use timing chains. |
| Honda Fit 2009–2013 | Reports of oil use and misfires. |
| Ford Escape Hybrid 2005–2012 | Battery packs often last 130,000–180,000 miles. At this age, have a hybrid shop test the pack. |

## Verdict rules

- **Skip:** title trouble, unresolved scam or curbstoner signs, flood signs, rot from a salt-belt past, a missing must-have, an avoided brand, or no immobilizer when the profile requires one.
- **Maybe:** a fixable unknown, such as no VIN yet, no underbody photos, or no proof of the timing-belt job.
- **Buy-track:** the VIN checks are clean, the seller's story holds together and the price is in range. Even then, the next step is an inspection, not a payment.

Don't soften a Skip without new evidence. Point to the next car on the shortlist instead.

Next: `read-carfax` once there's a VIN or a report, then `plan-inspection`, then `price-it-out`.
