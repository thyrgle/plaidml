load("//bzl:plaidml.bzl", "plaidml_cc_library", "plaidml_cc_test", "plaidml_proto_library")

plaidml_cc_library(
    name = "file",
    srcs = [
        "eventlog.cc",
        "eventlog.h",
        "factory.cc",
    ],
    hdrs = [
        "factory.h",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":proto_cc",
        "//base/context",
        "//base/util",
        "@com_google_protobuf//:protobuf",
    ],
    alwayslink = 1,
)

plaidml_proto_library(
    name = "proto",
    srcs = [
        "eventlog.proto",
    ],
    visibility = ["//visibility:public"],
    deps = ["//base/context:proto"],
)

plaidml_cc_test(
    name = "eventlog_test",
    srcs = ["eventlog_test.cc"],
    deps = [
        ":file",
        "//testing:matchers",
    ],
)
