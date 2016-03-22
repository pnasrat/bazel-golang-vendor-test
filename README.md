This is an example of using bazel rules with the vendor
subdirectory introduced in go1.6.

This demonstrates some issues with the rules
deined by bazelbuild/rules_go


## Building vendored tests

Bazel should also be able to successfully run this:

```sh
$ bazel test //vendor/...
```

However this also fails.

Notice that there is a dependency from vendor/github.com/tinylib/msgp
to vendor/github.com/philhofer/fwd, and that the fwd tests all
run.

The msgp tests compile, but fail to link. It appears that
the library output is not referenced correctly when the following
command is run:

```sh
$ bazel test //vendor/... --verbose_failures
```

## Building all tests in the workspace.

Bazel should also be able to successfully run this:

```sh
$ git clone https://github.com/laramiel/bazel-golang-vendor-test
$ bazel test ...
```

However this fails as above.

See https://github.com/bazelbuild/bazel/issues/1072

