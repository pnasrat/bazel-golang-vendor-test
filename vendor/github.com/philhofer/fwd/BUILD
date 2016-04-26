# BUILD file for vendor library github.com/philhofer/fwd

load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test", "go_prefix")

go_prefix("github.com/phihofer/fwd")

go_library(
    name = "go_default_library",
    srcs = [
	"reader.go",
	"writer.go",
	"writer_unsafe.go",
    ],
    visibility = ["//visibility:public"],
)

go_test(
    name = "fwd_test",
    srcs = [
	"reader_test.go",
	"writer_test.go",
    ],
    library = ":go_default_library",
)
