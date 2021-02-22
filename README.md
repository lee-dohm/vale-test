# Vale Linter Bug Reproduction

I'm running into what appears to be a bug with [vale][vale-linter]. This repo contains a minimal repro for the bug.

## Repro Steps

1. [Clone the repo](https://docs.github.com/en/github/using-git/which-remote-url-should-i-use)
1. Execute the command: `vale test.md`

**Expected:** No errors \
**Actual:** 1 error (see Erroneous Output below)

### Erroneous Output

```text
 test.md
 1:169  error  Use 'GitHub' instead of         Vale.Terms
               'github'.
```
