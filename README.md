# The Agentic Automation Canvas: a structured framework for agentic AI project design

Read by following the badge links:

<!-- usage note: edit the H1 title above to personalize the manuscript -->

[![Preprint](https://img.shields.io/badge/preprint-arXiv-blue.svg)](https://arxiv.org/abs/2602.15090)
[![HTML Manuscript](https://img.shields.io/badge/manuscript-HTML-blue.svg)](https://slolab.github.io/aac-manuscript/)
[![GitHub Actions Status](https://github.com/slolab/aac-manuscript/workflows/Manubot/badge.svg)](https://github.com/slolab/aac-manuscript/actions)

## Manuscript description

<!-- usage note: edit this section. -->

Agentic AI prototypes are being deployed across domains with increasing speed, yet no methodology for their structured design, governance, and prospective evaluation has been established.
Existing AI documentation practices and guidelines – Model Cards, Datasheets, or NIST AI RMF – are either retrospective or lack machine-readability and interoperability.
We present the Agentic Automation Canvas (AAC), a structured framework for the prospective design of agentic systems and a tool to facilitate communication between their users and developers.
The AAC captures six dimensions of an automation project: definition and scope; user expectations with quantified benefit metrics; developer feasibility assessments; governance staging; data access and sensitivity; and outcomes.
The framework is implemented as a semantic web-compatible metadata schema with controlled vocabulary and mappings to established ontologies such as Schema.org and W3C DCAT.
It is made accessible through a privacy-preserving, fully client-side web application with real-time validation.
Completed canvases export as FAIR-compliant RO-Crates, yielding versioned, shareable, and machine-interoperable project contracts between users and developers.
We describe the schema design, benefit quantification model, and prospective application to diverse use cases from research, clinical, and institutional settings.
The AAC and its web application are available as open-source code and interactive web form at [https://aac.slolab.ai](https://aac.slolab.ai).

## Manubot

<!-- usage note: do not edit this section -->

Manubot is a system for writing scholarly manuscripts via GitHub.
Manubot automates citations and references, versions manuscripts using git, and enables collaborative writing via GitHub.
An [overview manuscript](https://greenelab.github.io/meta-review/ "Open collaborative writing with Manubot") presents the benefits of collaborative writing with Manubot and its unique features.
The [rootstock repository](https://git.io/fhQH1) is a general purpose template for creating new Manubot instances, as detailed in [`SETUP.md`](SETUP.md).
See [`USAGE.md`](USAGE.md) for documentation how to write a manuscript.

Please open [an issue](https://git.io/fhQHM) for questions related to Manubot usage, bug reports, or general inquiries.

### Repository directories & files

The directories are as follows:

+ [`content`](content) contains the manuscript source, which includes markdown files as well as inputs for citations and references.
  See [`USAGE.md`](USAGE.md) for more information.
+ [`output`](output) contains the outputs (generated files) from Manubot including the resulting manuscripts.
  You should not edit these files manually, because they will get overwritten.
+ [`webpage`](webpage) is a directory meant to be rendered as a static webpage for viewing the HTML manuscript.
+ [`build`](build) contains commands and tools for building the manuscript.
+ [`ci`](ci) contains files necessary for deployment via continuous integration.

### Local execution

The easiest way to run Manubot is to use [continuous integration](#continuous-integration) to rebuild the manuscript when the content changes.
If you want to build a Manubot manuscript locally, install the [conda](https://conda.io) environment as described in [`build`](build).
Then, you can build the manuscript on POSIX systems by running the following commands from this root directory.

```sh
# Activate the manubot conda environment (assumes conda version >= 4.4)
conda activate manubot

# Build the manuscript, saving outputs to the output directory
bash build/build.sh

# At this point, the HTML & PDF outputs will have been created. The remaining
# commands are for serving the webpage to view the HTML manuscript locally.
# This is required to view local images in the HTML output.

# Configure the webpage directory
manubot webpage

# You can now open the manuscript webpage/index.html in a web browser.
# Alternatively, open a local webserver at http://localhost:8000/ with the
# following commands.
cd webpage
python -m http.server
```

Sometimes it's helpful to monitor the content directory and automatically rebuild the manuscript when a change is detected.
The following command, while running, will trigger both the `build.sh` script and `manubot webpage` command upon content changes:

```sh
bash build/autobuild.sh
```

### Continuous Integration

Whenever a pull request is opened, CI (continuous integration) will test whether the changes break the build process to generate a formatted manuscript.
The build process aims to detect common errors, such as invalid citations.
If your pull request build fails, see the CI logs for the cause of failure and revise your pull request accordingly.

When a commit to the `main` branch occurs (for example, when a pull request is merged), CI builds the manuscript and writes the results to the [`gh-pages`](https://github.com/slolab/aac-manuscript/tree/gh-pages) and [`output`](https://github.com/slolab/aac-manuscript/tree/output) branches.
The `gh-pages` branch uses [GitHub Pages](https://pages.github.com/) to host the following URLs:

+ **Preprint (arXiv)** at https://arxiv.org/abs/2602.15090
+ **HTML manuscript** at https://slolab.github.io/aac-manuscript/

For continuous integration configuration details, see [`.github/workflows/manubot.yaml`](.github/workflows/manubot.yaml).

## License

<!--
usage note: edit this section to change the license of your manuscript or source code changes to this repository.
We encourage users to openly license their manuscripts, which is the default as specified below.
-->

[![License: CC BY 4.0](https://img.shields.io/badge/License%20All-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![License: CC0 1.0](https://img.shields.io/badge/License%20Parts-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Except when noted otherwise, the entirety of this repository is licensed under a CC BY 4.0 License ([`LICENSE.md`](LICENSE.md)), which allows reuse with attribution.
Please attribute by linking to https://github.com/slolab/aac-manuscript.

Since CC BY is not ideal for code and data, certain repository components are also released under the CC0 1.0 public domain dedication ([`LICENSE-CC0.md`](LICENSE-CC0.md)).
All files matched by the following glob patterns are dual licensed under CC BY 4.0 and CC0 1.0:

+ `*.sh`
+ `*.py`
+ `*.yml` / `*.yaml`
+ `*.json`
+ `*.bib`
+ `*.tsv`
+ `.gitignore`

All other files are only available under CC BY 4.0, including:

+ `*.md`
+ `*.html`
+ `*.pdf`
+ `*.docx`

Please open [an issue](https://github.com/slolab/aac-manuscript/issues) for any question related to licensing.
