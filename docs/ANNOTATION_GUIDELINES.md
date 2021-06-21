# ANNOTATION GUIDELINES

## Variables

name | description | type
---|---|---
text    | The name (lower-cased) of the entity | `str`
cat     | The category of the entity. `"RES_INSTITUTE"` for research institute/agency, `"UNIVERSITY"` for university/graduate schools, `"HOSPITAL"` for hospitals and `"OTHER"` for others (non research agents, incl. people and companies)| `int`
country\_code    | The country code of the main country of the entity | `str`

## Sources

country\_code   | University/graduate school | Research institute/agency | Hospital | Other
---|---|---|---|---
DE  | [Wiki Liste der Hochschulen in Deutschland](https://de.wikipedia.org/wiki/Liste_der_Hochschulen_in_Deutschland)| | [Wiki Liste von Klinikgruppen](https://de.wikipedia.org/wiki/Liste_von_Klinikgruppen) | [CIO list of top 500 companies](https://www.cio.de/top500)
FR  | [univ-ag list of main higher education ](http://www1.univ-ag.fr/aoc/liens/organismes.html) | [Wiki Liste des Etablissements publics à caractères scientifique](https://fr.wikipedia.org/wiki/Liste_des_%C3%A9tablissements_publics_%C3%A0_caract%C3%A8re_scientifique,_culturel_et_professionnel) | [Solidarité-santé.gouv](https://solidarites-sante.gouv.fr/IMG/pdf/ListeESvolontaires2013.pdf) | [List of registered companies](https://www.data.gouv.fr/fr/datasets/entreprises-immatriculees-en-2017/)
GB  | [Wiki list of universities in the UK](https://en.wikipedia.org/wiki/List_of_universities_in_the_United_Kingdom)| [Wiki lists of research institutes](https://en.wikipedia.org/wiki/Category:Lists_of_research_institutes) | [Wiki list of hospitals in England](https://en.wikipedia.org/wiki/List_of_hospitals_in_England )| [Wiki List of registered companies](https://en.wikipedia.org/wiki/List_of_companies_of_the_United_Kingdom_A-J)
US  | [Wiki list of American universities and colleges](https://en.wikipedia.org/wiki/Lists_of_American_universities_and_colleges)| [Wiki lists of research institutes](https://en.wikipedia.org/wiki/Category:Lists_of_research_institutes) | [Wiki list of hospitals in the United States](https://en.wikipedia.org/wiki/Lists_of_hospitals_in_the_United_States) | [Wiki list of US companies](https://en.wikipedia.org/wiki/List_of_companies_of_the_United_States_by_state)

!!! note
    In order to keep the training data balanced, we had to sample some lists:

    - FR Other: random sample - 600
    - US Hospitals: restrict to Colorado, Florida and Minnesota
    - US Other: Restrict to Alabama, Hawai, Indiana, Iowa, Missouri, New-Jersey, Ohio, Virginia, Wisconsin
    - GB Other: Sample Companies

## Training sample

| `country_code`/`cat`   |    `OTHER` |   `RES_INSTITUTE` |   `UNIVERSITY` |   `HOSPITAL` |
|:---------------|-----:|----:|----:|----:|
| `DE`             |  821 | 105 | 427 |  79 |
| `FR`             |  770 |  53 | 147 | 124 |
| `GB`             |  895 |  67 | 264 | 771 |
| `US`             | 1067 | 295 | 406 | 612 |
