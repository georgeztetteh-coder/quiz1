Prompt 1 (plan, no code):

I’m building a responsive webpage with a flexbox hero section and a 4-column CSS grid layout. I need breakpoints for desktop, tablet, and mobile. The hero should display in two columns on desktop and stack vertically on mobile. The grid should be 4 columns on desktop, 2 on tablet, and 1 on mobile. Please give me a structured plan for implementing this using only HTML and CSS. No frameworks and no code examples.

Response snippet:

Use max-width media queries to progressively reduce layout complexity.
Set desktop as the default layout.
Use flex-direction: column in the mobile breakpoint for the hero section.
Adjust grid-template-columns at different breakpoints.

Prompt 2 (debug):

My hero section is not stacking vertically on mobile even though I added a media query. Here is my CSS:

@media (max-width: 600px) {
  .hero {
    flex-direction: column;
  }
}

It still displays side-by-side. What could be wrong?

Ensure that .hero has display: flex; declared outside the media query. If display: flex is missing or overridden elsewhere, flex-direction will not apply.

