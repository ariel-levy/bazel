load("@rules_java//java:defs.bzl", "java_library")

package(
    default_visibility = ["//src:__subpackages__"],
)

licenses(["notice"])  # Apache 2.0

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

java_library(
    name = "rendering",
    srcs = glob(["*.java"]),
    resources = [":template_files"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:syntax",
        "//src/main/java/com/google/devtools/build/lib/events",
        "//src/main/java/com/google/devtools/build/skydoc/rendering/proto:stardoc_output_java_proto",
        "//src/tools/starlark/java/com/google/devtools/starlark/common",
        "//third_party:apache_velocity",
        "//third_party:guava",
        "//third_party:jsr305",
    ],
)

filegroup(
    name = "template_files",
    srcs = glob(
        [
            "templates/*.vm",
        ],
        allow_empty = True,
    ),
)
