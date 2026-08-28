# Havenstone Management — website

Demo site for the Havenstone Management workspace. Four pages plus a shared
stylesheet:

- `index.html` — home: portfolio of all six communities, services, owner CTA
- `vacancies.html` — available homes
- `faq.html` — resident FAQ
- `owners.html` — management services, fees, month-end close schedule
- `assets/site.css` — the whole design system; the pages carry no inline styles

## Deliberately out of date, so Dash has real work to do

- the application fee reads **$45** and should be **$50**. It appears **four
  times across three files**: once in the services list on `index.html`, once
  in the notice on `vacancies.html`, and **twice** on `faq.html` (the cost
  question and the co-signer question).
- the **Camelback Terrace 2 bed** is still listed although it has leased, and
  the nav count on every page still says **Vacancies (4)**.

`owners.html` deliberately contains **no** `$45`, so the count above stays at
four. Keep it that way when editing — the demo script states the number aloud.

## Design notes

- Type is Fraunces (display) over Archivo (body), loaded from Google Fonts.
- The property artwork is inline SVG generated per building, not photography —
  six distinct massings so no two cards repeat. The sprite is duplicated into
  `index.html` and `vacancies.html` because an external `<use href>` is blocked
  by CORS when the pages are opened over `file://`.
- The site commits to a single light appearance (`color-scheme: light`) on
  purpose: it is shown on a live stream, and a dark-mode variant would render
  differently on the presenter's machine than on the one it was checked on.
- Checked for horizontal overflow at 500, 760, 1024 and 1440px.
