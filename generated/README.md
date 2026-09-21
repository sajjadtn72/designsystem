# ANT Design System . Custom

## Install

Import generated/tailwind.css from your application stylesheet. Tailwind 4 must be installed in the consuming project. theme.css maps ds-prefixed utilities to runtime CSS variables using @theme inline. Do not import components.css a second time.

Example: @import "./generated/tailwind.css";

## Plain CSS

variables.css and components.css are standalone CSS: import both if Tailwind utilities are not needed. Per-component CSS requires variables.css; per-component variable files include transitive aliases.

## Usage

Import generated/index.css for plain CSS. Open any file under examples/ directly in a browser; it includes the matching HTML, CSS and CSS-only geometry. components.json lists every component and example path. diagnostics.json records extraction warnings. Keep the directory structure intact. Font files must be supplied and licensed by your application; font-family tokens alone do not install fonts.

Open docs/index.html locally for component previews, exact HTML data attributes, token-to-class mappings and variants. Classes use the ds- prefix for tokens, e.g. bg-ds-primary when a color/primary token exists. Set data-theme to a documented mode name. Use the generated markup structure to preserve child-node styles, but supply accessible semantics and interaction behavior.

## Updating

Review generated Git pull requests and merge them, then pull the changes into your application. Never edit generated files: update Figma and regenerate.

## Coverage

Supported: solid fills, basic borders, opacity, typography, shadows, auto-layout, per-side padding, radius, token bindings and compound variants. Complex paints, mixed text runs, unavailable CSS-only geometry, absolute positioning, responsive behavior and interactive logic require implementation and visual review. SVG export is disabled. Complex vector shapes and exact stroke caps require developer implementation. These previews use generated CSS, not a pixel-accuracy guarantee.
