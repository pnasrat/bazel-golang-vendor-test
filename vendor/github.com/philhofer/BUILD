# BUILD file for vendor library github.com/philhofer/fwd

load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "fwd",
    srcs = [
	"fwd/reader.go",
	"fwd/writer.go",
	"fwd/writer_unsafe.go",
    ],
    visibility = ["//visibility:public"],
)

go_test(
    name = "fwd_test",
    srcs = [
	"fwd/reader_test.go",
	"fwd/writer_test.go",
    ],
    library = ":fwd",
)
