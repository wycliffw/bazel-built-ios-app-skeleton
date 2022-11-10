load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    name = "SkeletoniOSClasses",
    visibility = [ "//visibility:private" ],
    srcs = [
        "Skeleton-iOS/ContentView.swift",
        "Skeleton-iOS/SkeletonApp.swift"
    ]
)

ios_application(
    name = "Skeleton-iOS",
    visibility = ["//visibility:public"],
    app_icons = glob(["Skeleton-iOS/Assets.xcassets/**"]),
    bundle_id = "wycliffw.Skeleton",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = [":Skeleton-iOS/Info.plist"],
    minimum_os_version = "14.0",
    deps = [":SkeletoniOSClasses"],
)
