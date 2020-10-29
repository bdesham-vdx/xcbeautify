load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

git_repository(
    name = "build_bazel_rules_swift",
    commit = "6408d85da799ec2af053c4e2883dce3ce6d30f08",
    remote = "https://github.com/bazelbuild/rules_swift.git",
)

load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

load(
    "@com_google_protobuf//:protobuf_deps.bzl",
    "protobuf_deps",
)

protobuf_deps()

http_archive(
    name = "Colorizer",
    build_file = "//external:External.BUILD",
    sha256 = "b4bfc4d4172e8ee8be1bbfc39379b821cc93f2551df12ceb95fe5231513058ed",
    strip_prefix = "Colorizer-0.2.0",
    url = "https://github.com/getGuaka/Colorizer/archive/0.2.0.zip",
)

http_archive(
    name = "ArgumentParser",
    build_file = "//external:External.BUILD",
    sha256 = "3ed7c5f36ebbd6436221348b4c56f51a23434fdb0955236c291e29bd6f19499b",
    strip_prefix = "swift-argument-parser-0.3.1",
    url = "https://github.com/apple/swift-argument-parser/archive/0.3.1.zip",
)
