# Moonlight Roller Rink

A one-page site concept for Moonlight Roller Rink, the original music project of Washington, DC songwriter Paul B.

This is an unofficial design concept. The band's official site is [moonlightrollerrink.com](https://moonlightrollerrink.com/), and the page says so in a fixed strip along the bottom edge and in the footer.

## Files

- `index.html`: the whole page. Markup, styles and script are in this one file.
- `assets/hero-figure.webp`: the hero photo, cut out and re-toned from the band's own image.
- `assets/*.webp` (all the others): artwork for every release, from Spin (2012) to Meet Me in Tucson (2026).

## Preview

Open `index.html` in a browser. There is no build step. Fonts (Space Grotesk and DM Mono) load from Google Fonts.

## What is real and what is placeholder

Real, taken from the band's site, Apple Music listing and October show poster:

- Releases from 2012 to 2026, the three video titles, the bio, the streaming and social links, and the contact address.
- The two remaining October 2026 shows.
- The hero photo.
- Release artwork and dates for every release.
- Gallery photos in `assets/gallery/`, taken from the band's Instagram posts.

Placeholder or approximate:

- The newsletter form shows its states but sends nothing.
- Every song row has two links. The Apple Music link goes to that song's own page. The Spotify link opens a Spotify search for that song until its track id is added to the `albums` array.
- Video cards open a search for that title inside the band's YouTube channel, not the video itself. "Knights & Queens" has no sleeve, so its card shows a plain gradient.
- Show rows open a Google Maps search for the venue name.
- The hero backdrop (moon, light, sound waves) is drawn in code.

## Updating content

- Shows: the `<ol class="gigs">` list in the "Upcoming shows" section of `index.html`. Each row needs a `<time datetime="YYYY-MM-DD">`: the page hides a show once its date has passed, and the hero's top-left slot shows the next upcoming one (or the latest single when there are none).
- Releases: the `albums` array in the script at the bottom of `index.html`. Each song is `[title, label, artwork key, Apple Music path, Spotify track id]`. The track id is the last part of a song's Spotify share link (`open.spotify.com/track/<id>`); leave it out and the Spotify link searches for the song instead. Artwork lives in the `ART` table just above it.
- Videos: the `vids` array in the same script. Give a video an `art` key from the `ART` table to show that sleeve.
- Hero lights: the `slides` array. Keep the frames inside the site palette, since the hero photo is toned to match it.

## Type

Space Grotesk has a single axis, weight 300 to 700, and no width axis. The hierarchy uses three weights on purpose: 700 caps for display, 500 or 600 in sentence case for sub-heads and titles, 300 for numerals. DM Mono carries the labels.

## Motion and accessibility

- "Pause motion" in the hero stops everything that moves by itself. With the system's reduced-motion setting on, nothing animates and the button is hidden.
- The year list in Music is a tab list (arrow keys move between years). The mobile menu takes focus, locks the page behind it, and closes with Escape.
