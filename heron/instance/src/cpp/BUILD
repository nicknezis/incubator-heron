load("@rules_cc//cc:defs.bzl", "cc_binary")

package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "heron-cpp-instance",
    srcs = [
        "boltimpl/bolt-instance.cpp",
        "boltimpl/bolt-instance.h",
        "boltimpl/bolt-metrics.cpp",
        "boltimpl/bolt-metrics.h",
        "boltimpl/bolt-output-collector-impl.cpp",
        "boltimpl/bolt-output-collector-impl.h",
        "boltimpl/tick-tuple.cpp",
        "boltimpl/tick-tuple.h",
        "boltimpl/tuple-impl.cpp",
        "boltimpl/tuple-impl.h",
        "gateway/gateway.cpp",
        "gateway/gateway.h",
        "gateway/gateway-metrics.cpp",
        "gateway/gateway-metrics.h",
        "gateway/stmgr-client.cpp",
        "gateway/stmgr-client.h",
        "instance-main.cpp",
        "executor/imetrics-registrar-impl.cpp",
        "executor/imetrics-registrar-impl.h",
        "executor/instance-base.h",
        "executor/outgoing-tuple-collection.cpp",
        "executor/outgoing-tuple-collection.h",
        "executor/executor.cpp",
        "executor/executor.h",
        "executor/task-context-impl.cpp",
        "executor/task-context-impl.h",
        "spoutimpl/root-tuple-info.h",
        "spoutimpl/spout-instance.cpp",
        "spoutimpl/spout-instance.h",
        "spoutimpl/spout-metrics.cpp",
        "spoutimpl/spout-metrics.h",
        "spoutimpl/spout-output-collector-impl.cpp",
        "spoutimpl/spout-output-collector-impl.h",
        "utils/communicator.h",
        "utils/notifying-communicator.h",
    ],
    copts = [
        "-Iheron",
        "-Iheron/instance/src/cpp",
        "-Iheron/api/src/cpp",
        "-Iheron/common/src/cpp",
        "-I$(GENDIR)/heron",
        "-I$(GENDIR)/heron/common/src/cpp",
    ],
    linkopts = ["-ldl"],
    linkstatic = 1,
    deps = [
        "//heron/api/src/cpp:cxx-api",
        "//heron/common/src/cpp/basics:basics-cxx",
        "//heron/common/src/cpp/config:config-cxx",
        "//heron/common/src/cpp/metrics:metrics-cxx",
        "//heron/common/src/cpp/network:network-cxx",
        "//heron/proto:proto-cxx",
        "@com_github_jbeder_yaml_cpp//:yaml-cxx",
    ],
)
