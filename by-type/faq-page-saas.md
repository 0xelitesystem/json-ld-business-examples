# FAQPage: SaaS product FAQ

For a Frequently Asked Questions page on a SaaS product.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "url": "https://signalforge.example.com/faq",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Do I need to create an account to use SignalForge?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. SignalForge runs entirely in your browser. Open the page, fill in your invoice details, download the PDF. No signup, no email collection, no recurring fee. Your invoice data never leaves your device."
      }
    },
    {
      "@type": "Question",
      "name": "How does the one-time Pro payment work?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The Pro upgrade is a single $29 payment via Stripe. You receive an unlock key by email. Paste the key into SignalForge and the watermark goes away on the same device. The key works on all browsers on that device. To use on additional devices, contact support and we will send another key at no charge."
      }
    },
    {
      "@type": "Question",
      "name": "Can I use SignalForge for commercial invoicing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. SignalForge has no restrictions on commercial use, even on the free tier. The only differences in Pro are the removed PDF watermark and access to all 24 templates. The free tier with 3 templates produces fully valid invoices acceptable in all jurisdictions we have tested."
      }
    },
    {
      "@type": "Question",
      "name": "What currencies and tax formats does SignalForge support?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "SignalForge supports USD, EUR, GBP, JPY, AUD, CAD, CHF, and SGD. Tax fields accept any single-line tax label (VAT, GST, Sales Tax, IVA) with a percentage. Multi-tax invoices (combined federal and state tax) are supported in the Pro version only."
      }
    },
    {
      "@type": "Question",
      "name": "Can I customize the invoice with my logo and brand colors?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Upload a PNG or JPG logo (max 2MB) and pick a primary brand color. The logo and color apply to all 24 templates. You can save your branding to your browser so it loads automatically next time you visit (uses local storage; no server upload)."
      }
    }
  ]
}
</script>
```

## Notes

- Every `Question.name` must match a visible H3 on the page. AI engines verify the rendering matches the schema.
- `acceptedAnswer.text` should be 30 to 100 words, fact-rich, self-contained. Short answers ("Yes") waste the schema.
- Do NOT invent questions. Use real questions you receive from customers (support tickets, sales calls).
- Avoid hype answers. The answer should be the answer, not a sales pitch.
- Only ONE `FAQPage` per URL; never put FAQ schema on a product page that also has Product schema (use Q&A inside the Product schema instead).
