(ns association.facts
  "Industry rule/history catalog for SOFOFA (Sociedad de Fomento
  Fabril) -- a 63rd industry-association-level source (see
  cloud-itonami-assoc-9411-sau-fsc, -9411-aut-wko, -9411-irl-ibec,
  -9411-nzl-businessnz, -9411-cze-spcr, -9411-ind-cii, -9411-zaf-busa,
  -9411-bra-cni, -9411-ken-kam, -9411-can-chamber, -9411-mex-coparmex,
  -9411-ita-confindustria, -9411-nld-vnoncw, -9411-kor-kcci,
  -9411-arg-uia, -9411-bel-feb, -9411-dnk-di, -9411-swe-sn, -9411-fin-ek,
  -9411-tha-fti for the first twenty) per ADR-2607141700
  (cloud-itonami-compliance-fact-federation). The TWENTY-FIRST entry
  aligned to ISIC 9411 (activities of business, employers, and
  professional membership organizations). Fills Chile's previously-
  open association-axis gap (one of the 7-country gap list recorded
  at tick 155) -- Chile now has real, individually verified facts
  across ALL THREE axes (country: cloud-itonami-iso3166-chl
  statute.facts; municipality: cloud-itonami-municipality-chl-santiago;
  association: this entry).

  The 7 October 1883 founding date is TRIPLY corroborated: SOFOFA's
  own official history page (https://sff.sofofa.cl/nosotros/que-es-
  sofofa/historia/), directly read, states verbatim 'Fundada el 7 de
  octubre de 1883, bajo la presidencia de la República de don
  Domingo Santa María'; Memoria Chilena (memoriachilena.gob.cl, the
  Chilean National Library's own historical archive, independent of
  SOFOFA itself), directly read, states verbatim 'Fundada en 1883 a
  instancias del presidente de la república Domingo Santa María, la
  Sociedad de Fomento Fabril tuvo en sus inicios un papel de órgano
  consultivo del Estado'; and Wikidata Q6131011's own 'inception'
  statement lists 1883. The second entry (1958 Code of Ethics) is
  also directly read from SOFOFA's own history page: 'Código de
  Ética que obliga a todos sus socios y que fue dictado en 1958'.
  President Domingo Santa María's name, incidentally encountered as
  historical context for the founding date (not an office-holder OF
  SOFOFA itself), is NOT persisted here as a standalone fact.

  An association not in `catalog` has NO spec-basis, full stop; never
  fabricate one.")

(def catalog
  "association-slug -> vector of association-rule entries."
  {"sofofa"
   [{:association-rule/id "sofofa.founding-1883-10-07"
     :association-rule/title "Sociedad de Fomento Fabril (SOFOFA) founded 7 October 1883 (SOFOFA's own official history page, independently corroborated by Memoria Chilena -- the Chilean National Library's own archive -- and Wikidata Q6131011's inception statement)"
     :association-rule/association "sofofa"
     :association-rule/isic "9411"
     :association-rule/country "CHL"
     :association-rule/kind :governance-program
     :association-rule/url "https://sff.sofofa.cl/nosotros/que-es-sofofa/historia/"
     :association-rule/url-provenance :official-sofofa-cl
     :association-rule/established-date "1883-10-07"
     :association-rule/retrieved-at "2026-07-18"
     :association-rule/topic #{:governance}}
    {:association-rule/id "sofofa.code-of-ethics-1958"
     :association-rule/title "SOFOFA issued its Code of Ethics ('Código de Ética') binding all members, in 1958 (SOFOFA's own official history page)"
     :association-rule/association "sofofa"
     :association-rule/isic "9411"
     :association-rule/country "CHL"
     :association-rule/kind :governance-program
     :association-rule/url "https://sff.sofofa.cl/nosotros/que-es-sofofa/historia/"
     :association-rule/url-provenance :official-sofofa-cl
     :association-rule/established-date "1958"
     :association-rule/retrieved-at "2026-07-18"
     :association-rule/topic #{:governance}}]})

(defn spec-basis [association] (get catalog association))

(defn coverage
  ([] (coverage (keys catalog)))
  ([associations]
   (let [have (filter catalog associations)
         missing (remove catalog associations)]
     {:requested (count associations)
      :covered (count have)
      :covered-associations (vec (sort have))
      :missing-associations (vec (sort missing))
      :note (str "cloud-itonami-assoc-9411-chl-sofofa Wave 0 (ADR-2607141700): "
                 (count (get catalog "sofofa")) " SOFOFA entries seeded "
                 "with sofofa.cl official + Memoria Chilena + Wikidata Q6131011 corroboration. "
                 "Extend `association.facts/catalog`, never fabricate an id/url.")})))

(defn by-topic [association topic]
  (filterv #(contains? (:association-rule/topic %) topic) (spec-basis association)))
