# Wished Workflow

- **1** Edit Packages in Branch develop
- **2** Create Issue which represent the Version increase
- **3** Enter a comment in the before created issue like '/create release [branch]' 
     - **3.1** Increases the Version count in the packages that have updated
     - **3.2** Creates a new branch from [branch] and creates a Pull Request called after the new Version
     - **3.3** Tests the whole Project
- **4** Merge the Pull Request into master
     - **4.1** Checks if Tag with a version exists, if so exit
     - **4.2** Creates new Releases and Tags called after the version and package that changes
     - **4.3** Publishes Packages to npm that version has changed compared on the last release
  
@agile-ts/core@0.0.1
@agile-ts/multieditor@0.1.8-beta
   
  
# Options

## [Changeset][1]
- **1** Edit Packages in Branch develop
- **2** Type Command 'yarn changeset' in the wished [branch]
     - **2.1** It does list all branches in the cmd and shows which branches have changed
     - **2.2** Select the branches whose version has to be updated
     - **2.3** It gives you the option of (major, minor, patch) version bumps
     - **2.4** Enter a summary
     - **2.5** Confirm selection
     - This creates a file in the '.changeset' folder that includes all the changes wished version changes
- **3** Merge the [branch] into the master
     - **3.1** Creates a new branch based called 'changesets/release'
     - **3.2** Updates the version based on the generated file in '.changeset'
     - **3.3** Creates pull request back into the master
     - **3.4** 
     
## Custom
TODO

[1]: https://github.com/changesets/action


#### Resources
https://dev.to/stackdumper/setting-up-ci-for-microservices-in-monorepo-using-github-actions-5do2
https://github.community/t/basic-workflow-structure-for-a-monorepo/17093/5
https://github.com/zladovan/monorepo

