# GitHub profile maintenance

Updated: 2026-10-28.

## Current design

The profile uses a 3840×1085 panoramic header with short native Markdown sections. The latest user-uploaded television scene is on the left; the existing personal character screen is on the right. Both complete sources are scaled proportionally to the same height and joined flush at the top and bottom, with restrained sharpening and WebP encoding. The combined ratio is about 3.54:1, reducing header height by about 44% at the same display width. No source scene or portrait is cropped.

The character screen was previously edited from the user's supplied references: the first screen was the edit target, the third photograph the identity reference, and the second screen a detail reference. The composite retains the original interface composition, costume and backdrop. The original modern photograph is not stored in the repository.

The header is a generative face composite, not a claim of pixel-identical restoration. The vertical red nameplate is corrected to 董信步 at the user's request. Other character-screen lettering belongs to the supplied reference. No design titles, element labels, legends, or explanatory annotations are added to the displayed profile. The introductory slogan was removed at the user's request; the introduction now contains education only.

assets/pal3-profile-panorama-v4.webp is the current optimized header; the versioned path avoids stale image caches. The white CC watermark and adjacent clipped white mark in the upper-right corner of the left panel were removed through local crop inpainting. The 3840×1085 source PNG was verified pixel-identical outside that repair region before WebP encoding. assets/pal3-sword.png and assets/pal3-pearl.png are transparent decorative icons. All four section headings use H2 with a leading 24px sword; all six repository headings use H3 with a leading 20px pearl. Project technology rows follow descriptions consistently. Native GitHub heading typography is used throughout. The portrait and icons were produced with the built-in image generation tool; final panoramic assembly uses the original sources to preserve exact panel proportions. All displayed assets live in this repository, without third-party image hosts or scripts.

Names, education, project descriptions, paper details and links remain native text. Portfolio order: ccagent, Classroom Annotator, the live-auction collaboration, research, resume templates, awards. ccagent is described as a workbench with user-confirmed memory and reusable experience; no unverified company performance or autonomous external operations are claimed.

## Validation

Check local image references and transparent alpha, render with GitHub's Markdown API, inspect desktop/mobile widths and light/dark colors, then verify published files. This static profile update does not require an application test framework.

## Previous version and rollback

Previous profile commit: 8bc8736111d7440fc3ab27a2a696714d788c6fce.

Existing Shan-Hai SVG assets are preserved. To restore, restore README.md from the previous commit and publish a new commit without rewriting history. An earlier version is also preserved at backup/profile-before-guofeng-2026-10-16.
