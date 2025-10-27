# Overview

An experimental Drupal theme.

## Starting

'npm i'

### To compile postCSS

'npm run dev'

## Front-end Development

### Tech Stack
We are using:

- node
- vite
- PostCSS
- BEM CSS methodology
- Prettier

### PostCSS
PostCSS is in a separate directory from compiled CSS. We are using vite to compile into CSS.

⚠️ DO NOT WRITE CSS IN THE CSS EXTENSION FILES
✅ Write CSS in the pcss files
✅ Add components as imports to dist/style.css

CSS should be written using ancestor nesting and Block-Object-Modifier methodology. We are using postCSS (instead of native nesting) so that BEM methodology can be applied through concatenation of class partials.

### CSS
All Component CSS is contained within /components (do not edit directly).

### Variables

CSS Variables are in components/00-base/vars.

We are using a two-level color system:

- Primitive colors (sets the values)
- Semantic colors (references the primitive colors, resetting the names to meaningful system-wide names)

### Assets
This directory in /dist/assets contains shared graphics such as logos and icons which are needed by the theme. Some assets here may be referenced in our components CSS.

### Linting
 We should lint only the folder src/postcss (do not lint compiled CSS). We can apply SCSS rules for nesting.

This repo has stylelintrc.json for setting linting rules and stylelintignore for ignore files.

To run linting on PostCSS:
'npx stylelint "src/postcss/*.css"'

## Contributing

Reference (contributing docs)[docs/contributing.md]
