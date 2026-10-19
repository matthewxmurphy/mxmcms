# MXMCMS — proposal

**Concept documentation; no installable CMS or released product is present.**

This repository records an early proposal for a CMS with multi-site publishing
and marketing automation. Its tracked source does not contain Grav, a CMS fork,
a tenant runtime, provisioning scripts, API endpoints, payment integration or an
installer. No passing build, test suite, deployment or paid-service capability is
established by this repository.

The earlier README described possible features as implemented software and linked
to placeholder badges, a placeholder logo and installation paths that do not
exist here. This documentation corrects that status; the earlier concept remains
available in Git history. Proposed prices and hosting/provider assumptions are
not current offers or verified infrastructure.

## Proposed direction

The proposed upstream is [Grav](https://github.com/getgrav/grav), the PHP flat-file
CMS maintained in the official `getgrav/grav` repository. Grav core uses the
[MIT license](https://github.com/getgrav/grav/blob/develop/LICENSE.txt).
No Grav source is included here, no upstream revision has been selected, and
MXMCMS is not an implemented Grav fork. Before importing code, select a reviewed
upstream revision, preserve its copyright/license notice, and review the licenses
of any included plugins, themes and dependencies.

Installable source, tenant isolation and authorization tests, reproducible setup,
operational rollback and reviewed CI evidence are prerequisites to claiming a
working platform or offering its CMS/tenant capabilities for paid delivery.
No implementation roadmap is committed by this status correction.

## Attribution and licensing status

Author/developer: Matthew X Murphy, https://MatthewxMurphy.com. Product attribution:
https://builtnotbegged.com. Original proposal credit: Bold Tee Hub; its original
text remains in Git history.

The original proposal identified MIT but supplied no LICENSE file. This change
preserves that recorded statement; it does not relicense prior material, add a
new license grant or select distribution terms for future custom software.
Grav's license above applies to Grav, not to an implementation shipped here.

## Maintenance

Source documentation only. There are no application tests or CI workflows to run
in this snapshot. The [shared engineering SOP](https://github.com/matthewxmurphy/developer-standards/blob/main/docs/ENGINEERING-SOP.md)
was reviewed for this change; engineering metadata, complete license/notices and
portable checker integration remain adoption gaps. CI/branch enforcement and
release/runtime acceptance have not been verified. The internal checker is not
vendored into this public proposal repository. No release version, server,
repository visibility or deployment is changed. Roll back this documentation
with a scoped Git revert while preserving later work.
