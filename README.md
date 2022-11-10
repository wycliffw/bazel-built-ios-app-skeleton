# Skeleton bazel-built iOS Application

Use this skeleton application to quickly setup and start working on a new bazel-built iOS application.

## Usage
Clone the repository and cd into it
```
% git clone https://github.com/wycliffw/bazel-built-ios-app-skeleton.git skeleton
% cd skeleton
```

To run the application on a Simulator, you can run this commands
```
% bazel run //:Skeleton-iOS
```

To generate xcode project
```
bazel run -- @tulsi//:tulsi -- \
    --genconfig "`pwd`/Skeleton-iOS.tulsiproj" \
    --outputfolder=`pwd` \
    --no-open-xcode \
    --quiet
```
