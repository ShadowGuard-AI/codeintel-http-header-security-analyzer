![Banner](banner.png)

# codeintel-HTTP-Header-Security-Analyzer
Analyzes HTTP response headers for common security misconfigurations (for example missing Strict-Transport-Security, X-Frame-Options, Content-Security-Policy). Focused on tools for static code analysis, vulnerability scanning, and code quality assurance.

## Install
`git clone https://github.com/ShadowGuard-AI/codeintel-http-header-security-analyzer`

## Usage
`python3 main.py URL [--verbose]`

## Parameters
- `-h`: Show help message and exit
- `url`: The URL to analyze. Required.
- `--verbose`, `-v`: Enable verbose logging.

## Verified behavior
- Against a local server that sends none of the checked headers, the tool reports all six as missing: HSTS, X-Frame-Options, CSP, X-Content-Type-Options, Referrer-Policy, and Permissions-Policy, and exits 0. Read the findings in the output: an exit code of 0 does not mean the headers are present.

## License
See LICENSE.
