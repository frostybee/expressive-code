# @expressive-code/plugin-text-markers

## 0.41.3

### Patch Changes

- Updated dependencies [eb82591]
  - @expressive-code/core@0.41.3

## 0.41.2

### Patch Changes

- @expressive-code/core@0.41.2

## 0.41.1

### Patch Changes

- Updated dependencies [a53e749]
  - @expressive-code/core@0.41.1

## 0.41.0

### Minor Changes

- 6497f09: Uses the new `preventUnitlessValues` property of `PluginStyleSettings` to make style calculations in the plugins "Collapsible Sections", "Frames" and "Text Markers" more robust.

### Patch Changes

- Updated dependencies [380bfcc]
- Updated dependencies [0f33477]
- Updated dependencies [6497f09]
- Updated dependencies [a826a4a]
- Updated dependencies [0f33477]
- Updated dependencies [0f33477]
  - @expressive-code/core@0.41.0

## 0.40.2

### Patch Changes

- Updated dependencies [1734d73]
  - @expressive-code/core@0.40.2

## 0.40.1

### Patch Changes

- Updated dependencies [ecf6ca1]
  - @expressive-code/core@0.40.1

## 0.40.0

### Patch Changes

- @expressive-code/core@0.40.0

## 0.39.0

### Patch Changes

- @expressive-code/core@0.39.0

## 0.38.3

### Patch Changes

- @expressive-code/core@0.38.3

## 0.38.2

### Patch Changes

- @expressive-code/core@0.38.2

## 0.38.1

### Patch Changes

- Updated dependencies [440bb83]
  - @expressive-code/core@0.38.1

## 0.38.0

### Patch Changes

- @expressive-code/core@0.38.0

## 0.37.1

### Patch Changes

- @expressive-code/core@0.37.1

## 0.37.0

### Patch Changes

- @expressive-code/core@0.37.0

## 0.36.1

### Patch Changes

- @expressive-code/core@0.36.1

## 0.36.0

### Patch Changes

- Updated dependencies [ca54f6e]
  - @expressive-code/core@0.36.0

## 0.35.6

### Patch Changes

- @expressive-code/core@0.35.6

## 0.35.5

### Patch Changes

- @expressive-code/core@0.35.5

## 0.35.4

### Patch Changes

- Updated dependencies [876d24c]
  - @expressive-code/core@0.35.4

## 0.35.3

### Patch Changes

- @expressive-code/core@0.35.3

## 0.35.2

### Patch Changes

- dd54846: Fixes text marker labels including special characters like `\` by properly escaping CSS variable contents. Thank you @stancl!
- Updated dependencies [dd54846]
  - @expressive-code/core@0.35.2

## 0.35.1

### Patch Changes

- @expressive-code/core@0.35.1

## 0.35.0

### Patch Changes

- @expressive-code/core@0.35.0

## 0.34.2

### Patch Changes

- Updated dependencies [cbc16e9]
  - @expressive-code/core@0.34.2

## 0.34.1

### Patch Changes

- Updated dependencies [1b2279f]
  - @expressive-code/core@0.34.1

## 0.34.0

### Minor Changes

- b94a91d: Updates dependencies `hast`, `hastscript` and `hast-util-*` to the latest versions.

  **Potentially breaking change:** Unfortunately, some of the new `hast` types are incompatible with their old versions. If you created custom plugins to manipulate HAST nodes, you may need to update your dependencies as well and probably change some types. For example, if you were using the `Parent` type before, you will probably need to replace it with `Parents` or `Element` in the new version.

- b94a91d: Adds a new `/hast` entrypoint to `@expressive-code/core`, `expressive-code`, `remark-expressive-code` and `astro-expressive-code` to simplify plugin development.

  This new entrypoint provides direct access to the correct versions of HAST types and commonly used tree traversal, querying and manipulation functions. Instead of having to add your own dependencies on libraries like `hastscript`, `hast-util-select` or `unist-util-visit` to your project and manually keeping them in sync with the versions used by Expressive Code, you can now import the internally used functions and types directly from this new entrypoint.

- b6e7167: **Potentially breaking change:** Since this version, all packages are only distributed in modern ESM format, which greatly reduces bundle size.

  Most projects should not be affected by this change at all, but in case you still need to import Expressive Code packages into a CommonJS project, you can use the widely supported `await import(...)` syntax.

- 2ef2503: Makes Expressive Code compatible with Bun. Thank you @tylergannon for the fix and @richardguerre for the report!

  This fixes the error `msg.match is not a function` that was thrown when trying to use Expressive Code with Bun.

  Additionally, the `type` modifier was added to some imports and exports to fix further Bun issues with plugins and integrations found during testing.

### Patch Changes

- Updated dependencies [af2a10a]
- Updated dependencies [b94a91d]
- Updated dependencies [af2a10a]
- Updated dependencies [9eb8619]
- Updated dependencies [b6e7167]
- Updated dependencies [2ef2503]
- Updated dependencies [b94a91d]
  - @expressive-code/core@0.34.0

## 0.33.5

### Patch Changes

- Updated dependencies [2469749]
  - @expressive-code/core@0.33.5

## 0.33.4

### Patch Changes

- @expressive-code/core@0.33.4

## 0.33.3

### Patch Changes

- @expressive-code/core@0.33.3

## 0.33.2

### Patch Changes

- Updated dependencies [a408e31]
  - @expressive-code/core@0.33.2

## 0.33.1

### Patch Changes

- Updated dependencies [f3ac898]
  - @expressive-code/core@0.33.1

## 0.33.0

### Minor Changes

- b7a0607: Adds `metaOptions` read-only property to `ExpressiveCodeBlock` instances.

  This new property contains a parsed version of the code block's `meta` string. This allows plugins to easily access the options specified by users in the opening code fence of a code block, without having to parse the `meta` string themselves.

  All official plugins now use this new API to merge any meta options into the new extensible `ExpressiveCodeBlock.props` property.

### Patch Changes

- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
  - @expressive-code/core@0.33.0

## 0.32.4

### Patch Changes

- 20e900a: Improves automatic color contrast correction when using CSS variables in styleOverrides. Thanks @heycassidy!

  It is now possible to use CSS variables in the `styleOverrides` setting `codeBackground` without negatively affecting the automatic color contrast correction controlled by the `minSyntaxHighlightingColorContrast` setting. If a CSS variable is encountered that cannot be resolved to a color value on the server, Expressive Code now automatically uses the theme's background color as a fallback for color contrast calculations. You can also provide your own fallback color using the CSS variable fallback syntax, e.g. `var(--gray-50, #f9fafb)`.

- Updated dependencies [20e900a]
  - @expressive-code/core@0.32.4

## 0.32.3

### Patch Changes

- @expressive-code/core@0.32.3

## 0.32.2

### Patch Changes

- @expressive-code/core@0.32.2

## 0.32.1

### Patch Changes

- @expressive-code/core@0.32.1

## 0.32.0

### Patch Changes

- @expressive-code/core@0.32.0

## 0.31.0

### Minor Changes

- 60eb02a: It is now possible to add text labels to marked lines. Thanks @bdenham!

  The label text is rendered inside a colorful box in the first line of the marked range. This allows you to reference specific parts of your code in the surrounding text.

  To add any text as a label, enclose it in single or double quotes and add it directly after the opening curly brace, followed by a colon (`:`). For example, `ins={"A":6-10}` would mark lines 6 to 10 as inserted and add the label `A` to them.

### Patch Changes

- @expressive-code/core@0.31.0

## 0.30.2

### Patch Changes

- a9bbb5c: Fixes unexpected `InlineStyleAnnotation` behaviors to improve DX for plugin authors.

  - Inline styles now use `:where()` in selectors to reduce specificity and make them easier to override.
  - When applying multiple overlapping inline styles to the same line, render phases are now properly respected and later styles override earlier ones.
  - The `styleVariantIndex` property is no longer required. Inline styles without an index now apply to all style variants.
  - The default `InlineStyleAnnotation` render phase is now `normal`. The previous default setting `earliest` is now explicitly applied by `plugin-shiki` instead. This improves the API while still rendering syntax highlighting in the `earliest` phase to allow other annotations to wrap and modify the highlighted code.

- Updated dependencies [a9bbb5c]
- Updated dependencies [1a3ae04]
- Updated dependencies [a9bbb5c]
- Updated dependencies [1a3ae04]
  - @expressive-code/core@0.30.2

## 0.30.1

### Patch Changes

- @expressive-code/core@0.30.1

## 0.30.0

### Patch Changes

- @expressive-code/core@0.30.0

## 0.29.4

### Patch Changes

- Updated dependencies [765dd00]
- Updated dependencies [765dd00]
  - @expressive-code/core@0.29.4

## 0.29.3

### Patch Changes

- @expressive-code/core@0.29.3

## 0.29.2

### Patch Changes

- @expressive-code/core@0.29.2

## 0.29.1

### Patch Changes

- @expressive-code/core@0.29.1

## 0.29.0

### Patch Changes

- Updated dependencies [85dbab8]
  - @expressive-code/core@0.29.0

## 0.28.2

### Patch Changes

- @expressive-code/core@0.28.2

## 0.28.1

### Patch Changes

- @expressive-code/core@0.28.1

## 0.28.0

### Patch Changes

- @expressive-code/core@0.28.0

## 0.27.1

### Patch Changes

- @expressive-code/core@0.27.1

## 0.27.0

### Minor Changes

- f19746b: Rendering multiple themes no longer generates duplicate CSS and HTML output.

  In previous versions, a full set of CSS styles was generated for each individual theme, and each code block was rendered multiple times to include the HTML for each theme.

  In this version, the CSS output has been changed to a single static set of base styles that uses CSS variables to allow efficient switching between themes.

  Also, the HTML output for code blocks is now generated only once, and theme-dependent styles are applied using CSS variables.

  These changes significantly reduce page size when using multiple themes, especially on pages with many code blocks.

  If you have added CSS code to your site that relies on the old output (e.g. by selectively hiding or showing theme-specific code blocks based on their class name), you will need to update it to work with the new output.

  > **Note**: Before writing new custom CSS, please consider if you can achieve your desired result out of the box now. For example, if your `themes` option contains one dark and one light theme, the `useDarkModeMediaQuery` option will generate a `prefers-color-scheme` media query for you by default.

- f19746b: Config option `textMarkers` can no longer be an object.

  In previous versions, the `textMarkers` config option could be an object containing plugin options. This is no longer supported, as the only option that was available (`styleOverrides`) has been nested into the top-level `styleOverrides` object now.

  ```diff lang="js"
    /** @type {import('remark-expressive-code').RemarkExpressiveCodeOptions} */
    const remarkExpressiveCodeOptions = {
  -   textMarkers: {
  -     styleOverrides: {
  -       markHue: '310',
  -     },
  -   },
  +   styleOverrides: {
  +     textMarkers: {
  +       markHue: '310',
  +     },
  +     // You could override other plugin styles here as well:
  +     // frames: { ... },
  +   },
    },
  ```

- f19746b: Moves all plugin styles into nested sub-objects of top-level config option `styleOverrides`.

  In previous versions, there could be multiple `styleOverrides` scattered through the configuration (one per plugin with configurable style settings). This has been simplified to a single top-level `styleOverrides` object that contains all style overrides.

  Plugins can contribute their own style settings to this object as well by nesting them inside under their plugin name.

  ```diff lang="js"
    /** @type {import('remark-expressive-code').RemarkExpressiveCodeOptions} */
    const remarkExpressiveCodeOptions = {
      frames: {
        showCopyToClipboardButton: false,
  -     styleOverrides: {
  -       shadowColor: '#124',
  -     },
      },
  +   styleOverrides: {
  +     frames: {
  +       shadowColor: '#124',
  +     },
  +     // You could override other plugin styles here as well:
  +     // textMarkers: { ... },
  +   },
    },
  ```

### Patch Changes

- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
  - @expressive-code/core@0.27.0

## 0.26.2

### Patch Changes

- f2e6b81: Fixes multiple different inline marker types on the same line. Thanks @7c78!

  The logic inside `flattenInlineMarkerRanges` had a flaw that caused various combinations of `mark`, `ins` and `del` inline markers on the same line to fail. This was fixed and more tests were added.

  - @expressive-code/core@0.26.2

## 0.26.1

### Patch Changes

- @expressive-code/core@0.26.1

## 0.26.0

### Minor Changes

- d2277ba: Themed selection now keeps the code foreground color intact (like VS Code).

  Color overlays no longer prevent text from being selectable.

### Patch Changes

- Updated dependencies [d2277ba]
- Updated dependencies [d2277ba]
  - @expressive-code/core@0.26.0

## 0.25.0

### Patch Changes

- Updated dependencies [126563e]
- Updated dependencies [126563e]
  - @expressive-code/core@0.25.0

## 0.24.0

### Patch Changes

- af3171b: Passes global `styleOverrides` to plugin style resolver functions.

  This allows plugins to access their individual `styleOverrides` extensions even when values were defined at the global config level.

- Updated dependencies [af3171b]
- Updated dependencies [2c375b1]
  - @expressive-code/core@0.24.0

## 0.23.0

### Patch Changes

- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
  - @expressive-code/core@0.23.0

## 0.22.2

### Patch Changes

- @expressive-code/core@0.22.2

## 0.22.1

### Patch Changes

- @expressive-code/core@0.22.1

## 0.22.0

### Patch Changes

- @expressive-code/core@0.22.0

## 0.21.0

### Patch Changes

- Updated dependencies [becc145]
  - @expressive-code/core@0.21.0

## 0.20.0

### Patch Changes

- @expressive-code/core@0.20.0

## 0.19.2

### Patch Changes

- @expressive-code/core@0.19.2

## 0.19.1

### Patch Changes

- @expressive-code/core@0.19.1

## 0.19.0

### Minor Changes

- f95d3f1: Adds support for `diff`-like syntax and `lang` meta attribute. Thanks for the idea @hirasso!

  To mark lines as inserted or deleted, you can now use the widely supported `diff` language as an alternative to adding line numbers to the opening code fence.

  You can even specify a separate syntax highlighting language by adding a `lang="..."` attribute to the opening fence. See [README.md](https://github.com/expressive-code/expressive-code/blob/main/packages/%40expressive-code/plugin-text-markers/README.md) for more details.

### Patch Changes

- @expressive-code/core@0.19.0

## 0.18.1

### Patch Changes

- @expressive-code/core@0.18.1

## 0.18.0

### Patch Changes

- @expressive-code/core@0.18.0

## 0.17.0

### Patch Changes

- @expressive-code/core@0.17.0

## 0.16.0

### Patch Changes

- @expressive-code/core@0.16.0

## 0.15.0

### Minor Changes

- Synchronizes package versions to prevent future dependency issues.

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.15.0

## 0.2.11

### Patch Changes

- Updated dependencies [f98937c]
  - @expressive-code/core@0.11.0

## 0.2.10

### Patch Changes

- Makes marked text selectable (#15). Thanks @hirasso!

## 0.2.9

### Patch Changes

- Updated dependencies [276d221]
  - @expressive-code/core@0.10.0

## 0.2.8

### Patch Changes

- Updated dependencies [5da8685]
  - @expressive-code/core@0.9.0

## 0.2.7

### Patch Changes

- Enables stricter TypeScript checks (exactOptionalPropertyTypes), improves types.
- Updated dependencies
  - @expressive-code/core@0.8.1

## 0.2.6

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.8.0

## 0.2.5

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.7.0

## 0.2.4

### Patch Changes

- Updated dependencies [f8ed803]
  - @expressive-code/core@0.6.0

## 0.2.3

### Patch Changes

- Updated dependencies [af207b0]
  - @expressive-code/core@0.5.0

## 0.2.2

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.4.0

## 0.2.1

### Patch Changes

- Updated dependencies [6d316f6]
  - @expressive-code/core@0.3.0

## 0.2.0

### Minor Changes

- Initial release.

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.2.0
