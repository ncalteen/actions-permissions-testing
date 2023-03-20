# Test results

## Test 1

- **Enterprise setting:** Read repository contents and packages permissions
- **Workflow permissions:** None
- **Result:** Failure

```plain
remote: Write access to repository not granted.
fatal: unable to access 'https://github.com/enterprise-actions/actions-permissions-test/': The requested URL returned error: 403
```

## Test 2

- **Enterprise setting:** Read repository contents and packages permissions
- **Workflow permissions:** `contents: write`
- **Result:** Success

```plain
[main 70f672f] Adding test file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test-1-file.md
To https://github.com/enterprise-actions/actions-permissions-test
   628a5b8..70f672f  main -> main
```

## Test 3

- **Enterprise setting:** Read repository contents and packages permissions
- **Workflow permissions:** `permissions: write-all`
- **Result:** Failure

## Test 4

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** None
- **Result:** Success

## Test 5

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** `contents: write`
- **Result:** Success

## Test 6

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** `permissions: write-all`
- **Result:** Success
