load("//tensorboard/defs:web.bzl", "tf_web_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])  # Apache 2.0

# bazel run //tensorboard/plugins/graph/tf_graph/demo
tf_web_library(
    name = "demo",
    srcs = ["index.html"] + glob(["data/**"]),
    path = "/tf-graph/demo",
    deps = [
        "//tensorboard/components/tf_imports:polymer",
        "//tensorboard/plugins/graph/tf_graph",
        "//tensorboard/plugins/graph/tf_graph_common",
        "//tensorboard/plugins/graph/tf_graph_loader",
        "@org_polymer_iron_demo_helpers",
        "@org_polymer_paper_styles",
    ],
)
