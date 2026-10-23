# 08-claude-design-input/ — what you take to the build tool (Step 20)

- `master-spec.md` — every section with the approved copy, visuals, actions and states; foundation and `:root` block; components; coverage; measurement hooks; image slots. The single source for the build.
- `image-prompts.md` — one image-generation prompt per `IMG##` slot, sharing one style line. Generate them first, save into `02-assets/images/`.
- `build-prompt.md` — the prompt you paste into the build tool, plus the list of files to attach (and what to load into its design system, if it has one).

Only these three files live here. Images stay in `02-assets/images/` — do not copy `02-assets/` in here.
