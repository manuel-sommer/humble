# humble

<p align=center>
<a target="_blank" href="https://www.python.org/downloads/" title="Minimum Python version required to run this tool"><img src="https://img.shields.io/badge/Python-%3E%3D3.9-blue?labelColor=343b41"></a>
<a target="_blank" href="LICENSE" title="License of this tool"><img src="https://img.shields.io/badge/License-MIT-blue.svg?labelColor=343b41"></a>
<a target="_blank" href="https://github.com/rfc-st/humble/releases" title="Latest release of this tool"><img src="https://img.shields.io/github/v/release/rfc-st/humble?display_name=release&label=Latest%20release&labelColor=343b41"></a>
<a target="_blank" href="https://github.com/rfc-st/humble/commits/master" title="Latest commit of this tool"><img src="https://img.shields.io/badge/Latest_Commit-2023--10--14-blue.svg?labelColor=343b41"></a>
<a target="_blank" href="https://github.com/rfc-st/humble/actions?query=workflow%3ACodeQL" title="Results of the last analysis of this tool with CodeQL"><img src="https://github.com/rfc-st/humble/workflows/CodeQL/badge.svg"></a>
<a target="_blank" href="https://owasp.org/www-project-secure-headers/#div-technical" title="Tool accepted as a technical resource for OWASP"><img src="https://img.shields.io/badge/OWASP-Resource-blue?labelColor=343b41"></a>
<a target="_blank" href="https://www.kali.org/tools/humble/" title="Tool accepted in Kali"><img src="https://img.shields.io/badge/Kali%20Linux-Tool-blue?labelColor=343b41"></a>

<br />
<br />
HTTP Headers Analyzer<br />
<br />
<i>"A journey of a thousand miles begins with a single step. - Lao Tzu"</i>
<br />
<br />
<i>"And if you don't keep your feet, there's no knowing where you might be swept off to. - Bilbo Baggins"</i>
<br />
<br />

### Table of contents

[Features](#features)<br />
[Screenshots](#screenshots)<br />
[Installation & Update](#installation--update)<br />
[Usage](#usage)<br />
[Advanced Usage](#advanced-usage)<br />
 [Linux: Show only the analysis summary](#linux-show-only-the-analysis-summary)<br />
 [Windows: In spanish. Show only the analysis summary (PowerShell >= 7 required)](#windows-in-spanish-show-only-the-analysis-summary-powershell--7-required)<br />
 [Linux: Show only the URL, date and analysis summary](#linux-show-only-the-url-date-and-analysis-summary)<br />
 [Linux: Show only the deprecated headers/protocols and insecure values](#linux-show-only-the-deprecated-headersprotocols-and-insecure-values)<br />
 [Linux: Check for HTTP client errors (4XX)](#linux-check-for-http-client-errors-4xx)<br />
 [Linux: Analyze multiple URLs and save the results as PDFs](#linux-analyze-multiple-urls-and-save-the-results-as-pdfs)<br />
[Checks: Missing Headers](#checks-missing-headers)<br />
[Checks: Fingerprint Headers](#checks-fingerprint-headers)<br />
[Checks: Deprecated Headers and Insecure Values](#checks-deprecated-headersprotocols-and-insecure-values)<br />
[Checks: Empty Values](#checks-empty-values)<br />
[Guidelines included](#guidelines-included-to-enable-security-http-headers)<br />
[To-Do](#to-do)<br />
[Further Reading](#further-reading)<br />
[Contribute](#contribute)<br />
[Acknowledgements](#acknowledgements)<br />
[License](#license)<br />
<br />

## Features

:heavy_check_mark: 13 [checks](#checks-missing-headers) of missing HTTP response headers.<br />
:heavy_check_mark: 996 [checks](#checks-fingerprint-headers) of fingerprinting through HTTP response headers.<br />
:heavy_check_mark: 85 [checks](#checks-deprecated-headersprotocols-and-insecure-values) of deprecated HTTP response headers/protocols or with insecure/wrong values.<br />
:heavy_check_mark: Browser compatibility check for enabled security headers.<br />
:heavy_check_mark: Two types of analysis: brief and detailed, along with HTTP response headers.<br />
:heavy_check_mark: Export of analysis to HTML5, PDF 1.4, TXT and JSON.<br />
:heavy_check_mark: The analysis includes dozens of references, official documentation and technical articles.<br />
:heavy_check_mark: i10n: analysis results in English or Spanish.<br />
:heavy_check_mark: Saves each analysis, showing (at the end) the improvements or deficiencies in relation to the last one.<br />
:heavy_check_mark: Shows analysis statistics: either against a specific URL or all of them.<br />
:heavy_check_mark: Shows fingerprint statistics: either against a specific term or the Top 20.<br />
:heavy_check_mark: Code reviewed via <a href="https://pypi.org/project/pycodestyle/" target="_blank">pycodestyle<a>, <a href="https://marketplace.visualstudio.com/items?itemName=SonarSource.sonarlint-vscode" target="_blank">SonarLint<a> and <a href="https://marketplace.visualstudio.com/items?itemName=sourcery.sourcery" target="_blank">Sourcery<a>.<br />
:heavy_check_mark: Tested, one by one, on thousands of URLs.<br />
:heavy_check_mark: Fully tested and working on Windows (10 20H2 - 19042.985) and Linux (Kali 2021.1).<br />
:heavy_check_mark: All code under one of the most permissive licenses: <a href="https://github.com/rfc-st/humble/blob/master/LICENSE" target="_blank">MIT<a>.<br />
:heavy_check_mark: Regularly <a href="https://github.com/rfc-st/humble/commits/master" target="_blank">updated</a>.<br />
:heavy_check_mark: Developed in my spare time, with no relationship with clients/companies: try it and integrate it into your projects!.<br />
:heavy_check_mark: Technical resource accepted in the OWASP <a href="https://owasp.org/www-project-secure-headers/#div-technical" target="_blank">Secure Headers</a> Project and <a href="https://www.kali.org/tools/humble/" target="_blank">Kali Linux</a>.<br />
<br />

## Screenshots

.: (Windows) - Brief analysis.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_b.PNG" alt="Brief Analysis">
</p>
<br />
.: (Linux) - Brief analysis and retrieved HTTP headers.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_br.PNG" alt="Brief analysis + retrieved headers">
</p>
<br />
.: (Linux) - Detailed analysis in Spanish.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble.PNG" alt="Full analysis" width=70% height=70%>
</p>
<br />
.: (Linux) - List of HTTP fingerprint headers based on a specific term.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_fng.jpg" alt="Specific fingerprint headers" width=70% height=70%>
</p>
<br />
.: (Windows) - Detailed analysis exported to PDF. <a href="https://github.com/rfc-st/humble/raw/master/samples/tesla_headers_20230406.pdf">Example.</a><br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_pdf_s.PNG" alt="Export analysis to PDF" width=70% height=70%>
</p>
<br />
.: (Linux) - Detailed analysis exported to HTML. <a href="https://htmlpreview.github.io/?https://github.com/rfc-st/humble/blob/master/samples/tesla_headers_20230406.html">Example.</a><br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_html_s.PNG" alt="Export analysis to HTML" width=70% height=70%>
</p>
<br />
.: (Linux) - Analysis history file: Date, URL, Missing, Fingerprint, Deprecated/Insecure, Empty headers & Total warnings (the four previous totals).<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_ah.PNG" alt="History of analysis performed">
</p>
<br />
.: (Linux) - Statistics of the analysis performed against a specific URL.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_analytics.jpg" alt="Statistics of the analysis performed against a URL">
</p>
<br />
.: (Linux) - Statistics of the analysis performed against all URLs.<br />
<p></p>
<p align="center">
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_global_analytics.jpg" alt="Global statistics of the analysis performed">
</p>
<br />

## Installation & Update

**NOTE**: Python 3.9 or higher is required.

```bash
# install python3 and python3-pip if not exist
(Windows) https://www.python.org/downloads/windows/
(Linux) if not installed by default, install them via, e.g. Synaptic, apt, dnf, yum ...

# install git
(Windows) https://git-scm.com/download/win
(Linux) https://git-scm.com/download/linux

# clone the repository
$ git clone https://github.com/rfc-st/humble.git

# change the working directory to humble
$ cd humble

# install the requirements
$ pip3 install -r requirements.txt

# update humble (every week, inside humble's working directory)
$ git pull

# or download the latest release (every four to five weeks)
https://github.com/rfc-st/humble/releases
```

## Usage

```console
(Windows) $ py humble.py
(Linux)   $ python3 humble.py

usage: humble.py [-h] [-a] [-b] [-f [TERM]] [-g] [-l {es}] [-o {html,pdf,txt,json}] [-r] [-u URL] [-v]

humble (HTTP Headers Analyzer) - https://github.com/rfc-st/humble

options:
  -h, --help              show this help message and exit
  -a                      show statistics of the performed analysis (will be global if '-u URL' is omitted)
  -b                      show a brief analysis (if omitted, a detailed one will be shown)
  -f [TERM]               show fingerprint statistics (will be the Top 20 if "TERM", e.g. "Google", is omitted)
  -g                      show guidelines for securing popular web servers/services
  -l {es}                 show the analysis in the indicated language (if omitted, English will be used)
  -o {html,pdf,txt,json}  save analysis to file (with the format URL_headers_yyyymmdd.ext)
  -r                      show full HTTP response headers and a detailed analysis
  -u URL                  schema and URL to analyze. E.g. https://google.com
  -v, --version           show the version of this tool and check for updates
```

## Advanced Usage

### Linux: Show only the analysis summary

```
$ python3 humble.py -u https://www.spacex.com | grep -A 8 "\!." | sed $'1i \n'
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_linux.jpg" alt="Show only the analysis summary (Linux)">


### Windows (in Spanish): show only the analysis summary (PowerShell >= 7 required)

```
$ py humble.py -u https://www.spacex.com -l es | Select-String -Pattern '!.' -Context 1,8 -NoEmphasis
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_windows.jpg" alt="Show only the analysis summary (Windows, in Spanish. PowerShell >= 7 required)">


### Linux: Show only the URL, date and analysis summary
```
$ python3 humble.py -u https://www.spacex.com | grep -A7 -E "0. Info|\!." | grep -v "^\[1\." | sed 's/[--]//g' | sed -e '/./b' -e :n -e 'N;s/\n$//;tn' | sed $'1i \n'
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_linux_2.jpg" alt="Show URL, date and the analysis summary (Linux)">


### Linux: Show only the deprecated headers/protocols and insecure values
```
$ python3 humble.py -u https://www.spacex.com | sed '/3. /,/4. /!d' | sed '$d' | sed $'1i \n'
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_linux_3.jpg" alt="Show only the deprecated headers/protocols and insecure values (Linux)">


### Linux: Check for HTTP client errors (4XX)
```
$ python3 humble.py -u https://block.fiverr.com | grep -A1 -B5 'Note : \|Nota : ' --color=never
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_linux_4.jpg" alt="Check for HTTP client errors (4XX) (Linux)">


### Linux: Analyze multiple URLs and save the results as PDFs
```
$ datasets=('https://facebook.com' 'https://www.microsoft.com' 'https://www.spacex.com'); for dataset in "${datasets[@]}"; do python3 humble.py -u "$dataset" -o pdf; done
```
<img src="https://github.com/rfc-st/humble/blob/master/screenshots/humble_adv_linux_5.jpg" alt="Analyze multiple URLs and save the results as PDFs">


## Checks: Missing Headers
<details>

<br />

<summary>Show / Hide</summary>

||||
| ------------- | ------------- | ------------- | 
| `Cache-Control` | `Clear-Site-Data` | `Content-Type` |
| `Content-Security-Policy` | `Cross-Origin-Embedder-Policy` | `Cross-Origin-Opener-Policy` |
| `Cross-Origin-Resource-Policy` | `NEL` | `Permissions-Policy` |
| `Referrer-Policy` | `Strict-Transport-Security` | `X-Content-Type-Options` | 
| `X-Frame-Options` |||
||||

</details>

## Checks: Fingerprint headers

Check <a href="https://github.com/rfc-st/humble/blob/master/additional/fingerprint.txt">this</a> file.

## Checks: Deprecated headers/protocols and insecure values

Check <a href="https://github.com/rfc-st/humble/blob/master/additional/insecure.txt">this</a> file.

## Checks: Empty values

Any HTTP response header.

## Guidelines included to enable security HTTP headers
* Amazon AWS
* Apache HTTP Server
* Cloudflare
* MaxCDN
* Microsoft Internet Information Services
* Nginx

## To-do

- [ ] Add more header/value checks (only security-oriented)
- [ ] Google Style Python Docstrings and maybe documentation via Sphinx.

## Further reading

https://caniuse.com/<br />
https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers<br />
https://github.com/search?q=http+headers+analyze<br />
https://github.com/search?q=http+headers+secure<br />
https://github.com/search?q=http+headers+security<br />
https://owasp.org/www-project-secure-headers/<br />
https://securityheaders.com/<br />
https://scotthelme.co.uk/<br />
https://webtechsurvey.com/common-response-headers<br />
https://www.w3.org<br />

## Contribute
* Report a <a href="https://github.com/rfc-st/humble/issues/new?assignees=&labels=&template=bug_report.md&title=">Bug</a>.
* Create a <a href="https://github.com/rfc-st/humble/issues/new?assignees=&labels=&template=feature_request.md&title=">Feature request</a>.
* Report a <a href="https://github.com/rfc-st/humble/security/policy">Security Vulnerability</a>.
* Send me an email with your suggestions!: rafael.fcucalon@gmail.com

Thanks for your time!! :).

## Acknowledgements
* <a href="https://github.com/Azathothas">Azathothas</a> for reporting <a href="https://github.com/rfc-st/humble/issues/4">this</a> bug.
* <a href="https://github.com/bulaktm">bulaktm</a> for <a href="https://github.com/rfc-st/humble/issues/5">this</a> suggestion.
* <a href="https://www.linkedin.com/in/eduardo-boronat/">Eduardo</a>, for making possible the first Demo and <a href="https://github.com/rfc-st/humble#linux-analyze-multiple-urls-and-save-the-results-as-pdfs">this</a> example.
* <a href="https://github.com/gl4nce">gl4nce</a> for <a href="https://github.com/rfc-st/humble/issues/6">this</a> suggestion.
* İDRİS BUDAK for reporting the need to <a href="https://github.com/rfc-st/humble/commit/f85dd7811859fd2e403a0ecd848b21db20949841">this</a> check.

## License

MIT © 2020-2023 Rafa 'Bluesman' Faura (rafael.fcucalon@gmail.com)<br/>
Original Creator - Rafa 'Bluesman' Faura (rafael.fcucalon@gmail.com)
