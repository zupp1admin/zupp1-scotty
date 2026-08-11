# Zupp1 Card Alignment Standard

CTA buttons inside cards should align consistently without page authors inserting spacer elements or empty paragraphs.

## Shared CSS pattern

```css
.zupp-card-content{
    display:flex;
    flex-direction:column;
    height:100%;
}

.zupp-card-content .zupp-actions{
    margin-top:auto;
}

.zupp-grid > .zupp-card{
    height:100%;
}
```

## Design-system rule

Prefer global component fixes over page-specific patches when the same layout defect can recur across multiple pages.

The objective is for authors to focus on content rather than manually correcting layout.

## Acceptance criteria

- Buttons in the same card row align horizontally despite unequal text lengths.
- Cards stretch naturally within their grid row.
- Desktop, tablet, and mobile behavior remain stable.
- No page-specific spacer markup is required.
- Shared CSS remains the source of truth.