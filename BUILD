load("@rules_python//python:defs.bzl", "py_binary", "py_library")
load("@rules_python//python:proto.bzl", "py_proto_library")

proto_library(
    name = "dummy_pb2",
    srcs = ["dummy.proto"],
)

py_proto_library(
    name = "dummy_py_pb2",
    deps = [":dummy_pb2"],
)

py_library(
    name = "lib",
    srcs = ["lib.py"],
    visibility = ["//visibility:public"],
    deps = [":dummy_py_pb2"],
)

py_binary(
    name = "main",
    srcs = ["main.py"],
    visibility = ["//visibility:public"],
    deps = [":lib"],
)
