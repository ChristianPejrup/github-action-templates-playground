# Github actions repository

Repository for shared Github actions templates and shared repository configuration synchronization.

## Features

### Workflow sharing

Demonstration of how workflows can be shared with another repository.

[template1.yaml](.github/workflows/template1.yml)
[template2.yaml](.github/workflows/template1.yml)

### Workflow nesting

Shows how workflows are nested inside the same repository and shared.

[template1and2.yaml](.github/workflows/template1and2.yml)

### Template versioning

Shows a simple way of versioning templates (using tags) that can be used to reference the workflows from other repositories. This allows for more flexibility when updating workflows that others are depending on.

Versioning uses the [conventional commits](http://www.conventionalcommits.org) to determine the version.

[GitVersion](https://github.com/GitTools/actions) action is used to resolve the next version.

[rickstaa/action-create-tag](https://github.com/rickstaa/action-create-tag) is used to set the tag (this supports force push).

Two tags are maintained using this model.

* major.minor (tag is never changed)
* major (tag is updated when ever a new minor version is created)

(this model might have problems if the user uses the conventional commit approach with patches as major.minor is intended to be static - it is however easy to change, but i thought i would keep the sample simple)

[tset-template-version.yaml](.github/workflows/set-template-version.yml)

testing new feature