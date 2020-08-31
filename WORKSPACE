workspace(name = 'brpc_to_grpc')

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

http_archive(
    name = "com_github_grpc_grpc",
    url = "https://github.com/grpc/grpc/archive/v1.26.0.tar.gz",
    strip_prefix = "grpc-1.26.0",
)
load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
grpc_deps()

load("@com_github_grpc_grpc//bazel:grpc_extra_deps.bzl", "grpc_extra_deps")
grpc_extra_deps()

http_archive(
    name = "com_github_brpc_brpc",
    url = "https://github.com/apache/incubator-brpc/archive/0.9.7.tar.gz",
    strip_prefix = "incubator-brpc-0.9.7",
)

http_archive(
    name = "com_github_gflags_gflags",
    strip_prefix = "gflags-46f73f88b18aee341538c0dfc22b1710a6abedef",
    url = "https://github.com/gflags/gflags/archive/46f73f88b18aee341538c0dfc22b1710a6abedef.tar.gz",
)
bind(
    name = "gflags",
    actual = "@com_github_gflags_gflags//:gflags",
)

http_archive(
    name = "com_github_google_leveldb",
    build_file = "@com_github_brpc_brpc//:leveldb.BUILD",
    strip_prefix = "leveldb-a53934a3ae1244679f812d998a4f16f2c7f309a6",
    url = "https://github.com/google/leveldb/archive/a53934a3ae1244679f812d998a4f16f2c7f309a6.tar.gz"
)

http_archive(
    name = "com_github_google_glog",
    build_file = "@com_github_brpc_brpc//:glog.BUILD",
    strip_prefix = "glog-a6a166db069520dbbd653c97c2e5b12e08a8bb26",
    url = "https://github.com/google/glog/archive/a6a166db069520dbbd653c97c2e5b12e08a8bb26.tar.gz"
)
bind(
    name = "glog",
    actual = "@com_github_google_glog//:glog",
)
