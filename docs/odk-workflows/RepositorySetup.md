# Ontology Creation Workflow

The ontology creation workflow specifies how you can quickly set up an ontology repository uing ODK.

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

After executing the steps above, you should end up with a repository structure similar to [this example](https://github.com/ckindermann/radx-ontology-workflows).
