PROMPTS.md — Mistvale Tea Co. / MeroxIO Web Developer Assessment
1. Purpose of This File
This file organizes the documented AI-assisted workflow for the Mistvale Tea Co. assessment in chronological order. It distinguishes the original Claude master prompt from the additional development, image sourcing, conversion, and debugging steps described during the project.

Tools used (as reported):
- Claude / Claude Code: Main website development, worked on part by part.
- ChatGPT: Assistance with debugging, including the reported checkout-button issue.
- Web browser / internet image sources: Initial product and website images were sourced online.
- Image conversion tool: The downloaded images were converted to WebP before being used. The exact conversion tool was not specified in the available notes.
Record-keeping note: The complete Claude master prompt is reproduced verbatim in Section 3. The other workflow sections below are organized summaries based on the process described; they are not claimed to be word-for-word copies of earlier chat messages. If the assessment requires every historical prompt verbatim, copy any additional prompts directly from the original Claude and ChatGPT conversations.

2. Chronological Workflow
Step 1 — Inspect the supplied project and assessment
Tool: Claude / Claude Code
Task: Use the supplied project ZIP, assessment README, BRAND.md, existing index.html, product data, simulated API, checkout form, legal footer text, and image assets as the source of truth.

Objective: Understand the starter project and constraints before making changes. Preserve the protected product data, API block, checkout contract, and approved legal text.

Outcome recorded: The user reports that Claude was used to build the website. The exact outcome of each individual implementation step should be verified against the final submitted files.
Step 2 — Develop the website in parts
Tool: Claude / Claude Code
Task summary: Build and refine the existing Mistvale Tea Co. website in smaller parts, following the assessment brief and brand direction.

The documented scope included:
- Page structure, navigation, hero, trust strip, product section, delivery check, reviews, FAQ, newsletter, and footer.
- Product search, category filters, sorting, quick view, cart interactions, quantity and stock limits.
- Coupon and shipping calculations.
- Pincode serviceability and delivery feedback.
- Responsive styling, accessibility, SEO metadata, and structured data.
Prompt record: The master prompt used for the main implementation is reproduced verbatim in Section 3. Additional part-by-part prompts should be copied from the original Claude conversation if a verbatim history is required.
Step 3 — Source the images from the internet
Tool: Web browser / internet image sources
Task: Find and save suitable images for the tea website.

Process described by the user:
1. Search for relevant images online.
2. Download or save selected image files.
3. Convert the saved images to WebP format.
4. Place the converted files in the project's images/ folder.
5. Reference those image files from the website.
Important: These were internet-sourced images, not AI-generated images. Add the actual source URLs here if available. Do not invent source URLs or claim image generation took place.
Step 4 — Convert the sourced images to WebP
Tool: Image conversion software or online converter (exact tool not specified)
Task: Convert the sourced image files to WebP before using them in the website.

Record to complete if known:
- Conversion tool: [Enter the actual tool used]
- Original image source URLs: [Add actual URLs if available]
- Final image filenames: [Use the actual filenames in images/]
No image dimensions, compression percentages, or file-size improvements are claimed here because those values were not provided.
Step 5 — Debug the checkout issue with ChatGPT
Tool: ChatGPT
Reported issue: The checkout page or expected checkout flow did not appear after clicking the checkout button.

Debugging focus described in the conversation:
1. Inspect the checkout button click handler.
2. Inspect the existing checkout-form.
3. Confirm that items contains the cart items as a JSON array using actual product IDs and quantities.
4. Confirm that coupon contains the applied coupon code or an empty string.
5. Preserve the required POST form contract and avoid unrelated changes.
6. Re-test the checkout interaction after applying the fix.
Checkout contract that must remain unchanged:
- Form ID: checkout-form
- Action: https://mistvale.example/cart/checkout
- Method: POST
- Required fields: items and coupon
The checkout URL is a placeholder. A destination error page from that placeholder does not, by itself, prove that the frontend form payload or submission code is incorrect.

Prompt history: This section summarizes the reported debugging work. The exact original ChatGPT request and answer should be copied from that conversation if verbatim historical prompts are required.
Step 6 — Final functional testing
Tool: Manual testing / browser testing, as performed by the user
Reported status: The user stated that all testing passed.
Test area	Reported result
Page layout and responsive design	PASS
Product image loading	PASS
Search and category filters	PASS
Product sorting	PASS
Product quick-view functionality	PASS
Cart add and remove operations	PASS
Quantity limits and stock validation	PASS
Coupon validation and discount calculations	PASS
Shipping calculations	PASS
Checkout form payload and submission	PASS
Pincode validation and delivery response	PASS
Newsletter interaction	PASS
Accessibility and keyboard navigation	PASS


These results are recorded as reported by the user; this document does not independently execute or certify the tests. Keep PASS only for checks that were actually performed on the final version.
3. Original Claude Master Prompt — Verbatim
Tool: Claude / Claude Code
Purpose: Main implementation of the existing Mistvale Tea Co. project according to the MeroxIO assessment.

The following is the original master prompt supplied by the user, preserved verbatim.
MASTER PROMPT — MeroxIO Mistvale Tea Co. Assessment
Act as a senior frontend engineer, premium e-commerce UI/UX designer, JavaScript debugging specialist, accessibility engineer, SEO specialist, and QA tester.

Your mission is to transform my existing Mistvale Tea Co. starter project into a polished, professional, production-quality single-page tea store for the MeroxIO Web Developer Assessment.

IMPORTANT: I have limited AI usage and a strict submission deadline. Work efficiently, avoid unnecessary questions, avoid lengthy explanations, and complete as much of the implementation as possible in one carefully planned pass. Inspect first, make changes systematically, and validate your own work.

I will provide the original assessment ZIP containing index.html, images/, BRAND.md, and the assessment README.
1. FIRST: READ THE PROJECT AND PROTECT IT
Read the complete README, BRAND.md, and existing index.html before making changes.

Inspect the original product data, CSS, JavaScript functions, simulated API, checkout form, legal footer text, image paths, and every existing feature.

Make a backup if file-editing tools are available.

Do not ask me to explain requirements already present in the supplied files. Do not replace the project blindly with a generic website template.

Create a short internal implementation checklist, then proceed directly to implementation.
2. ABSOLUTE TECHNICAL CONSTRAINTS
These are mandatory:
- Keep all HTML, CSS, and JavaScript inside the existing index.html.
- No React, Next.js, Vue, jQuery, Tailwind, Bootstrap, icon libraries, external JavaScript libraries, build tools, or separate CSS/JS files.
- Google Fonts are allowed.
- Keep images inside the existing images/ directory.
- Do not change any product ID, name, or price inside PRODUCTS.
- Do not modify any code between the API START and API END markers.
- Fix how the frontend uses the simulated API, not the API implementation itself.
- Preserve the checkout form contract exactly:
  - id="checkout-form"
  - action="https://mistvale.example/cart/checkout"
  - method="POST"
  - Required field names: items and coupon
- Before checkout submission, populate items with JSON such as [{"id":101,"qty":2}] using the actual product IDs, and populate coupon with the applied code or an empty string.
- Do not change approved footer legal text.
- Do not invent company facts, product details, review counts, ratings, awards, certifications, customer statistics, or unsupported claims.
- Keep the existing product data and backend contract as the source of truth.
If an instruction conflicts with the existing code, preserve the mandatory contract and document unresolved ambiguities in NOTES.md.
3. VISUAL DIRECTION — PREMIUM, HUMAN-CRAFTED DESIGN
Create a refined, editorial tea-shopping experience inspired by quiet mountain mornings, misty tea gardens, natural materials, traditional craftsmanship, and premium Indian tea packaging.

The website must feel deliberately art-directed, warm, calm, trustworthy, and commercially usable.

Avoid the generic AI-generated landing-page appearance. Do not use a predictable collection of oversized gradient backgrounds, floating glass cards, random decorative blobs, excessive pills, huge empty spaces, excessive centered text, or unnecessary animations.

Instead, use:
- Strong editorial typography and a clear visual hierarchy.
- Thoughtful asymmetry in the hero where appropriate.
- Carefully aligned product photography.
- Consistent spacing, restrained borders, subtle shadows, and intentional negative space.
- Specific, concise copy based only on approved facts.
- A visually consistent design system across every section.
- Clear shopping affordances and a mobile-first layout.
Make deliberate design decisions rather than adding decoration everywhere. The result should look like a real designer refined it through several considered iterations.
Mandatory brand colours
Define CSS custom properties and reuse them throughout:
- Tea green: #1f3d2b
- Leaf: #4f7942
- Cream: #f6f1e7
- Parchment: #ebe2cf
- Saffron: #d9962b
- Ink: #1b1b1b
- Error: #b3261e
Do not introduce unrelated colours. Use tints and shades only when appropriate. Use saffron sparingly, not as a dominant colour.

Verify WCAG AA text contrast, including buttons, muted text, labels, and focus indicators.
Typography
Use exactly two font families, loaded through one Google Fonts link with display=swap.
- Headings: Fraunces or Playfair Display.
- Body: Inter, DM Sans, or Manrope.
Use sentence-case headings and responsive typography with clamp().
- Body text: 16px.
- Small text: 14px, never below 13px.
- H3: 20–24px.
- H2: 28–40px.
- H1: 40–64px using clamp().
Use an 8px-based spacing scale, with 4px allowed for tight gaps. Content maximum width is 1200px, with 16px side padding on phones.

Use one consistent corner radius across the site. Filter chips and badges may be pill-shaped.
4. SUBTLE, PURPOSEFUL ANIMATIONS
Add polished micro-interactions without making the website distracting or gimmicky.

Implement where useful:
- Smooth hover and focus transitions lasting 150–300ms.
- Product cards that lift no more than 4px on hover.
- Subtle image scaling on hover, with no layout shift.
- A refined cart drawer that slides in smoothly.
- A short confirmation toast after adding a product.
- Subtle accordion open/close behavior.
- Button press feedback and clear loading states.
- Small, purposeful opacity transitions for interface feedback.
Use specific transition properties with ease or ease-out; never use transition: all.

Do not add blinking, bouncing, spinning decorations, autoplaying carousels, marquees, or looping animations.

Respect prefers-reduced-motion: reduce. Animations must not interfere with keyboard navigation, cart interaction, or screen readers.

Do not animate every element. Keep the experience elegant and fast.
5. REQUIRED PAGE STRUCTURE
Follow the exact order specified in BRAND.md:
1. Optional announcement strip with one short, factual message.
2. Header with logo, navigation, accessible search, and cart button with item count.
3. Hero with one clear value proposition, one primary CTA labelled "Shop the teas", at most one secondary CTA, and a compelling image.
4. Trust strip with three or four truthful promises.
5. Shop section with search, category filters, sorting, and product grid.
6. Delivery check.
7. The three existing review quotes, unchanged in factual meaning. Do not invent ratings or counts.
8. Accessible FAQ accordion using the six approved questions and answers.
9. Inline newsletter signup, not an automatically appearing popup.
10. Footer with approved contact information, unchanged legal text, and copyright.
Make navigation links work and point to the appropriate sections. The logo should return to the top of the page.

Use a two-column product grid on phones and three or four columns on desktop. Ensure product cards have consistent heights and aligned actions.
6. COMPLETE SHOPPING FUNCTIONALITY
Audit and fix every feature in the existing implementation.
Product discovery
- Search products by the relevant existing product fields.
- Combine search, category filters, and sorting without resetting other selections.
- Keep results synchronized with the current search input.
- Prevent sold-out products from appearing before in-stock products in any sorting mode.
- Make clear-filter and empty-results states usable.
- Ensure search remains correct during rapid typing.
Product cards and quick view
- Display accurate product names, prices, and available stock information from the original data.
- Show real ratings only for products that actually have ratings.
- Provide accessible quick-view interactions if included in the original functionality.
- Prevent duplicate event handlers and broken image states.
- Disable purchase actions for sold-out products.
Cart and quantity rules
- Read prices from PRODUCTS, never from rendered text.
- Maximum quantity per product is five and must never exceed its available stock.
- Reject invalid quantities and prevent sold-out products from being added.
- Correctly handle repeated clicks, removal, empty carts, and quantity changes.
- Ensure cart count, subtotal, discount, shipping, progress indicator, and final total remain synchronized.
- Persist cart state across reloads if the existing implementation supports it, without crashing on empty or malformed browser storage.
- Provide accessible confirmation when a product is added or removed.
Coupon rules
WELCOME10 must:
- Be case-insensitive.
- Require a cart subtotal of at least ₹399.
- Apply a 10% discount to eligible products only.
- Exclude all products whose category is Gifts.
- Cap the total discount at ₹150.
- Never stack discounts when applied repeatedly.
- Be recalculated correctly when quantities or cart contents change.
- Show clear, accurate validation and removal states.
Shipping and totals
- Shipping is ₹49.
- Free shipping applies when the post-discount amount reaches the existing free-shipping threshold.
- Inspect the original code to determine the intended threshold; do not invent a replacement.
- Round only the final total to the nearest rupee.
- Display every monetary value using ₹ and Indian digit grouping, such as ₹1,23,456.
- Ensure the free-shipping progress bar uses the correct amount and updates immediately.
Delivery check
Use the existing API.checkPincode().

Handle serviceable pincodes, unserviceable pincodes, invalid input, API failures, rapid repeated submissions, and delayed responses.

Display the delivery time in days when returned by the API. Show a helpful error when necessary. Never leave the interface stuck on "Checking…".

Do not invent delivery promises beyond the approved FAQ.
Newsletter, countdown, and forms
- Preserve the existing newsletter functionality and validate input.
- Provide clear success and error feedback without falsely claiming a backend subscription succeeded.
- Audit the countdown for correct timing and sensible expiry behavior.
- Avoid fabricated urgency, resetting countdowns on every refresh, or misleading scarcity.
- Inspect every existing form and interactive control.
- Add visible labels, accessible validation messages, loading states, and success feedback.
7. CREATE AND OPTIMISE THE IMAGES
Replace the original placeholder assets with genuine, coherent product imagery.

Required deliverables:
- Eight product images matching the eight existing products.
- One hero banner.
- One clean logo for Mistvale Tea Co.
Product image direction
Use natural window light, soft shadows, premium packaging, realistic tea leaves, restrained compositions, and cream, linen, wood, or stone backgrounds.

All eight product images must share the same 1:1 aspect ratio, framing, lighting direction, visual quality, and premium art direction. Each image must accurately reflect the corresponding product description.

Use realistic, tasteful packaging without inventing unsupported certifications, awards, or brand claims. Do not bake promotional text into product images.

The hero should have a strong visual focal point and leave sufficient negative space for readable HTML text.

The logo should remain recognisable at 32px and feature the word "Mistvale" with a simple leaf, hill, or mist mark. Prefer a clean SVG logo.

Use actual image-generation capabilities if available. Do not pretend to have generated or saved files when you have not.

If image generation is unavailable in the current environment, produce precise, ready-to-use prompts for all ten image assets, with consistent art direction and individual product accuracy. Do not silently substitute unrelated stock images or fabricated image URLs.

Optimise the final assets to WebP or AVIF where supported:
- Each product image under 150 KB.
- Hero image under 250 KB.
- Correct image paths and descriptive alt text.
- No broken references or unnecessary oversized images.
Keep the site functional if an image fails to load.
8. ACCESSIBILITY AND RESPONSIVENESS
Support screen widths from 360px to desktop.

Test:
- No horizontal overflow.
- Readable typography and touch targets.
- At least 44px button height.
- Visible keyboard focus.
- Correct tab order and semantic headings.
- Proper labels, accessible names, and inline errors.
- Accessible cart drawer and quick-view interactions.
- Escape-key handling where appropriate.
- Focus management when opening and closing dialogs or drawers.
- Screen-reader-friendly cart feedback.
- Sufficient colour contrast.
- Meaningful image alt text.
- Reduced-motion preferences.
- No unnecessary keyboard traps.
Use inline SVG icons with consistent stroke widths, not icon fonts or icon libraries.
9. SEO AND STRUCTURED DATA
Implement:
- A unique 50–60 character title.
- A 120–160 character meta description.
- One H1 and logical H2/H3 hierarchy.
- Canonical link using only the approved website URL.
- Open Graph and Twitter card metadata.
- JSON-LD for Organization or OnlineStore.
- Product structured data for each of the eight products.
- Accurate INR prices and availability based on original product stock.
- Aggregate or individual rating properties only where supported by genuine existing ratings.
- FAQPage structured data using the exact six approved FAQ answers.
- Descriptive alt text for meaningful images.
Use only approved company facts and original product data. Do not fabricate review ratings, review counts, stock claims, shipping claims, or other structured data.
10. DOCUMENTATION AND AI WORKFLOW
Create NOTES.md containing:
1. What changed.
2. Bugs fixed and business rules implemented.
3. What AI got wrong, with actual examples discovered during this work.
4. Image-generation tools and actual optimisation performed.
5. Testing performed and any limitations.
6. Questions or ambiguities for the MeroxIO team.
7. Honest estimated time spent.
8. Extra features, if any.
9. What I would improve with more time.
Create PROMPTS.md containing the actual prompts used during this task, in order, with their exact wording, tool, type, outcome, and honest reason for accepting, modifying, or rejecting each output.

Do not fabricate prompts, testing results, tool usage, or completed image-generation work. Preserve the real workflow.
11. FINAL VALIDATION
Before declaring the task complete:
1. Recheck the full index.html for syntax errors, missing functions, and broken references.
2. Verify that the original PRODUCTS IDs, names, and prices remain unchanged.
3. Verify that the API object is untouched.
4. Verify that the checkout contract and approved legal text remain unchanged.
5. Test cart arithmetic, coupon edge cases, stock limits, shipping threshold, sorting, filtering, and delivery API failures.
6. Check all required page sections and responsive breakpoints.
7. Verify image paths, image sizes, metadata, JSON-LD, and accessibility.
8. Remove unnecessary code and avoid duplicate event listeners.
9. Check browser console errors where browser testing is available.
10. Distinguish tests actually performed from tests that could not be performed.
If browser automation or screenshot tools are available, use them for the most important interaction and responsive checks. Otherwise, clearly report the limitation rather than claiming browser tests passed.

Do not spend time on optional bonus features until the mandatory requirements work.
12. REQUIRED FINAL DELIVERABLES
Provide the following:
1. Final index.html with all CSS and JavaScript embedded.
2. Complete images/ directory containing the final assets that were actually created.
3. NOTES.md.
4. PROMPTS.md.
5. One ZIP named yourname-mistvale.zip, under 20 MB, containing the required files.
6. A concise summary of implemented features, tests performed, remaining issues, and any manual steps.
If you can edit files and create archives directly, do so. If you cannot, provide complete replacement file contents or downloadable artifacts rather than vague instructions.

Do not stop after merely describing the plan. Implement the project as far as the available tools allow in this pass. Do not ask me to approve every individual change. Make sensible, documented decisions while preserving every mandatory constraint.

My priority is a premium, human-crafted design, accurate shopping logic, reliable functionality, strict brand compliance, subtle animation, optimised imagery, and an honest, complete submission.

Begin by inspecting all supplied files, then implement, validate, and prepare the deliverables efficiently.
if possible just use my zip file to edit and make
4. Notes for Final Submission
- Keep PROMPTS.md separate from NOTES.md.
- Keep the final index.html and images/ directory in the project ZIP.
- Add the real image source URLs if they are available and required.
- Replace any bracketed placeholders only with facts you can confirm.
- Do not describe internet-sourced images as AI-generated.
- Do not claim the checkout placeholder endpoint is a working live payment backend.
- The final ZIP should follow the assessment's required structure and remain under its size limit.
5. Integrity Statement
This document includes the original Claude master prompt verbatim and organizes the additional workflow described by the user. Sections about part-by-part development, image sourcing/conversion, ChatGPT debugging, and testing are summaries where the exact historical message text was not supplied. They are not presented as verbatim prompts. Additional original prompts can be appended from the corresponding chat histories without changing the chronology above.