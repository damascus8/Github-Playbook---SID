# Is this repository supposed to be named `.github`?

No. This Playbook is designed for people to read and manually apply to any repository. A public repository named `.github` has a special GitHub use: supported community health files can act as defaults for other repositories owned by the same account when those repositories do not supply their own files. The exact behavior depends on account/repository eligibility and supported file types.

That special behavior does **not** automatically apply every rule in this Playbook. In particular, it does not globally enforce CI workflows, Dependabot configuration, branch-protection settings, code-scanning workflows, or application-specific documentation. Those require separate setup in each repository unless you build an appropriate organization-level mechanism.

For this Playbook, keep the repository name descriptive, such as `github-standard-playbook`. That makes the intent clear: a handbook and template library for humans to adopt.

Official reference: [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).
