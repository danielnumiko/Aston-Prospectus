# Aston University Digital Prospectus

Working prototype of a personalised digital prospectus for Aston University, replacing
the printed undergraduate prospectus. Built in Claude Design and exported from there.

## What's here

```
design/
  Aston Prospectus Preview.dc.html      Device-preview harness — open this one
  Aston Digital Prospectus v2.dc.html   The prototype
  AstonLogo.dc.html                     Shared logo component
  support.js                            Claude Design runtime
  public/assets/                        Images and icons
```

## Running it

The `.dc.html` files need a static server — `support.js` fetches sibling files, so
`file://` will not work. It also pulls React 18 and Babel from unpkg at runtime, so
you need to be online.

```
cd design && python3 -m http.server 8000
```

Then open <http://localhost:8000/Aston%20Prospectus%20Preview.dc.html>.

The preview gives you a mobile / tablet / desktop frame switcher, jumps to the Start,
Form and Prospectus screens, and a Reset that clears the saved profile. Mobile is the
primary design — most readers arrive by scanning a QR code.

## Notes

- This is a design artefact, not production code. Section intros, tour copy and hero
  framing are hard-coded; courses, events and stories are simulated with real content.
- Images came straight out of Figma and are not optimised. Several PNGs are over 5 MB
  and one is 18 MB. Compress them before this goes anywhere near production.
