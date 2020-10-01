Initializes a Cloudify CLI profile.

Use this Action if your job actually requires a CLI profile; for example - when using the Cloudify CLI
(`cfy`) directly. `cfyci` commands create a CLI profile automatically.

# Environment Variables

This Action uses the Cloudify Profile environment variables described in the official
Cloudify documentation (see [More Information](#more-information) below).

# Example

```yaml
jobs:
  test_job:
    steps:
      - name: Initialize Profile
        uses: cloudify-cosmo/init-action@v1.0
```

# More Information

Refer to [Cloudify CI/CD Integration](https://docs.cloudify.co/latest/working_with/integration/) for additional information about
Cloudify's integration with CI/CD tools.
