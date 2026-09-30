# Production readiness plan — Power Baze

Assessment date: 2026-09-30. Estimated readiness: **45%** for a public ordering landing page. This is a judgment from repository contents, not a measured completion metric.

## Evidence
- Two identical static HTML pages contain a menu, hours, WhatsApp order links, FAQ, reviews, and loyalty section.
- There is no build pipeline, automated check, content owner checklist, or deployment configuration in this repository.
- The original loyalty form reported success without saving or sending the entered number. This branch replaces it with an explicit WhatsApp message link.
- The pages contain claims about customer counts, ratings, testimonials, ingredients, allergens, discounts, delivery, and hours that require business verification.

## Work completed on this branch
- Changed loyalty signup into a real WhatsApp opt-in action; no false success message or unused phone collection.
- Kept both HTML copies in sync, added safe external-link attributes, keyboard operation and expanded state for FAQ items, and reduced-motion support.

## Remaining, in priority order
1. Business owner verifies menu prices, availability, WhatsApp number, location, hours, delivery radius, promotions, nutrition/allergen statements, reviews and customer metrics. Remove any claim without evidence.
2. Decide whether the second HTML copy is needed. Keep one canonical page and add a redirect if it is not.
3. Replace placeholder `#` footer/social/legal links with real destinations or remove them. Provide privacy and terms information appropriate to actual operations.
4. Complete an accessibility review: visible keyboard focus, semantic FAQ structure, heading order, screen-reader behavior, and meaningful alt text. Keyboard FAQ operation and reduced-motion support have been added but need browser testing.
5. Add a repeatable HTML/link check and a deployment smoke check for mobile and desktop.
6. Publish to a chosen host and test ordering end to end with the business operator.
