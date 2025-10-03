# Hardware Collective - October 4th Meet Sizzle Reel

## The Concept

This page is a scrolling experience synced to "Fire Walk With Me" by The Black Keys. As the song plays (84 seconds), it auto-scrolls through 11 sections that tell the story of:
1. What the collective is
2. Who Amit is and why he started it
3. What actually happens at meetups
4. Why you should join

Think of it as a sizzle reel that doubles as an onboarding page.

## Story Arc

The narrative follows the song's emotional beats:

**0-35s: Setup** - What we do, who Amit is, what Absurd Industries is about  
**35-52s: The Struggle** - "Hardware is hard" / "bruised soul" moment  
**52-73s: The Community** - How we work together, what open hardware means  
**73-84s: The Invitation** - "Fire walk with me" finale, join us call-to-action

## Content That Needs Work

### Copy Review
All the text lives in `index.html` in the `<section>` tags. Amit should read through and adjust tone/accuracy. Look for:
- Does this sound like how Amit actually talks?
- Are the Absurd Industries descriptions accurate?
- Is the "Full Stack" section selling the right story?

### Images Needed

We need 9 photos for this to work. These are guidelines—use what actually represents the collective well.

**Image list:**
1. **what-we-do.webp** - Where we actually meet. Needs to feel inviting, not intimidating.
2. **who-hosts.jpg** - Amit's photo. Already have this one.
3. **full-stack.jpg** - Full stack work. Could be laptop + breadboard.
4. **why-exists.gif** - Animated! Hardware struggle in action.

**Supporting shots:**
5. **ABSURD.png** - Absurd Industries branding/product shot.
6. **reality.jpg** - Failed or working prototype. Shows the process.
7. **together.jpg** - People working together. Captures the collective vibe.
8. **shipping.jpg** - Finished PCBs or products. The payoff.
9. **obsession.jpg** - Action shot of building. Can be any hands-on work.

**Technical specs:**
- Square aspect ratio (1:1) preferred
- Minimum 1200x1200px
- JPG format
- Try to keep under 500KB each for web performance

**Note:** Amit's photo is already pulling from absurd.industries, so that's covered.

### Links to Update

Two links need replacing before launch:

**Line 216:**
```html
href="https://lu.ma/your-event-link"
```
Replace with actual Luma event URL once created.

**Discord link (line 222) is already set:**
```html
href="https://discord.gg/DUSUtguG2H"
```
This goes to Absurdity Central. Confirm this is the right Discord.

## Technical Notes

### Timing Adjustments

If the sync feels off when you hear the actual song, you can adjust timestamps at line 82-92:

```javascript
const sections = [
    { id: 'hero', title: 'HARDWARE COLLECTIVE', start: 0, end: 7 },
    { id: 'what-we-do', title: 'WHAT WE DO', start: 7, end: 14 },
    // ... etc
];
```

Change the `start` and `end` values to match where story beats should land.

### Audio Length

Currently set to stop at 83 seconds. To change this, edit line 79:

```javascript
const AUDIO_END_TIME = 83;
```

This controls when the audio stops and affects the progress bar calculation.

### File Structure

```
project-root/
├── index.html          # Everything lives here
├── firewalk.m4a        # Licensed audio (don't redistribute)
└── images/             # Create this folder
    ├── meetup-space.jpg
    ├── code-hardware.jpg
    ├── absurd-products.jpg
    ├── workbench.jpg
    ├── prototype.jpg
    ├── collaboration.jpg
    ├── shipped-boards.jpg
    └── soldering.jpg
```

## Content Philosophy

This page represents first contact for most people. The goal is:
- **Welcoming but not pandering** - "Beginners welcome. Experts appreciated."
- **Honest about the work** - Hardware is actually hard. We don't sugarcoat.
- **Conversational, not corporate** - Amit's voice, not a marketing department.
- **Action-oriented** - By the end, they should know exactly how to join.

The copy deliberately avoids:
- Excessive enthusiasm or hype
- Gatekeeping language (no "10x engineers" nonsense)
- Vague promises
- Making it sound easier than it is

## Next Steps

1. Amit reviews and edits copy in index.html
2. Photography session for the 8 images
3. Create Luma event and update link
4. Test full playthrough with actual audio
5. Deploy

---

This is the first of a series. Each meetup gets a different host, different song, different story. This one's Amit's. Make it good.
