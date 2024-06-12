
![Build Status](https://github.com/ckindermann/radx-ontology-workflows/actions/workflows/qc.yml/badge.svg)
# RADx Ontology Workflows

Description: This repository specifies standard operating procedures for the creation, review, publication, and maintenance of ontologies in the RADx Data Hub.

We use the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit) to execute [standardized workflows](https://doi.org/10.1093/database/baac087) based on [best practices](https://obofoundry.org/principles/fp-000-summary.html) recommended by the [OBO Foundry](https://obofoundry.org/).

## Summary  

Every branch in this repository specifies a separate workflow and exemplifies the results of its execution.

Every branch in this repository specifies a separate workflow and exemplifies the results of its execution.
This branch (**main**) specifies the workflow for creating a new ontology repository.
All other workflows require an existing ontology repository and branch off **main**.

- [Ontology Creation](https://github.com/ckindermann/radx-ontology-workflows?tab=readme-ov-file#ontology-creation): **main** (this branch) 
- [Contributing on GitHub](https://github.com/ckindermann/radx-ontology-workflows/tree/github) : **github**
- [Manual Ontology Editing](https://github.com/ckindermann/radx-ontology-workflows/tree/edit): **manual-edit** 
- [Pattern-Based Editing](https://github.com/ckindermann/radx-ontology-workflows/tree/patterns): **patterns**
- [Ontology Import](https://github.com/ckindermann/radx-ontology-workflows/tree/import): **import**
- [Ontology Release](https://github.com/ckindermann/radx-ontology-workflows/tree/release): **release**
- [Ontology Documentation](https://github.com/ckindermann/radx-ontology-workflows/tree/documentation): **documentation**
- [Automated Testing](https://github.com/ckindermann/radx-ontology-workflows/tree/testing): **testing**
- [Continuous Integration](https://github.com/ckindermann/radx-ontology-workflows/tree/integration): **integration**


## Ontology Creation

1. Create a new folder for the ontology: `mkdir ontology-name` (in this example, we use `radx-ontology-workflows` as an example name)
2. Navigate into the folder: `cd ontology-name`
3. Download the ODK seed script: `wget https://raw.githubusercontent.com/INCATools/ontology-development-kit/master/seed-via-docker.sh`
4. Download the RADx config file: `wget https://raw.githubusercontent.com/ckindermann/radx-ontology-workflows/main/src/ontology/rxow-odk.yaml`
    1. Change the value of `id` from `rdow` to an acronym of your ontology (if possible, no less than 4 characters)
    2. Change the value of `title` from `RADx Ontology Workflows` to a suitable title of your ontology
    3. Change the value of `github_org` from `ckindermann` to your GitHub organization
    4. Change the value of `uribase` from `https://github.com/bmir-radx` to the preferred base URI of your ontology
5. Generate the repository: `sh seed-via-docker.sh -c -C rxow-odk.yaml` --- the results will be in the folder `./target/`
6. Push to GitHub: Follow the instructions printed by `seed-via-docker.sh` when it finishes successfully

You should now have a repository structure as shown in this branch (**main**).
Next, you should familiarize yourself with the general workflow for contributing to an ontology repository hosted on GitHub: [Contributing on GitHub](todo.fix.me) (**github**).

For more details see the ODK [tutorial for setting up an ODK repository](https://oboacademy.github.io/obook/tutorial/setting-up-project-odk/).

## Acknowledgements

This ontology repository was created using the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit).
