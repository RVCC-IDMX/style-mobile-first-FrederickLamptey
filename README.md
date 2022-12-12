# Mobile Rules

A page with minimal mobile-first styling using a reset/normalize library followed by some local CSS rules to make the page useable and accessible.

## Rules For Minimum Functionality

1. The page must view well starting at 320px viewport width and above (with **no media queries** affecting layout or font sizes). Note: The iphone 5/SE in Chrome dev tools is 320px wide in profile mode.
2. Line widths and heights must allow for readability.
3. Elements must have room to breath and text **cannot** hug the sides of the device.
4. You must use @import to load one or more Google fonts (no user agent default fonts).
5. You must use a reset/normalize library to start your CSS.
6. The skip link must be hidden but will display when tabbed.
7. Be sure to include accessibility features that are not necessarily present in the default user agent styles or the reset/normalize styles. For example, line-height by default is too small. If your reset/normalize does not fix this, your local code should.
8. You may use fluid type and spacing (See below for examples).
9. The nav bar will be simple and remain visible (and not collapse to a hamburger at small widths).
10. Consider using grid and gap to vertically space out elements instead of margins (this protects against margin collapse). And consider using flex on the nav ul.
11. You may give the body a colored background and a contrasting font color, as long as the color contrast > 7. (Something other than stark black on stark white actually improves accessibility for most people.)
12. Colors and font sizes should be declared using custom properties.
13. You may style lists.
14. If you feel the need to cite a resource, add it to this README.


> NOTE: This challenge is partly an exercise in accessibility and layout. One default property that tends to make layout hard are lists. This is because the position of the list marker (or list style) is, by default, outside of the element. Consider changing the marker to be inside the element.

```css
:where(ul, ol) {
  list-style-position: inside;
}
```

---

### Available Fluid Code Examples

[Andy Bell's spacing.css - Consistent spacing sizes, based on a ratio, with min and max sizes.](https://gist.github.com/cynthiateeters/88825c17225ce01ef7461e3cd22997ca)

[Andy Bell's text-sizes.css - A minimum and maximum text size allows you to pick the right size from a ratio, depending on the context size.](https://gist.github.com/cynthiateeters/5af47329cbe01e4497b3a0647a5aece4)

### Searching for CSS Reset/Normalize Libraries

[Search GitHub](https://github.com/search?o=desc&q=css+normalize&s=stars&type=Repositories)

[Search CDNJS - search for normalize ](https://cdnjs.com/libraries)

---
## IDMX 11ty Sass Starter

The set of development scripts in this starter is configured to watch and compile a simple Sass structure using 11ty.

The code is located in the `src` folder and the page is created in the `public` folder.

The `settings.json` in the `.vscode` folder sets the `LiveServer` configuration to serve from the `public` folder and can be used to serve the built page.

The build process includes minifiying and autoprefixing of styles via the `postbuild` script, which runs automatically after a `build`.

## Installation

**`npm install`**

>Run this command once to install the needed node modules.

## Development Scripts

**`npm start`**

> This script runs 11ty with hot reload and served at the url localhost:8080. It will reload whenever there are HTML or Sass changes.

**`npm run build`**

> This script does a production build and includes minified, autoprefixed CSS.

Use this as the "Publish command" if needed by hosting services such as Netlify.
---

### Resources

[HTML Content from Style Stage by Stephanie Eckles](https://stylestage.dev)

[Build Excellent Websites by Andy Bell](https://buildexcellentwebsit.es/)

[Code for Bell's Build Excellent Websites (the source for the Fluid CSS code linked above) ](https://glitch.com/edit/#!/build-excellent-websites)

