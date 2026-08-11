# Zupp1 Standard — Safe Hero Video HTML

Use the approved shared hero classes and keep the video and overlay as siblings.

## Required structure

```html
<section class="zupp-video-hero">
  <video class="zupp-video-hero__media" preload="metadata" autoplay loop muted playsinline><source src="VIDEO-URL.mp4" type="video/mp4"></video>
  <div class="zupp-video-hero__overlay">
    <div class="zupp-container">
      <span class="zupp-eyebrow">SECTION LABEL</span>
      <h1 class="zupp-display">Hero heading</h1>
      <p class="zupp-lead">Hero supporting text.</p>
      <div class="zupp-actions">
        <a class="zupp-btn zupp-btn-primary" href="#target">Primary action</a>
        <a class="zupp-btn zupp-btn-light" href="/destination/">Secondary action</a>
      </div>
    </div>
  </div>
</section>
```

## Critical rule

The closing `</video>` must appear immediately after the `<source>` element.

Nothing may appear between `<source>` and `</video>`.

Do not insert `&nbsp;`, paragraphs, `<br>`, comments, fallback text, invisible characters, overlay elements, or extra containers inside the video element.

Required DOM relationship:

```text
section.zupp-video-hero
├── video.zupp-video-hero__media
└── div.zupp-video-hero__overlay
```

## WordPress procedure

1. Edit with the Classic Editor in Code mode.
2. Paste the complete hero HTML.
3. Avoid repeated switching between Visual and Code modes.
4. Search the video block for `&nbsp;`, `<p>`, and `<br>` before updating.
5. Confirm `.zupp-video-hero__overlay` begins after `</video>`.
6. Update and verify the public page in a fresh tab.

## CSS contract

Do not recreate page-specific hero CSS when the shared Zupp1 stylesheet already provides sizing, cropping, overlay positioning, typography, buttons, and responsive behavior.

## Acceptance checklist

- Video loads and plays.
- Video is muted.
- Video plays inline on mobile.
- Eyebrow, H1, lead, and buttons are visible.
- Overlay is a sibling of video.
- No `&nbsp;` exists inside video.
- Desktop and mobile layouts render naturally.
- No unrelated content or CSS changed.