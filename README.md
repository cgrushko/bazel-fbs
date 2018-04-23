# bazel-fbs
Rules for building projects using foreign build systems inside Bazel projects.

## ./configure && make

**NOTE**: this requires building Bazel from head after https://github.com/bazelbuild/bazel/commit/060b1624e4d64dbdbeb375f9a55a3da9bd055a54

Example:

```bash
$ devbazel build  //:async_dns //:libevent_echosrv1
...
ls bazel-bin/async_dns bazel-bin/libevent_echosrv1
```

* In `WORKSPACE`, we use a `new_http_archive` to download tarballs with the libraries we use.
* In `BUILD`, we instantiate a `cc_configure_make_library` macro which behaves similarly to a `cc_library`, which can then be used in a C++ rule (`cc_binary` in this case).
