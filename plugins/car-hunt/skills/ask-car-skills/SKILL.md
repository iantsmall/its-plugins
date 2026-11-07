---
name: ask-car-skills
description: This skill should be used when a session mentions "car hunt", "the car-hunt skills", "which car skill", "help me buy a car", "I need a new car", "used car shopping", or asks how the car-buying skills fit together. It is a self-triggering index — read it to decide which sibling skill (setup-car-hunt, grill-car-needs, find-cars, vet-listing, read-carfax, plan-inspection, price-it-out, negotiate-car, bring-it-home) fits the moment, even when the user never names one. Once the right skill is clear, invoke that one instead, since it carries the actual guidance.
---

# Car hunt: pick the right skill

Buying a used car is a chain of small decisions. Each skill in this plugin handles one link and hands off to the next, so only the guidance that matters right now gets loaded.

## The flow

| Step | Skill | Use it when | Leaves behind |
|---|---|---|---|
| 0 | `setup-car-hunt` | Once per household, or when something durable changes (a move, a new rule) | `car-hunt/profile.md` |
| 1 | `grill-car-needs` | Starting a purchase, or the criteria are fuzzy | `car-hunt/<hunt>/needs.md` |
| 2 | `find-cars` | Searching for listings, or refreshing the list | `car-hunt/<hunt>/shortlist.md` |
| 3 | `vet-listing` | A specific listing is on the table | `car-hunt/<hunt>/cars/<car>.md` |
| 4 | `read-carfax` | A VIN or a history report is in hand | A "History" section in the car file |
| 5 | `plan-inspection` | The car survived vetting and money is close | An inspection plan, then the results |
| 6 | `price-it-out` | A price is on the table, and always before an offer | The out-the-door total and a walk-away number |
| 7 | `negotiate-car` | Ready to make or answer an offer | The offer and the messages to send |
| 8 | `bring-it-home` | The deal is agreed: transport, plates, insurance, registration | A paperwork checklist |

Steps repeat and get skipped. A quick "is this a good price?" goes straight to `price-it-out`, and a pasted listing goes straight to `vet-listing`. Don't block a quick question on setup.

## Self-trigger index

| Situation | Invoke |
|---|---|
| No `car-hunt/profile.md` yet, and the user is starting a real search | `setup-car-hunt` |
| "What car should we get?", or the criteria are missing or conflict | `grill-car-needs` |
| "Find me...", "what's for sale", "pull listings" | `find-cars` |
| A listing URL, screenshot, ad text or photos | `vet-listing` |
| A VIN, or a Carfax, AutoCheck or NMVTIS report | `read-carfax` |
| "Should I get it inspected?", or a car is about to be bought unseen | `plan-inspection` |
| "Is this a good price?", "what will it cost me?" | `price-it-out` |
| "What should I offer?", or a counter-offer arrived | `negotiate-car` |
| "How do I get it home?", temporary plates, the DMV, registration | `bring-it-home` |

More than one row can apply. Run them in flow order.

## The hunt folder

When files can be saved, every skill reads and writes here, so nothing gets asked twice:

```
car-hunt/
├── profile.md                 # setup-car-hunt
└── <hunt-name>/               # one folder per purchase, e.g. 2026-daily-driver
    ├── needs.md               # grill-car-needs
    ├── shortlist.md           # find-cars
    └── cars/
        └── <year-make-model-city>.md   # vet-listing starts it; later skills add sections
```

When files can't be saved (a plain chat), keep the same sections in the conversation. End each step with a short summary the user can paste into the next session.

## Rules every car-hunt skill follows

- **A listing is a sales pitch.** Check its claims against the VIN, the history report, the photos and the inspection.
- **Condition beats reputation.** A well-kept average car beats a neglected "reliable" one, especially at 15 or more years old.
- **No money before the checks.** Nothing moves until the title matches the seller's ID, the VIN checks come back clean and the car has been inspected. Never wire money, or pay a deposit by gift card, crypto or payment app, to a seller you haven't met.
- **Prices and rules go stale.** Date every price and say where it came from. Re-check tax rates, fees and DMV rules with a search whenever the answer depends on them.
- **Speak plainly.** Short sentences, and say what to do next.

## Boundaries

These skills give research, checklists and drafts. They don't replace a mechanic's inspection, a DMV clerk's answer or legal advice.
