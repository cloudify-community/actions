Creates an environment by uploading a blueprint, creating a deployment and running the `install` workflow.

# Environment Variables

This Action uses the Cloudify Profile environment variables described in the official
Cloudify documentation (see [More Information](#more-information) below).

# Inputs

(Certain commonly-used inputs are documented in our official website; see [More Information](#more-information) below)

Name | Description
-----|------------
`blueprint` | Path/URL to blueprint (YAML file or archive file)
`inputs-file` | Path to YAML/JSON inputs file

# Example

```yaml
jobs:
  test_job:
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Create environment
        uses: cloudify-cosmo/create-environment-action@v1.0
        with:
          environment-name: "test-simple-$GITHUB_RUN_ID"
          blueprint: simple/blueprint.yaml
          outputs-file: env-data.json
```

The blueprint file is taken from the repository that was checked out during the "Checkout code" step.
 
# More Information

Refer to [Cloudify CI/CD Integration](https://docs.cloudify.co/latest/working_with/integration/) for additional information about
Cloudify's integration with CI/CD tools.
