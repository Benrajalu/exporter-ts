# Custom SCSS Exporter for Talend

The TS Exporter exports a theme into a TS object. It runs for:

- [x] Colors
- [x] Text Styles
- [x] Sizes
- [x] Shadows
- [x] Borders
- [x] Opacities
- [x] Radii

It outputs two files.

An `index.ts` exporting a single `tokens` object listing all the available tokens and their values:

```ts
const tokens = {
  coralColorNeutralText: `var(--coral-color-neutral-text, hsla(0,0%,13%,1))`,
  coralColorNeutralTextWeak: `var(--coral-color-neutral-text-weak, hsla(0,0%,42%,1))`,
  coralColorNeutralTextDisabled: `var(--coral-color-neutral-text-disabled, hsla(0,0%,55%,1))`,
  coralColorNeutralTextInverted: `var(--coral-color-neutral-text-inverted, hsla(0,0%,100%,1))`,
  coralColorNeutralBackground: `var(--coral-color-neutral-background, hsla(0,0%,100%,1))`,
  coralColorNeutralBackgroundMedium: `var(--coral-color-neutral-background-medium, hsla(0,0%,97%,1))`,
  coralColorNeutralBackgroundStrong: `var(--coral-color-neutral-background-strong, hsla(0,0%,91%,1))`,
...
};
```

And a `dictionary.ts` exporting a single `dictionary` array listing a detailled view of all available tokens:

```ts
const dictionary = [
    {
        name: 'coralColorNeutralText',
        type: 'Color',
        description: `Default text color`,
        hsla: 'hsla(0,0%,13%,1)',
        hex: '#202020',
        value: 'hsla(0,0%,13%,1)',
    },
    {
        name: 'coralColorNeutralTextWeak',
        type: 'Color',
        description: ``,
        hsla: 'hsla(0,0%,42%,1)',
        hex: '#6b6b6b',
        value: 'hsla(0,0%,42%,1)',
    },
...
];
```
