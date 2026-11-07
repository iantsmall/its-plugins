---
name: setup-car-hunt
description: This skill should be used when a session mentions "set up my car hunt", "car-hunt setup", "save my car-buying profile", "update my car profile", "use my car defaults", or when another car-hunt skill finds no car-hunt/profile.md at the start of a real search. Run it once per household, and again when something durable changes, such as a move, a new parts habit or a brand to avoid. It records where the car will be registered, how the buyer pays and wrenches, and the house rules (rust, theft, unseen cars) that every other car-hunt skill applies.
---

# Set up the car hunt

Capture the facts that don't change from one purchase to the next, once, so the other skills stop re-asking them. Questions about a specific purchase (budget, size, features) belong to `grill-car-needs`, not here.

## What the profile holds

- **Home and registration.** The city, county and state where the car will be registered. This decides sales tax, registration paperwork, inspection rules, and how much road salt the car will live in.
- **Paying.** Cash, a loan or a trade-in as the usual approach.
- **Wrenching.** How much the buyer fixes themselves and where they buy parts. This changes how scary a known repair is.
- **Brands.** An avoid list and a deprioritize list, each with its reason, so later skills can explain a skip.
- **House rules.** Rust tolerance, theft protection, how far they'll travel to buy, and what it takes to buy a car they can't see.
- **Other household vehicles.** A new car can specialize when another car already covers long trips or hauling.

## Ian's defaults

When the buyer is Ian, or the user says "use my defaults", pre-fill these and confirm them in one pass:

- **Home:** Rochester, NY (Monroe County), so New York registration. Sales tax is 8% combined in Monroe County, charged at registration even when the car is bought out of state. Re-check the rate.
- **Parts:** RockAuto. Prefers older, simple cars he can work on himself.
- **Avoid:** GM brands (Chevrolet, GMC, Buick and Cadillac, plus the old Pontiac and Saturn), from personal experience.
- **Deprioritize:** Subaru, because parts and repairs for its known weak spots cost more.
- **Rust:** home is in the salt belt, so prefer cars that lived in low-salt states.
- **Theft:** require a factory immobilizer, meaning a chip key or a fob.
- **Unseen cars:** require an independent pre-purchase inspection or a dealer return window.

## How to run it

Ask in one turn. Show the defaults, if any apply, and list only the fields still missing. Accept "yes, all of that" as an answer. Don't grill here: a profile should take a minute.

## Save it

Write `car-hunt/profile.md` in the working folder, using this template. If files can't be saved, show the filled-in template in the reply and tell the user to paste it back next time. Put it in long-term memory only if the user asks; it's a working document.

```markdown
# Car-hunt profile
Updated: YYYY-MM-DD

## Home and registration
- Registers in: city, county, state
- Sales tax at registration: rate (source, date checked)

## Paying
- Usual approach: cash / loan / trade-in

## Wrenching
- Does their own work: none / basic jobs / most jobs
- Parts source:

## Brands
- Avoid: brands (why)
- Deprioritize: brands (why)

## House rules
- Rust:
- Theft:
- Unseen cars:
- Max travel to buy: miles, or "ship only"

## Other household vehicles
- Year, make, model: what it's used for
```

Next: `grill-car-needs` to start a purchase.
