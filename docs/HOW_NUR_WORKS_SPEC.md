# Nūr Website — How Nūr Works Section

**Status:** Proposed content and interaction specification; not implemented  
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

Present the cycle as a connected loop, not a staircase, scorecard or linear achievement path:

1. **PROTECT — Create healthier boundaries.**  
   Reduce exposure to things that pull you away from your intentions. Protection tools should be described only to the extent they are implemented and verified.

2. **RESIST — Make room for a different choice.**  
   Recognise a difficult moment and create space before acting. Avoid suggesting that urges can always be controlled or eliminated.

3. **RECOVER — Return without shame.**  
   When a plan breaks or a setback happens, help the person consider a next step. Do not frame a setback as failure or erase progress.

4. **REBUILD — Strengthen better patterns.**  
   Support intentional habits and routines through manageable actions. Do not promise automatic habit formation or guaranteed outcomes.

5. **LIVE — Put attention back into life.**  
   The goal is not endless app use or monitoring. It is to make more room for relationships, responsibilities, creativity, faith where relevant, rest and meaningful activities.

6. **LEARN — Understand what helps.**  
   Reflect on patterns and personal experience where the product actually supports it. Do not claim comprehensive behavioural analysis unless verified.

7. **ADAPT — Adjust your approach.**  
   Change goals and boundaries as circumstances change. The person remains in control; Nūr should not punish, pressure or make decisions on their behalf.

**Closing line:** You can move through this cycle more than once. A difficult day does not erase the work you've already done.

## 4. Visual and interaction direction

Follow `docs/DESIGN_SYSTEM.md`.

- Use a clear circular or gently curved cycle diagram on wide screens.
- On mobile, use a readable vertical sequence or compact stacked cards; do not force a tiny circular diagram.
- Make the cycle understandable without animation.
- If motion is used, keep it slow, subtle and optional; respect `prefers-reduced-motion`.
- Use restrained glass treatment for selected cards only, with solid accessible fallbacks.
- Keep each stage concise, with one short description.
- Do not use progress percentages, locked stages, badges implying user achievement, streaks or gamified rewards.
- Avoid a design that implies users must complete all seven steps in order.
- Keep the layout light enough for mid-range Android devices and slow connections.

## 5. Interaction behaviour

The preferred first version is primarily explanatory, not a complex interactive widget.

Optional enhancement: selecting a stage may reveal its longer explanation in an adjacent panel on desktop or below the selected item on mobile.

If implemented:
- All stages remain accessible without interaction.
- Use semantic buttons only when an item changes displayed content.
- Support keyboard operation and visible focus.
- Do not store selected stages or visitor activity.
- Do not use remote services or analytics.
- Provide a static, readable fallback if JavaScript is unavailable.

## 6. Islamic Mode positioning

Islamic Mode may be mentioned as an optional part of Nūr's wider experience, but it must not define the whole cycle or imply that Nūr is exclusively for Muslims.

Suggested supporting line, only when the current app implementation is re-verified:

"Optional Islamic Mode can help people who want their personal growth journey to include faith-based reminders and intentions."

Do not make religious rulings, present AI as a Qur'an authority, or imply that using Nūr is a measure of someone's faith.

## 7. Product truth and publication safeguards

Before publishing feature-specific statements, compare them with the current Nūr app repository, documentation, implementation and tests.

- Clearly distinguish available features from features in development.
- Do not claim all seven stages are automated app features.
- Do not claim Nūr guarantees self-control, prevents every unwanted action, cures a condition or replaces professional support.
- Do not claim complete behavioural insight, adaptive intelligence, or comprehensive recovery outcomes without evidence.
- Do not imply that accountability partners can see private activity or browsing history.
- Use language such as "Nūr is being built to support..." for concepts that are not yet fully implemented.

## 8. Acceptance criteria

The section is ready for design review when:

1. The seven stages and their relationship are understandable within a short scan.
2. The cycle is presented as repeatable and non-linear.
3. Copy is non-judgemental and avoids shame, guilt and guaranteed outcomes.
4. Desktop and mobile layouts are both readable.
5. The section works without animation and, if interactive, has a static fallback.
6. Keyboard and screen-reader behaviour are usable.
7. No visitor data is collected or stored.
8. Claims about actual app features have been checked against the current app repository.
9. The section does not imply that the website demo itself performs app protection.

## 9. Implementation status

This document records proposed copy, structure and behaviour only. The section has not been implemented or tested.

Implementation must wait until the existing local Astro project is synchronised with this GitHub branch and its current structure has been inspected.
