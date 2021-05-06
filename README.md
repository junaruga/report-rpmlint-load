# report-rpmlint-load

We can build from the spec file.

```
$ fedpkg --release rawhide srpm
$ mock *.src.rpm
```

But the `rpmlint` fails to parse the `load` builtin macro [1] in the spec file.

```
$ rpmlint test.spec
test.spec: E: specfile-error error: test.spec: line 9: failed to load macro file /tmp/rpmlint.test.spec.qx47qrtr/macros.test
test.spec: E: specfile-error error: query of specfile test.spec failed, can't parse
0 packages and 1 specfiles checked; 2 errors, 0 warnings.
```

## References

* [1] http://rpm.org/user_doc/macros.html
