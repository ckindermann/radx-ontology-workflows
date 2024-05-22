# RADx Ontology Workflows

We use the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit) to execute [standardized workflows](https://doi.org/10.1093/database/baac087) based on [best practices](https://obofoundry.org/principles/fp-000-summary.html) recommended by the [OBO Foundry](https://obofoundry.org/).


## Ontology Developer Roles

In the context of ontologies for the RADx Data Hub, we distinguish between *two* roles of ontology developers: ontology *maintainers* and ontology *curators*.


### Ontology Maintainers

Ontology maintainers are responsible for

1. [Setting up ontology repositories](RepositorySetup.md),
2. [Managing documentation](ManageDocumentation.md), 
3. [Managing ontology imports](SettingUpImports.md)
4. Managing pattern-based axiom generation pipelines,
5. [Managing ontology quality control measures](ManageAutomatedTest.md),
6. [Merging pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request),
7. [Creating ontology releases](ReleaseWorkflow.md),

### Ontology Curators

Ontology curators are primarily concerned with the development of the *content* of an ontology.
This means that ontology curators will only perform actions that result in changes to the ontology's content, i.e, axioms. There are only three ways in which an ontology curator can contribute:

1. [Authoring axioms directly](EditorsWorkflow.md),
2. [Requesting terms/axioms to be imported from external ontologies](UpdateImports.md), 
3. Authoring axioms via patterns


## Config Workflows

- [Updating your ODK Repository](RepoManagement.md)
- [Setting up Docker for ODK](SettingUpDockerForODK.md)
