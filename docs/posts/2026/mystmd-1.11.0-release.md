---
title: "New release MyST 1.11.0: Improved Rendering, Builds, and Documentation"
date: 2026-09-24
license: CC-BY-4.0
authors:
  - id: jb-team
---

We've just released [**mystmd 1.11.0**](https://github.com/jupyter-book/mystmd/releases/tag/mystmd%401.11.0) and [**myst-theme 1.4.1**](https://github.com/jupyter-book/myst-theme/releases#release-myst-to-react@1.4.1)! 
Here are some of the bigger improvements and fixes that we made!

## What's new

- **New HTML Rendering Pathway**.
This release introduces a [new `html` rendering pathway](https://github.com/jupyter-book/mystmd/pull/3027), providing a more direct way to produce HTML output from MyST projects.
We’ve also added a [public manifest to site builds](https://github.com/jupyter-book/mystmd/pull/3002), making it easier for downstream tools and deployments to identify publicly available project files.
- **Improved Build Performance and Infrastructure**.
We’ve made several improvements to the build system, including
switching to a [`.ipynb` build cache](https://github.com/jupyter-book/mystmd/pull/2970) and
using the [available system parallelism](https://github.com/jupyter-book/mystmd/pull/2957) rather than the total number of CPUs.
These changes help MyST make better use of available resources during builds.
- **More Robust MyST Specifications**. The `myst-spec` ecosystem has been streamlined by
fusing [`myst-spec-ext` into `myst-spec`](https://github.com/jupyter-book/mystmd/pull/2908) and
generating the [schema as TypeScript](https://github.com/jupyter-book/mystmd/pull/2914).
We’ve also vendored [`markdown-it-myst-extras` into `markdown-it-myst`](https://github.com/jupyter-book/mystmd/pull/2953), simplifying the dependency structure.
- **Better Notebook and Document Rendering**.
This release includes several improvements to rendered content, including
stable [deep-link anchors for notebook cells](https://github.com/jupyter-book/mystmd/pull/2975),
support for [figures using grid directives](https://github.com/jupyter-book/mystmd/pull/2899),
and improved handling of [outputs as subfigures](https://github.com/jupyter-book/mystmd/pull/3059).
Together, these changes make it easier to create and link to rich, structured content.
- **More Reliable Cross-References and Metadata**. We’ve improved
handling of Typst [cross-references containing spaces](https://github.com/jupyter-book/mystmd/pull/3047) and
relaxed overly aggressive [DOI coercion](https://github.com/jupyter-book/mystmd/pull/2960).
We’ve also fixed several edge cases involving
[CSL HTML entities](https://github.com/jupyter-book/mystmd/pull/2986),
[multi-extension paths such as `.tar.gz`](https://github.com/jupyter-book/mystmd/pull/3045), and
[Creative Commons license URLs](https://github.com/jupyter-book/mystmd/pull/3044).
- **Improved Compatibility and Documentation**. This release includes a number of compatibility fixes, including
[Windows kernel path normalization](https://github.com/jupyter-book/mystmd/pull/3023)
and updates for [Node 24-compatible GitHub Actions](https://github.com/jupyter-book/mystmd/pull/2905).
The documentation has also been expanded with new guidance on
[host customization](https://github.com/jupyter-book/mystmd/pull/3051),
[documentation plugins](https://github.com/jupyter-book/mystmd/pull/2997),
[multi-page transforms](https://github.com/jupyter-book/mystmd/pull/2950), and
[AST structure and metadata](https://github.com/jupyter-book/mystmd/pull/2865),
as well as improved deployment guidance for
[GitLab](https://github.com/jupyter-book/mystmd/pull/2966) and
[GitHub Pages](https://github.com/jupyter-book/mystmd/pull/2990).

## Changelogs

You can also read about this release at [jupyterbook.org/releases](https://jupyterbook.org/releases). 
For more details, see
[mystmd release notes](https://github.com/jupyter-book/mystmd/releases/tag/mystmd%401.11.0) 
and 
[myst-theme release notes](https://github.com/jupyter-book/myst-theme/releases#release-myst-to-react@1.4.1).

## Upgrade notes

- To upgrade `mystmd`:   
    `npm install -g mystmd` (or `pip install -U mystmd`)

- To upgrade `myst-theme`:   
     Delete `_build`; it will be downloaded again during the next build.

## Try it out!

We'd love your feedback! Try the new release and let us know what works well and where we can improve.

## Thank you contributors!

This release would not have been possible without the help of our community!
Thanks to everyone who contributed discussions, ideas, code, and review across this release:
[@agoose77](https://github.com/agoose77),
[@bsipocz](https://github.com/bsipocz),
[@choldgraf](https://github.com/choldgraf),
[@ciyer](https://github.com/ciyer),
[@claude](https://github.com/claude),
[@coretl](https://github.com/coretl),
[@cursoragent](https://github.com/cursoragent),
[@Darshan808](https://github.com/Darshan808),
[@DobbiKov](https://github.com/DobbiKov),
[@dylanpulver](https://github.com/dylanpulver),
[@FernandoBasso](https://github.com/FernandoBasso),
[@fperez](https://github.com/fperez),
[@FreekPols](https://github.com/FreekPols),
[@fwkoch](https://github.com/fwkoch),
[@humitos](https://github.com/humitos),
[@jasongrout](https://github.com/jasongrout),
[@JimMadge](https://github.com/JimMadge),
[@Jorge-Polanco-Roque](https://github.com/Jorge-Polanco-Roque),
[@KirstieJane](https://github.com/KirstieJane),
[@kmuehlbauer](https://github.com/kmuehlbauer),
[@krassowski](https://github.com/krassowski),
[@mfisher87](https://github.com/mfisher87),
[@Montanajim](https://github.com/Montanajim),
[@nocomplexity](https://github.com/nocomplexity),
[@parmentelat](https://github.com/parmentelat),
[@rowanc1](https://github.com/rowanc1),
[@sbonaretti](https://github.com/sbonaretti),
[@sinclairtarget](https://github.com/sinclairtarget),
[@stefanv](https://github.com/stefanv),
[@stevejpurves](https://github.com/stevejpurves), and
[@TimMonko](https://github.com/TimMonko).