![The straight road at dusk: the nearest sign fixed on its post with its shutter lit and its transformer housing and cable drop plain against dusk violet, the office window and key hooks in the middle distance, a second sign dark with one tube broken at the bend, and smaller signs pricking the dark far off, no lettering anywhere](intro-banner.png)


# codeintel-HTTP-Header-Security-Analyzer

![A census reach of the old road at last light: the foreground sign lit on its post, a second sign dark with a broken tube and a lit office window below it, smaller signs far down the straight road, and the name codeintel-http-header-security-analyzer in neon across the foreground parapet, the one inscription in the picture](banner.png)

![One roadside motel sign at dusk on a single post above a low parapet, its vacancy shutter lit in neon, its transformer housing behind the cabinet, its painted arrow pointing down, and the name in Bebas Neue in diner chrome on dusk violet beneath the post, the heading plate](logo.png)

![The census reach in three depths: far signs stay fixed while dusk deepens once, the nearest sign warms its tubes in sequence and its shutter lights, holds, darkens, and lights again, one tube on the second sign flickers at its broken bend, and the atlas, register, and key hooks on the counter stay still](scene.svg)

Analyzes HTTP response headers for common security misconfigurations (for example missing Strict-Transport-Security, X-Frame-Options, Content-Security-Policy). Focused on tools for static code analysis, vulnerability scanning, and code quality assurance.

> **Presence Only, Values Not Judged.** Each header is judged on presence alone. A Strict-Transport-Security value of max-age=0 still counts as found, and Permissions-Policy is credited where the older Feature-Policy name appears instead. The count records whether the tubes answer, not what the rooms behind the sign hold.

![Major separator](sep-heavy.svg)

## Install
`git clone https://github.com/ShadowGuard-AI/codeintel-http-header-security-analyzer`

![Major separator](sep-heavy.svg)

## Usage
`python3 main.py URL [--verbose]`

![Major separator](sep-heavy.svg)

## Parameters
- `-h`: Show help message and exit
- `url`: The URL to analyze. Required.
- `--verbose`, `-v`: Enable verbose logging.

![Major separator](sep-heavy.svg)

## Verified behavior
- Against a local server that sends none of the checked headers, the tool reports all six as missing: HSTS, X-Frame-Options, CSP, X-Content-Type-Options, Referrer-Policy, and Permissions-Policy, and exits 0. Read the findings in the output: an exit code of 0 does not mean the headers are present.

> **Frame-Ancestors Counts as Framing Protection.** Framing protection is credited where a Content-Security-Policy carries frame-ancestors, even when X-Frame-Options itself is absent.

![Major separator](sep-heavy.svg)

## License
See LICENSE.

> **All Six Missing Still Exits 0.** The verified entry above is the caution of this ledger: the printed findings are the verdict and the exit figure is not. A run that finds every header missing still closes at 0.
