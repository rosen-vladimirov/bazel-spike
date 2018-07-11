#git_repository(
#    name = "build_bazel_rules_nodejs",
#    remote = "https://github.com/bazelbuild/rules_nodejs.git",
#    tag = "0.10.0", # check for the latest tag when you install
#)

local_repository(
    name = "build_bazel_rules_nodejs",
    path = "/Users/vladimirov/Work/bazel/rules_nodejs",
)
load("@build_bazel_rules_nodejs//:defs.bzl", "node_repositories")

node_repositories(
  node_path = "/Users/vladimirov/.nvm/versions/node/v8.11.1/",
  package_json = ["//app:package.json"]
)

print ("111111")

load("@build_bazel_rules_nodejs//:defs.bzl", "npm_install")
npm_install(
    name = "foo",
    package_json = "//app:package.json",
    package_lock_json = "//app:package-lock.json",
)

print ("FINAL WORKSPACE")
