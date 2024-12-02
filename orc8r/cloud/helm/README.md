Orchestrator Helm Charts
===
If you update any of the `magma/or8r/cloud/helm charts`, you will need to build your own helm repository for the orchestrator charts

Create a private GitHub repo to use as your Helm chart repo. We'll refer to this as GITHUB_REPO.


Then:

```
export GITHUB_REPO=<magma-charts>
export GITHUB_REPO_URL=https://github.com
export GITHUB_USERNAME=<github username>
export MAGMA_ROOT=<MAGMA_ROOT>
read -p "Enter Github Access Token: " GITHUB_ACCESS_TOKEN
export GITHUB_ACCESS_TOKEN
${MAGMA_ROOT}/orc8r/tools/helm/package.sh -d all
```
