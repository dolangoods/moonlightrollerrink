# Moonlight Roller Rink

A one-page site concept for Moonlight Roller Rink, the original music project of Washington, DC songwriter Paul B.

This is an unofficial design concept. The band's official site is [moonlightrollerrink.com](https://moonlightrollerrink.com/), and the page says so in a fixed label and in the footer.

## Files

- `index.html`: the whole page. Markup, styles and script are in this one file.
- `assets/hero-figure.webp`: the hero photo, cut out and re-toned from the band's own image.
- `assets/*.webp` (all the others): release artwork for Meet Me in Tucson, Every Breaking Color, Bobby Pins, Crystal Skulls, The Show Goes On and the All This Madness EP.

## Preview

Open `index.html` in a browser. There is no build step. Fonts (Space Grotesk and DM Mono) load from Google Fonts.

## What is real and what is placeholder

Real, taken from the band's site, Apple Music listing and October show poster:

- Releases from 2022 to 2026, the three video titles, the bio, the streaming and social links, and the contact address.
- The two remaining October 2026 shows.
- The hero photo.
- Release artwork and dates for every release except the 2023 singles and Hold Steady.

Placeholder:

- Cover art for the 2023 singles and Hold Steady, gallery frames and the image strip are generated in the browser.
- The newsletter form shows its states but sends nothing.
- Song rows link to the Spotify artist page, and the video button links to the YouTube channel, not to individual tracks or videos.

## Updating content

- Shows: the `<ol class="gigs">` list in the "Upcoming shows" section of `index.html`.
- Releases: the `albums` array in the script at the bottom of `index.html`. Artwork lives in the `ART` table just above it; give a song a key from that table to show its sleeve.
- Videos: the `vids` array in the same script.
