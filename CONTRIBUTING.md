# Contributing to Awesome EmDash

Thanks for helping keep this list useful. Adding a plugin is a single pull request.

## Adding a plugin

1. Find the right section in [`README.md`](README.md) (e.g. **Email & transactional delivery**, **Content blocks & field widgets**, **Utility & ops**). If nothing fits, propose a new section in your PR.
2. Add one bullet, keeping the list alphabetical-ish within its section and matching the existing format:

   ```markdown
   - [plugin-name](https://github.com/owner/repo) — One-line description of what it does. [`npm`](https://www.npmjs.com/package/plugin-name)
   ```

3. Guidelines for the entry:
   - **Link** to the source repo if there is one; otherwise link the npm page.
   - **Description** is a single sentence, present tense, no marketing fluff ("blazing-fast", "revolutionary", etc.). Say what it does.
   - Include the **`npm`** link when the plugin is published.
   - No trailing period rules to stress about — just match the surrounding lines.

## What belongs here

- Plugins for [EmDash](https://emdashcms.com) — anything keyworded `emdash-plugin` on npm, or shared in the EmDash discussions, is fair game.
- Themes, starters, docs, and tutorials go under **Resources**.

## What doesn't

- Abandoned or non-functional packages. If a plugin no longer installs or has been unpublished, a PR to remove it is welcome.
- Duplicate entries. Monorepos (e.g. a payments plugin split into `core` / `admin` / `sdk`) should be listed **once** with the sub-packages summarized in the description.
- Anything that isn't actually an EmDash plugin or resource.

## Quality bar

This is a curated list, not a mirror of npm. Maintainers may decline entries that are empty scaffolds, obvious spam, or can't be verified as working. Corrections, de-duplications, and re-categorizations are always welcome.

## Not affiliated

This list is community-maintained and is not affiliated with or endorsed by the EmDash team.
