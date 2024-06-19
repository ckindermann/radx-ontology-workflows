
![Build Status](https://github.com/bmir-radx/radx-ontology-workflows/actions/workflows/qc.yml/badge.svg)
# RADx Ontology Workflows

This repository specifies standard operating procedures for the creation, review, publication, and maintenance of ontologies in the RADx Data Hub.

We use the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit) to execute [standardized workflows](https://doi.org/10.1093/database/baac087) based on [best practices](https://obofoundry.org/principles/fp-000-summary.html) recommended by the [OBO Foundry](https://obofoundry.org/).

## Summary  

Every branch in this repository specifies a separate workflow and exemplifies the results of its execution.
This branch (**release**) specifies the workflow for releasing a new version of the ontology.
All other workflows require an existing ontology repository and branch off **main**.

- [Ontology Creation](https://github.com/bmir-radx/radx-ontology-workflows?tab=readme-ov-file#ontology-creation): **main**
- [Contributing on GitHub](https://github.com/bmir-radx/radx-ontology-workflows/tree/github) : **github**
- [Manual Ontology Editing](https://github.com/bmir-radx/radx-ontology-workflows/tree/edit): **manual-edit** 
- [Pattern-Based Editing](https://github.com/bmir-radx/radx-ontology-workflows/tree/patterns): **patterns**
- [Ontology Import](https://github.com/bmir-radx/radx-ontology-workflows/tree/import): **import**
- [Ontology Release](https://github.com/bmir-radx/radx-ontology-workflows/tree/release): **release** (this branch)
- [Ontology Documentation](https://github.com/bmir-radx/radx-ontology-workflows/tree/documentation): **documentation**
- [Automated Testing](https://github.com/bmir-radx/radx-ontology-workflows/tree/testing): **testing**
- [Continuous Integration](https://github.com/bmir-radx/radx-ontology-workflows/tree/integration): **integration**


## Ontology Release

1. Checkout a new branch (e.g. git checkout -b release-2024-01-01)
2. Navigate to the ontology folder: `cd rxow/src/ontology`
3. Run release pipeline: `sh run.sh make prepare_release -B` (This will create all the specified release targets at the top level of your repository) 
4. Commit and create a pull request following the [Contributing on GitHub](https://github.com/bmir-radx/radx-ontology-workflows/tree/github) workflow.

For more details see the ODK [workflow for creating releases](https://bmir-radx.github.io/radx-ontology-workflows/odk-workflows/ReleaseWorkflow/).

## Acknowledgements

This ontology repository was created using the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit).
