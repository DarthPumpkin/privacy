package(default_visibility = ["//visibility:public"])

licenses(["notice"])  # Apache 2.0

py_library(
    name = "dp_query",
    srcs = ["dp_query.py"],
)

py_library(
    name = "gaussian_query",
    srcs = ["gaussian_query.py"],
    deps = [
        ":dp_query",
        ":normalized_query",
        "//third_party/py/tensorflow",
    ],
)

py_test(
    name = "gaussian_query_test",
    srcs = ["gaussian_query_test.py"],
    deps = [
        ":gaussian_query",
        ":test_utils",
        "//third_party/py/absl/testing:parameterized",
        "//third_party/py/tensorflow",
    ],
)

py_library(
    name = "no_privacy_query",
    srcs = ["no_privacy_query.py"],
    deps = [
        ":dp_query",
        "//third_party/py/tensorflow",
    ],
)

py_test(
    name = "no_privacy_query_test",
    srcs = ["no_privacy_query_test.py"],
    deps = [
        ":no_privacy_query",
        ":test_utils",
        "//third_party/py/absl/testing:parameterized",
        "//third_party/py/tensorflow",
    ],
)

py_library(
    name = "normalized_query",
    srcs = ["normalized_query.py"],
    deps = [
        ":dp_query",
        "//third_party/py/tensorflow",
    ],
)

py_test(
    name = "normalized_query_test",
    srcs = ["normalized_query_test.py"],
    deps = [
        ":gaussian_query",
        ":normalized_query",
        ":test_utils",
        "//third_party/py/tensorflow",
    ],
)

py_library(
    name = "nested_query",
    srcs = ["nested_query.py"],
    deps = [
        ":dp_query",
        "//third_party/py/tensorflow",
    ],
)

py_test(
    name = "nested_query_test",
    srcs = ["nested_query_test.py"],
    deps = [
        ":gaussian_query",
        ":nested_query",
        ":test_utils",
        "//third_party/py/absl/testing:parameterized",
        "//third_party/py/tensorflow",
    ],
)

py_library(
    name = "test_utils",
    srcs = ["test_utils.py"],
    deps = [],
)
