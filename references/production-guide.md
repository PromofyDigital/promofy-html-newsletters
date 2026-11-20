# Promofy HTML production guide

Use these instructions to build or revise Promofy marketing newsletters. Deliver a complete, editable HTML email for Brevo, a reviewable preview, and campaign setup notes. Optimize for the reader’s next action, the approved visual direction, and the experience in the inbox.

## 1. Establish the campaign brief

| Input | What to capture |
| --- | --- |
| Campaign and audience | Campaign name, language, segment, familiarity with Promofy, and why the message matters now |
| Conversion | One primary action, the exact destination, and the conversion to measure |
| Content | Approved product names, offer details, claims, dates, names, titles, and proof points |
| Design | Latest approved HTML, campaign artwork and logos, palette, hero treatment, and mobile requirements |
| Brevo setup | Subject, preview text, tracking convention, existing template variables, and any sender or campaign settings supplied |

Use the current brief and the latest approved campaign materials. Make reversible layout decisions from the closest reference. If an offer, claim, asset, or destination is missing, finish the parts you can and list the exact open item. Mark any HTML with unresolved production URLs or assets as a draft.

For a revision, duplicate the approved source first and check the final diff against the request. A logo swap, color fix, button layout change, or subject update each has its own scope. Carry forward approved wording, images, link mappings, tracking, and template variables unless the request changes them.

## 2. Write around one primary action

- Lead with the audience’s benefit or reason to act. Use one headline, a short supporting paragraph, and a specific button near the top. Use concrete language about what operators can do, with short paragraphs that scan easily on mobile.
- A common sequence is brand header, hero and primary action, product capabilities or proof, closing prompt, and branded footer. Include the sections the campaign needs. Keep dates, offer terms, product names, and buttons as live HTML text.
- Repeat the primary action near the end of a longer email. Add secondary links if they support the same outcome. Named team booking buttons can sit beneath the main event booking CTA. Button labels should set the right expectation for the destination.
- Supply one recommended subject and preview-text pair. Put the benefit, offer, or relevant deadline early in the subject. Use the preview to add a concrete detail in one short sentence. Match the hidden HTML preheader to the Brevo preview-text field and check the resulting inbox snippet. Supply an A/B alternative when requested or when the campaign brief calls for one.
- Set the level of explanation by audience. Returning clickers can go directly to the offer. A new audience may need a sentence explaining the product. Verify offer eligibility, dates, integrations, proof, and results claims against the approved brief.

### Patterns from previous Promofy newsletters

| Campaign | Pattern to reuse | Primary action |
| --- | --- | --- |
| AI Suite announcement | Show the promotion workflow and describe each approved add-on in one line. The previous campaign covered Flow AI, Target AI, Localize AI, Canvas AI, and Insight AI. | Book a demo |
| Spark trial | Lead with the approved trial offer and tie it to the acquisition problem. Explain what happens when the reader clicks. | Use the approved trial request or booking flow |
| Seasonal gamification | Use seasonal creative to show what operators can build. Align the newsletter promise with the landing page and eventual demo flow. | Explore the campaign landing page |
| SBC event | Put the confirmed date, location, and stand near the top. Use the team image as support and map each named button to its own approved calendar. | Book an event meeting |
| Anniversary or roundup | Lead with the milestone or strongest story, then group verified updates into scannable sections. | Use the campaign’s approved destination |

Treat past details as examples. Verify current offers, attendee lists, product wording, and destinations for every new campaign.

## 3. Design the email

- Start from the closest approved Promofy HTML. Use a centered shell around 600px wide as a working default and retain the approved shell width in revisions. Use consistent vertical spacing, restrained cards, one visual focal point, and a clear primary button. Provide solid color and square-corner fallbacks when gradients, radii, or shadows drop out.
- Use the campaign palette. AI Suite examples use a dark violet base, soft lavender text, and pink or violet accents. SBC uses a pale lavender canvas, white and lilac sections, and a deep purple hero and footer. Spark’s Halloween artwork uses seasonal accents. Use approved artwork and logos for the campaign at hand.
- For the AI Suite hero pattern, blend the approved 16:9 artwork into the background. Reserve quiet space on the left for the live headline, supporting text, and button. Put the mascot on the right on desktop, then reframe it or move it below the copy on mobile. Where a second visual should blend into the email, align its edge colors with the adjacent sections. Give the hero a solid fallback color that keeps the content readable.
- Start with 15–16px body text and comfortable line spacing. The reference layouts use approximately 48–52px buttons. Aim for 4.5:1 contrast for normal text and check the actual colors, especially accent buttons and footer links. For example, dark ink #201135 on bright pink #FF3366 gives approximately 5:1 contrast.
- Check 320px and 390px layouts for content order, padding, overflow, and readable button labels. For SBC’s desktop-row variant, keep equal-width booking buttons on desktop and stack them full width with about 12px gaps around the template’s 620px breakpoint. For the approved stacked variant, use separate button rows at every width.

## 4. Build the production HTML

1. Deliver a full document with doctype, correct language, UTF-8, viewport metadata, a title, and the hidden preheader near the top of the body. Use presentation tables, explicit widths and alignment where needed, inline critical CSS, and a small head style block for responsive behavior. Use the source’s Outlook conditional wrappers where relevant.
2. Use live text and real anchors for buttons. Where the approved design uses an Outlook VML fallback, keep both button labels, destinations, and tracking identical. Supply a solid background with HTML background color and inline CSS for key sections. For a background-image hero, use the existing Outlook fallback or add one if needed. Keep the baseline readable and actionable if background images or media queries are dropped.
3. Use a common font fallback stack. Give informative images meaningful alt text and decorative images empty alt text. Use explicit image widths with fluid scaling and automatic height. Verify hosted images load over public HTTPS without signing in, resize and compress them for the display area, and check the mobile crop. Keep scripts, forms, iframes, and critical flexbox or grid layouts out of production email.
4. Preserve the campaign’s palette across device settings, including visually dark campaigns. Carry over the approved template’s color-scheme declarations, inline backgrounds, solid fallbacks, and text colors. Reuse client-specific overrides where they help the target clients and fit the approved design. Check actual contrast in both inbox modes, since some clients apply their own color changes.
5. Preserve Brevo variables literally in anchor destinations. Use `{{ mirror }}` for View in browser where the template calls for it, `{{ update_profile }}` for preferences, and `{{ unsubscribe }}` for the visible unsubscribe link. Keep the approved privacy link and sender details. Check for duplicated boilerplate if the campaign also uses Brevo’s default footer or header. [Brevo template variables](https://help.brevo.com/hc/en-us/articles/4402386448530--Manual-Personalize-your-messages-with-dynamic-content-Brevo-Template-Language)
6. Keep approved URLs and existing query parameters. Use the project’s tracking convention. Previous campaigns used `utm_source=brevo` and `utm_medium=email`. Confirm the correct `utm_campaign` and any `utm_content` values. Escape query-string ampersands as `&amp;` in HTML, keep UTMs off native Brevo merge links, and confirm each event booking link goes to the correct person.
7. Keep the source readable and lean. Preserve conditional comments, required selectors, and inline styles during cleanup. Use public HTTPS images in production and reserve local paths or embedded images for the review copy. Use a working size budget of about 90 KB for the production HTML and check for clipping after Brevo adds its markup and tracking when inbox tests are available.

## 5. Verify before handoff

| Check | Pass condition |
| --- | --- |
| Campaign review | Approved facts, names, artwork, subject, preheader, CTA labels, and destinations agree. The revision diff matches the request. |
| HTML review | Tables and conditional blocks are balanced. Merge tags remain literal. Production images are hosted. Standard and Outlook CTA URLs match. Resolve or flag placeholders, stale campaign names, and duplicated tracking. |
| Browser preview | Review desktop and 320px and 390px mobile layouts for overflow, image crop, reading order, button size, spacing, and footer legibility. Generate desktop and mobile screenshots when rendering is available. |
| Images-off review | The reader can identify the sender, understand the message, and take the primary action with images hidden. |
| Brevo import | Paste the complete source into **HTML custom code**. Keep the head styles and conditional markup. Enter the subject and preview text in Brevo, then review the generated plain-text version for meaningful content and links. [Custom HTML import](https://help.brevo.com/hc/en-us/articles/4672127581074-Upload-an-HTML-file-to-design-your-emails-HTML-custom-code-editor) · [Plain-text version](https://help.brevo.com/hc/en-us/articles/360000486460-How-do-I-create-edit-the-plain-text-version-of-HTML-emails) |
| Inbox verification | When authorized and available, test from Brevo in Gmail, Apple Mail/iOS, Outlook web, and classic Outlook where relevant. Review light and dark rendering, tracking, image loading, preheader, clipping, and resolved footer links. Verify unsubscribe with a test contact. Report which clients and modes were actually checked. [Brevo preview and test](https://help.brevo.com/hc/en-us/articles/4741964626066-Preview-and-test-your-email) |

Report browser and inbox checks separately. If Brevo access or test recipients are unavailable, deliver the files and indicate which checks remain pending. Sending or scheduling a live campaign requires explicit authorization.

## 6. Deliver the files

- **campaign-brevo.html** — Editable Brevo HTML. Label it a draft if it still needs a production image, URL, or approved fact.
- **campaign-preview.html** — A browser preview with the same layout and copy. Include local preview assets or embed them so the user can open the file.
- **campaign-setup.md** — Recommended subject and preview text, audience and primary action, exact CTA destinations, any image upload and replacement steps, supplied campaign settings, and checks completed or pending.
- **Assets and screenshots** — Include new optimized graphics and the desktop/mobile views when available. Use a ZIP when it makes a multi-file preview easier to share.

In the handoff message, link the HTML, preview, and setup notes. Include the recommended subject and preview text and state whether the files are ready for import or still need a named input.

## Campaign examples

Find the campaign HTML, previews, and setup notes in the [template library](template-library.md).
