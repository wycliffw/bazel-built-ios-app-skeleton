workspace(name = "moneybook")

load(
    "@bazel_tools//tools/build_defs/repo:http.bzl",
    "http_archive",
)

http_archive(
    name = "build_bazel_rules_apple",
    sha256 = "90e3b5e8ff942be134e64a83499974203ea64797fd620eddeb71b3a8e1bff681",
    url = "https://github.com/bazelbuild/rules_apple/releases/download/1.1.2/rules_apple.1.1.2.tar.gz",
)

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)

apple_rules_dependencies()

load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

load(
    "@build_bazel_rules_swift//swift:extras.bzl",
    "swift_rules_extra_dependencies",
)

swift_rules_extra_dependencies()

load(
    "@build_bazel_apple_support//lib:repositories.bzl",
    "apple_support_dependencies",
)

apple_support_dependencies()

TULSI_COMMIT_HASH = "518f18da4948192c72074e07fa1dfe15858d40f4"

http_archive(
    name = "tulsi",
    sha256 = "92c89fcabfefc313dafea1cbc96c9f68d6f2025f2436ee11f7a4e4eb640fa151",
    strip_prefix = "tulsi-{0}".format(TULSI_COMMIT_HASH),
    url = "https://github.com/bazelbuild/tulsi/archive/{0}.tar.gz".format(TULSI_COMMIT_HASH),
)
