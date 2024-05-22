# Managing your ODK repository

## Updating your ODK repository

Your ODK repositories configuration is managed in `src/ontology/rxow-odk.yaml`. The [ODK Project Configuration Schema](https://github.com/INCATools/ontology-development-kit/blob/master/docs/project-schema.md) defines all possible parameters that can be used in this config YAML. Once you have made your changes, you can run the following to apply your changes to the repository:


```
sh run.sh make update_repo
```

There are a large number of options that can be set to configure your ODK, but we will only discuss a few of them here.

NOTE for Windows users:

You may get a cryptic failure such as `Set Illegal Option -` if the update script located in `src/scripts/update_repo.sh` 
was saved using Windows Line endings. These need to change to unix line endings. In Notepad++, for example, you can 
click on Edit->EOL Conversion->Unix LF to change this.

## Managing imports

You can use the update repository workflow described on this page to perform the following operations to your imports:

1. Add a new import
2. Modify an existing import
3. Remove an import you no longer want
4. Customise an import

We will discuss all these workflows in the following.
