# VideoObject: Video tutorial

For an embedded video tutorial or how-to with transcript.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "How to set up the OpenAI API key for BYOK SaaS tools",
  "description": "Five-minute walkthrough showing how to create an OpenAI account, generate an API key, set spending limits, and paste the key into a BYOK SaaS tool safely.",
  "thumbnailUrl": [
    "https://example.com/videos/openai-key-setup/thumb-16x9.jpg",
    "https://example.com/videos/openai-key-setup/thumb-1x1.jpg"
  ],
  "uploadDate": "2026-02-18T10:00:00-08:00",
  "duration": "PT5M14S",
  "contentUrl": "https://example.com/videos/openai-key-setup.mp4",
  "embedUrl": "https://www.youtube.com/embed/dQw4w9WgXcQ",
  "publisher": {
    "@type": "Organization",
    "name": "Cole Research",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo-square-512.png"
    }
  },
  "creator": {
    "@type": "Person",
    "name": "Jane Cole",
    "url": "https://example.com/team/jane-cole"
  },
  "transcript": "Hi, I am Jane Cole. In this five-minute video we will set up an OpenAI API key for use in BYOK SaaS tools. First, go to platform.openai.com and sign in or create an account. Once logged in, click your profile in the top right and pick 'View API keys' from the menu. Click 'Create new secret key', give it a name like 'BYOK-SaaS' so you remember what it is for, and copy the key to your clipboard. Important: this key gives anyone full access to your OpenAI account. Treat it like a password. Next, before you use the key anywhere, set a spending limit. Go to Settings, Billing, Usage limits. Set a hard limit and a soft limit. For BYOK use I recommend $20 hard and $10 soft to start. You can raise it later. Now you have a key and a safety net. Open your BYOK SaaS tool, find the API key field in settings, paste it in. Most BYOK tools store the key in browser memory only and never send it to a server. Check the tool's docs to confirm. That is it. Five steps: account, key, hard limit, soft limit, paste. Thanks for watching.",
  "interactionStatistic": {
    "@type": "InteractionCounter",
    "interactionType": {"@type": "WatchAction"},
    "userInteractionCount": 14820
  }
}
</script>
```

## Notes

- `duration` MUST be ISO 8601 format (PT5M14S = 5 minutes 14 seconds, PT1H22M = 1 hour 22 minutes).
- `thumbnailUrl` array covering 16:9 and 1:1 helps Google Discover and YouTube preview.
- `transcript` is the most underused field; AI engines parse it as searchable text, which means your video becomes findable by every word said in it.
- `interactionStatistic` for view counts only when you have a reliable number.
- `embedUrl` for the embeddable player URL (YouTube embed URL or your own); `contentUrl` for the raw video file URL.
