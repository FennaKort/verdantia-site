# Project Description
Verdantia is a demo website for a hypothetical company selling plant-related services. The Verdantia site is designed to appeal to creative urban millenials who value incorporating meaningful experiences into their daily lives. Verdantia offers these experiences through their curated events that let their customers bring the beauty of plants into their every day spaces. The website communicates with these target consumers through lush images of calladiums, a refined yet fun green and pink colour pallette, and site organization that allows visitors to quickly and easily learn about what Verdantia offers and how to inquire about Verdantia's services. 

# General Task Distribution - Part 2
mobile responsiveness - Fenna focus
accessibility - Damon focus

# Task Log - Part 2
31 Mar. Fenna updating page organization and stylesheet links. Fenna updating class/id naming convention
To-do:
[x]change css folder to styles and update on all pages
[x]create pages folder and update links on all pages
[x]add normalize-css.css to all pages, above link to main.css
[x]update class/id naming conventions to lowercase with dashes
[x]remove duplicate styles/consolidate styles where possible
[x]replace what we offer and contact us h1s with h2s and ensure good document outline

[x]put fullsize styles into correct media queries
[x]main needs to be <=790px in large size
	-because of full width backgrounds, the site needs a workaround instead
[x]adjust table styles to be responsive
- added responsive sticky nav :3
	[]adjustments needed for:
	- iphone 12/13 pro max - not enough smol
	- galaxy s20+ - too smol

[x]may be able to consolidate styles for price table container and tagline container
[]may be able to consolidate styles for what we offer and contact form hover styles
[x]may be able to remove styles for entire call to action section at around line 370
[x]add scrollbar-gutter and style scrollbar
[x]adjust .buttons class name to be more descriptive

2 Apr 25. Fenna finishing mobile display; making adjustments to where links jump to on the page; adjustments to offer details section including adding another offer


2 Apr 25 - Damon

Implemented accessibility fixes based on WCAG 2.1 guidelines
Ran WAVE automated accessibility testing and resolved flagged issues
Added 2x2 grid layout using CSS Grid on medium screens (590px-789px)
Forced vertical stacking of image/text in offer cards on medium screens
Standardized card sizing with grid auto-rows and flex layout
Centered content text properly in cards by overriding inherited margins
Replaced orphaned <label> elements with <fieldset> and <legend> for grouped inputs
Added a visually hidden <h2> to the Price List section to satisfy section heading validation
Validated all pages through W3C validator and corrected structure where needed

------------------------------------------------------------------------------------------------------------------------------------------
Accessibility Review:

We conducted both manual and automated accessibility reviews.

Manual Accessibility Review:

We performed a thorough manual accessibility audit of the Verdantia website using WCAG 2.1 AA guidelines, focusing on the four main principles: Perceivable, Operable, Understandable, and Robust.

---

Perceivable:
- All images on the site have descriptive and meaningful `alt` attributes.
- Headings are used in a logical and hierarchical structure. Pages start with an `<h1>` or `<h2>` and follow with `<h3>` as needed.
- Decorative images (e.g., logo) have empty or omitted alt text where appropriate.
- Color contrast meets WCAG AA for large text:
  - `#A04D69` (dark pink) on `#F6DDDD` (light pink) has a ratio of 4.33:1, which passes for large text (used in headings).
  - `#11451F` (green) on light backgrounds has excellent contrast (>9:1).
  - Lighter pinks such as `#CC6D8A` on `#F6DDDD` are only used for large or decorative text to avoid failing contrast.
- Text remains readable when zoomed in up to 200%.
- Font sizing is consistent and legible (base size 20px, responsive typography for headers).

---

Operable:
- All interactive elements are accessible via keyboard (tested using Tab/Shift+Tab navigation).
- Visual focus indicators are clearly visible when tabbing through links and form fields.
- Form fields and buttons are spaced sufficiently for easy interaction.
- No keyboard traps are present, and users can navigate smoothly through the entire site.
- Site uses sticky navigation, improving usability on small screens.
- Skip links are not implemented, but the site is still easily navigable.

---

Understandable:
- Every form field is associated with a `<label>` element using `for="id"`, improving clarity for screen reader users.
- Required fields are clearly marked with an asterisk and use `required` in the markup.
- Form inputs use appropriate types (`email`, `tel`, `number`) to trigger device-optimized keyboards.
- Placeholder text provides helpful context without replacing labels.
- Navigation is consistent across all pages, and link behavior is predictable.
- Pages use `<html lang="en">` to define language properly.

---

Robust:
- All HTML passes validation via the W3C Validator.
- The site uses semantic HTML5 structure: `<header>`, `<main>`, `<section>`, `<nav>`, and `<footer>` are used meaningfully.
- ARIA attributes were not required, as semantic tags and labels are sufficient for current structure.
- The design remains functional and consistent across modern browsers and devices.

---

Conclusion:
The Verdantia website adheres to most WCAG 2.1 AA guidelines and was built with accessibility in mind from the ground up. Color contrast, form accessibility, keyboard navigation, and semantic structure were all evaluated and adjusted where necessary. No known accessibility blockers remain.


Automated Accessibility Review (WAVE):

We used the WAVE Web Accessibility Evaluation Tool to test all three pages of our website. WAVE flagged the following issues:

---

1. ⚠️ Long Alternative Text
- One image was flagged for having overly long alternative text.
- Issue: The `alt` attribute for the image in the "Plant Party" section was detailed enough to be a caption.
- Resolution: We shortened the `alt` text to briefly describe the image content and moved extra details into a `<figcaption>` or body text when appropriate. Long descriptions are better placed in visible content, not alt text.

---

2. ⚠️ Orphaned Form Labels (2)
- Labels for “Preferred contact method” and “I am interested in…” were flagged as orphaned.
- Issue: WAVE detected that the `<label>` elements are not correctly associated with corresponding inputs (radio buttons and checkboxes).
- Resolution: We reviewed and adjusted the form markup to ensure that each label wraps its corresponding input OR uses `for` and `id` pairs correctly. For groups (like checkboxes), we ensured the label is either:
  - Associated individually (`<label for="input-id">`)
  - Or used a `fieldset` with a `legend` for clarity
  




--------------------------------------------------------------------------

# General Task Distribution - Part 1 
site design - Fenna focus
site content - Both focus
html - Damon focus 
css - Fenna focus
conformity to project reqs - distribute 50/50 so we've got equal eyes making sure we've got everything

# Task Log
5 Feb 25
- Damon made discord server for communication
- Fenna proposed various ideas for site
- both discussed site reqs and content

6 Feb 25
- continued discussion of site reqs
- Fenna started mockup in Figma
- hammered out task distributions and group expectations

8 Feb 25
- Fenna continued draft of site design https://www.figma.com/proto/rFTSPAskqrZJrXROk0hsXx/Plant-Site?node-id=2-2

10-11 Feb 25
- Damon worked on majority of HTML; also on css

13 Feb 25
- Fenna working on CSS; primarily adjusting display for homepage and reorganizing font heirarchy structure
[x] site needs a figure and figcaption - added 20 feb to services page

HTML changes:
- replaced div with nav for menu buttons
- added main and footer tags
[x] footer tags need content
- changed id structure for tagline container on homepage

20 Feb 25. 
- Fenna working on CSS
- resized all images according to design specs
- replaced outer divs on services page with section elements for improved semantic html

22 Feb 25. Damon worked on form html, button links html, and form css.

25 Feb 25. Fenna
- adjusted fieldsets and item order for form
[x] needs regex for phone and email
[x] needs reset button for form
[x] needs subject textarea for form - replaced with checkboxes to indicate type of inquiry
[x] would be nice to improve styling of radio buttons+labels
[x] would be nice to swap services select for checkboxes
[x] why won't the top and bottom padding for label.formField push out more space between the items? - because <label> doesn't have height+width that can be set. I added a margin-bottom value to the input fields instead
- validated all three html pages and corrected errors
[x] table needs alternating colours
[x] Use the first-letter pseudo element selector to style a first letter of (at least) one of 
your paragraphs differently. - added to footer

26 Feb 25. Fenna working:
Remaining:
MUST:
[x] site needs logo
[x] float an image to the right side of a paragraph of your choice in your website. 
- where to even do this hmmmmm
- contact button on offer page?? NOPE LOL that looks like dogshit
	- I fixed it by doing two small images, one on either side of the text

[x] NEED TO VISUALLY DISTINGUISH REQUIREDS FROM NONREQS ON FORM

NICE TO HAVE:
[x] need to fix table styling to conform to design specs
[x] fix contact button at bottom of services page 
[x] fix styling of contact page to coordinate with other pages
[] adjust body/main margin+padding and child element padding for a more maintainable organization - may come back to in the future
[] rename variables - jim says consistent format is best, but he won't mark down for it - may come back to this in the future

28 Feb 25. Fenna giving final pass to project reqs and packaging zip file for submission. 