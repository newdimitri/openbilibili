package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
    "go_library",
)

go_test(
    name = "go_default_test",
    srcs = ["service_test.go"],
    embed = [":go_default_library"],
    rundir = ".",
    tags = ["automanaged"],
    deps = [
        "//app/interface/main/app-player/conf:go_default_library",
        "//app/interface/main/app-player/model:go_default_library",
        "//vendor/github.com/smartystreets/goconvey/convey:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "bnj.go",
        "service.go",
    ],
    importpath = "go-common/app/interface/main/app-player/service",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/interface/main/app-player/conf:go_default_library",
        "//app/interface/main/app-player/dao:go_default_library",
        "//app/interface/main/app-player/dao/account:go_default_library",
        "//app/interface/main/app-player/dao/archive:go_default_library",
        "//app/interface/main/app-player/dao/resource:go_default_library",
        "//app/interface/main/app-player/dao/ugcpay:go_default_library",
        "//app/interface/main/app-player/model:go_default_library",
        "//app/interface/main/app-player/model/archive:go_default_library",
        "//app/service/main/account/api:go_default_library",
        "//app/service/main/ugcpay/api/grpc/v1:go_default_library",
        "//library/ecode:go_default_library",
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
