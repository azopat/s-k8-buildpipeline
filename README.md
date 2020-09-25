# s-k8-buildpipeline

If you are working on this project via Upwork, see also our [Upwork Rules of Engagement](https://github.com/filetrust/Open-Source/blob/master/upwork/rules-of-engagement.md)

### Project brief

**Objective**: Standardize a set of common CI Pipeline patterns that all projects will follow  using GitHub Actions

- The CI pipeline will inherit principles from [CI/CD for GitHub Repository guideline] https://engineering.glasswallsolutions.com/docs/guides/ci-cd-pipeline 

- It will implement feaseible security checks outlined in [Abridged Amendment 3 ] (https://github.com/filetrust/program-icap/wiki/Abridged-Amendment-3)

**Process Flow:**
<br><img src="../img/CI-CD.png" alt="CI CD pipeline" width="650"/><br>
source : CI/CD for GitHub Repository guideline from Glasswall Engineering.

	###Gated Build
AGated build which will build our code and run tests on pull requests
On the GitHub repo, go to Actions > New workflow > set up a workflow will be done by the respective repo editors.
Name the file 'gated.yml'
The Gated file code from the this repo will be inherited by respective repo.
Standardize to trigger unit tests, publishing code coverage. 
Start commit > create new branch and start a pull request

	###CI Build
Next step is to set-up a CI build which will deploy code to a QA environment, run tests, and merge to the master branch if successful.

On the GitHub repo, go to Actions > New workflow > set up a workflow will be done by the respective repo editors.
Name the file 'ci.yml'
The CI file code from the this repo will be inherited by respective repo.
Standardize to trigger unit tests, publishing code coverage, environment and deployment.
Add any needed secrets (Access Ids and key) to the repo settings.
Start commit > create new branch and start a pull request

	###Deploy Build
Next step is to set-up a Deploy build which will deploy our code to a Stage environment, run tests, and deploy to product if successful.

On the GitHub repo, go to Actions > New workflow > set up a workflow will be done by the respective repo editors.
Name the file 'deploy.yml'
The Deploy file code from the this repo will be inherited by respective repo.
Make any changes specific to your project (deployment, environment, build steps, tests used)
Add any needed secrets (Access Ids and key) to the repo settings.
Start commit > create new branch and start a pull request


