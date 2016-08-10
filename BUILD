java_library(
    name = "coffee_lib",
    srcs = glob(["java/coffee/**/*.java"]),
    deps = ["//third_party:dagger"],
)

java_library(
    name = "coffee_tests",
    srcs = glob(["javatests/coffee/**/*.java"]),
    deps = [
        ":coffee_lib",
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

java_binary(
    name = "coffee",
    main_class = "coffee.CoffeeApp",
    runtime_deps = [":coffee_lib"],
    jvm_flags = [
        "-Xms32m",
        "-Xmx128m",
        ],
)

