# Dynamic Gallery

A single-page HTML/CSS photo gallery that shows four images in a four-column layout. Each column lists the same four images in a different order, which creates a varied, mosaic-style grid.

## Files

| File | Description |
|------|-------------|
| `index.html` | The gallery page (HTML and CSS in one file) |
| `image1.JPG` | Two sea-stack rock formations, one with a natural arch, at sunset |
| `image2.JPG` | Silhouette of a runner on a wet beach with a reflection |
| `image3.JPG` | Close-up of the rock arch with waves in front |
| `image4.JPG` | Runner on the beach with the rock arches and a blue sky |

## How It Works

- The page has a centered heading, "dynamic gallery", which is shown as "Dynamic Gallery" because of `text-transform: capitalize`.
- `.con` is a full-height flex container holding four `.box` columns.
- Each `.box` is 25% wide and stacks four full-width images.
- The image order in each column is rotated, so no two columns look the same:

| Column | Image order |
|--------|-------------|
| 1 | 1, 2, 3, 4 |
| 2 | 4, 1, 2, 3 |
| 3 | 2, 1, 3, 4 |
| 4 | 3, 4, 1, 2 |

## Project Structure

```
.
├── index.html
├── image1.JPG
├── image2.JPG
├── image3.JPG
├── image4.JPG
└── README.md
```

Keep all files in the same folder, because the images are referenced by file name only (for example, `src="image1.JPG"`). The file names are uppercase `.JPG`, which matters on case-sensitive servers.

## Getting Started

No installation or build step is needed.

1. Put `index.html` and the four images in the same folder.
2. Open `index.html` in any modern web browser.

## Tech Stack

- HTML5
- CSS3 (flexbox, percentage widths, `text-transform`)

## Known Issues

- **Overflow:** `.con` has a fixed height of `100vh`, but each column holds four images stacked at full column width, so the content is taller than the container and spills past the border.
- **Uneven columns:** the images have different sizes and aspect ratios, so the columns end at different heights.
- **Image quality:** `image3.JPG` is small, so it may look soft when stretched to a quarter of the page width.
- **Accessibility:** every image has an empty `alt` attribute.
- **Not responsive:** four fixed 25% columns will be very narrow on small screens.
- **Global rules:** the `*` selector applies `text-transform: capitalize` to all text, and the `img` rule affects every image on the page.
- The page title is the default "Document".

## Possible Improvements

- Use `object-fit: cover` with a fixed image height so all tiles line up
- Use CSS Grid or multi-column layout for a true masonry look
- Add descriptive `alt` text to each image
- Add hover zoom or a lightbox to view images larger
- Use media queries to reduce the columns to 2 or 1 on small screens
- Set a descriptive `<title>`
