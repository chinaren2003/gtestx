package(default_visibility = ["//visibility:public"])

cc_library(
  name = "gtestx",
  includes = ["src"],
  copts = [
    "-g",
    "-Wall",
  ],
  linkstatic = 1,
  srcs = glob([
    "src/gtestx/gtestx.cc",
    "src/gtestx/gtestx.h",
  ]),
  deps = [
    "//third_party/gtest-170",
    "//third_party/gflags-20",
  ],
)

cc_test(
  name = "test",
  copts = [
    "-g",
    "-Wall",
  ],
  srcs = glob(["test/*_test.cc"]),
  deps = [
    ":gtestx",
  ],
)

cc_binary(
  name = "examples",
  copts = [
    "-g",
    "-Wall",
  ],
  srcs = glob(["examples/*.cc"]),
  deps = [
    ":gtestx",
  ],
)
