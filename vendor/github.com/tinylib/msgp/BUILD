# BUILD file for vendor library tinylib/msgp
#
load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "msgp",
    srcs = [
        "msgp/advise_linux.go",
        "msgp/circular.go",
        "msgp/defs.go",
        "msgp/edit.go",
        "msgp/elsize.go",
        "msgp/errors.go",
        "msgp/extension.go",
        "msgp/file.go",
        "msgp/integers.go",
        "msgp/json.go",
        "msgp/json_bytes.go",
        "msgp/number.go",
        "msgp/read.go",
        "msgp/read_bytes.go",
        "msgp/size.go",
        "msgp/unsafe.go",
        "msgp/write.go",
        "msgp/write_bytes.go",
    ],
    visibility = ["//visibility:public"],
    deps = [ "//vendor/github.com/philhofer:fwd" ],
)

# The above configuration works for linux. For
# Appengine, windows, or others, the following files
# may need to replace the defaults:
#
#   "msgp/advise_other.go"
#   "msgp/appengine.go"
#   "msgp/file_port.go",
#

go_test(
    name = "msgp_test",
    srcs = [
        "msgp/edit_test.go",
        "msgp/extension_test.go",
        "msgp/floatbench_test.go",
        "msgp/json_bytes_test.go",
        "msgp/json_test.go",
        "msgp/number_test.go",
        "msgp/raw_test.go",
        "msgp/read_bytes_test.go",
        "msgp/read_test.go",
        "msgp/write_bytes_test.go",
        "msgp/write_test.go",
    ],
    library = ":msgp",
)

# TODO: To get this test package working we
# have to have go:generate rules work.
#
# go_test(
#    name = "msgp_other_test",
#    srcs = [
#        "msgp/defs_test.go",
#        "msgp/file_test.go",
#    ],
#    deps = [ ":msgp" ],
#)
