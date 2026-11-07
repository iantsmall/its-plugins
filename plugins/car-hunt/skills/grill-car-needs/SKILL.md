---
name: grill-car-needs
description: This skill should be used when a session mentions "grill me on what car I need", "help me figure out what car to get", "what should we look for in a car", "we need a car for...", "replace my car", or starts a car purchase without clear criteria such as budget, size, must-have features, drivetrain or daily miles. It interviews the buyer one question at a time until every decision that would change the search is settled, then writes the hunt's needs file. Self-invoke when find-cars or vet-listing is asked for while the needs are still vague.
---

# Grill the car needs

Interview the buyer one question at a time. After each answer, ask the question that would most change which cars you'd look at. Stop when another answer wouldn't change the search.

Read `car-hunt/profile.md` first, and don't re-ask anything it settles.

## Why one at a time

People answer the first question carefully and skim the rest. One question at a time also lets an answer delete later questions: "it's the around-town car" removes the road-trip questions.

## Decisions to settle

Go roughly in this order, and skip whatever the profile or the conversation already answers.

1. **The job.** Daily driver or second car? Who drives it? Ask for the miles on a typical day, the longest regular day, and town versus highway. This sets the range needed from anything electric, and how much wear matters.
2. **What it carries.** People, cargo, crates, pets or tools, and how often. Does the floor need to be flat, or easy to clean?
3. **Size.** The smallest and biggest acceptable. If they name a car they loved, ask what they loved about it. The features usually matter more than the looks, and features point to other models.
4. **Weather.** Snow and hills? Is all-wheel drive wanted, or will front-wheel drive with winter tires do?
5. **Budget.** Cash on hand, any car to sell and its rough value, and a hard ceiling for the all-in cost. Tell them tax, fees and transport come on top of the sticker price; `price-it-out` does that math.
6. **Age and wrenching.** Older and simple, or newer with less to fix? How much will they repair themselves?
7. **Powertrain.** Gas, hybrid, plug-in or electric? Is a manual okay, or required?
8. **Must-haves versus nice-to-haves.** Ask why each one matters. The why often opens up models they hadn't considered.
9. **Deal-breakers.** Brands, body styles, and technology they don't trust.
10. **How far they'll go.** Local only, drive or fly to buy, or ship it? Are private sellers okay, or dealers only? Is a return window needed?

## Name conflicts out loud

If answers fight each other, such as "a small car" and "carries six crates", say so and ask which wins. Don't settle it silently inside the search.

## Write the needs file

Write `car-hunt/<hunt-name>/needs.md`, suggesting a hunt name like `2026-daily-driver`. Add candidate models only once the buyer agrees to them. For each one, mark which trims and years have the must-haves, since features often change by trim.

```markdown
# Needs: hunt name
Updated: YYYY-MM-DD

## The job
## Must-haves (and why)
## Nice-to-haves
## Deal-breakers
## Budget
- Cash:
- From selling: car, rough value
- All-in ceiling:
## Search limits
- Years and miles:
- Where: states, max distance, shipping okay?
- Sellers: private, dealer or both; return window needed?
## Candidate models (agreed)
| Model and years | Trims with the must-haves | Why it's on the list |
|---|---|---|
```

Next: `find-cars`.
