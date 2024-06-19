
![Build Status](https://github.com/bmir-radx/radx-ontology-workflows/actions/workflows/qc.yml/badge.svg)
# RADx Ontology Workflows

This repository specifies standard operating procedures for the creation, review, publication, and maintenance of ontologies in the RADx Data Hub.

We use the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit) to execute [standardized workflows](https://doi.org/10.1093/database/baac087) based on [best practices](https://obofoundry.org/principles/fp-000-summary.html) recommended by the [OBO Foundry](https://obofoundry.org/).

## Summary  

Every branch in this repository specifies a separate workflow and exemplifies the results of its execution.
This branch (**import**) specifies the workflow for working with ontology imports, e.g., adding/removing terms (for customizing import strategies, like changing the module type, see [here](https://bmir-radx.github.io/radx-ontology-workflows/odk-workflows/RepoManagement/).

.
All other workflows require an existing ontology repository and branch off **main**.

- [Ontology Creation](https://github.com/bmir-radx/radx-ontology-workflows?tab=readme-ov-file#ontology-creation): **main**
- [Contributing on GitHub](https://github.com/bmir-radx/radx-ontology-workflows/tree/github) : **github**
- [Manual Ontology Editing](https://github.com/bmir-radx/radx-ontology-workflows/tree/edit): **manual-edit** 
- [Pattern-Based Editing](https://github.com/bmir-radx/radx-ontology-workflows/tree/patterns): **patterns**
- [Ontology Import](https://github.com/bmir-radx/radx-ontology-workflows/tree/import): **import** (this branch)
- [Ontology Release](https://github.com/bmir-radx/radx-ontology-workflows/tree/release): **release**
- [Ontology Documentation](https://github.com/bmir-radx/radx-ontology-workflows/tree/documentation): **documentation**
- [Automated Testing](https://github.com/bmir-radx/radx-ontology-workflows/tree/testing): **testing**
- [Continuous Integration](https://github.com/bmir-radx/radx-ontology-workflows/tree/integration): **integration**


## Ontology Imports

Every imported ontology has, by default, a term file associated with it (located here: `src/ontology/imports/`).
For example, we configured [rxow-odk.yml](https://github.com/bmir-radx/radx-ontology-workflows/blob/main/src/ontology/rxow-odk.yaml) to import the Symptom Ontology (SYMP) (see line [19](https://github.com/bmir-radx/radx-ontology-workflows/blob/main/src/ontology/rxow-odk.yaml#L19)).
So, there is a `symp_terms.txt` in `src/ontology/imports/`.

1. Add/Remove a term: Here, we add `SYMP:0000567 (general symptom) to `symp_terms.txt`. 
2. Update the import  `sh run.sh make refresh-symp` (this runs the configured import strategy for SYMP, in this case, a bottom module for terms in `symp_terms.txt` is extracted and saved in `src/ontology/imports/symp_import.owl`.
3. Commit and create a pull request following the [Contributing on GitHub](https://github.com/bmir-radx/radx-ontology-workflows/tree/github) workflow.

You should now have a repository structure as shown in this branch (**import**).

For more details see the ODK [workflow for imports](https://bmir-radx.github.io/radx-ontology-workflows/odk-workflows/UpdateImports/).

## Acknowledgements

This ontology repository was created using the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit).
