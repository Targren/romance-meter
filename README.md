# Romance Meter Extension for SillyTavern
Description:

Spice up your roleplay sessions with the Romance Meter, a custom extension for SillyTavern that tracks the romantic connection between you and your AI character (e.g., Ani)!
 
This extension adds a dynamic romance score (0-100+) that evolves through flirty chats, unlocking six distinct relationship levels with tailored behavior prompts.
 
Watch your bond grow from shy first impressions (Level 1) to passionate intimacy (Level 6), complete with a sultry lingerie outfit change at max score.

---

Key features:

- **Progressive Levels:** Six stages (e.g., Downhearted, Intrigued, Intimate) with unique AI responses, injecting flirty or romantic prompts as you level up.
- **Keyword-Driven Scoring:** Earn points with positive words like “love” (+5) or “cute” (+2), balanced by negatives like “hurt” (-5) or “sad” (-2) to keep it challenging.
- **Outfit Dynamics:** Triggers a lingerie switch at 100, with a spiteful revert if the score drops, reflected in the UI.
- **Custom UI:** Real-time progress bar and outfit display, with a reset button to start fresh.

Perfect for roleplayers who love building emotional arcs or testing their charm! Designed for solo chats with characters like Ani, it’s still a work in progress negative levels (-1 to -6) are on the roadmap.

---

# Installation:

1. Clone or download from this repo.
2. Add to your SillyTavern extensions folder.
3. Enable in the extensions settings and reset to start.

---

## Notes:

- Tested with KoboldCpp and Sillytavern 1.13.1
- Solo chat optimized; group chat issues noted - Group Chat currently does not work properly with my extension. 
- Swiping for new responses will count towards the your overall score on the romance meter, so if you continue swiping it will accumulate, hopefully I'll find a way to fix this in the future.

---

## Roadmap: Negative Romance Levels (Coming Soon)

### Planned Features:

- Add Negative Levels (-1 to -6):

- Extend getLevel to include negative tiers: 

    -1 (0 to -15)

    -2 (-16 to -35) 

    -3 (-36 to -60) 

    -4 (-61 to -75) 

    -5 (-76 to -99) 

    -6 (-100 and below) 

- Inject escalating negative prompts in romanceInterceptor on level drops (once per change):

    1: Mildly annoyed, snappy, distant replies.

    2: Frustrated, sarcastic, probing user’s behavior.

    3: Angry, outbursts, questioning trust.

    4: Hurtful, possessive-toxic, tears/insults.

    5: Volatile, jealousy rants, threats to end.

    6: Unhinged psycho

# Negative Scoring:

- Use existing negative keywords (hurt, angry, etc.) for natural drops (-2/-5 per hit), driven by user cruelty, no forced acceleration.

- Outfit and UI Updates:

- Revert to 'normal' outfit on any negative level, with spiteful narration on entry.
- Extend UI bar left (red gradient), show “Hostility Level: X” below 0, and “Fatal Attraction Mode” at -100.

---

MIT License—free to use, modify, and share.

---

Contribute:

Found a bug or have ideas? Open an issue or pull request.
