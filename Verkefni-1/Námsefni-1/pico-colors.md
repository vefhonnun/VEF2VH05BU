# Pico color themes

[Pico colors](https://picocss.com/docs/colors)

Pico comes with 380 manually crafted colors to help you personalize your brand design system.

In the Pico css folder there is a stylesheet named *pico.colors.css*. **This stylesheet is almost the same size as the entire Pico library**.

> We do not recommend including all colors on a production site. You should include only the color families and shades that you use. 

For example if you are using the *pico-orange.css* library, then copy all **--pico-color-orange-** varibles from *pico.colors.css* into your own color.css document

```
  --pico-color-orange-950: #1b0d06;
  --pico-color-orange-900: #2d1509;
  --pico-color-orange-850: #411a0a;
  --pico-color-orange-800: #561e0a;
  --pico-color-orange-750: #6b220a;
  --pico-color-orange-700: #7f270b;
  --pico-color-orange-650: #942d0d;
  --pico-color-orange-600: #a83410;
  --pico-color-orange-550: #bd3c13;
  --pico-color-orange-500: #d24317;
  --pico-color-orange-450: #e74b1a;
  --pico-color-orange-400: #f45d2c;
  --pico-color-orange-350: #f56b3d;
  --pico-color-orange-300: #f68e68;
  --pico-color-orange-250: #f8a283;
  --pico-color-orange-200: #f8b79f;
  --pico-color-orange-150: #f8cab9;
  --pico-color-orange-100: #f9dcd2;
  --pico-color-orange-50: #faeeea;
  --pico-color-orange: #d24317;

```

## Color schemes

Pico CSS comes with both Light and Dark color schemes, automatically enabled based on user preferences.

### CSS variables for color schemes

To add or edit CSS variables for light mode only (the default mode), define them inside:

```CSS
    /* Light color scheme (Default) */
    /* Can be forced with data-theme="light" */
    [data-theme="light"],
    :root:not([data-theme="dark"]) {
    ... all colors as defined in above list
    }
```

```CSS
    /* Dark color scheme (Auto) */
    /* Automatically enabled if user has Dark mode enabled */
    @media only screen and (prefers-color-scheme: dark) {
        :root:not([data-theme]) {
            ... all colors are in rewersed order
        }
    }
```