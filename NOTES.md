# Mistvale Tea Co. — Project Notes

## 1. Project Overview

**Project:** Mistvale Tea Co. Ecommerce Storefront  
**Assessment:** MeroxIO Web Developer Assessment  
**Purpose:** Improve the existing single-page ecommerce storefront for an Indian specialty tea brand while following the supplied assessment requirements.

The website presents tea products and supports product discovery, shopping cart interactions, coupon calculations, delivery checking, and checkout form submission.

**Brand tagline:** “Hill-grown tea, honestly made.”

## 2. Project Structure

The submission contains the following files and directories:

- `index.html` — Main storefront containing the HTML, CSS, and JavaScript.
- `images/` — Product images, hero image, and other website assets.
- `PROMPTS.md` — Documentation of AI prompts and the development workflow.
- `NOTES.md` — Project overview, implementation decisions, testing, and limitations.

The implementation follows the assessment's single-file requirement for HTML, CSS, and JavaScript. Image assets are stored separately in the `images/` directory.

## 3. Changes and Improvements

### Storefront and Visual Design

- Refined the storefront using the supplied brand direction.
- Used a restrained colour palette based on forest green, leaf green, cream, parchment, and limited saffron accents.
- Improved the presentation and consistency of product cards.
- Integrated product-specific imagery and a hero banner.
- Kept website text and interactive controls separate from photographic assets.
- Preserved the existing product data and required project structure.

### Product Discovery and Shopping

The implementation was developed to support the following assessment requirements:

- Product search, category filtering, and sorting.
- Product details and quick-view interactions, where provided.
- Add-to-cart, quantity updates, and item removal.
- Stock validation and sold-out product handling.
- Coupon validation and discount calculations.
- Shipping calculations and delivery checking.
- Checkout form preparation and submission.

The final implementation should be reviewed against the original assessment requirements to confirm the behaviour of each feature.

## 4. Image Assets and Preparation

The following filenames are intended for the product images and hero banner:

| File | Product or purpose |
|---|---|
| `images/p101.webp` | Assam Breakfast Black Tea |
| `images/p102.webp` | Darjeeling First Flush |
| `images/p103.webp` | Kashmiri Kahwa |
| `images/p104.webp` | Masala Chai Blend |
| `images/p105.webp` | Nilgiri Green Tea |
| `images/p106.webp` | Chamomile & Tulsi |
| `images/p107.webp` | Hibiscus Rose Infusion |
| `images/p108.webp` | Tea Lover's Sampler Gift Box |
| `images/hero.webp` | Tea garden hero banner |

**Image sourcing:** The initial images were sourced from the internet.

**Image preparation:** The images were converted to WebP before being used in the website.

**Image conversion tool:** [Enter the actual tool used.]

**Image source URLs:** [Add the original URLs if available.]

**Image verification:** Confirm that all listed files exist, their formats are correct, and their paths match the references in `index.html`.

Do not describe the images as AI-generated unless that accurately reflects how the specific assets were created.

## 5. Business Rules and Implementation Constraints

The following requirements are based on the supplied assessment instructions:

- Preserve the original product IDs, names, and prices in `PRODUCTS`.
- Do not modify the code between the `API START` and `API END` markers.
- Keep the required checkout form ID, action, method, and field names unchanged.
- Preserve the approved legal footer text.
- Restrict each product quantity to a maximum of five and the available stock.
- Prevent sold-out products from being added to the cart.
- Keep sold-out products at the end of every sorting order.
- Make search, category filtering, and sorting work together.
- Apply the `WELCOME10` coupon case-insensitively, with a 10% discount on eligible items, a maximum discount of ₹150, a minimum eligible subtotal of ₹399, and no discount on products in the Gifts category.
- Prevent coupon stacking.
- Apply ₹49 shipping unless the applicable free-shipping condition is met.
- Display prices using Indian currency formatting.
- Handle valid, invalid, unserviceable, and failed pincode checks with appropriate feedback.

### Free-Shipping Threshold

The supplied project material contains conflicting references to ₹499 and ₹599.

**Threshold in the final code:** [Verify the actual implementation.]

**Decision:** Document which requirement the implementation follows and retain the discrepancy as an unresolved assessment ambiguity if it has not been clarified.

## 6. AI-Assisted Development Workflow

Claude / Claude Code was used for website development in multiple parts. ChatGPT was used for debugging assistance, including investigation of the reported checkout-button issue.

The workflow included:

1. Reviewing the supplied project and assessment requirements.
2. Developing and refining website sections.
3. Integrating the product and shopping interactions.
4. Sourcing and preparing images for the website.
5. Investigating reported code issues.
6. Reviewing the final implementation and recording test results.

The original master prompt and the documented development workflow are included in `PROMPTS.md`.

## 7. Testing and Verification

The user reported that all listed tests passed. The table below records that reported status; it is not an independent test report.

| Test area | Reported result |
|---|---|
| Page layout and responsive design | PASS |
| Product images and hero banner | PASS |
| Product search | PASS |
| Category filtering and sorting | PASS |
| Cart add and remove operations | PASS |
| Quantity limits and stock validation | PASS |
| Sold-out product behaviour | PASS |
| Coupon validation and discount calculations | PASS |
| Shipping calculations | PASS |
| Pincode validation and delivery response | PASS |
| Checkout form payload and submission | PASS |
| Newsletter interaction | PASS |
| Accessibility and keyboard navigation | PASS |

**Testing method:** [Describe the actual manual or automated testing performed.]

**Browser and device coverage:** [Enter the browsers and devices actually tested.]

**Automated tests:** [Enter the tool and actual results, or write “No automated test results recorded” if applicable.]

Only retain PASS for checks that were actually performed on the final version.

## 8. Known Limitations and External Dependencies

- The assessment checkout URL uses a placeholder domain. A successful live payment cannot be claimed unless a real payment integration exists and has been verified.
- External API behaviour depends on the supplied simulated API and its responses.
- Image loading and Google Fonts may depend on network availability.
- Browser compatibility, screen-reader support, Lighthouse results, and physical-device testing should be reported only if those checks were performed.
- The free-shipping threshold ambiguity should be documented until the intended value is confirmed.

## 9. Issues and Corrections

### Checkout Button Issue

**Issue reported:** Clicking the checkout button did not open or execute the expected checkout flow.

**Debugging assistance:** ChatGPT was used to investigate the checkout handler and form-submission behaviour.

**Areas reviewed:** Checkout button handling, cart item serialization, coupon field population, and the required checkout form contract.

**Verification:** The checkout test was reported as passing. The external placeholder checkout destination is not evidence of a functioning live payment backend.

Other issues should be added only when they were actually encountered, along with the correction and the method used to verify it.

## 10. Further Improvements

Potential future improvements include:

- Additional cross-browser testing.
- Accessibility audits using appropriate tools.
- Physical-device testing on mobile screens.
- Image performance measurements.
- More automated tests for coupon, stock, shipping, and checkout edge cases.

These are potential improvements, not claims of completed work.

## 11. Final Submission Checklist

- [ ] `index.html` is included.
- [ ] The `images/` directory contains all required assets.
- [ ] All image references resolve correctly.
- [ ] `PROMPTS.md` is included.
- [ ] `NOTES.md` is included.
- [ ] Product data remains unchanged.
- [ ] The protected API block remains unchanged.
- [ ] The checkout form contract remains unchanged.
- [ ] The approved legal footer text remains unchanged.
- [ ] Business rules have been checked against the assessment.
- [ ] Testing results accurately reflect the tests performed.
- [ ] The ZIP archive is under 20 MB.
- [ ] The final ZIP has been extracted and checked before submission.
- [ ] The resume is prepared separately if required.

## 12. Final Statement

This document summarises the project structure, intended functionality, reported development workflow, testing status, and known constraints for the Mistvale Tea Co. assessment.

Any unresolved requirements, external dependencies, or unverified results should remain explicitly documented rather than being presented as completed or independently verified.
