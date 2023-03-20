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
- **Result:** Success

```plain
[main 497de15] Adding test file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test-3-file.md
To https://github.com/enterprise-actions/actions-permissions-test
   85a26fc..497de15  main -> main
```

## Test 4

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** None
- **Result:** Success

```plain
[main 980835f] Adding test file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test-4-file.md
To https://github.com/enterprise-actions/actions-permissions-test
   df18edf..980835f  main -> main
```

## Test 5

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** `contents: write`
- **Result:** Success

```plain
[main a192043] Adding test file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test-5-file.md
To https://github.com/enterprise-actions/actions-permissions-test
   d6f3700..a192043  main -> main
```

## Test 6

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** `permissions: write-all`
- **Result:** Success

```plain
[main 56071fe] Adding test file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test-6-file.md
To https://github.com/enterprise-actions/actions-permissions-test
   c306da0..56071fe  main -> main
```

## Test 7

- **Enterprise setting:** Read repository contents and packages permissions
- **Workflow permissions:** `statuses: write`
- **Result:** Failure

```plain
Error: fatal: repository 'https://github.com/enterprise-actions/actions-permissions-test/' not found
The process '/usr/bin/git' failed with exit code 128
```

## Test 8

- **Enterprise setting:** Read and write permissions
- **Workflow permissions:** `statuses: write`
- **Result:** Failure

```plain
Error: fatal: repository 'https://github.com/enterprise-actions/actions-permissions-test/' not found
The process '/usr/bin/git' failed with exit code 128
```
