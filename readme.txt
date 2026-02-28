Name: TettehGeorge

Tools used: ChatGPT, Google Colab, Chrome Browser

--------------------------------------------------

Q1:

- Key finding (2–4 sentences):

The scatter plot of study hours versus exam score shows a strong positive linear relationship, supported by a clearly upward-sloping trendline. As study hours increase, exam scores increase consistently. In contrast, the sleep-hours plot shows a weaker and more scattered pattern, suggesting sleep is less predictive of performance in this dataset. Based on visual strength and the slope value, study time appears to be the more influential variable.

- Outlier:

Student L appears to be a mild outlier because they scored 80 while sleeping 8 hours, performing slightly above others with similar study-hour ranges.

--------------------------------------------------

Q2:

- What was broken:

The layout was not responsive. The header did not properly align logo left and navigation right on desktop, the hero section did not stack correctly on mobile, and the grid did not adjust column counts at different breakpoints.

- What I changed:

I added flexbox alignment to the header, implemented max-width breakpoints for tablet and mobile, set the hero section to use flex-direction: column under 600px, and adjusted grid-template-columns to 4 columns on desktop, 2 on tablet, and 1 on mobile. I also added hover effects for the cards and button.

--------------------------------------------------

Q3:

Prompt 1 (plan, no code):

I’m building a responsive webpage using flexbox for the hero section and CSS grid for a 4-column layout. I need it to work for desktop, tablet, and mobile. The hero should be two columns on desktop and stack vertically on mobile. The grid should be 4 columns on desktop, 2 on tablet, and 1 on mobile. Please give me a structured implementation plan using only HTML and CSS. No frameworks and no code examples.

Response snippet:

"Start with the desktop layout as the default. Use max-width media queries to progressively reduce layout complexity. Apply flex-direction: column inside the mobile breakpoint for the hero section. Adjust grid-template-columns at each breakpoint."

Accepted:

- Use desktop as default and scale down with max-width queries.
- Use flex-direction: column inside the mobile breakpoint.

Rejected:

- A suggestion to use CSS frameworks, because the assignment requires pure HTML and CSS only.

--------------------------------------------------

Prompt 2 (debug):

My hero section is not stacking vertically on mobile even though I added this:

@media (max-width: 600px) {
  .hero {
    flex-direction: column;
  }
}

It still shows side-by-side. What could be wrong?

Response snippet:

"Make sure that .hero has display: flex declared in the base styles. If display: flex is missing or overridden, flex-direction will not apply."

What I verified:

- viewport sizes tested: 375px, 768px, 1200px
- what I checked visually:
  - Logo left / nav right on desktop
  - Nav stacked on mobile
  - Hero stacking under 600px
  - Grid changing 4 → 2 → 1 columns
  - Hover effects working on cards and button

--------------------------------------------------

Q4:

- Chart caption:

This chart shows a strong positive relationship between study hours and exam score, with performance increasing steadily as study time increases. Based on this trend, I would recommend increasing structured study hours to improve exam outcomes.

- Decision based on chart:

Encourage students to dedicate more consistent study hours, since the data suggests that increased study time has a measurable impact on performance.
