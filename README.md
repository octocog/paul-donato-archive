# The Paul A. Donato Archive

A sourced, growing archive of the running life of **Paul A. Donato** (circa 1915, Italy,
to 2004), winner of the 1937 Mount Washington Road Race and first alternate on the 1940
United States Olympic marathon team. The record is carried to 1970.

Live site: **https://octocog.github.io/paul-donato-archive/**

> ### Before you make this repository private
>
> Do not. Or rather, understand what it costs first.
>
> This repository must stay **public** for the archive to be readable. On a free
> plan a private repository cannot publish GitHub Pages, and switching to private
> does not simply hide the site, it **deletes the Pages configuration entirely**.
>
> Switching the repository back to public afterwards does **not** bring the site
> back. Pages has to be switched on again as a separate step:
> **Settings, then Pages, then source `main` and folder `/ (root)`.**
>
> That two step recovery is why the archive has gone dark twice and stayed dark
> for weeks each time. The repository looked fine and public, while Pages had
> quietly been removed. A daily workflow in `.github/workflows/uptime.yml` now
> checks the live URL and emails on failure.

## Ground rules for this repository

1. **Every factual claim carries a source.** Markers in the text link to the source
   register at the foot of the page. If you cannot cite it, mark it as sought rather
   than stating it.
2. **Gaps stay visible.** Unknowns are tagged rather than filled with plausible guesses.
   The "Still Missing" section is the live want list.
3. **Images link to their origin.** Every plate carries collection, identifier, rights,
   and a link to the holding institution where one exists.
4. **Family held items are labelled as such**, so their evidentiary status is never
   ambiguous.

## Not to be confused with

- **Paul G. Donato** of Lynnfield, his son.
- **Paul J. Donato**, longtime Massachusetts state representative from Medford.

The 2004 Boston Globe obituary of the runner is headlined "Paul G. Donato" while naming
Paul A. Donato in the text. Any index built from the headline inherits that error.

## Structure

```
index.html            the archive itself
assets/archive.css    styles
images/plates/        source images, one per plate
.nojekyll             serve files as-is on GitHub Pages
```

## Adding a plate

1. Drop the image in `images/plates/` with a descriptive name beginning with the year.
2. Add a `<figure class="plate">` inside the relevant event entry in `index.html`.
3. Fill in the `.prov` block: collection, identifier, object description, rights, and a
   link to the source.
4. If the plate supports a new factual claim, add a numbered entry to the source
   register and point the footnote at it.

## Publishing

This is plain HTML and CSS with no build step.

```
git remote add origin git@github.com:USER/paul-donato-archive.git
git push -u origin main
```

Then in the repository settings, under Pages, set the source to the `main` branch,
root folder.

## Corrections

Corrections are as welcome as additions. Name the source register entry the claim rests
on and what the better source says.
