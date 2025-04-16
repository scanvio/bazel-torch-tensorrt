load("@python_deps//:requirements.bzl", "requirement")
load("@rules_python//python:defs.bzl", "py_binary")

py_binary(
    name = "dummy_torch_tensorrt",
    srcs = ["dummy_torch_tensorrt.py"],
    deps = [
        requirement("torch-tensorrt"),
    ],
)
