package(default_visibility = ["//visibility:public"])

java_library(
    name = "coffee_lib",
    srcs = glob(["**/*.java"]),
    deps = ["//third_party:dagger"],
)

java_binary(
    name = "coffee",
    main_class = "coffee.CoffeeApp",
    runtime_deps = [":coffee_lib"],
    jvm_flags = [
        "-Xms32m",
        "-Xmx128m",
        ],
)

