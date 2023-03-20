# Actions Permissions Test

Testing out using a workflow that has different permissions than the enterprise settings. The workflow simply tries to add an empty markdown file to the repo.

I expect the following tests to have the listed results. In each test, I am updating the enterprise and workflow permissions.

- [Enforcing policies for GitHub Actions in your enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-actions-in-your-enterprise)
- [Assigning permissions to jobs](https://docs.github.com/en/actions/using-jobs/assigning-permissions-to-jobs)

| Test | Enterprise Permissions                            | Workflow Permissions     | Result  | Actual Result |
| ---- | ------------------------------------------------- | ------------------------ | ------- | ------------- |
| 1    | Read repository contents and packages permissions | None                     | Failure | Failure       |
| 2    | Read repository contents and packages permissions | `contents: write`        | Failure | Success       |
| 3    | Read repository contents and packages permissions | `permissions: write-all` | Failure | Success       |
| 4    | Read and write permissions                        | None                     | Success | Success       |
| 5    | Read and write permissions                        | `contents: write`        | Success | Success       |
| 6    | Read and write permissions                        | `permissions: write-all` | Success |               |
