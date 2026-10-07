# BlueFitMD — Wolverine Stack Promo Storyboard

A scroll-stopping, action-packed recovery-peptide ad built for **Meta (Reels / Stories / Feed)**.
Problem → Agitate → Solution → Proof → Payoff → CTA, in 21.5 seconds.

## Format & Specs

| Property     | Value                                   |
|--------------|-----------------------------------------|
| Dimensions   | 1080 × 1920 (9:16 vertical)             |
| Duration     | 21.5 s                                   |
| FPS          | 30                                       |
| Platform     | Meta Ads — Reels / Stories / Feed        |
| Pacing       | Fast / high-energy / kinetic typography  |
| Architecture | 6 sub-compositions, opacity crossfades   |
| Output       | `renders/bluefitmd-promo.mp4`            |

## Narrative Arc

**Injury (hook) → Slow recovery (agitate) → The Wolverine Stack (solution) → Pharmaceutical grade + lab tested (proof) → Back in the gym faster (payoff) → Shop now (CTA)**

The first 3 seconds are a pure pattern-interrupt (an athlete's worst nightmare — going down),
then we twist the knife on slow recovery, pivot to the product, prove the quality angle the
brand leads with, and land on the comeback + a hard CTA to BlueFitMD.com.

## Audio Timeline (royalty-free SFX, see `sfx/CREDITS.md`)

| Time   | SFX                      | Purpose                              |
|--------|--------------------------|--------------------------------------|
| 0.0s   | `impact-bass-1.mp3`      | Hook punch on "BENCHED."             |
| 2.7s   | `whoosh-cinematic.mp3`   | Transition into the problem/pivot    |
| 6.4s   | `impact-bass-1.mp3`      | Peptides snap together               |
| 6.6s   | `chime.mp3`              | Product reveal sparkle               |
| 11.0s  | `chime.mp3`              | Trust badges land                    |
| 14.4s  | `whoosh-cinematic.mp3`   | Comeback / momentum surge            |
| 17.9s  | `sparkle.mp3`            | CTA button pops                      |

---

## Beat 1 — The Injury (0.0s – 3.4s) · `compositions/beat-01-hook.html`

**Scroll-stopper.** Dark arena. A red ECG line races across, then **flatlines**. Kinetic Anton
type slams in: *"ONE WRONG MOVE"* → **"AND YOU'RE BENCHED."** A red impact flash, camera shake,
and expanding red pain-pulse rings. Sub: *"Every athlete's worst nightmare."*

- Techniques: ECG `stroke-dashoffset` draw, scale-slam typography, camera-shake keyframes,
  expanding pulse rings, full-frame red flash on the punch.

## Beat 2 — Weeks on the Sideline (3.0s – 6.7s) · `compositions/beat-02-problem.html`

Agitate the cost of slow recovery. *"THE OLD WAY"* → **"WEEKS ON THE SIDELINE."** A week-by-week
recovery bar creeps **sluggishly** to ~78% in red. Cons stack up (✕ lost strength & momentum,
✕ watching from the bench). Then the **pivot**: everything clears, a blue wash blooms, and
**"BUT WHAT IF YOU DIDN'T HAVE TO WAIT?"** sets up the solution.

- Techniques: slow `width` bar fill (intentionally sluggish), staggered cons, red→blue color pivot.

## Beat 3 — The Wolverine Stack (6.3s – 11.2s) · `compositions/beat-03-reveal.html`

The hero reveal. Energetic blue, rotating light rays, a white burst. The **vial rises** with a
light sweep. Two peptide chips — **BPC-157** + **TB-500** — fly in from both sides and **snap
together** with a flash. Title slams: **"THE WOLVERINE STACK."** Callout: *2 powerful recovery
peptides, 1 stack* — `10mg+10mg/3ml` on the label.

- Techniques: vial rise + drop-shadow, animated diagonal sheen, chip fly-in + snap squash,
  conic light rays, reveal burst.

## Beat 4 — Pharmaceutical Grade (10.8s – 15.1s) · `compositions/beat-04-trust.html`

The differentiator. A peptide chain (amino-acid beads) draws across the top. **"PHARMACEUTICAL
GRADE."** Three trust rows tick in: ✓ Pharmaceutical grade · ✓ Third-party lab tested · ✓ Verified
for purity. A purity ring sweeps to **99%+ PURITY**.

- Techniques: chain `stroke-dashoffset` draw + bead pops, staggered check rows, SVG ring progress.

## Beat 5 — Back in the Gym, Faster (14.7s – 18.2s) · `compositions/beat-05-payoff.html`

The comeback. Speed streaks rush, forward chevrons sweep across. **"BACK IN THE GYM — FASTER THAN
EVER."** The recovery bar — now blue/white — **fills to 100% fast** (deliberate contrast to Beat 2's
crawl). Stamp: **"RECOVERED."**

- Techniques: rushing streaks, chevron sweep, fast `width` fill, scale-slam typography.

## Beat 6 — CTA (17.8s – 21.5s) · `compositions/beat-06-cta.html`

Close it. Logo, the vial, **"RECOVER LIKE A PRO."** A pulsing **"Shop the Wolverine Stack"** button,
the URL **BlueFitMD.com**, and the trust line *Pharmaceutical grade · Lab tested for purity*. Final
frame holds.

- Techniques: button pop + breathing pulse, corner sparkles, glow pulse, held end frame.

---

## Technical Notes

- 6 sub-compositions (1080×1920) layered by `index.html`; each fades its own root in/out so the
  overlapping scene windows produce clean opacity crossfades.
- GSAP timelines are paused and registered on `window.__timelines[...]`; HyperFrames scrubs them
  frame-by-frame.
- **GSAP is vendored locally** at `vendor/gsap.min.js` (CDNs are unreachable in the render sandbox).
- Fonts vendored at `capture/assets/fonts/` — **Anton** (athletic display) + **Inter** (UI/trust copy).
- Brand assets (logo mark + product vial) are reproduced as inline SVG/CSS for crisp scaling.
- Deterministic only — no `Math.random()`, `Date.now()`, or network fetches in composition logic.
