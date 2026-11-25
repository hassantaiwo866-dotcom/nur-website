# Nūr Website — How Nūr Works Section

**Status:** Initial homepage implementation committed; build and browser verification pending  
**Date:** 25 November 2026  
**Branch:** `feature/website-design-system`

## 1. Purpose

Explain Nūr's core approach immediately after the homepage Hold demonstration.

The visitor should understand that Nūr is not only about blocking distractions or preventing unwanted actions. It is intended to support a wider process: protection, self-control, recovery, rebuilding, living intentionally, learning and adapting.

This section explains the product philosophy. It must not imply that every part of this system is already implemented or available in the current app.

## 2. Core message

**Headline:** Change is a process. Nūr helps you work through it.

**Supporting copy:**

Real progress is not a perfectly straight line. Some days you protect your attention. Some days you need to recover and begin again. Nūr is being built to support the whole process—not just the moment when things go wrong.

## 3. The seven-part cycle

Present the cycle as a connected, repeatable framework—not a staircase, scorecard or linear achievement path:

1. **PROTECT — Create healthier boundaries.** Reduce exposure to things that pull you away from your intentions. Protection tools should be described only to the extent they are implemented and verified.
2. **RESIST — Make room for a different choice.** Recognise a difficult moment and create space before acting. Avoid suggesting that urges can always be controlled or eliminated.
3. **RECOVER — Return without shame.** When a plan breaks or a setback happens, help the person consider a next step. Do not frame a setback as failure or erase progress.
4. **REBUILD — Strengthen better patterns.** Support intentional habits and routines through manageable actions. Do not promise automatic habit formation or guaranteed outcomes.
5. **LIVE — Put attention back into life.** The goal is not endless app use or monitoring. It is to make more room for relationships, responsibilities, creativity, faith where relevant, rest and meaningful activities.
6. **LEARN — Understand what helps.** Reflect on patterns and personal experience where the product actually supports it. Do not claim comprehensive behavioural analysis unless verified.
7. **ADAPT — Adjust your approach.** Change goals and boundaries as circumstances change. The person remains in control; Nūr should not punish, pressure or make decisions on their behalf.

**Closing line:** You can move through this cycle more than once. A difficult day does not erase the work you've already done.

## 4. Visual and interaction direction

Follow `docs/DESIGN_SYSTEM.md`.

- Use a clear circular or gently curved cycle motif on wide screens.
- On mobile, use a readable vertical sequence or compact stacked cards; do not force a tiny circular diagram.
- Make the cycle understandable without animation.
- If motion is used, keep it slow, subtle and optional; respect `prefers-reduced-motion`.
- Use restrained glass treatment for selected cards only, with solid accessible fallbacks.
- Keep each stage concise, with one short description.
- Do not use progress percentages, locked stages, badges implying user achievement, streaks or gamified rewards.
- Avoid a design that implies users must complete all seven steps in order.
- Keep the layout light enough for mid-range Android devices and slow connections.

## 5. Interaction behaviour

The first implementation is explanatory and static. It does not require JavaScript, does not store selected stages and does not contact remote services.

Future enhancements must keep all stage information accessible without interaction. If a stage selector is later added, use semantic controls, keyboard support, visible focus and no visitor-data storage.

## 6. Islamic Mode positioning

Islamic Mode may be mentioned as an optional part of Nūr's wider experience, but it must not define the whole cycle or imply that Nūr is exclusively for Muslims.

Do not make religious rulings, present AI as a Qur'an authority, or imply that using Nūr is a measure of someone's faith.

## 7. Product truth and publication safeguards

- Clearly distinguish available features from features in development.
- Do not claim all seven stages are automated app features.
- Do not claim Nūr guarantees self-control, prevents every unwanted action, cures a condition or replaces professional support.
- Do not claim complete behavioural insight, adaptive intelligence, or comprehensive recovery outcomes without evidence.
- Do not imply that accountability partners can see private activity or browsing history.
- Use language such as "Nūr is being built to support..." for concepts that are not yet fully implemented.

## 8. Acceptance criteria

- [x] Seven stages and their relationship are presented in concise copy.
- [x] The cycle is described as repeatable and non-linear.
- [x] Copy avoids shame, guilt and guaranteed outcomes.
- [x] Desktop and mobile responsive layouts are authored.
- [x] Core content is static and does not depend on JavaScript.
- [x] No visitor data is collected or stored by this section.
- [x] Product-availability boundary is explicit.
- [ ] Astro build and browser rendering verified.
- [ ] Keyboard, screen-reader and responsive checks completed.
- [ ] Visual review on a representative mid-range Android completed.

## 9. Implementation status

Initial implementation is in `src/components/home/ProductLoop.astro`, imported by `src/pages/index.astro` immediately after the Hold demonstration. The source has been committed to `feature/website-design-system`. Build, accessibility and device verification remain pending.
