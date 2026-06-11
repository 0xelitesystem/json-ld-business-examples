# Common schema mistakes

Things people get wrong, what they look like, and how to fix them.

## 1. Author as a string

```json
"author": "Jane Cole"
```

Validates. Useless. Replace with:

```json
"author": {
  "@type": "Person",
  "name": "Jane Cole",
  "url": "https://example.com/authors/jane-cole",
  "sameAs": ["https://www.linkedin.com/in/janecole"]
}
```

## 2. Fake aggregateRating

```json
"aggregateRating": {
  "@type": "AggregateRating",
  "ratingValue": "5",
  "ratingCount": "1"
}
```

This is the classic fake-rating signature. AI engines and Google both spot this. Either get real reviews or omit the field.

## 3. Schema-content mismatch

Schema says:
```json
"offers": {"price": "99", "priceCurrency": "USD"}
```

Page shows: "$149/month"

Pick one. They have to match. AI engines verify rendering.

## 4. Logo that isn't square

```json
"logo": {
  "@type": "ImageObject",
  "url": "https://example.com/logo-horizontal-300x80.png"
}
```

Google requires square or near-square logos at minimum 112x112. Rebuild a square version for schema even if your visible logo is horizontal.

## 5. Missing datePublished

Article schema without `datePublished` is rejected for AMP/news eligibility and discounted by AI engines.

## 6. dateModified earlier than datePublished

```json
"datePublished": "2026-04-15",
"dateModified": "2026-03-20"
```

Validates as a warning. Doesn't make sense. Often caused by CMS auto-fill bugs.

## 7. URL fields without https://

```json
"url": "example.com/page"
"image": "/images/cover.jpg"
```

Both broken. URLs must be absolute and start with `https://`.

## 8. Wrong @type for the content

Recipe content with `Article` schema. Product page with `BlogPosting` schema. Job posting with `Article`. Pick the type that matches the content.

## 9. Multiple competing types on one page

```json
[
  {"@type": "Article", ...},
  {"@type": "Product", ...},
  {"@type": "FAQPage", ...}
]
```

On one page. Google picks one and ignores the rest, often the wrong one. Pick the primary entity for the page and use only that.

Exception: BreadcrumbList plus the primary type is fine. Organization on every page is fine. Multiple primary entities on one page is the issue.

## 10. FAQPage on a product page

Don't. Use Q&A inside the Product schema, or move the FAQ to its own page with FAQPage schema. Don't combine on one page.

## 11. Outdated openingHours

```json
"openingHours": "Mo-Fr 09:00-17:00"
```

Page says "Open until 9pm Mon-Thu". Mismatch. Use `openingHoursSpecification` and update seasonally.

## 12. Self-referential canonical mismatch

```json
"mainEntityOfPage": {
  "@type": "WebPage",
  "@id": "https://example.com/post/"
}
```

But `<link rel="canonical" href="https://example.com/post">` (no trailing slash). Pick one and align everything.

## 13. Person schema with no sameAs

```json
{
  "@type": "Person",
  "name": "Jane Cole"
}
```

Validates. Useless. Without sameAs, AI engines can't disambiguate this Jane Cole from any other.

## 14. Schema in `<noscript>`

Some old guides suggested wrapping JSON-LD in `<noscript>`. Don't. It's an HTML rendering issue and Google sometimes ignores it.

## 15. JSON syntax errors

A trailing comma, smart quotes, or unescaped quote inside a string breaks the whole block silently. Validate.

The fastest catch is to copy the block, paste into [jsonlint.com](https://jsonlint.com/) first, then into the Schema validator.

## 16. PaywallContent without cssSelector

If you have a paywall, mark it explicitly:

```json
"isAccessibleForFree": false,
"hasPart": {
  "@type": "WebPageElement",
  "isAccessibleForFree": false,
  "cssSelector": ".paywall-content"
}
```

Without this, Google flags your page for cloaking when AI engines fetch and see different content than human visitors.

## 17. Missing publisher on Article

Article schema must have a publisher Organization with a logo. Without it, Article validates but loses news-eligibility.

## 18. Wrong availability values

```json
"availability": "in stock"
```

Wrong. Must be the schema.org URL form:

```json
"availability": "https://schema.org/InStock"
```

Valid values: `InStock`, `OutOfStock`, `PreOrder`, `LimitedAvailability`, `Discontinued`, `BackOrder`, `SoldOut`.

## 19. Empty arrays

```json
"sameAs": []
```

If you have nothing, omit the field. Empty arrays are valid but signal a half-implemented schema.

## 20. Schema added but page is gated/JS-rendered

Schema is in the source but the page content is rendered after JavaScript. AI bots that don't run JS see the schema referencing content they can't read. Pre-render or use SSR.
