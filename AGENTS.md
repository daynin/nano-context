# nano-context

A `pi.dev` extension that replaces pi's default context meter with a segmented context bar under the editor.

## Idea

The smallest possible context display that's still useful. One widget, one footer replacement, one file — nothing more.

## Goal

Every line of code is on a budget. The less code, the better. Refuse abstractions that don't pay for themselves.

## Stack

- TypeScript strict (`strict`, `noUncheckedIndexedAccess`, `exactOptionalPropertyTypes`, `noImplicitOverride`)
- jiti — extension loads as `.ts` source, no build step
- Deps: `@mariozechner/pi-coding-agent`. Nothing else.

## Standards

- No `any`. Prefer `unknown` and narrow.
- Functional by default: pure functions, immutable data (`Readonly<>` / `readonly`), closures over classes. Deviate only when it would significantly violate performance.
- Self-explanatory names. No abbreviations.
- No comments unless the WHY is non-obvious. Never narrate WHAT.
- Validate at system boundaries only. Trust internal code.
- Edit existing files; don't add new ones unless required.
