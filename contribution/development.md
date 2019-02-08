---
description: setup for developing Tuist
---

# Setup

Tuist is a Swift package which requires [Swift Package Manager](https://swift.org/package-manager/) (Swift PM) to build and develop it. If you already have [Xcode](https://developer.apple.com/xcode/) installed, then you are set! See the [Swift PM installation section](https://github.com/apple/swift-package-manager#installation) for details on alternate methods of setting it up.
Getting
# Building 

To build Tuist, you can run the `build` command:

```sh
swift build
```

This will produce a binary for `tuist` and `tuistenv` within the `.build` folder. To run the built binaries you can use:

```sh
swift run tuist <arguments>
```

or 

```sh
swift run tuistenv <arguments>
```

# Testing
Tuist has a suite of unit tests as well as acceptance tests to ensure it continues to function correctly without regressions throughout its development cycle.

## Unit tests

Unit tests are `XCTest` style tests which can be run either within Xcode or from the command line using:

```sh
swift test
```

These tests live within the [`Tests`](https://github.com/tuist/tuist/tree/master/Tests) directory.

## Acceptance tests

Acceptance tests are cucumber style tests that test the Tuist command line as a whole.

To run those, you’ll first need to setup your environment:

```sh
gem install bundler
bundle install
```

Once setup, you can run the acceptance tests via:

```sh
bundle exec rake features
```

These tests live within the [`features`](https://github.com/tuist/tuist/tree/master/features) directory.

# Xcode

Tuist can also be developed within Xcode. To generate an Xcode project you can run:

```sh
swift package generate-xcodeproj
```
