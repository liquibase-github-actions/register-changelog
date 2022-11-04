# Liquibase Register Changelog Action
Official GitHub Action to run Liquibase Register Changelog in your GitHub Action Workflow. For more information on how register changelog works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Register Changelog
Register the changelog with a Liquibase Hub project
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/register-changelog@v4.17.1
  with:
    # The root changelog
    # string
    # Required
    changelogFile: ""

    # Used to identify the specific Project in which to record or extract data at Liquibase Hub. Available in your Liquibase Hub account at https://hub.liquibase.com.
    # string
    # Optional
    hubProjectId: ""

    # The Hub project name
    # string
    # Optional
    hubProjectName: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase register changelog action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/register-changelog@v4.17.1
    with:
      changelogFile: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
