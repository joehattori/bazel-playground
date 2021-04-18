load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")
load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/joehattori/bazel-playground
gazelle(name = "gazelle")

go_library(
    name = "bazel-playground_lib",
    srcs = ["main.go"],
    importpath = "github.com/joehattori/bazel-playground",
    visibility = ["//visibility:private"],
    deps = ["@com_github_joehattori_wasmer_go//wasmer:wasmer"],
)

go_binary(
    name = "bazel-playground",
    embed = [":bazel-playground_lib"],
    visibility = ["//visibility:public"],
)
