load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_github_ali5h_rules_pip",
    strip_prefix = "rules_pip-3.0.0",
    urls = ["https://github.com/ali5h/rules_pip/archive/3.0.0.tar.gz"],
)

load("@com_github_ali5h_rules_pip//:defs.bzl", "pip_import")

pip_import(
  name = "pip_deps",
  requirements = "//:requirements.lock",
  python_interpreter="python3",
)

load("@pip_deps//:requirements.bzl", "pip_install")
pip_install()
