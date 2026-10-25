# Installation

Install official MapleMCP beta builds from:

https://maplemcp.ca/downloads

## Windows

Use the current MapleMCP Windows installer from the downloads page.

Existing installations intentionally preserve compatibility-sensitive MapleRemote service/task/path identifiers during upgrades.

## Linux

Use the current Linux installer from the downloads page. Review shell installers before running them with elevated privileges.

**Known upgrade compatibility issue (reported 2026-10-24):** the advertised 0.2.63-beta Linux Pro **sequence 247** failed to upgrade an existing Linux Pro **sequence 167** installation. The original service and enrollment were preserved through rollback. Do not force that specific old-to-new upgrade, disable immutable-directory safeguards, or globally change /tmp permissions. Check for a newly signed fixed successor and verified upgrade/rollback acceptance before upgrading an older Pro installation.

## Browser Companion

Browser Companion is distributed with supported MapleMCP release channels and is paired locally with the endpoint.

## Mobile

Mobile support is distributed through the supported beta channel and requires the operating-system permissions appropriate to the enabled capabilities.

## Source builds

MapleMCP implementation source is not published in this repository. Official supported builds are distributed through MapleMCP release/download channels.
