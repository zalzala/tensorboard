load("//tensorboard/defs:defs.bzl", "tensorboard_webcomponent_library")
load("//tensorboard/defs:web.bzl", "tf_web_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])  # Apache 2.0

tf_web_library(
    name = "vz_histogram_timeseries",
    srcs = ["vz-histogram-timeseries.html"],
    path = "/vz-histogram-timeseries",
    deps = [
        "//tensorboard/components/tf_imports:d3",
        "//tensorboard/components/tf_imports:polymer",
    ],
)

tf_web_library(
    name = "demo",
    srcs = ["index.html"],
    path = "/vz-histogram-timeseries",
    deps = [
        ":vz_histogram_timeseries",
        "//tensorboard/components/tf_imports:polymer",
        "@org_polymer_iron_demo_helpers",
        "@org_polymer_paper_button",
        "@org_polymer_paper_styles",
    ],
)

tensorboard_webcomponent_library(
    name = "legacy",
    srcs = [":vz_histogram_timeseries"],
    visibility = ["//learning/vis/vz_elements/catalog:__pkg__"],
    destdir = "vz-histogram-timeseries",
    deps = [
        "//tensorboard/components/tf_imports:polymer_lib",
        "//tensorboard/components/tf_imports_google:lib",
    ],
)
