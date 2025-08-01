# expressive-code

## 0.41.3

### Patch Changes

- eb82591: Fixes WCAG 4.1.2 compliance issue by dynamically adding `role="region"` to scrollable code blocks. Thank you @ruslanpashkov!
- Updated dependencies [eb82591]
  - @expressive-code/core@0.41.3
  - @expressive-code/plugin-frames@0.41.3
  - @expressive-code/plugin-shiki@0.41.3
  - @expressive-code/plugin-text-markers@0.41.3

## 0.41.2

### Patch Changes

- @expressive-code/core@0.41.2
- @expressive-code/plugin-frames@0.41.2
- @expressive-code/plugin-shiki@0.41.2
- @expressive-code/plugin-text-markers@0.41.2

## 0.41.1

### Patch Changes

- a53e749: Fixes a regression that caused inline text markers to be rendered with two layered background colors.
- Updated dependencies [a53e749]
  - @expressive-code/core@0.41.1
  - @expressive-code/plugin-frames@0.41.1
  - @expressive-code/plugin-shiki@0.41.1
  - @expressive-code/plugin-text-markers@0.41.1

## 0.41.0

### Minor Changes

- 380bfcc: Adds new `createInlineSvgUrl` export that creates an inline SVG image data URL from the given contents of an SVG file.

  You can use it to embed SVG images directly into a plugin's styles or HAST, or pass it to an existing `styleOverrides` icon setting.

- 0f33477: Updates Shiki to the latest version (3.2.2).

  This adds support for the strikethrough ANSI control code, updates language grammars and adds the bundled themes `gruvbox-dark-hard`, `gruvbox-dark-medium`, `gruvbox-dark-soft`, `gruvbox-light-hard`, `gruvbox-light-medium`, and `gruvbox-light-soft`.

- 6497f09: Adds new `preventUnitlessValues` property to `PluginStyleSettings`. Thank you @RantingHuman!

  Plugins can set this property to an array of style setting paths to prevent unitless values for specific style settings. If the user passes a unitless value to one of these settings, the engine will automatically add `px` to the value. This is recommended for settings used in CSS calculations which would otherwise break if a unitless value is passed.

- a826a4a: Adds a new `hangingIndent` prop to all code blocks. Thank you @Signum!

  By setting this prop to a positive number of columns (either in the opening code fence, as a prop on the `<Code>` component, or in the `defaultProps` config option), you can now further refine the indentation of wrapped lines.

  If the prop `preserveIndent` is `true` (which is the default), the `hangingIndent` value is added to the indentation of the original line. If `preserveIndent` is `false`, the value is used as the fixed indentation level of all wrapped lines.

  This option only affects how the code block is displayed and does not change the actual code. When copied to the clipboard, the code will still contain the original unwrapped lines.

- 0f33477: Extends ANSI formatting support to allow background colors and strikethrough text. Thank you @dhruvkb!
- 380bfcc: Adds the following new `styleOverrides` settings:

  - `frames.copyIcon`: Allows overriding the SVG icon used for the copy button. Thank you @louisescher!
  - `frames.terminalIcon`: Allows overriding the SVG icon used for the terminal window frame. Defaults to three dots in the top left corner.

- 0f33477: Adds support for `bgColor` and `strikethrough` to `InlineStyleAnnotation`. Thank you @dhruvkb!

### Patch Changes

- Updated dependencies [380bfcc]
- Updated dependencies [6497f09]
- Updated dependencies [0f33477]
- Updated dependencies [6497f09]
- Updated dependencies [a826a4a]
- Updated dependencies [0f33477]
- Updated dependencies [380bfcc]
- Updated dependencies [0f33477]
  - @expressive-code/plugin-frames@0.41.0
  - @expressive-code/core@0.41.0
  - @expressive-code/plugin-text-markers@0.41.0
  - @expressive-code/plugin-shiki@0.41.0

## 0.40.2

### Patch Changes

- 1734d73: Prevents the default [style reset](https://expressive-code.com/reference/configuration/#usestylereset) from interfering with more complex SVGs inside Expressive Code blocks. Now, not only `path` elements, but all SVGs and their contents are excluded from the reset. Thank you @xt0rted!
- Updated dependencies [1734d73]
  - @expressive-code/core@0.40.2
  - @expressive-code/plugin-frames@0.40.2
  - @expressive-code/plugin-shiki@0.40.2
  - @expressive-code/plugin-text-markers@0.40.2

## 0.40.1

### Patch Changes

- ecf6ca1: Removes unnecessary end padding from the first code line if the copy to clipboard button is disabled. Thank you @goulvenclech!
- Updated dependencies [ecf6ca1]
  - @expressive-code/plugin-frames@0.40.1
  - @expressive-code/core@0.40.1
  - @expressive-code/plugin-shiki@0.40.1
  - @expressive-code/plugin-text-markers@0.40.1

## 0.40.0

### Patch Changes

- @expressive-code/core@0.40.0
- @expressive-code/plugin-frames@0.40.0
- @expressive-code/plugin-shiki@0.40.0
- @expressive-code/plugin-text-markers@0.40.0

## 0.39.0

### Minor Changes

- 9149332: Updates Shiki to the latest version (1.26.1).

### Patch Changes

- Updated dependencies [9149332]
  - @expressive-code/plugin-shiki@0.39.0
  - @expressive-code/plugin-frames@0.39.0
  - @expressive-code/plugin-text-markers@0.39.0
  - @expressive-code/core@0.39.0

## 0.38.3

### Patch Changes

- 90b614e: Makes the types used by the `shiki.langs` config option less strict to align them better with actual grammars found in the wild. This attempts to reduce the amount of type errors that occurred before when using external grammars, while still being supported by the language processing code.
- Updated dependencies [90b614e]
  - @expressive-code/plugin-shiki@0.38.3
  - @expressive-code/plugin-frames@0.38.3
  - @expressive-code/core@0.38.3
  - @expressive-code/plugin-text-markers@0.38.3

## 0.38.2

### Patch Changes

- @expressive-code/core@0.38.2
- @expressive-code/plugin-frames@0.38.2
- @expressive-code/plugin-shiki@0.38.2
- @expressive-code/plugin-text-markers@0.38.2

## 0.38.1

### Patch Changes

- Updated dependencies [440bb83]
  - @expressive-code/core@0.38.1
  - @expressive-code/plugin-frames@0.38.1
  - @expressive-code/plugin-shiki@0.38.1
  - @expressive-code/plugin-text-markers@0.38.1

## 0.38.0

### Patch Changes

- Updated dependencies [944dda0]
- Updated dependencies [944dda0]
- Updated dependencies [944dda0]
- Updated dependencies [944dda0]
  - @expressive-code/plugin-shiki@0.38.0
  - @expressive-code/plugin-frames@0.38.0
  - @expressive-code/plugin-text-markers@0.38.0
  - @expressive-code/core@0.38.0

## 0.37.1

### Patch Changes

- @expressive-code/core@0.37.1
- @expressive-code/plugin-frames@0.37.1
- @expressive-code/plugin-shiki@0.37.1
- @expressive-code/plugin-text-markers@0.37.1

## 0.37.0

### Patch Changes

- @expressive-code/core@0.37.0
- @expressive-code/plugin-frames@0.37.0
- @expressive-code/plugin-shiki@0.37.0
- @expressive-code/plugin-text-markers@0.37.0

## 0.36.1

### Patch Changes

- @expressive-code/core@0.36.1
- @expressive-code/plugin-frames@0.36.1
- @expressive-code/plugin-shiki@0.36.1
- @expressive-code/plugin-text-markers@0.36.1

## 0.36.0

### Minor Changes

- bff1106: Adds the experimental `transformers` option to the Shiki plugin. Thank you @MichaelMakesGames!

  This option allows you to specify a list of Shiki transformers to be called during syntax highlighting.

  **Important:** This option is marked as experimental because it only supports a **very limited subset** of Shiki transformer features right now. Most importantly, transformers cannot modify a code block's text contents in any way, so most popular transformers will not work.

  In its current state, this option allows you to use transformers that solely modify the tokens produced by Shiki to improve syntax highlighting, e.g. applying bracket matching or changing the color of certain tokens.

  Attempting to pass incompatible transformers to this option will throw an error. This is not a bug, neither in Expressive Code, nor in Shiki or the transformers. Please do not report incompatibilities to other authors, as they are unable to fix them. The current limitations exist because the Shiki transformer API is incompatible with Expressive Code's architecture, and we will continue to work on closing the gap and improving this feature.

- ca54f6e: Updates Shiki dependency to the latest version.

### Patch Changes

- Updated dependencies [bff1106]
- Updated dependencies [ca54f6e]
  - @expressive-code/plugin-shiki@0.36.0
  - @expressive-code/core@0.36.0
  - @expressive-code/plugin-frames@0.36.0
  - @expressive-code/plugin-text-markers@0.36.0

## 0.35.6

### Patch Changes

- ffab5a5: Hides the copy code button in case JavaScript is disabled. Thank you @imkunet!
- Updated dependencies [ffab5a5]
  - @expressive-code/plugin-frames@0.35.6
  - @expressive-code/core@0.35.6
  - @expressive-code/plugin-shiki@0.35.6
  - @expressive-code/plugin-text-markers@0.35.6

## 0.35.5

### Patch Changes

- @expressive-code/core@0.35.5
- @expressive-code/plugin-frames@0.35.5
- @expressive-code/plugin-shiki@0.35.5
- @expressive-code/plugin-text-markers@0.35.5

## 0.35.4

### Patch Changes

- 876d24c: Improves performance of client script managing `tabindex` on code samples. Thanks @delucis!
- Updated dependencies [876d24c]
  - @expressive-code/core@0.35.4
  - @expressive-code/plugin-frames@0.35.4
  - @expressive-code/plugin-shiki@0.35.4
  - @expressive-code/plugin-text-markers@0.35.4

## 0.35.3

### Patch Changes

- Updated dependencies [c892206]
  - @expressive-code/plugin-frames@0.35.3
  - @expressive-code/core@0.35.3
  - @expressive-code/plugin-shiki@0.35.3
  - @expressive-code/plugin-text-markers@0.35.3

## 0.35.2

### Patch Changes

- dd54846: Fixes text marker labels including special characters like `\` by properly escaping CSS variable contents. Thank you @stancl!
- Updated dependencies [dd54846]
  - @expressive-code/plugin-text-markers@0.35.2
  - @expressive-code/core@0.35.2
  - @expressive-code/plugin-frames@0.35.2
  - @expressive-code/plugin-shiki@0.35.2

## 0.35.1

### Patch Changes

- @expressive-code/core@0.35.1
- @expressive-code/plugin-frames@0.35.1
- @expressive-code/plugin-shiki@0.35.1
- @expressive-code/plugin-text-markers@0.35.1

## 0.35.0

### Minor Changes

- 1875948: Adds the new package `rehype-expressive-code` as the successor to `remark-expressive-code`, which is now considered deprecated.

  If you're using the Astro integration `astro-expressive-code`, you will be automatically using the new package and don't need to do anything.

  If your project has a dependency on `remark-expressive-code`, you should replace it with `rehype-expressive-code` and pass it as a rehype plugin instead of a remark plugin. See the [installation instructions](https://expressive-code.com/installation/#nextjs) for an example.

  The new package includes performance improvements and also works with the latest versions of MDX in popular site generators.

### Patch Changes

- @expressive-code/core@0.35.0
- @expressive-code/plugin-frames@0.35.0
- @expressive-code/plugin-shiki@0.35.0
- @expressive-code/plugin-text-markers@0.35.0

## 0.34.2

### Patch Changes

- Updated dependencies [cbc16e9]
  - @expressive-code/core@0.34.2
  - @expressive-code/plugin-frames@0.34.2
  - @expressive-code/plugin-shiki@0.34.2
  - @expressive-code/plugin-text-markers@0.34.2

## 0.34.1

### Patch Changes

- 1b2279f: Fixes a11y property `tabindex="0"` being set on non-scrollable code blocks.

  Instead of always adding `tabindex="0"` to the `<pre>` element of code blocks, a small JS module is now used to conditionally add the property to scrollable code blocks only. This ensures that scrollable regions can be accessed via keyboard navigation while avoiding audit warnings about `tabindex` being used on non-scrollable elements.

- Updated dependencies [1b2279f]
  - @expressive-code/core@0.34.1
  - @expressive-code/plugin-frames@0.34.1
  - @expressive-code/plugin-shiki@0.34.1
  - @expressive-code/plugin-text-markers@0.34.1

## 0.34.0

### Minor Changes

- b94a91d: Updates dependencies `hast`, `hastscript` and `hast-util-*` to the latest versions.

  **Potentially breaking change:** Unfortunately, some of the new `hast` types are incompatible with their old versions. If you created custom plugins to manipulate HAST nodes, you may need to update your dependencies as well and probably change some types. For example, if you were using the `Parent` type before, you will probably need to replace it with `Parents` or `Element` in the new version.

- b94a91d: Adds a new `/hast` entrypoint to `@expressive-code/core`, `expressive-code`, `remark-expressive-code` and `astro-expressive-code` to simplify plugin development.

  This new entrypoint provides direct access to the correct versions of HAST types and commonly used tree traversal, querying and manipulation functions. Instead of having to add your own dependencies on libraries like `hastscript`, `hast-util-select` or `unist-util-visit` to your project and manually keeping them in sync with the versions used by Expressive Code, you can now import the internally used functions and types directly from this new entrypoint.

- b6e7167: **Potentially breaking change:** Since this version, all packages are only distributed in modern ESM format, which greatly reduces bundle size.

  Most projects should not be affected by this change at all, but in case you still need to import Expressive Code packages into a CommonJS project, you can use the widely supported `await import(...)` syntax.

### Patch Changes

- Updated dependencies [af2a10a]
- Updated dependencies [b94a91d]
- Updated dependencies [af2a10a]
- Updated dependencies [9eb8619]
- Updated dependencies [b6e7167]
- Updated dependencies [2ef2503]
- Updated dependencies [b94a91d]
  - @expressive-code/core@0.34.0
  - @expressive-code/plugin-text-markers@0.34.0
  - @expressive-code/plugin-frames@0.34.0
  - @expressive-code/plugin-shiki@0.34.0

## 0.33.5

### Patch Changes

- 2469749: Improves word wrap behavior on very narrow screens and when using larger font sizes by allowing wrapping to start at column 20 instead of 30.
- Updated dependencies [2469749]
  - @expressive-code/core@0.33.5
  - @expressive-code/plugin-frames@0.33.5
  - @expressive-code/plugin-shiki@0.33.5
  - @expressive-code/plugin-text-markers@0.33.5

## 0.33.4

### Patch Changes

- Updated dependencies [6f26c3b]
  - @expressive-code/plugin-shiki@0.33.4
  - @expressive-code/plugin-frames@0.33.4
  - @expressive-code/core@0.33.4
  - @expressive-code/plugin-text-markers@0.33.4

## 0.33.3

### Patch Changes

- f15b9f4: Reverts language loading of `plugin-shiki` to the previous behavior to work around an apparent race condition.
- Updated dependencies [f15b9f4]
  - @expressive-code/plugin-shiki@0.33.3
  - @expressive-code/plugin-frames@0.33.3
  - @expressive-code/core@0.33.3
  - @expressive-code/plugin-text-markers@0.33.3

## 0.33.2

### Patch Changes

- Updated dependencies [a408e31]
  - @expressive-code/plugin-shiki@0.33.2
  - @expressive-code/core@0.33.2
  - @expressive-code/plugin-frames@0.33.2
  - @expressive-code/plugin-text-markers@0.33.2

## 0.33.1

### Patch Changes

- f3ac898: Fixes an issue where lines containing a very long word after the initial indentation would wrap incorrectly.
- Updated dependencies [f3ac898]
  - @expressive-code/core@0.33.1
  - @expressive-code/plugin-frames@0.33.1
  - @expressive-code/plugin-shiki@0.33.1
  - @expressive-code/plugin-text-markers@0.33.1

## 0.33.0

### Patch Changes

- Updated dependencies [b7a0607]
- Updated dependencies [77e4142]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
- Updated dependencies [b7a0607]
  - @expressive-code/core@0.33.0
  - @expressive-code/plugin-frames@0.33.0
  - @expressive-code/plugin-text-markers@0.33.0
  - @expressive-code/plugin-shiki@0.33.0

## 0.32.4

### Patch Changes

- 20e900a: Improves automatic color contrast correction when using CSS variables in styleOverrides. Thanks @heycassidy!

  It is now possible to use CSS variables in the `styleOverrides` setting `codeBackground` without negatively affecting the automatic color contrast correction controlled by the `minSyntaxHighlightingColorContrast` setting. If a CSS variable is encountered that cannot be resolved to a color value on the server, Expressive Code now automatically uses the theme's background color as a fallback for color contrast calculations. You can also provide your own fallback color using the CSS variable fallback syntax, e.g. `var(--gray-50, #f9fafb)`.

- Updated dependencies [20e900a]
  - @expressive-code/plugin-text-markers@0.32.4
  - @expressive-code/core@0.32.4
  - @expressive-code/plugin-frames@0.32.4
  - @expressive-code/plugin-shiki@0.32.4

## 0.32.3

### Patch Changes

- @expressive-code/core@0.32.3
- @expressive-code/plugin-frames@0.32.3
- @expressive-code/plugin-shiki@0.32.3
- @expressive-code/plugin-text-markers@0.32.3

## 0.32.2

### Patch Changes

- @expressive-code/core@0.32.2
- @expressive-code/plugin-frames@0.32.2
- @expressive-code/plugin-shiki@0.32.2
- @expressive-code/plugin-text-markers@0.32.2

## 0.32.1

### Patch Changes

- @expressive-code/core@0.32.1
- @expressive-code/plugin-frames@0.32.1
- @expressive-code/plugin-shiki@0.32.1
- @expressive-code/plugin-text-markers@0.32.1

## 0.32.0

### Patch Changes

- @expressive-code/core@0.32.0
- @expressive-code/plugin-frames@0.32.0
- @expressive-code/plugin-shiki@0.32.0
- @expressive-code/plugin-text-markers@0.32.0

## 0.31.0

### Minor Changes

- 60eb02a: It is now possible to add text labels to marked lines. Thanks @bdenham!

  The label text is rendered inside a colorful box in the first line of the marked range. This allows you to reference specific parts of your code in the surrounding text.

  To add any text as a label, enclose it in single or double quotes and add it directly after the opening curly brace, followed by a colon (`:`). For example, `ins={"A":6-10}` would mark lines 6 to 10 as inserted and add the label `A` to them.

### Patch Changes

- Updated dependencies [60eb02a]
  - @expressive-code/plugin-text-markers@0.31.0
  - @expressive-code/core@0.31.0
  - @expressive-code/plugin-frames@0.31.0
  - @expressive-code/plugin-shiki@0.31.0

## 0.30.2

### Patch Changes

- a9bbb5c: Fixes missing CSS output for `uiFontWeight` and `codeFontWeight` style settings. Changed font weights are now properly respected. Thank you @depatchedmode!
- 1a3ae04: Individual code blocks can now be switched to the base theme while an alternate theme is selected on the page level.

  Expressive Code differentiates between your base theme (= the first theme in `themes`) and your alternate themes (= any other entries in `themes`). Previously, as soon as an alternate theme was selected on the page level, e.g. by using `<html data-theme="some-theme-name">`, it wasn't possible to switch individual code blocks to the base theme anymore because of selector specificity issues. This has been resolved and block-level overrides should work as expected now.

- a9bbb5c: Fixes unexpected `InlineStyleAnnotation` behaviors to improve DX for plugin authors.

  - Inline styles now use `:where()` in selectors to reduce specificity and make them easier to override.
  - When applying multiple overlapping inline styles to the same line, render phases are now properly respected and later styles override earlier ones.
  - The `styleVariantIndex` property is no longer required. Inline styles without an index now apply to all style variants.
  - The default `InlineStyleAnnotation` render phase is now `normal`. The previous default setting `earliest` is now explicitly applied by `plugin-shiki` instead. This improves the API while still rendering syntax highlighting in the `earliest` phase to allow other annotations to wrap and modify the highlighted code.

- 1a3ae04: Themes that use transparency in unexpected places (e.g. the `rose-pine` themes) are now displayed correctly.
- Updated dependencies [a9bbb5c]
- Updated dependencies [1a3ae04]
- Updated dependencies [a9bbb5c]
- Updated dependencies [1a3ae04]
  - @expressive-code/core@0.30.2
  - @expressive-code/plugin-text-markers@0.30.2
  - @expressive-code/plugin-shiki@0.30.2
  - @expressive-code/plugin-frames@0.30.2

## 0.30.1

### Patch Changes

- c3758cd: Fixes parallel execution of multiple syntax highlighter creations and tasks.

  The Shiki plugin now ensures that async tasks like creating syntax highlighters, loading themes or languages are never started multiple times in parallel. This improves performance, reduces memory usage and prevents build errors on large sites.

- Updated dependencies [c3758cd]
  - @expressive-code/plugin-shiki@0.30.1
  - @expressive-code/plugin-frames@0.30.1
  - @expressive-code/core@0.30.1
  - @expressive-code/plugin-text-markers@0.30.1

## 0.30.0

### Minor Changes

- 05c6ad8: Changes the syntax highlighter used by `plugin-shiki` to Shikiji. Adds a `shiki: { langs: [...] }` option for loading custom languages.

  This change should not cause any differences in HTML output as all rendering is done by Expressive Code. The new `langs` option allows registering custom TextMate grammars in JSON form.

### Patch Changes

- Updated dependencies [05c6ad8]
  - @expressive-code/plugin-shiki@0.30.0
  - @expressive-code/plugin-frames@0.30.0
  - @expressive-code/plugin-text-markers@0.30.0
  - @expressive-code/core@0.30.0

## 0.29.4

### Patch Changes

- 765dd00: Unknown code block languages now log a warning and render as plaintext instead of throwing an error.
- 765dd00: Adds the config option `useStyleReset`.

  This option determines if code blocks should be protected against influence from site-wide styles. This protection was always enabled before this release and could not be turned off.

  When enabled, Expressive Code uses the declaration `all: revert` to revert all CSS properties to the values they would have had without any site-wide styles. This ensures the most predictable results out of the box.

  You can now set this to `false` if you want your site-wide styles to influence the code blocks.

- Updated dependencies [765dd00]
- Updated dependencies [765dd00]
  - @expressive-code/plugin-shiki@0.29.4
  - @expressive-code/core@0.29.4
  - @expressive-code/plugin-frames@0.29.4
  - @expressive-code/plugin-text-markers@0.29.4

## 0.29.3

### Patch Changes

- @expressive-code/core@0.29.3
- @expressive-code/plugin-frames@0.29.3
- @expressive-code/plugin-shiki@0.29.3
- @expressive-code/plugin-text-markers@0.29.3

## 0.29.2

### Patch Changes

- e18c69d: Comments like `// ...` are now no longer incorrectly detected as file names. Thanks @kdheepak!
- Updated dependencies [e18c69d]
  - @expressive-code/plugin-frames@0.29.2
  - @expressive-code/core@0.29.2
  - @expressive-code/plugin-shiki@0.29.2
  - @expressive-code/plugin-text-markers@0.29.2

## 0.29.1

### Patch Changes

- @expressive-code/core@0.29.1
- @expressive-code/plugin-frames@0.29.1
- @expressive-code/plugin-shiki@0.29.1
- @expressive-code/plugin-text-markers@0.29.1

## 0.29.0

### Minor Changes

- 85dbab8: Updates default fonts to match Tailwind CSS.

  The previous set of default fonts could result in very thin character line widths on iOS devices. This is now fixed by using the same widely tested set of fonts that Tailwind CSS uses.

- e020b64: Cleans up frontmatter after file name comment extraction.

  If a file name comment gets extracted from a code block without a `title` attribute, additional cleanup work is now performed on the surrounding lines:

  - If the code block's language supports frontmatter, and the comment was located in a frontmatter block that has now become empty, the empty frontmatter block gets removed.
  - If the line following the removed comment (or removed frontmatter block) is empty, it gets removed as well.

### Patch Changes

- Updated dependencies [85dbab8]
- Updated dependencies [e020b64]
  - @expressive-code/core@0.29.0
  - @expressive-code/plugin-frames@0.29.0
  - @expressive-code/plugin-shiki@0.29.0
  - @expressive-code/plugin-text-markers@0.29.0

## 0.28.2

### Patch Changes

- @expressive-code/core@0.28.2
- @expressive-code/plugin-frames@0.28.2
- @expressive-code/plugin-shiki@0.28.2
- @expressive-code/plugin-text-markers@0.28.2

## 0.28.1

### Patch Changes

- @expressive-code/core@0.28.1
- @expressive-code/plugin-frames@0.28.1
- @expressive-code/plugin-shiki@0.28.1
- @expressive-code/plugin-text-markers@0.28.1

## 0.28.0

### Patch Changes

- @expressive-code/core@0.28.0
- @expressive-code/plugin-frames@0.28.0
- @expressive-code/plugin-shiki@0.28.0
- @expressive-code/plugin-text-markers@0.28.0

## 0.27.1

### Patch Changes

- @expressive-code/core@0.27.1
- @expressive-code/plugin-frames@0.27.1
- @expressive-code/plugin-shiki@0.27.1
- @expressive-code/plugin-text-markers@0.27.1

## 0.27.0

### Minor Changes

- f19746b: Adds `useDarkModeMediaQuery` config option.

  This new option determines if CSS code is generated that uses a `prefers-color-scheme` media query to automatically switch between light and dark themes based on the user's system preferences.

  Defaults to `true` if your `themes` option is set to one dark and one light theme (which is the default), and `false` otherwise.

- f19746b: Rendering multiple themes no longer generates duplicate CSS and HTML output.

  In previous versions, a full set of CSS styles was generated for each individual theme, and each code block was rendered multiple times to include the HTML for each theme.

  In this version, the CSS output has been changed to a single static set of base styles that uses CSS variables to allow efficient switching between themes.

  Also, the HTML output for code blocks is now generated only once, and theme-dependent styles are applied using CSS variables.

  These changes significantly reduce page size when using multiple themes, especially on pages with many code blocks.

  If you have added CSS code to your site that relies on the old output (e.g. by selectively hiding or showing theme-specific code blocks based on their class name), you will need to update it to work with the new output.

  > **Note**: Before writing new custom CSS, please consider if you can achieve your desired result out of the box now. For example, if your `themes` option contains one dark and one light theme, the `useDarkModeMediaQuery` option will generate a `prefers-color-scheme` media query for you by default.

- f19746b: Adds `minSyntaxHighlightingColorContrast` config option.

  This new option determines if Expressive Code should process the syntax highlighting colors of all themes to ensure an accessible minimum contrast ratio between foreground and background colors.

  Defaults to `5.5`, which ensures a contrast ratio of at least 5.5:1. You can change the desired contrast ratio by providing another value, or turn the feature off by setting this option to `0`.

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

- f19746b: Renames config option `theme` to `themes`.

  Efficient multi-theme support using CSS variables is now a core feature, so the `theme` option was deprecated in favor of the new array `themes`.

  Please migrate your existing config to use `themes` and ensure it is an array. If you only need a single theme, your `themes` array can contain just this one theme. However, please consider the benefits of providing multiple themes.

  ```diff lang="js"
    /** @type {import('remark-expressive-code').RemarkExpressiveCodeOptions} */
    const remarkExpressiveCodeOptions = {
  -   theme: 'dracula',
  +   // Rename to `themes` and ensure it is an array
  +   // (also consider adding a light theme for accessibility)
  +   themes: ['dracula'],
    },
  ```

- f19746b: Adds `cascadeLayer` config option.

  This new option allows to specify a CSS cascade layer name that should be used for all generated CSS styles.

  If you are using [cascade layers](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_layers) on your site to control the order in which CSS rules are applied, set this option to a non-empty string, and Expressive Code will wrap all of its generated CSS styles in a `@layer` rule with the given name.

### Patch Changes

- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
- Updated dependencies [f19746b]
  - @expressive-code/core@0.27.0
  - @expressive-code/plugin-text-markers@0.27.0
  - @expressive-code/plugin-frames@0.27.0
  - @expressive-code/plugin-shiki@0.27.0

## 0.26.2

### Patch Changes

- f2e6b81: Fixes multiple different inline marker types on the same line. Thanks @7c78!

  The logic inside `flattenInlineMarkerRanges` had a flaw that caused various combinations of `mark`, `ins` and `del` inline markers on the same line to fail. This was fixed and more tests were added.

- Updated dependencies [f2e6b81]
  - @expressive-code/plugin-text-markers@0.26.2
  - @expressive-code/core@0.26.2
  - @expressive-code/plugin-frames@0.26.2
  - @expressive-code/plugin-shiki@0.26.2

## 0.26.1

### Patch Changes

- Updated dependencies [3e0e8c4]
  - @expressive-code/plugin-frames@0.26.1
  - @expressive-code/core@0.26.1
  - @expressive-code/plugin-shiki@0.26.1
  - @expressive-code/plugin-text-markers@0.26.1

## 0.26.0

### Minor Changes

- d2277ba: Themed selection now keeps the code foreground color intact (like VS Code).

  Color overlays no longer prevent text from being selectable.

### Patch Changes

- Updated dependencies [d2277ba]
- Updated dependencies [d2277ba]
- Updated dependencies [ef93adf]
  - @expressive-code/core@0.26.0
  - @expressive-code/plugin-text-markers@0.26.0
  - @expressive-code/plugin-frames@0.26.0
  - @expressive-code/plugin-shiki@0.26.0

## 0.25.0

### Patch Changes

- Updated dependencies [126563e]
- Updated dependencies [126563e]
  - @expressive-code/core@0.25.0
  - @expressive-code/plugin-frames@0.25.0
  - @expressive-code/plugin-shiki@0.25.0
  - @expressive-code/plugin-text-markers@0.25.0

## 0.24.0

### Minor Changes

- af3171b: Renders frame borders on top of background, adds `editorActiveTabHighlightHeight` style setting.

  Previously, borders were rendered around the editor / terminal window, which could lead to unwanted empty margins between the window background and the drop shadow (e.g. in theme `nord`). Now, the border is rendered on top of the background to resolve this issue, making fully transparent borders act like padding instead.

  Additionally, the `editorActiveTabHighlightHeight` style setting was introduced, which allows customizing the colorful line that highlights the active editor tab. It defaults to `borderWidth`.

### Patch Changes

- af3171b: Passes global `styleOverrides` to plugin style resolver functions.

  This allows plugins to access their individual `styleOverrides` extensions even when values were defined at the global config level.

- Updated dependencies [af3171b]
- Updated dependencies [2c375b1]
- Updated dependencies [af3171b]
  - @expressive-code/plugin-text-markers@0.24.0
  - @expressive-code/plugin-frames@0.24.0
  - @expressive-code/plugin-shiki@0.24.0
  - @expressive-code/core@0.24.0

## 0.23.0

### Patch Changes

- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
- Updated dependencies [bfed62a]
  - @expressive-code/core@0.23.0
  - @expressive-code/plugin-frames@0.23.0
  - @expressive-code/plugin-shiki@0.23.0
  - @expressive-code/plugin-text-markers@0.23.0

## 0.22.2

### Patch Changes

- @expressive-code/core@0.22.2
- @expressive-code/plugin-frames@0.22.2
- @expressive-code/plugin-shiki@0.22.2
- @expressive-code/plugin-text-markers@0.22.2

## 0.22.1

### Patch Changes

- @expressive-code/core@0.22.1
- @expressive-code/plugin-frames@0.22.1
- @expressive-code/plugin-shiki@0.22.1
- @expressive-code/plugin-text-markers@0.22.1

## 0.22.0

### Patch Changes

- @expressive-code/core@0.22.0
- @expressive-code/plugin-frames@0.22.0
- @expressive-code/plugin-shiki@0.22.0
- @expressive-code/plugin-text-markers@0.22.0

## 0.21.0

### Patch Changes

- Updated dependencies [becc145]
  - @expressive-code/core@0.21.0
  - @expressive-code/plugin-frames@0.21.0
  - @expressive-code/plugin-shiki@0.21.0
  - @expressive-code/plugin-text-markers@0.21.0

## 0.20.0

### Minor Changes

- 7c5c3c7: Adds `removeCommentsWhenCopyingTerminalFrames` config option to `plugin-frames`. Thanks @AkashRajpurohit!

  If `true` (which is the default), the "Copy to clipboard" button of terminal window frames will remove comment lines starting with `#` from the copied text.

  This is useful to reduce the copied text to the actual commands users need to run, instead of also copying explanatory comments or instructions.

### Patch Changes

- Updated dependencies [7c5c3c7]
  - @expressive-code/plugin-frames@0.20.0
  - @expressive-code/core@0.20.0
  - @expressive-code/plugin-shiki@0.20.0
  - @expressive-code/plugin-text-markers@0.20.0

## 0.19.2

### Patch Changes

- @expressive-code/core@0.19.2
- @expressive-code/plugin-frames@0.19.2
- @expressive-code/plugin-shiki@0.19.2
- @expressive-code/plugin-text-markers@0.19.2

## 0.19.1

### Patch Changes

- Updated dependencies [6da5008]
  - @expressive-code/plugin-frames@0.19.1
  - @expressive-code/core@0.19.1
  - @expressive-code/plugin-shiki@0.19.1
  - @expressive-code/plugin-text-markers@0.19.1

## 0.19.0

### Minor Changes

- f95d3f1: Adds support for `diff`-like syntax and `lang` meta attribute. Thanks for the idea @hirasso!

  To mark lines as inserted or deleted, you can now use the widely supported `diff` language as an alternative to adding line numbers to the opening code fence.

  You can even specify a separate syntax highlighting language by adding a `lang="..."` attribute to the opening fence. See [README.md](https://github.com/expressive-code/expressive-code/blob/main/packages/%40expressive-code/plugin-text-markers/README.md) for more details.

### Patch Changes

- Updated dependencies [f95d3f1]
  - @expressive-code/plugin-text-markers@0.19.0
  - @expressive-code/core@0.19.0
  - @expressive-code/plugin-frames@0.19.0
  - @expressive-code/plugin-shiki@0.19.0

## 0.18.1

### Patch Changes

- Updated dependencies [ccc727e]
  - @expressive-code/plugin-frames@0.18.1
  - @expressive-code/core@0.18.1
  - @expressive-code/plugin-shiki@0.18.1
  - @expressive-code/plugin-text-markers@0.18.1

## 0.18.0

### Minor Changes

- 4e26180: Adds support for ANSI formatted code blocks. Thanks @fflaten!

  You can now use the new language `ansi` to render code blocks containing ANSI escape sequences. This allows you to render colorful terminal output.

### Patch Changes

- Updated dependencies [4e26180]
  - @expressive-code/plugin-frames@0.18.0
  - @expressive-code/plugin-shiki@0.18.0
  - @expressive-code/plugin-text-markers@0.18.0
  - @expressive-code/core@0.18.0

## 0.17.0

### Patch Changes

- Updated dependencies [aba43e2]
  - @expressive-code/plugin-frames@0.17.0
  - @expressive-code/core@0.17.0
  - @expressive-code/plugin-shiki@0.17.0
  - @expressive-code/plugin-text-markers@0.17.0

## 0.16.0

### Minor Changes

- 07012f7: Improves file type support when extracting file names from comments. Thanks @fflaten!

  - Adds more file types to the `LanguageGroups` object
  - Exports `LanguageGroups` to allow external modification
  - Extends automatic detection of frame type to differentiate between shell scripts and terminal sessions based on file name and/or shebang (if any)

### Patch Changes

- Updated dependencies [07012f7]
  - @expressive-code/plugin-frames@0.16.0
  - @expressive-code/core@0.16.0
  - @expressive-code/plugin-shiki@0.16.0
  - @expressive-code/plugin-text-markers@0.16.0

## 0.15.0

### Minor Changes

- Synchronizes package versions to prevent future dependency issues.

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.15.0
  - @expressive-code/plugin-frames@0.15.0
  - @expressive-code/plugin-shiki@0.15.0
  - @expressive-code/plugin-text-markers@0.15.0

## 0.14.0

### Minor Changes

- aa8f09d: Adds support to override frame types per code block. Thanks @Princesseuh!

  By default, the plugin will automatically select the frame type (code editor or terminal) based on the language identifier in your code block's opening fence.

  You can override this behavior and force a specific frame type by adding an optional `frame="..."` attribute after the language identifier.

  The supported values for this attribute are `code`, `terminal`, `none` and `auto`. The default value is `auto`.

### Patch Changes

- Updated dependencies [aa8f09d]
  - @expressive-code/plugin-frames@0.11.0

## 0.13.0

### Minor Changes

- f98937c: Adds config options `useThemedScrollbars` and `useThemedSelectionColors`. Thanks @Princesseuh!

  Both options default to `true`. Set any of them to `false` to prevent themes from customizing their appearance and render them using the browser's default style.

### Patch Changes

- Updated dependencies [f98937c]
  - @expressive-code/core@0.11.0
  - @expressive-code/plugin-frames@0.10.2
  - @expressive-code/plugin-shiki@0.3.9
  - @expressive-code/plugin-text-markers@0.2.11

## 0.12.2

### Patch Changes

- 66de505: Fixes non-working copy buttons in dynamically loaded content.
- Updated dependencies [66de505]
  - @expressive-code/plugin-frames@0.10.1

## 0.12.1

### Patch Changes

- Makes marked text selectable (#15). Thanks @hirasso!
- Updated dependencies
  - @expressive-code/plugin-text-markers@0.2.10

## 0.12.0

### Patch Changes

- Updated dependencies [e010774]
  - @expressive-code/plugin-frames@0.10.0

## 0.11.0

### Minor Changes

- 276d221: Reduces potential of unexpected changes through site-wide CSS.

### Patch Changes

- Updated dependencies [276d221]
  - @expressive-code/core@0.10.0
  - @expressive-code/plugin-frames@0.9.1
  - @expressive-code/plugin-shiki@0.3.8
  - @expressive-code/plugin-text-markers@0.2.9

## 0.10.0

### Minor Changes

- 5da8685: Adds RTL support (ensure that code lines are always LTR).

### Patch Changes

- Updated dependencies [5da8685]
  - @expressive-code/plugin-frames@0.9.0
  - @expressive-code/core@0.9.0
  - @expressive-code/plugin-shiki@0.3.7
  - @expressive-code/plugin-text-markers@0.2.8

## 0.9.1

### Patch Changes

- Enables stricter TypeScript checks (exactOptionalPropertyTypes), improves types.
- Updated dependencies
  - @expressive-code/plugin-text-markers@0.2.7
  - @expressive-code/plugin-frames@0.8.2
  - @expressive-code/core@0.8.1
  - @expressive-code/plugin-shiki@0.3.6

## 0.9.0

## 0.8.4

### Patch Changes

- Fixes feedback tooltip on mobile Safari.
- Updated dependencies
  - @expressive-code/plugin-frames@0.8.1

## 0.8.3

### Patch Changes

- Updated dependencies
  - @expressive-code/plugin-frames@0.8.0
  - @expressive-code/core@0.8.0
  - @expressive-code/plugin-shiki@0.3.6
  - @expressive-code/plugin-text-markers@0.2.6

## 0.8.2

### Patch Changes

- Updated dependencies
  - @expressive-code/plugin-frames@0.7.0
  - @expressive-code/core@0.7.0
  - @expressive-code/plugin-shiki@0.3.5
  - @expressive-code/plugin-text-markers@0.2.5

## 0.8.1

## 0.8.0

### Patch Changes

- Updated dependencies [f8ed803]
  - @expressive-code/plugin-frames@0.6.0
  - @expressive-code/core@0.6.0
  - @expressive-code/plugin-shiki@0.3.4
  - @expressive-code/plugin-text-markers@0.2.4

## 0.7.0

## 0.6.0

### Patch Changes

- Updated dependencies [af207b0]
- Updated dependencies [af207b0]
  - @expressive-code/plugin-frames@0.5.0
  - @expressive-code/core@0.5.0
  - @expressive-code/plugin-shiki@0.3.3
  - @expressive-code/plugin-text-markers@0.2.3

## 0.5.0

### Minor Changes

- Automatically trims whitespace at the end of lines, and removes empty lines at the beginning & end of code blocks.

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.4.0
  - @expressive-code/plugin-frames@0.4.1
  - @expressive-code/plugin-shiki@0.3.2
  - @expressive-code/plugin-text-markers@0.2.2

## 0.4.2

### Patch Changes

- Turns off explanations to improve Shiki performance.
- Updated dependencies
  - @expressive-code/plugin-shiki@0.3.1

## 0.4.1

### Patch Changes

- Fixes issues with color transforms.
- Updated dependencies
  - @expressive-code/core@0.3.1

## 0.4.0

### Patch Changes

- Updated dependencies [6d316f6]
- Updated dependencies [6cdc248]
- Updated dependencies [3ffa599]
  - @expressive-code/core@0.3.0
  - @expressive-code/plugin-frames@0.4.0
  - @expressive-code/plugin-shiki@0.3.0
  - @expressive-code/plugin-text-markers@0.2.1

## 0.3.0

## 0.2.1

### Patch Changes

- Updated dependencies
  - @expressive-code/plugin-frames@0.3.0

## 0.2.0

### Minor Changes

- Initial release.

### Patch Changes

- Updated dependencies
  - @expressive-code/core@0.2.0
  - @expressive-code/plugin-frames@0.2.0
  - @expressive-code/plugin-shiki@0.2.0
  - @expressive-code/plugin-text-markers@0.2.0
