![Build Status](https://github.com/bmir-radx/radx-ontology-workflows/actions/workflows/qc.yml/badge.svg)
# RADx Ontology Workflows

Description: This repository specifies standard operating procedures for the creation, review, publication, and maintenance of ontologies in the RADx Data Hub.

We use the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit) to execute [standardized workflows](https://doi.org/10.1093/database/baac087) based on [best practices](https://obofoundry.org/principles/fp-000-summary.html) recommended by the [OBO Foundry](https://obofoundry.org/).

## Summary  

Every branch in this repository specifies a separate workflow and exemplifies the results of its execution.

This branch (**github**) specifies the workflow for making changes in an ontology repository hosted on GitHub.

- [Ontology Creation](https://github.com/bmir-radx/radx-ontology-workflows?tab=readme-ov-file#ontology-creation): **main** 
- [Contributing on GitHub](todo.fix.me) : **github** (this branch)
- [Manual Ontology Editing](todo.fix.me): **manual-edit**
- [Pattern-Based Editing](todo.fix.me): **pattern**
- [Ontology Import](todo.fix.me): **import**
- [Ontology Release](todo.fix.me): **release**
- [Ontology Documentation](todo.fix.me): **documentation**
- [Automated Testing](todo.fix.me): **testing**
- [Continuous Integration](todo.fix.me): **integration**

## Contributing on GitHub

1. **Create an issue**: GitHub Issues are used to *plan* and *discuss* future work as well as to track progress. Technical details on how to create issues can be found [here](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).

2. **Update target branch**: `git pull` It is good practice to keep up to date with upstream changes in the repository. 

3. **Create feature branch**: `git checkout -b issueNumberAndTitle` Any change to an online repository needs to be submitted via a pull request (see step 5 below). So, any work needs to be performed in a dedicated feature branch (do **not** use the branch *main* or *dev* as a feature branch. You can inspect existing branches with the command `git branch` and you should check whether the repository reserves certain branches for specific purposes). More information about creating branches can be found [here](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-a-branch-for-an-issue).
 
4. **Make your changes**: Changes should be small and each change should be recorded with a dedicated `git commit -m "change description"`.

5. **Push changes**: `git push -u origin issueNumberAndTitle` To contribute your changes to an upstream repository, you need to push your feature branch.

6. **Create a pull request** After pushing a feature branch to an upstream repository, you can create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) so that your work can be integrated into the *main* branch. It is good practice to link a pull request to  the issue you created in step 1. Technical information on how to do this can be found [here](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue).

7. **Request review**: After creatig a pull request, you want to get a sanity check and possibly feedback on your submitted work. It is good practice to request a review from one of the maintainers or main contributers of the repository.

8. **Merge**: A pull request should be integrated into the *main* branch by a maintainer of the repository who makes sure that the pull request has been reviewed, the submitted changes are adequate, and all quality control measures, i.e., tests, style guidelines, quality control checks, coding conventions, etc, are satisfied. After a pull request is merged in, the feature branch will be deleted and the corresponding issue will be marked as closed.

For more information on tracking changes with issues, see [GitHub docs](https://docs.github.com/en/issues/tracking-your-work-with-issues).

## Acknowledgements

This ontology repository was created using the [Ontology Development Kit (ODK)](https://github.com/INCATools/ontology-development-kit).
