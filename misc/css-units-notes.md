# On CSS units

- all options are viable and have their pros and cons
- no strict rules
- good practices for each

## Em, Rem, and Pixel
  https://codepen.io/angeliquejw/pen/RYxxpO?editors=1100

### em

- Relative to the font-size of the direct parent. 3em is 3x the font-size of the parent element
- Often used in media-queries, em is great for responsiveness, but it can get really confusing tracing back the exchange rate of ems to pixels for each element (1.25em of 1.4em of 16px = ?).
- It's been recommended in the past to set the body size to 10px or 62.5% (which also works out to 10px) to make the math easier on ems -- 2ems would then equal 20px; but then we're
  1. setting the body font size to something pretty tiny and unreadable
  2. as a result, absolutely must set the font-size on every element we create
  3. and we're doing this all to make things easier on ourselves as developers :(
  4. if we end up later setting the p tag to be 16px -- is 10px really our base font size?

### rem

- Stands for root em, relative to the font-size of the html element, rem makes it really easy to scale all headings and paragraphs on the page. Leaving the html with it's default fontsize and setting everything else with rem is a great approach accessibility-wise.
- For example, if the font size of the HTML tag is 16px (that is the default size for an html document), then 1rem unit is equal to 16px. That makes .5rem=8px, 2rem=32px, etc.

### px
- Pixels give you the most precision but don't offer any scaling when used in responsive designs.
- They are reliable, easy to understand, and present a good visual connection between value and actual result (15px is close, maybe just a pixel or two more). No fraction of pixels. Doesn't scale with user-set font-size (does scale with % zoom increase).

## vw/vh
  https://codepen.io/angeliquejw/pen/jvYxxy?editors=1100

## %
  https://codepen.io/angeliquejw/pen/gdozJa?editors=1100

- also relative to parent, like em; can be useful for utility classes like .u-text-small

## Units for elements, width height
  https://codepen.io/angeliquejw/pen/dqJdLp?editors=1100
