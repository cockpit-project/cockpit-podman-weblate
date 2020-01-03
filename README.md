# Weblate helper repository for cockpit-podman

Repository for syncing Weblate translation. If you are not a bot, please ignore this repository.

## I want to translate cockpit-podman plugin
Great! Please do so in https://translate.stg.fedoraproject.org/projects/cockpit-podman

## I found wrong translation
You can fix it in https://translate.stg.fedoraproject.org/projects/cockpit-podman directly, but if you don't want
to register and become translator, please open issue in https://github.com/cockpit-project/cockpit-podman/ and maintainers
will fix it in Weblate directly.

## Then what is this repository good for?
Weblate introduced a "push" workflow - meaning that project keeps source document (`.pot` file) upstream and Weblate has hooks
with which it controls, if this file was updates. When upstream updates `.pot` file, Weblate also updates this source document
for translators. When strings are translated, Weblate pushes these changes into upstream (or sends pull request).
Cockpit team does not want to keep `.pot` file upstream, also we are not eager with getting loads of commits and pull requests
from Weblate. We prefer "pull" workflow - meaning that we regularly update `.pot` file and also download current translated
strings - on which we firstly run tests and only then allow it in our codebase.
This repository acts like intermediate step - we update here `.pot` file and Weblate pushes here translations. We then take
translation files from this repository, tests them and land into the project itself.
All is done by our and Weblate bots, so there should be no manual interaction.
