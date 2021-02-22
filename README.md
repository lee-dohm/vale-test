# Vale Linter Bug Reproduction

I'm running into what appears to be a bug with [vale][vale-linter]. This repo contains a minimal repro for the bug.

[vale-linter]: https://github.com/errata-ai/vale

## Explanation

We use Liquid tags in our Markdown documentation to dereference things like product names. I've configured vale to ignore any inline text in Liquid tags `{% ... %}` via the `TokenIgnores` configuration option. And, most of the time, that seems to exclude things. But occasionally, it appears that what shows up inside the Liquid tags is getting linted anyway? :man_shrugging:

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
