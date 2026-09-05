# AI Trip Planning Mode

Use this reference only when the user wants the skill to research and design the trip rather than transform an existing itinerary.

## Intake

Collect the smallest useful brief. Ask together rather than one question per turn when possible:

1. Destination or candidate region, departure point, dates/season, and number of days.
2. Travelers, children/older adults, mobility limits, and any driving or hiking constraints.
3. Interests, must-do items, desired pace, transport preference, and budget band.
4. Lodging already booked or preferred overnight bases.
5. Avoidances, dietary needs, and whether the user wants iconic highlights, quieter alternatives, or a mix.

Do not ask again for facts already present in the conversation. If the user says “everything is up to AI,” choose balanced defaults, disclose them briefly, and continue.

## Research Standard

- Browse the web because itinerary feasibility and destination information are time-sensitive.
- Prefer official tourism boards, attraction operators, park/heritage authorities, transport operators, and government road or weather services.
- Use map services or reliable geographic sources to validate order and approximate travel time.
- Use current editorial sources only for subjective recommendations or when official sources do not cover the question.
- Cross-check critical closures, seasonal access, reservations, road restrictions, and transport schedules.
- Record source URLs and access date in working notes. Cite the useful sources when presenting the itinerary.
- Treat live weather as relevant only near departure. For distant travel, use seasonal climate guidance and label it as such.

## Itinerary Construction

Build the route around geography and energy, not a list of popular places.

- Choose practical overnight bases before filling daily stops.
- Cluster nearby stops and avoid unnecessary backtracking.
- Include realistic driving, parking, walking, queue, meal, and rest buffers.
- Limit each day to a plausible number of anchor experiences. Add optional stops separately.
- Put weather-sensitive or capacity-limited activities in the best slot and provide a fallback when worthwhile.
- Identify reservations, tickets, permits, driving requirements, trail difficulty, and important safety notes.
- For domestic China, consider holiday crowding, scenic-area shuttle systems, reservation identities, high-speed rail, and regional driving conditions.
- For international travel, consider visa/entry assumptions only when relevant, local driving rules, payment, connectivity, language, and holiday closures.

## Proposal Before Artwork

Present a concise planning draft containing:

- Trip concept and chosen pace.
- Recommended overnight bases.
- One line per day with ordered stops and approximate time blocks.
- Major transit legs.
- Reservations and risk notes.
- Optional substitutions or one meaningful tradeoff, only where useful.
- Sources for time-sensitive claims.

Ask the user to confirm the route and major tradeoffs. Do not spend image-generation budget on an unconfirmed plan unless the user explicitly requested autonomous end-to-end execution.

## Handoff To Journal Production

After approval:

1. Convert the route into the standard journal manifest.
2. Decide whole-trip versus single-day output and page count.
3. Research or source appropriate visual references when user photos are absent.
4. Preserve any facts marked “verify before departure” in a practical card rather than presenting them as fixed.
5. Generate the journal using the destination-specific domestic or international visual branch.

## Failure Prevention

- Never optimize for checking off the maximum number of attractions.
- Never claim a route is accurate because a decorative illustrated map resembles a real map.
- Never mix tentative suggestions into confirmed bookings without labeling them.
- Never present estimated costs or drive times as guarantees.
- Never omit a known seasonal closure merely because it disrupts the ideal-looking route.
