load("//tools:defs.bzl", "cc_binary", "cc_library", "gtest")

package(
    default_visibility = ["//:sandbox"],
    licenses = ["notice"],
)

cc_binary(
    name = "stat_test",
    testonly = 1,
    srcs = ["stat_test.cc"],
    deps = [
        gtest,
        ":fuse_base",
        "//test/util:test_main",
        "//test/util:test_util",
    ],
)

cc_library(
    name = "fuse_base",
    testonly = 1,
    srcs = ["fuse_base.cc"],
    hdrs = ["fuse_base.h"],
    deps = [
        gtest,
        "//test/util:posix_error",
        "//test/util:temp_path",
        "//test/util:test_util",
        "@com_google_absl//absl/strings:str_format",
    ],
)
