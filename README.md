# My Sass Package

A Sass package providing logical property mixins and functions. This package allows you to use CSS logical properties easily and provides utilities for working with CSS custom properties.

## Features

- Logical property mixins for margin, padding, border, and border-radius.
- Utility functions like `process-value` to work with CSS variables.
- Supports both static values and CSS custom properties.

## Installation

You can install this package via npm:

```bash
npm install sass-logical-properties
```

## Usage

To use the mixins and functions in your project, simply import the package into your Sass file.

### Importing the package

```scss
@use 'sass-logical-properties' as *;
```

## Examples

### Logical Margin

Use the `logical-`margin` mixin to apply logical margins based on the flow of the document (left-to-right or right-to-left).

```scss
.example {
  @include logical-margin(top, 20px);  // Output: margin-block-start: 20px;
}
```

### Logical Padding

Use the `logical-padding` mixin to apply logical paddings.

```scss
.example {
  @include logical-padding(left, --spacing);  // Output: padding-inline-start: var(--spacing);
}
```

### Border Radius

You can also apply logical border-radius using the `logical-border-radius` mixin:

```scss
.example {
  @include logical-border-radius(top-left, 10px);  // Output: border-start-start-radius: 10px;
}
```

## Functions

### process-value

This function processes a value and automatically converts CSS custom properties from the format `--value` to `var(--value)`.

```scss
.example {
  color: slp-process-value(--primary-color);  // Output: color: var(--primary-color);
}
```

## Available Mixins

- `logical-margin`(`$side`, `$value`): Sets logical margin based on the side.
- `logical-padding`(`$side`, `$value`): Sets logical padding based on the side.
- `logical-border`(`$side`, `$value`): Sets logical border based on the side.
- `logical-border-style`(`$side`, `$value`): Sets logical border style.
- `logical-border-color`(`$side`, `$value`): Sets logical border color.
- `logical-border-width`(`$side`, `$value`): Sets logical border width.
- `logical-border-radius`(`$corner`, `$value`): Sets logical border radius based on the corner.

## Development

If you want to work on this package locally, clone the repository and install the dependencies:

```bash
git clone https://github.com/sturobson/sass-logical-properties.git
cd sass-logical-properties
npm install
```

### Build the package

To build the Sass files, use the following command:

```bash
npm run build
```

### Watch for changes

To watch for changes and automatically rebuild, use the following command:

```bash
npm run watch
```

## Contributing

Contributions are welcome! If you’d like to contribute, please follow these steps:

 1. Fork the repository.
 2. Create a new branch (`git checkout -b my-feature-branch`).
 3. Make your changes.
 4. Commit your changes (`git commit -m 'Add new feature'`).
 5. Push to the branch (`git push origin my-feature-branch`).
 6. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](/LICENEE) file for details.
