package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
    "go_library",
)

go_test(
    name = "go_default_test",
    srcs = ["show_test.go"],
    embed = [":go_default_library"],
    rundir = ".",
    tags = ["automanaged"],
    deps = [
        "//app/interface/main/app-show/conf:go_default_library",
        "//vendor/github.com/smartystreets/goconvey/convey:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "dao.go",
        "redis.go",
        "show.go",
    ],
    importpath = "go-common/app/interface/main/app-show/dao/show",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/interface/main/app-show/conf:go_default_library",
        "//app/interface/main/app-show/model/show:go_default_library",
        "//library/cache/redis:go_default_library",
        "//library/database/sql:go_default_library",
        "//library/log:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
