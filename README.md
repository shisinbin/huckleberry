# Huckleberry Agency Website

In this workshop, you'll build a minimal landing page for an agency.

This mockup is built entirely using _flow layout_: no Flexbox, no grid, no absolute positioning, no media queries. It relies heavily on padding, margin, and border, as well as some of the tricks we learned in Module 1.

<img alt="Desktop-sized screenshot of an agency landing page" src="./docs/huckleberry-desktop.png" style="" />

The design is available on Figma:

- https://www.figma.com/file/6hGqKA5scrZJScb9KW3Hj2/Huckleberry

## Setup Instructions

This project uses an NPM package called "live-server" — it provides a basic local file server, so that you can view the HTML file in-browser, and automatically reloads the page when the HTML/CSS changes.

Start by installing dependencies:

```
npm install
```

Run the "start" script to start the server:

```
npm run start
```

You should see a confirmation message like this:

![Screenshot of a terminal, showing a server running at http://localhost:9000](./docs/terminal-example.png)

You can visit `http://localhost:9000` to view the page. You should see a bunch of unstyled content:

![Screenshot of an unstyled page with a couple headings and some paragraphs](./docs/initial.png)

> **Trouble with this process?**
>
> Because this project is vanilla HTML and CSS, you can always open the HTML file in your browser, without fussing with a local file server.
>
> Certain JS APIs won't work when viewing files in this way, but that isn't a concern for this project.

---

## Getting Started Notes

- You're given a decent start in terms of the HTML markup, but not much in the way of styles. You'll be expected to edit `style.css` to implement the styles. You can also edit `index.html` if you wish, though it should be possible to solve this project touching only `style.css`.

- Don't worry too much about "best practices". Later in this course, we'll see how to create scalable encapsulated styles. For now, the goal is simply to implement the designs in the screenshots, with whatever organizational strategy comes most naturally to you.

- You may be tempted to reach for CSS strategies we haven't yet seen in the course, like flexbox or absolute positioning. Please try and complete this workshop without them. This module is focused on flow-layout and the box-model, and it is possible to lay everything out on the page using only padding, border, and margin. It's important to be comfortable with these primitives before moving on to more-complex subjects.

- Future workshops will provide a React starter. For the early workshops, the focus is on the fundamentals, so we're using pure HTML and CSS. If you feel more comfortable using a JS framework like React, you can go ahead, but please don't use any component libraries or CSS frameworks. All CSS should be written by hand.

- **Pay close attention to alignment.** For example, you should be able to draw a line along the left, and all text should be neatly aligned:

![Desktop mockup with a vertical line showing alignment](./docs/aligned.png)

(I've made this image semi-transparent to highlight the alignment; see the Figma for a color-accurate reference!)

That said: Don't worry if you can't create a pixel-perfect recreation. In the solution video, I'll show you exactly how I did it. Spend an hour or so on this project, and submit whatever you have at that point.

## Design tokens

In the early days of the web, sites would be built largely on "feel". Colors and sizes would be chosen based on the whims of the moment. This led to some very inconsistent-looking websites!

Nowadays, it's common to have a set of _design tokens_. A design token is a value that can be reused. Typically, it's part of a collection or a scale.

We'll learn more about this idea later, but for now, you can copy/paste the values from this list as-needed. Don't worry about being DRY or using variables; Plop these values in, wherever you need them.

**If you find it difficult to use these tokens, or if you're not able to achieve a result you're happy with, don't worry about it.** Solve it however you can, and then watch the solution video to see how I did it.

### Spacing

This app uses an 8px unit. All spaces are a multiple of 8px:

- `8px`
- `16px`
- `24px`
- `32px`
- `48px`
- `64px`
- `96px`
- `128px`

When it comes to max widths (e.g. the maximum width of the card), arbitrary values can be used.

### Font

1 font is used in this project: `Lato`. It is already included in the stylesheet.

For font sizes, the `rem` unit should be used.

The scale is:

- `1rem`
- `1.25rem`
- `1.5rem`
- `2rem`

By default, `1rem` is equivalent to `16px`.

### Color palette

Primary (green):

- `hsl(160deg, 100%, 30%)`

Secondary (gold):

- `hsl(45deg, 100%, 50%)` (lighter)
- `hsl(45deg, 100%, 40%)` (darker)

Grays:

- `hsl(0deg, 0%, 0%)` (black)
- `hsl(0deg, 0%, 10%)` (very dark)
- `hsl(0deg, 0%, 30%)` (dark)
- `hsl(0deg, 0%, 40%)` (medium)
- `hsl(0deg, 0%, 60%)` (light)
- `hsl(0deg, 0%, 100%)` (white)

## Submissions

**Workshops are submitted through the course platform.** Commit your changes, push them to your fork, and submit the link by clicking the "Complete lesson" button on the workshop page.

If you're not comfortable with Git, you can upload a `.zip` file using Dropbox or Google Drive, and paste a link to the public file instead.

## Note to self

> This was a redo attempt. A sort of refresher. I mostly followed along with the solution video, pausing occasionally to attempt doing things on my own. This was what I put down in the README after completing the challenge months ago:

This was a CSS challenge to lay out a landing page using CSS flow layout. In other words, could I lay out a responsive web page using just margin, border and padding and nothing else?

I gained some practise and understanding of which units to use for different CSS properties. For example, rem seems to be most appropriate for font sizes for accessibility reasons, whereas pixels are better placed for margin and padding in most situations (an example where it might be better to use rem instead of px for margin is the margin-bottom of a paragraph, as when the font size increases it makes sense for the space below the paragraph to expand in kind).

I gained an appreciation for the benefit of using a wrapper element to help position sections, I also gained some practise with using hsl instead of hex codes for the color as they're more intuitive (for example, if I wanted a slightly darker colour for a border-bottom then I could just decrease the lightness of the color being used by 10%).

Using Figma to help with the specifics of colors, borders, pixels, etc, was a lot of fun.

Perhaps the coolest thing was understanding how to use negative margins to help in scenarios where you want text to be aligned. For example, say you have two sections and for each you use a wrapper element to position them (the wrapper element comes with some padding, say). The first section has simple text. The second has a card element that includes padding and text. In order to offset the card's padding so that the text is in line with the text in the section above, a really useful technique is to use negative margins.

Overall, this was a pretty cool workshop which got me thinking about how to use what I'd learnt up to this point to achieve the required layout. It was difficult to curb the instinctive desire to use flexbox or grid, but looking back I like how the challenge got me trying to think more intuitively about CSS.
