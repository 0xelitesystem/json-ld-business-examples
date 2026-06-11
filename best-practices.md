# Schema best practices

The non-obvious rules that separate schema that works from schema that validates but doesn't.

## Use the most specific subtype

`Restaurant` beats `LocalBusiness`. `BlogPosting` beats `Article`. `Dentist` beats `LocalBusiness`. The more specific, the more schema-specific fields you unlock and the better AI engines categorize you.

If your specific type isn't documented, look it up at schema.org/[YourGuess]. Many subtypes exist: `LegalService`, `MedicalBusiness`, `FinancialService`, `HomeAndConstructionBusiness`, etc.

## Match what's rendered

Schema must reflect what's on the page. If schema says price is $99 and the page shows $149, AI engines flag the mismatch and discount the whole entity. If schema says author is "Jane Cole" and the visible byline says "Cole, J", that's a mismatch.

## Person objects, not author strings

`"author": "Jane Cole"` is technically valid. `"author": {"@type": "Person", "name": "Jane Cole", "url": "..."}` is what actually helps. AI engines pin reputation to URLs, not strings.

## sameAs is the single most important Person field

It's the bridge between your local name and the public web. LinkedIn, GitHub, Twitter, Crunchbase, Wikipedia, Mastodon. Three is good, five is better, none is invisible.

## datePublished and dateModified, both, always

Without `datePublished`, AI engines can't gauge recency. Without `dateModified`, they assume the page is frozen at publish date. Both, in ISO 8601, with timezone.

`dateModified` should reflect real edits, not typo fixes. Faking freshness gets caught.

## Logo: square, 112px minimum, on your domain

Google's hard requirement. Many sites use a horizontal logo or a 32x32 favicon. Both fail.

## Don't over-schema

One Article schema, one Organization schema, one Person schema for the author, one BreadcrumbList. That's a complete blog post.

You don't need Article + WebPage + WebSite + BlogPosting + CreativeWork all stacked. Pick the most specific applicable type.

## Validate every block

Google Rich Results Test catches the common errors. Schema.org validator catches the spec compliance issues Google ignores. Run both.

Block deployment if validation fails.

## Don't fake ratings

`aggregateRating: 5` with `ratingCount: 1` on a brand-new product is the textbook fake-rating signal. AI engines pattern-match these and discount the whole site, not just the page.

Add aggregateRating after you have at least 20 real reviews. Until then, omit it.

## Match the canonical

`mainEntityOfPage.@id` should match the canonical URL exactly. Trailing slashes matter. WWW vs non-WWW matters. http vs https matters.

## Update when the page updates

Schema isn't a one-time setup. Pricing changes, address changes, opening hours seasonal changes, dateModified on edits. Build it into your CMS workflow.

## Keep it close to the content

The JSON-LD block can live in `<head>` or just before `</body>`. Both work. Just before `</body>` reduces head clutter; `<head>` is convention. Pick one and be consistent.

## One application/ld+json per "thing"

A page can have multiple JSON-LD blocks. Article + Person + Organization is common. Each in its own `<script>` tag is cleanest; combining into a single graph (`@graph` array) also works.

## Don't omit the `@context`

Every block needs `"@context": "https://schema.org"` at the top. Without it, the block is invalid even if everything else is perfect.
