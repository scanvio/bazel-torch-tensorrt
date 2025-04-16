# Use torch_tensorrt in Bazel

This repo is for reproducing an issue with Bazel ([rules-python](https://github.com/bazel-contrib/rules_python)) and the [torch_tensorrt](https://github.com/pytorch/TensorRT) Python package.

To reproduce the issue run the following on a Linux x86/64 machine

```bash
bazel run //:dummy_torch_tensorrt
```

This will execute a `py_binary` target that tries to import `torch_tensorrt` and prints it's version. Unfortunately, the import already fails with the following error:

```text
Traceback (most recent call last):
  File "***redacted***/execroot/_main/bazel-out/k8-fastbuild/bin/dummy_torch_tensorrt.runfiles/_main/dummy_torch_tensorrt.py", line 1, in <module>
    import torch_tensorrt
ModuleNotFoundError: No module named 'torch_tensorrt'
```
