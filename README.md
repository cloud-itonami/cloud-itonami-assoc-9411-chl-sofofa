# cloud-itonami-assoc-9411-chl-sofofa

Industry rule/history catalog for **SOFOFA** (Sociedad de Fomento
Fabril) — the TWENTY-FIRST entry aligned to **ISIC 9411** (activities
of business, employers, and professional membership organizations),
alongside
[`-9411-sau-fsc`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-sau-fsc)
(Saudi Arabia),
[`-9411-aut-wko`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-aut-wko)
(Austria),
[`-9411-irl-ibec`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-irl-ibec)
(Ireland),
[`-9411-nzl-businessnz`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-nzl-businessnz)
(New Zealand),
[`-9411-cze-spcr`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-cze-spcr)
(Czech Republic),
[`-9411-ind-cii`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-ind-cii)
(India),
[`-9411-zaf-busa`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-zaf-busa)
(South Africa),
[`-9411-bra-cni`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-bra-cni)
(Brazil),
[`-9411-ken-kam`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-ken-kam)
(Kenya),
[`-9411-can-chamber`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-can-chamber)
(Canada),
[`-9411-mex-coparmex`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-mex-coparmex)
(Mexico),
[`-9411-ita-confindustria`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-ita-confindustria)
(Italy),
[`-9411-nld-vnoncw`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-nld-vnoncw)
(Netherlands),
[`-9411-kor-kcci`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-kor-kcci)
(South Korea),
[`-9411-arg-uia`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-arg-uia)
(Argentina),
[`-9411-bel-feb`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-bel-feb)
(Belgium),
[`-9411-dnk-di`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-dnk-di)
(Denmark),
[`-9411-swe-sn`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-swe-sn)
(Sweden),
[`-9411-fin-ek`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-fin-ek)
(Finland), and
[`-9411-tha-fti`](https://github.com/cloud-itonami/cloud-itonami-assoc-9411-tha-fti)
(Thailand). Part of the
[`cloud-itonami`](https://github.com/cloud-itonami) compliance-fact
family (ADR-2607141700, `cloud-itonami-compliance-fact-federation`,
in `com-junkawasaki/root`).

## Sourcing note

This repo fills Chile's previously-open association-axis gap (one of
the 7-country gap list recorded at tick 155). Chile now has real,
individually verified facts across all three axes: country
([`cloud-itonami-iso3166-chl`](https://github.com/cloud-itonami/cloud-itonami-iso3166-chl)),
municipality
([`cloud-itonami-municipality-chl-santiago`](https://github.com/cloud-itonami/cloud-itonami-municipality-chl-santiago)),
and association (this repo).

The 30 entries cite documents SOFOFA serves from `www.sofofa.cl`,
declared per entry by `:url-provenance`:

- **SOFOFA itself** (`:official-sofofa-cl`) — the 2024 statute
  (`Estatutos-SOFOFA.pdf`: name and legal basis, object, member
  categories by ISIC section, General Assembly, General Council,
  councillor terms and half-renewal, president election, Electoral
  Commission, Executive Committee, Board, Ethics Commission, no
  distribution of surplus, dissolution, the 2025 electoral transition),
  the 2018 Ethics Charter (whose closing line dates the founding:
  *"Fundada en Santiago de Chile, el 7 de Octubre de 1883"*), the
  councillors' Code of Conduct, the Ethics Commission regulation, and the
  Quiénes Somos, Liceos SOFOFA, Transparencia and Políticas públicas
  pages.
- **The Subsecretaría de Economía** (`:ministry-certificate-published-by-sofofa`)
  — the 10 June 2025 registry certificate SOFOFA republishes: entered in
  the Register of Trade Associations under number 149, legal personality
  in force. The speaker is the ministry, so it has its own label; the
  host is still SOFOFA's.

Each entry carries the verbatim Spanish span it rests on
(`:source-quote`), taken from the document body rather than the site
menu, the footer blurb, or the statute's running page footer. Figures
SOFOFA gives about itself (142 years; more than 7,000 companies, 42
sectoral associations, 21 regional guilds) are recorded as what SOFOFA
states. Pages that name people (the Mesa Directiva, the policy
committee, the Liceos page, the certificate's board list) are quoted
only up to the name; no name is persisted.

**What changed from the July catalog.** Both July entries cited
`sff.sofofa.cl/nosotros/que-es-sofofa/historia/`, which answers HTTP 522
(measured 2026-09-24), so neither could be checked any more. The founding
date now rests on SOFOFA's own Ethics Charter. The July entry "Code of
Ethics dictated in 1958" is dropped: no page SOFOFA serves today says
1958, and a date nobody can re-read is not kept. The Memoria Chilena and
Wikidata (Q6131011) corroborations recorded in `organization.edn` in July
were not re-fetched in this pass.

## Scope

A **read-only reference/archive** catalog — not an Advisor⊣Governor
actuation actor. It proposes or executes nothing on SOFOFA's behalf.

Coverage is reported honestly (see `association.facts/coverage`): an
association not in `catalog` has **no spec-basis**, full stop — never
fabricate one.

## Data

- `data/datascript-tx.edn` — the catalog. The facts are authored here
  and nowhere else.
- `src/association/facts.kotoba` (Clojure reading) and
  `src/association_facts.kotoba` (Kotoba port) — both GENERATED from the
  data file; do not hand-edit.
- `schema/association-rule.edn` — DataScript schema.

Query it alongside other `cloud-itonami`/`etzhayyim` compliance-fact
sources via `com-junkawasaki/root`'s `scripts/compliance-fact-query.cljs`.

## Verify

```bash
kbb --backend sci scripts/gen-kotoba-port.cljk --check    # both readings match the data file
kbb --backend sci scripts/verify-catalog.cljk             # structural, offline
kbb --backend sci scripts/verify-catalog.cljk --live      # fetch every :url, require every quote
```

`verify-catalog` exits 0 (checked, nothing wrong), 1 (findings printed)
or 2 (REFUSED: it could not read the catalog or a source, which is
neither a pass nor a finding). Dates are checked in the Spanish the
sources write them in (`7 de Octubre de 1883`, `abril 2018`) and in the
certificate's `10-06-2025`. `--live` needs `curl` and, for the PDFs,
`pdftotext`.

## License

AGPL-3.0-or-later (matches the `cloud-itonami-iso3166-*` /
`-municipality-*` / `-assoc-*` / `-lei-*` convention). Policy text
itself remains SOFOFA's; this repo stores only citation metadata
(id/title/url/dates) and the short verbatim span each claim rests on,
not full text.
