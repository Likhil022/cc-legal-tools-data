# cc-legal-tools-data

**Creative Commons (CC) Legal Tools Data.** This repository contains data
associated with the license tools and public domain tools (static HTML,
internationalization and localization files, etc.). It includes data consumed
and generated by the [creativecommons/cc-legal-tools-app][cc-legal-tools-app]
application.

[cc-legal-tools-app]: https://github.com/creativecommons/cc-legal-tools-app


## Code of Conduct

[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md):
> The Creative Commons team is committed to fostering a welcoming community.
> This project and all other Creative Commons open source projects are governed
> by our [Code of Conduct][code_of_conduct]. Please report unacceptable
> behavior to [conduct@creativecommons.org](mailto:conduct@creativecommons.org)
> per our [reporting guidelines][reporting_guide].

[code_of_conduct]: https://opensource.creativecommons.org/community/code-of-conduct/
[reporting_guide]: https://opensource.creativecommons.org/community/code-of-conduct/enforcement/


## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

See [`generated_files_review.md`](generated_files_review.md) for instructions
on viewing the generated files (`docs/`) locally. This may be helpful to review the changes for prohibitively large pull requests.


## Data

The data includes both source files used by
[creativecommons/cc-legal-tools-app][cc-legal-tools-app] and output from it.
See that repository for additional instructions on the use of this repository.
This section uses project specific terms. Please reference
[Definitions](#definitions), below.

- **[`docs/`](docs)**
  - ***(:warning: NOT YET ACTIVE)*** CC Legal Tools Data served by
    creativecommons.org website
  - *generated* by [cc-legal-tools-app][cc-legal-tools-app] `publish` command
- **[`legacy/`](legacy)**
  - **[`legalcode/`](legacy/legalcode)**
    - Legacy legalcode (HTML and some plaintext)
    - *ingested* by [cc-legal-tools-app][cc-legal-tools-app] `load_html_files` command
  - **[`rdf-licenses/`](legacy/rdf-licenses)**
    - Legacy RDF files for legal code (including CC0 public domain declaration,
      which is not a license)
    - *ingested* by [cc-legal-tools-app][cc-legal-tools-app] `publish` command
  - **[`rdf-meta/`](legacy/rdf-meta)**
    - Legacy RDF files and HTML (description, schema, etc.)
    - *ingested* by [cc-legal-tools-app][cc-legal-tools-app] `publish` command
- **[`legalcode/`](legalcode)**
  - The immediate subdirectories are Locale Names
  - Contains Gettext Files for Legal Code
  - Each legal tool has a custom Django/gettext translation domain that is the
    same as the Transifex resource slug
- **[`locale/`](locale)**
  - The immediate subdirectories are Locale Names
  - Contains Gettext Files for Deeds & UX
  - The default Django/gettext translation domain is used (`django`)
  - The Transifex resource slug is `deeds_ux`
- Gettext Files details:
  - `.mo` machine object Gettext Files
    - *generated* by [cc-legal-tools-app][cc-legal-tools-app] `compilemessages`
      and `load_html_files` commands
    - *ingested* by [cc-legal-tools-app][cc-legal-tools-app] `publish` and
      `runserver` commands
  - `.po` portable object Gettext Files
    - *generated* by [cc-legal-tools-app][cc-legal-tools-app]
      `check_for_translation_updates` command
    - *ingested* by [cc-legal-tools-app][cc-legal-tools-app] `compilemessages`
      and `runserver` commands


## Legal Tools Namespace

[Namespace - Wikipedia][namespace], retrieved 2021-07-06:
> In computing, a **namespace** is a set of signs (names) that are used to
> identify and refer to objects of various kinds. A namespace ensures that all
> of a given set of objects have unique names so that they can be easily
> identified.

This section uses project specific terms. Please reference
[Definitions](#definitions), below.


[namespace]: https://en.wikipedia.org/wiki/Namespace


### License Tools


#### Example: CC BY-SA 4.0

- **Category:** `licenses`
- **Title:** Creative Commons Attribution-ShareAlike 4.0 International Public
  License
- **Identifier:** CC BY-SA 4.0
- **Canonical URL:** https://creativecommons.org/licenses/by-sa/4.0/
- **Unit:** `by-sa`
- **Version:** `4.0`
- **Jurisdiction Code:** *None*, (International)
- **Language Code:** `en`


#### Example: CC BY-NC-SA 3.0

- **Category:** `licenses`
- **Title:** Attribution-NonCommercial-ShareAlike 3.0 Unported
- **Identifier:** CC BY-NC-SA 3.0
- **Canonical URL:** https://creativecommons.org/licenses/by-nc-sa/3.0/
- **Unit:** `by-nc-sa`
- **Version:** `3.0`
- **Jurisdiction Code:** *None* (International (unported))
- **Language Code:** `en`


#### Example: CC BY-ND 3.0 NL

- **Category:** `licenses`
- **Title:** Naamsvermelding-GeenAfgeleideWerken 3.0
- **Identifier:** CC BY-ND 3.0 NL
- **Canonical URL:** https://creativecommons.org/licenses/by-nd/3.0/nl/
- **Unit:** `by-nc-nd`
- **Version:** `3.0`
- **Jurisdiction Code:** `nl`
- **Language Code:** `nl`


### Public Domain Tools


#### Example: CC0 1.0

- **Category:** `publicdomain`
- **Title:** CC0 1.0 Universal
- **Identifier:** CC0 1.0
- **Canonical URL:** https://creativecommons.org/publicdomain/zero/1.0/
- **Unit:** `zero`
- **Version:** `1.0`
- **Jurisdiction Code:** *None* (Universal)
- **Language Code:** `en`


## Definitions

The following terms are used by this dataset and the
[cc-legal-tools-app][cc-legal-tools-app] application that ingests/generates it.

[djangocodes]: https://github.com/django/django/blob/0dc25526d8daaaa59968d4b1b597968e197f040c/django/conf/global_settings.py#L50-L148
[django-localename]: https://docs.djangoproject.com/en/3.2/topics/i18n/#term-locale-name
[gettext-files]: https://www.gnu.org/software/gettext/manual/html_node/Files.html
[ietf-lang-tags]: https://en.wikipedia.org/wiki/IETF_language_tag
[iso15924]: https://en.wikipedia.org/wiki/ISO_15924
[iso3166-1-alpha-2]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
[iso3166-1]: https://en.wikipedia.org/wiki/ISO_3166-1
[iso639-1-alpha-2]: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
[iso639-1]: https://en.wikipedia.org/wiki/ISO_639-1
[iso639-2-alpha-3]: https://en.wikipedia.org/wiki/List_of_ISO_639-2_codes
[iso639-2]: https://en.wikipedia.org/wiki/ISO_639-2
[rfc5646]: https://datatracker.ietf.org/doc/html/rfc5646.html
[settings-base]: https://github.com/creativecommons/cc-legal-tools-app/blob/main/cc_legal_tools/settings/base.py
[transifex-languages]: https://explore.transifex.com/languages/
[wikipedia-cldr]: https://en.wikipedia.org/wiki/Common_Locale_Data_Repository
[wikipedia-iso3166-alpha2]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
[wikipedia-locale]: https://en.wikipedia.org/wiki/Locale_(computer_software)
[wikipedia-ports]: https://en.wikipedia.org/wiki/Creative_Commons_jurisdiction_ports
[wikipedia-posixlocale]: https://en.wikipedia.org/wiki/Locale_(computer_software)#POSIX_platforms


### Gettext Files

Gettext Files are are files conveying translations (internationalization and
localization files). Django relies on the GNU gettext toolset.
- machine object files with a `.mo` file extensions (ex. `django.mo`)
- portable object files with a `.po` file extensions (ex. `django.po`)
- [GNU gettext utilities: Files][gettext-files]


#### Portable Object File Metadata

The portable object files use the following values for these standard metadata
entries:
- `Project-Id-Version`: Transifex resource slug
- `Language`: Transifex Code

The portable object files use the following values for these custom metadata
entries:
- `Language-Django`: Language Code
- `Language-Transifex`: Transifex Code


### Jurisdiction Code

Jurisdiction Codes are legal jurisdiction identifiers used for Creative Commons
legal tool ports (ex. licenses versions 1.0 - 3.0). They consist of ISO 3166-1
alpha-2 codes.
- [Creative Commons jurisdiction ports - Wikipedia][wikipedia-ports]
- [ISO 3166-1 - Wikipedia][iso3166-1] *Codes for the representation of names of
  countries and their subdivisions – Part 1: Country codes*
  - [ISO 3166-1 alpha-2 - Wikipedia][iso3166-1-alpha-2]


### IETF language tag

IETF language tags are identifiers for human languages.

- [IETF language tag - Wikipedia][ietf-lang-tags]
  - [RFC5646 Tags for Identifying Languages][rfc5646]
    - [ISO 639-1 - Wikipedia][iso639-1] *Codes for the representation of names
      of languages—Part 1: Alpha-2 code*
      - [List of ISO 639-1 codes - Wikipedia][iso639-1-alpha-2]
    - [ISO 639-2 - Wikipedia][iso639-2] *Codes for the representation of names
      of languages — Part 2: Alpha-3 code*
      - [List of ISO 639-2 codes - Wikipedia][iso639-2-alpha-3]
    - [ISO 3166-1 - Wikipedia][iso3166-1] *Codes for the representation of
      names of countries and their subdivisions – Part 1: Country codes*
      - [ISO 3166-1 alpha-2 - Wikipedia][iso3166-1-alpha-2]
    - [ISO 15924 - Wikipedia][iso15924] *Codes for the representation of  names
      of scripts*


### Locale Name

Locale Names (`locale_name`) are Django locale names. Django locale names are
language/region identifiers programmatically generated by Django based on the
Language Code.  They are meant to match POSIX locales or Unicode locales.
- [locale name | Definitions | Internationalization and localization | Django
  documentation | Django][django-localename]
- [Locale (computer software) - Wikipedia][wikipedia-locale]


### Language Code

Language Codes (`language_code`) are Django language codes. They consist of
*lowercase* IETF language tags.
- The default Django languge codes are defined in
  `django/django`:`django/conf/global_settings.p`: [Lines 50-148][djangocodes]
- Additional codes are defined by the [cc-legal-tools-app][cc-legal-tools-app]
  application in [`cc_legal_tools/settings/base.py`][settings-base]


### POSIX locale

POSIX locales are language/region identifiers defined by POSIX.
- [POSIX platforms - Locale (computer software) -
  Wikipedia][wikipedia-posixlocale]
- [Locale (computer software) - Wikipedia][wikipedia-locale]


### Transifex Code

Transifex Codes (`transifex_code`) are Transifex language codes. *Most* consist
of POSIX locales or Unicode locales. *Some* consist of IETF language tags.
- [Languages on Transifex][transifex-languages]
- [Locale (computer software) - Wikipedia][wikipedia-locale]


### Unicode locale

Unicode locales are language/region identifiers defined by the Unicode
Consortium.
- [Common Locale Data Repository - Wikipedia][wikipedia-cldr]
- [Locale (computer software) - Wikipedia][wikipedia-locale]


## Copying and licenses

[![CC0 1.0 Universal (CC0 1.0) Public Domain Dedication
button][cc-zero-png]][cc-zero] [`COPYING`](COPYING): The text of the Creative
Commons legal tools is dedicated to the public domain under the [CC0 1.0
Universal (CC0 1.0) Public Domain Dedication][cc-zero].

[cc-zero-png]: https://licensebuttons.net/l/zero/1.0/88x31.png#floatleft "CC0 1.0 Universal (CC0 1.0) Public Domain Dedication button"
[cc-zero]: https://creativecommons.org/publicdomain/zero/1.0/


## Trademark

Except for the limited purpose of indicating that material is shared under a
Creative Commons public license or as otherwise permitted by the Creative
Commons policies published at [creativecommons.org/policies][policies],
Creative Commons does not authorize the use of the trademark "Creative Commons"
or any other trademark or logo of Creative Commons without its prior written
consent including, without limitation, in connection with any unauthorized
modifications to any of its public licenses or any other arrangements,
understandings, or agreements concerning use of licensed material.

[policies]: https://creativecommons.org/policies/


### vocabulary-theme

[![CC0 1.0 Universal (CC0 1.0) Public Domain Dedication
button][cc-zero-png]][cc-zero]

[`COPYING`](COPYING): All the code within Vocabulary is dedicated to
the public domain under the [CC0 1.0 Universal (CC0 1.0) Public Domain
Dedication][cc-zero].

[cc-zero-png]: https://licensebuttons.net/l/zero/1.0/88x31.png "CC0 1.0 Universal (CC0 1.0) Public Domain Dedication button"
[cc-zero]: https://creativecommons.org/publicdomain/zero/1.0/ "Creative Commons — CC0 1.0 Universal"


#### Normalize.css

normalize.css is licensed under the Expat/[MIT][mit] License.

[mit]: https://opensource.org/license/mit/


#### Fonts


##### Accidenz Commons

[Accidenz Commons][accidenzcommons] by Archetypo is licensed under the [Creative
Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)
License][ccbysa40].

[accidenzcommons]: https://creativecommons.org/2019/10/28/accidenz-commons-open-licensed-font/
[ccbysa40]: https://creativecommons.org/licenses/by-sa/4.0/


##### JetBrains Mono

[JetBrains Mono][jetbrainsmono] is licensed under the [OFL-1.1 License][ofl].

[jetbrainsmono]: https://www.jetbrains.com/lp/mono/
[ofl]: https://github.com/JetBrains/JetBrainsMono/blob/master/OFL.txt


##### Roboto Condensed

[Roboto Condensed][robotocondensed] by Christian Robertson is licensed under
the [Apache License, Version 2.0][apache20].

[robotocondensed]: https://fonts.google.com/specimen/Roboto+Condensed
[apache20]: http://www.apache.org/licenses/LICENSE-2.0


##### Source Sans Pro

[Source Sans Pro][sourcesanspro] by Paul D. Hunt is licensed under the [Open
Font License][oflsil].

[sourcesanspro]: https://fonts.adobe.com/fonts/source-sans
[oflsil]: https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL


##### Vocabulary Icons

Vocabulary Icons use icons from [Font Awesome][fontawesome] which are licensed
under the [Creative Commons Attribution 4.0 International (CC BY 4.0)
License][ccbysa40].

[fontawesome]: https://fontawesome.com/
[ccby40]: https://creativecommons.org/licenses/by/4.0/
