package(default_visibility = ["//visibility:public"])

java_library(
    name = "coffee_tests",
    srcs = glob(["**/*.java"]),
    deps = [
        "//java/coffee:coffee_lib",
        "//third_party:mockito",
        "//third_party:junit4",
        "//third_party:dagger",
    ]
)

java_test(
    name = "coffee_maker_test",
    size = "small",
    test_class = "coffee.CoffeeMakerTest",
    runtime_deps = [
        ":coffee_tests",
        "//third_party:dagger",
    ],
)

