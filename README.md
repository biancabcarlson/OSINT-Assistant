# OSINT Assistant

**🔗 Tool:** https://biancabcarlson.github.io/OSINT-Tool/

Given a subject's public identifiers — name, email, phone, town/county, age, a known associate — generates a ready-to-click list of investigator-relevant lookups, grouped by type:

- **Social media** — LinkedIn, X/Twitter, Facebook mutual-connection search
- **General** — email/phone reputation lookups
- **Public record** — obituary, police record

Also generates a Markdown checklist for tracking what's been reviewed. Works for any case typology, not just account takeover. A name alone is rarely enough to confirm identity — a town, age, or known associate narrows the record/relationship checks well beyond a generic name search.

It only builds query strings — it never queries, scrapes, or authenticates against any site.

## Web demo

`index.html` generates the clickable links instantly, entirely client-side, pre-filled with the `simulated-account` fixture (Jane Doe) as a working example.

## Python CLI

```
python osint_tool.py --name "Jane Doe" --email "jane.doe@example.com" \
    --phone "(415) 555-0148" --town "San Francisco, CA" --age 39 \
    --associate "Marcus" -o queries.md
```

## Privacy Mode

The 🔒 Privacy Mode toggle (top right, shared across the suite via `localStorage`) blurs the subject's email, phone, and known-associate name in the dossier header.

## Other tools in this series

- [Case Calculator](https://biancabcarlson.github.io/Case-Calculator/)
- [Report Template Filler](https://biancabcarlson.github.io/Report-Template-Filler/)
- [OSINT Assistant](https://biancabcarlson.github.io/OSINT-Tool/) *(this repo)*
- [Case Doc Tracker](https://biancabcarlson.github.io/Case-Doc-Tracker/)
- [Entity Name Matcher](https://biancabcarlson.github.io/Entity-Name-Matcher/)
- [Case Timeline Builder](https://biancabcarlson.github.io/Case-Timeline-Builder/)
