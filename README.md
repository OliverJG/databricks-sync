# databricks-terraformer
Use Terraformer to backup restore and sync Databricks workspaces


# Common commands

```shell

# make; GIT_PYTHON_TRACE=full databricks-terraformer cluster-policies export --hcl --profile demo-aws -g git@github.com:stikkireddy/test-demo-repo.git --dry-run --delete
# make; GIT_PYTHON_TRACE=full databricks-terraformer cluster-policies export --hcl --profile demo-aws -g git@github.com:stikkireddy/demo-test-repo.git --delete --dry-run --tag
# make; GIT_PYTHON_TRACE=full databricks-terraformer notebooks export --hcl --notebook-path /Users/sri.tikkireddy@databricks.com/ --profile demo-aws -g git@github.com:stikkireddy/demo-test-repo.git --delete --dry-run
# make; GIT_PYTHON_TRACE=full databricks-terraformer dbfs export --hcl --dbfs-path dbfs:/databricks/init_scripts --profile demo-aws -g git@github.com:stikkireddy/test-demo-repo.git --delete --dry-run
# make; GIT_PYTHON_TRACE=full databricks-terraformer dbfs export --hcl --dbfs-path dbfs:/databricks/init_scripts --profile demo-aws -g git@github.com:stikkireddy/test-export-2.git --delete --dry-run
# make; GIT_PYTHON_TRACE=full databricks-terraformer import --profile azure-my-vnet -g git@github.com:stikkireddy/test-export-2.git --revision master --plan --artifact-dir tmp
make; GIT_PYTHON_TRACE=full databricks-terraformer import \
    --profile azure-my-vnet \
    -g git@github.com:stikkireddy/test-demo-repo.git \
    --revision 1988b8fdafdc40ccd0ebe27ad898844e676aac4e \
    --plan \
    --artifact-dir tmp \
    --apply
```

# Commands to run

```python

```

# Docker instructions

docker build -t 
docker run commands

```