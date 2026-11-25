# Nūr Website — Hold Demonstration Specification

**Status:** Proposed interaction; not implemented
**Date:** 25 November 2026
**Branch:** `feature/website-design-system`

## 1. Purpose

The Hold demonstration is a short, optional homepage interaction that communicates one central Nūr idea: create a pause between an urge and an action, notice the moment without judgement, and choose a next step.

It is an explanatory website demo. It is not the Nūr app's protection engine, a diagnostic, a willpower test, or evidence that a visitor has changed a habit.

## 2. Visitor experience

The complete interaction should take approximately 10–20 seconds, depending on the visitor's choices. It must never force a visitor to finish.

### State A — Ready

**Heading:** Take a moment before the next move.

**Body:** Sometimes a small pause is enough to help you notice what is happening and choose what comes next.

**Primary action:** Begin a 10-second pause

**Secondary action:** Skip this and explore Nūr

The demo must be clearly labelled as an interactive preview.

### State B — Pause in progress

Show a calm 10-second countdown with a simple progress indicator.

**Prompt:** You don't have to fight the moment or judge it. Just notice it.

Optional supporting prompts may appear one at a time:
- What is pulling at your attention?
- What are you feeling right now?
- What would help you make your next choice?

Do not require an answer. Do not use a text input.

Provide a clearly visible **End pause** control throughout. Ending early must not produce failure language, negative colour, a score, or a warning.

### State C — Pause complete

**Heading:** You made space for a choice.

**Body:** A pause does not solve everything. It can give you a moment to decide what would help next.

Offer three equal, non-judgemental actions:
- **Return to what I was doing**
- **Take another moment**
- **Explore how Nūr works**

Do not label any option as the correct choice. Selecting an option should produce a simple, appropriate response:
- Return: show a brief neutral completion message and a way to restart or dismiss the demo.
- Another moment: restart the 10-second pause.
- Explore: move focus to the How Nūr works section.

## 3. Interaction rules

- Start only after an explicit visitor action.
- Use a real 10-second countdown; do not simulate loading.
- The visitor can end or leave the demo at any time.
- Do not automatically restart.
- Do not ask for a name, email, account, or personal explanation.
- Do not generate a score, streak, success percentage, or performance rating.
- Do not use guilt, failure, shame, urgency, or alarm language.
- Do not imply that completing the demo proves self-control or changes a habit.
- The demo must remain understandable if animation is disabled.

## 4. Privacy

The demo must run entirely in the browser.

- No network request is required for the interaction.
- Do not store choices, completion, duration, or interaction history.
- Do not use analytics, tracking pixels, fingerprinting, cookies, or local storage for the demo.
- Do not send visitor input to an AI service.
- No visitor input is needed.

The countdown is transient interface state only.

## 5. Visual direction

Follow `docs/DESIGN_SYSTEM.md`.

- Use a restrained glass panel for the demonstration.
- Use the approved forest-green palette and soft emerald illumination.
- Use one simple circular progress indicator or similarly lightweight visual.
- Keep the display quiet and uncluttered.
- Avoid flashing, rapid pulsing, particle effects, sound, vibration, or dramatic countdown effects.
- Use CSS and semantic HTML; do not add a heavy animation library.
- Provide a solid surface fallback when backdrop blur is unavailable.

## 6. Accessibility

- Use semantic headings and buttons.
- All actions must work with keyboard and touch.
- Show a visible focus indicator.
- Ensure text and controls meet WCAG 2.2 AA contrast requirements.
- Respect `prefers-reduced-motion`; progress must remain clear without animation.
- Announce meaningful state changes to assistive technology without announcing every countdown tick.
- Do not rely on colour alone to communicate progress or state.
- Keep controls large enough for comfortable touch use.
- Avoid moving focus unexpectedly. When a state changes, place focus only where it helps the visitor continue.

## 7. Performance and resilience

- No third-party scripts or external assets are required.
- Keep JavaScript minimal and isolated to this component.
- Do not delay page rendering or navigation while the demo is idle.
- The page must remain fully usable if JavaScript is unavailable; show the explanatory copy and a link to the How Nūr works section.
- Test on narrow mobile viewports and a mid-range Android device.
- Verify timer cleanup when the component is left or unmounted, so no background countdown continues.

## 8. Honest product boundary

Display a short note near the interaction:

**This is a website preview. It does not block apps, monitor your activity, or record your choices.**

Do not describe the demo as a live Shield feature or imply that it demonstrates the reliability of app protection.

## 9. Acceptance criteria

The interaction is ready for review when:

1. The ready, in-progress, early-exit, and complete states work as specified.
2. The countdown lasts 10 seconds and does not run before the visitor starts it.
3. Early exit has no punitive or shame-based response.
4. No personal data is requested or persisted.
5. No analytics or third-party network calls are introduced by the demo.
6. Keyboard, touch, focus, and screen-reader behaviour are usable.
7. Reduced-motion and no-JavaScript fallbacks are provided.
8. The product-boundary note is visible.
9. The component remains lightweight and does not compromise page performance.

## 10. Implementation status

This document specifies the intended behaviour only. The Hold demonstration has not been implemented or tested. Implementation must wait until the existing local Astro project is synchronised with this GitHub branch and its current structure has been inspected.
