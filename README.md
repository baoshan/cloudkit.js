# (Bug Fixed) cloudkit.js

If you encountered the same problem, this patch may be helpful.

## AUTH_PERSIST_ERROR

From a quick-n-dirty debugging, I find Apple use `path=` rather than `path=/`
when setting their cookie. Which will make the `setUpAuth` fail on pages from
different paths.
