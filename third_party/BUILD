package(default_visibility = ["//visibility:public"])

java_import(
    name = "guava",
    jars = ["guava/guava-19.0.jar"],
)

java_import(
    name = "junit4",
    jars = [
        "hamcrest/hamcrest-core-1.3.jar",
        "junit/junit-4.11.jar",
    ],
)

java_import(
    name = "mockito",
    jars = ["mockito/mockito-all-1.10.19.jar"],
)

java_import(
    name = "jsr330_inject",
    jars = ["jsr330_inject/javax.inject.jar"],
)

java_import(
    name = "dagger_api",
    jars = ["dagger/dagger-2.5.jar"],
)

java_import(
    name = "dagger_compiler",
    jars = ["dagger/dagger-compiler-2.5.jar"],
)

java_import(
    name = "dagger_producers",
    jars = ["dagger/dagger-producers-2.5.jar"],
)

java_library(
    name = "dagger",
    exported_plugins = [":dagger_plugin"],
    exports = [
        ":dagger_api",
        ":jsr330_inject",
    ],
)

java_plugin(
    name = "dagger_plugin",
    processor_class = "dagger.internal.codegen.ComponentProcessor",
    generates_api = True,
    deps = [
        ":dagger_api",
        ":dagger_compiler",
        ":dagger_producers",
        ":guava",
        ":jsr330_inject",
    ],
)

