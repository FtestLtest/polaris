# Versioning and changelog

The changelog is prepared manually immediately before a release, by moving changelog entries from `UNRELEASED.md` to `CHANGELOG.md`, under a new heading for the version number.

How to write a changelog entry:

- Use a positive, conversational tone (for example, use “support” over “allow” and other authoritative verbs)
- Use sentence case (refer to components as plain nouns, for example drop zone and not DropZone)
- Use plain language
- Avoid redundancy when possible (try to phrase a bug fix entry without the word “bug”)

Change log entry descriptions should be brief but descriptive and follow this structure:

```md
## 2.0.0 - 2018-05-07

### Breaking changes

- Past tense verb + brief issue/enhancement description ([#100](https://github.com/shopify/polaris/pull/100))

Contributed from the community:

- Past tense verb + brief issue/enhancement description ([#100](https://github.com/shopify/polaris/pull/100)) (thanks [@username](https://github.com/username) for the [original issue](issue link)) and/or (thanks [@username](https://github.com/username) for the [pull request](pull request link))
```

The possible groups in which to categorize changes are:

- Breaking changes
- New components
- Enhancements (new variations, accessibility improvements, etc.)
- Design updates (non-breaking design changes implemented in code)
- Bug fixes
- Documentation
- Dependency upgrades
- Development workflow (new yarn commands or changes to existing commands)

## Out of scope for `CHANGELOG.md`

Generally, changes related to these topics can be omitted:

- Style guide (update the [“What’s new” page](https://github.com/Shopify/polaris-styleguide/tree/master/pages/whats-new) instead)
- Sketch UIKit (unless noteworthy)
- Dev dependencies upgrades
- Chores (infrastructure, release process…)

## Unreleased changes

Unreleased changes must go under in the `UNRELEASED.md` file:

```md
### Bug fixes

- Fixed something ([#100](https://github.com/shopify/polaris/pull/100))
```

Entries must be moved from `UNRELEASED.md` to `CHANGELOG.md` at each release.

## Versioning scheme

Because we expose both React components (for which the markup, including class names, is an implementation detail) and static CSS/Sass builds, the versioning scheme for Polaris is somewhat unusual. The following sections detail what kinds of changes result in each of major, minor, and patch version bumps:

### Major

- Removal of a component
- Removal of a prop from a component
- Change to the type accepted for a prop
- Breaking changes to minimum version of dependencies
- Breaking changes to public Sass variables, functions and mixins

### Minor

- New component
- New prop for a component
- Additional type accepted for a prop
- Deprecation of a component, prop, public Sass variable, function, or mixin (ahead of its removal in the next major version)

### Patch

- Breaking change to the HTML generated by a component, including addition, removal, or renaming of classes
- Changes that do not impact public APIs
- Non-breaking changes to minimum version of dependencies
- Breaking changes to private Sass variables, functions, and mixins
